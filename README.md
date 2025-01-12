let timeFunc = (timer)=>{
 setInterval(function(){
    timer-- 
    document.getElementById("timerval").textContent = timer;
    if(timer <= 0){
        clearInterval(timeFunc);
        alert("Time's up!");
        document.getElementById("timerval").textContent = "0";
    }
    else if(isNaN(timer)){
        alert("please enter number")
    }
    else if(timer < 0){
        alert("Please enter a positive number")
    }

 },1000)
}
timeFunc(
    prompt("Enter a Time")
)

