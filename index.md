function timer(totalTime, dealine) {
  var time = totalTime * 100;
  var dayDuration = time / deadline;
  var actualDay = deadline;
  var timer = setInterval(countTime, dayDuration);
  function countTime() {
    --actualDay;
    $('.deadline-days .day').text(actualDay);
    if (actualDay == 0) {
      clearInterval(timer);
      $('.deadline-days .day').text(deadline);
      }
  }
