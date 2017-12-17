
##javascript 資料結構及演算法實作##
###chapter 1  簡介###
> 在關閉body標籤前引入javascript code
> 這樣瀏覽器會在載入腳本前解析＆顯示HTML，有利提升頁面效能

> javascript不是強類型語言，初始宣吿var為number，之後可更新成string or object... type

    typeof num;             //"number"
    typeof 'Packet';        //"string"
    typeof true;            //"boolean"
    typeof [1, 2, 3];       //"object"
    typeof { name:  John }; //"object"
    typeof doesntExist;     //"undefined"

當相等運算子( === )比較的類型為物件時

    var person1 = {name: 'John'};
    ver person2 = {name: 'John'};
    console.log(person1 === person2); //false, 因為引用不同object

other reference: [MDN-javascript-Expressions and operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)

###chapter 2 Array###
Array Methods: **splice vs. slice**

    /* splice */
    var ary1 = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    
    ary1.splice(5, 3); 
    // ary1 = [1, 2, 3, 4, 5, 9, 10]
    
    ary1.splice(5, 0, 'a', 'b', 'c'); 
    // ary1 = [1, 2, 3, 4, 5, 'a', 'b', 'c', 9, 10]


    /* slice */
    var animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];
    
    animals.slice(2); 
    //return new array ["camel", "duck", "elephant"]

    animals.slice(1, 4); 
    //return new array ["bison", "camel", "duck"]


> splice 可增加／刪除element, 並改變原來的array
> slice   將原array擷取並return 新的array