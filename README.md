# Chart.js   
## 사용법
``` html
    <head>
    <script src="https://cdn.jsdelivr.net/npm/chart.js@3.9.1/dist/chart.min.js"></script>
    </head>
```  
- 최신버전은 4.0.1 이지만 안정적인 3.9.1 으로 head 태그안에 CDN 추가  
- chart.js 는 canvas 기반으로 렌더링 하기 때문에 SVG 방식에 비해 빠름. 
-  공식 가이드 링크 https://www.chartjs.org/docs/3.9.1/  
-  https://yeon22.github.io/Chartjs-kr/docs/latest/?q=   
``` html
<body>
    <canvas id="myChart"></canvas>    
</body>
```  
``` javascript
new Chart(document.getElementById("myChart"), {
    type: '',
    data: {
        labels: [],
        datasets: []
    },
    options: {

    }
});  
```
  - body 태그 안에 그려줄곳에 canvas 작성  
  - 차트에 표현할 데이터를 백단에서 받고 렌더링 하여야 하기때문에 동기처리 필수 함수로 만들고 Ajax success 에서 호출
## 차트 크기 설정  
``` javascript
new Chart(document.getElementById("myChart"), {
    type: '',
    data: {
        labels: [],
        datasets: []
    },
    options: {
        responsive : false,

    }
}); 
```
- 차트 크기를 정적으로 설정하고 싶으면 options 안에 responsive 를 false로 바꿔준다. default 값 : true  
``` html
<body>
    <canvas id="myChart" width="500" height="500"></canvas>    
</body>
```  
-  canvas에 크기 지정
## 반응형 
``` html
<body>
    <canvas id="myChart" style="height:30vh; width:50vw">
    </canvas>
</body>
```  
-  반응형도 가능  
## 차트종류  
![chart](/bar.png)  
![chart](/line.png)
![chart](/pie.png)
![chart](/radar.png)
![chart](/polarArea.png)
![chart](/doughnut.png)
![chart](/horizontalBar.png)
![chart](/groupbar.png)
![chart](/mixed-chart.png)
![chart](/bubble.png)  
## 옵션
type : `'bar'` 차트 타입 쓰면 됨  
data : 차트에 나타낼 데이터  
>labels : 차트에 나타낼 라벨  
>backgroundColor : 차트 데이터 순서대로 나타낼 칼라  
>data : 데이터  
  
options :  
>  tooltip: 툴팁설정  
>  plugins :  
>> legend : 범례 설정  

차트 Event  
```
document.getElementById("bar-chart").onclick = () => {

}
```  
차트 이벤트도 가능하다.







