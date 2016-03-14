一：字体计算方法

比如我们可以使用rem对字体作为单位，对html元素设置10px来进行计算；如下html元素的字体：

html {font-size: 62.5%;/*10 ÷ 16 × 100% = 62.5%*/}

假如现在设计稿给到我们前端的是720像素的话，那么在如上媒体查询字体,宽度和高度及margin，padding需要等比例缩放操作；

复制代码
@media (min-width: 320px) and (max-width:359px){
     // 对于320-359 按照320px来计算
    /* 720/320 = 2.25*/ 
    html{font-size: 27.78%}  // 62.5% / 2.25
}
@media (min-width: 360px) and (max-width:399px){
     // 对于360-399按照360px来计算
    /* 720/360 = 2*/ 
    html{font-size: 31.25 %}  // 62.5% / 2 
}
@media (min-width: 400px) and (max-width:450px){
     // 对于400-450按照400px来计算
    /* 720/400 = 1.8*/ 
    html{font-size: 34.72 %}  // 62.5% / 1.8
}
@media (min-width: 640px) and (max-width:999px){
     // 对于640-999按照640px来计算
    /* 720/640 = 1.125 */ 
    html{font-size: 55.56%}  // 62.5% / 1.125
}

二：width,height,margin及padding的计算方法

对于width，height，margin，padding针对不同的手机也是等比例缩放的，比如在720像素下的margin-top是40px；那么在320，360，400，640分别如下计算：(其他属性的也一样计算)

复制代码
@media (min-width: 320px) and (max-width:359px){
    /* 720/320 = 2.25*/
    margin-top = 40px / 2.25
}

@media (min-width: 360px) and (max-width:399px){
        /* 720/360 = 2*/ 
    margin-top = 40px / 2 
}
@media (min-width: 400px) and (max-width:450px){
    /* 720/400 = 1.8*/ 
    margin-top = 40px / 1.8 
}
@media (min-width:640px) and (max-width:999px){
    /* 720/640 = 1.125 */ 
    margin-top = 40px / 1.125 
}
复制代码
