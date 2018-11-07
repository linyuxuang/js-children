# js-children
自己封装children 函数  功能  (获取当前元素的子元素)



              <div>
                <span></span>
                <p><span></span></p>
             </div>

               Element.prototype.myChildren=function(){
                var childer=this.childNodes;
                var arr=[];
                for(var i=0;i<childer.length;i++){
                  if(childer[i].nodeType==1){
                    arr.push(childer[i])
                  }
                }
              return arr;
             }

              var div=document.getElementsByTagName("div")[0];
              div.myChildren()   //[span, p]
