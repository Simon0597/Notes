# 封装css3的Transform属性值
```ruby
<script>
        // 2个参数 是获取属性值
        // 3个参数 是设置属性值
        // 前提 想要获取 必须先用此函数设置值

        cssTransform(box,'rotate',30);
        cssTransform(box,'translate',60);
        cssTransform(box,'translate',0);  // 初始化
        console.log(cssTransform(box, 'translate'));

        function cssTransform( obj,attr,val ) {
            if( !obj.transform ){
                obj.transform = {};
            }
            if( arguments.length === 3 ){ // 设置
                obj.transform[attr] = val;
                var str = '';
                for( var key in obj.transform ){
                    switch ( key ){
                        case 'rotate':
                        case 'rotateX':
                        case 'rotateY':
                            str += key + '('+obj.transform[key]+'deg) ';
                            break;
                        case 'translate':
                        case 'translateX':
                        case 'translateY':
                            str += key + '('+obj.transform[key]+'px) ';
                            break;
                        case 'scale':
                        case 'scaleX':
                        case 'scaleY':
                            str += key + '('+obj.transform[key]+') ';
                            break;
                    }
                    obj.style.transform = str;
                }
            }else{  //获取值
                val = obj.transform[attr];
                if( typeof val === 'undefined'){
                    if( attr === 'scale' || attr === 'scaleX' || attr === 'scaleY' ){
                        val = 1
                    }else{
                        val= 0
                    }
                }
                return val;
            }


        }
    </script>
```
