- 2022 2월 첫째주부터 호수 한칸 올라감; +1되서(코드 고치고 그런듯) - init 

year > 2022.json ; 2022년
```json
{
    "month_files":[
        "2201.json",
        "2202.json",
        "2203.json",
        "2204.json",
        "2205.json"
    ]
}
```
2201.json-> 22년 1월

```javascript
const ob0 = {}
const hanja = document.getElementsByClassName("u_word_dic")[0].innerText
ob0["hanja"] = hanja

ob0["name"] = document.getElementsByClassName("mean a")[0].innerText

const sub = document.getElementsByClassName("desc")[0].innerText
ob0["sub"] = sub

const count = document.getElementsByClassName("word")[1].innerText
ob0["count"] = count

const sub_list = [];
const strokList = document.getElementsByClassName("stroke_item")
for(var i = 0 ; i < strokList.length; i++){
    sub_list.push(strokList[i].firstElementChild.firstElementChild.src);
}
ob0["draw_list"] = sub_list

console.log(JSON.stringify(ob0));
```
