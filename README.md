# //document.write("Hello World");
console.log("It worked");

// alternative to DOMContentLoaded event
document.onreadystatechange = function () {
    if (document.readyState === "interactive") {
      initApplication();
    }
  }

  function initApplication () {
      let el = document.getElementById("RightOrWrong");
      console.log(el);

      el.addEventListener("change", function() {
          console.log(el.checked);
          let el2 = document.getElementById("result");
          el2.innerHTML = "checked: " + el.checked;
      });
  }
