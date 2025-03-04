<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Flipbook</title>
  <style>
    /* Set the entire body background to a wavy blue pattern */
    body {
      background: url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1200 120' preserveAspectRatio='none'><path d='M0,0 C300,50 900,0 1200,50 L1200,120 L0,120 Z' fill='%230072E3' opacity='0.5'/><path d='M0,20 C300,70 900,20 1200,70 L1200,120 L0,120 Z' fill='%2300A0FF' opacity='0.5'/></svg>") no-repeat center center;
      background-size: cover;
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      min-height: 100vh;
      justify-content: space-between;
      font-family: Arial, sans-serif;
    }
    /* Flipbook container: no separate background so body’s pattern shows through */
    #flipbook-container {
      width: 90vw;
      flex: 1;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      position: relative;
      text-align: center;
      background: transparent;
      padding-left: 30px;
    }
    /* The flipbook itself is centered */
    #flipbook {
      display: inline-block;
      margin: 0 auto;
    }
    /* Page styling for flipbook images */
    #flipbook .page {
      background-size: contain;
      background-repeat: no-repeat;
      background-position: center center;
      background-color: white;
      border: 1px solid #999;
      position: absolute; /* turn.js positions pages absolutely */
    }
    /* Footer controls with the specified blue background */
    .controls {
      width: 100%;
      text-align: center;
      padding: 10px 0;
      background: #0072E3;
      color: #fff;
    }
    .controls button {
      padding: 10px 20px;
      margin: 5px;
      font-size: 16px;
      cursor: pointer;
    }
    .controls #pageInfo {
      display: inline-block;
      margin: 0 20px;
      font-size: 18px;
      vertical-align: middle;
    }
  </style>
  <!-- jQuery and turn.js from CDN -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/turn.js/3/turn.min.js"></script>
</head>
<body>
  <div id="flipbook-container">
    <div id="flipbook">
      
        <div class="page" style="background-image: url('images/page1.jpg');"></div>
        <div class="page" style="background-image: url('images/page2.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page3.jpg');"></div>
        <div class="page" style="background-image: url('images/page4.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page5.jpg');"></div>
        <div class="page" style="background-image: url('images/page6.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page7.jpg');"></div>
        <div class="page" style="background-image: url('images/page8.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page9.jpg');"></div>
        <div class="page" style="background-image: url('images/page10.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page11.jpg');"></div>
        <div class="page" style="background-image: url('images/page12.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page13.jpg');"></div>
        <div class="page" style="background-image: url('images/page14.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page15.jpg');"></div>
        <div class="page" style="background-image: url('images/page16.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page17.jpg');"></div>
        <div class="page" style="background-image: url('images/page18.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page19.jpg');"></div>
        <div class="page" style="background-image: url('images/page20.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page21.jpg');"></div>
        <div class="page" style="background-image: url('images/page22.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page23.jpg');"></div>
        <div class="page" style="background-image: url('images/page24.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page25.jpg');"></div>
        <div class="page" style="background-image: url('images/page26.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page27.jpg');"></div>
        <div class="page" style="background-image: url('images/page28.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page29.jpg');"></div>
        <div class="page" style="background-image: url('images/page30.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page31.jpg');"></div>
        <div class="page" style="background-image: url('images/page32.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page33.jpg');"></div>
        <div class="page" style="background-image: url('images/page34.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page35.jpg');"></div>
        <div class="page" style="background-image: url('images/page36.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page37.jpg');"></div>
        <div class="page" style="background-image: url('images/page38.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page39.jpg');"></div>
        <div class="page" style="background-image: url('images/page40.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page41.jpg');"></div>
        <div class="page" style="background-image: url('images/page42.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page43.jpg');"></div>
        <div class="page" style="background-image: url('images/page44.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page45.jpg');"></div>
        <div class="page" style="background-image: url('images/page46.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page47.jpg');"></div>
        <div class="page" style="background-image: url('images/page48.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page49.jpg');"></div>
        <div class="page" style="background-image: url('images/page50.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page51.jpg');"></div>
        <div class="page" style="background-image: url('images/page52.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page53.jpg');"></div>
        <div class="page" style="background-image: url('images/page54.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page55.jpg');"></div>
        <div class="page" style="background-image: url('images/page56.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page57.jpg');"></div>
        <div class="page" style="background-image: url('images/page58.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page59.jpg');"></div>
        <div class="page" style="background-image: url('images/page60.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page61.jpg');"></div>
        <div class="page" style="background-image: url('images/page62.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page63.jpg');"></div>
        <div class="page" style="background-image: url('images/page64.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page65.jpg');"></div>
        <div class="page" style="background-image: url('images/page66.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page67.jpg');"></div>
        <div class="page" style="background-image: url('images/page68.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page69.jpg');"></div>
        <div class="page" style="background-image: url('images/page70.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page71.jpg');"></div>
        <div class="page" style="background-image: url('images/page72.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page73.jpg');"></div>
        <div class="page" style="background-image: url('images/page74.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page75.jpg');"></div>
        <div class="page" style="background-image: url('images/page76.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page77.jpg');"></div>
        <div class="page" style="background-image: url('images/page78.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page79.jpg');"></div>
        <div class="page" style="background-image: url('images/page80.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page81.jpg');"></div>
        <div class="page" style="background-image: url('images/page82.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page83.jpg');"></div>
        <div class="page" style="background-image: url('images/page84.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page85.jpg');"></div>
        <div class="page" style="background-image: url('images/page86.jpg');"></div>
        
        <div class="page" style="background-image: url('images/page87.jpg');"></div>
        <div class="page" style="background-image: url('images/page88.jpg');"></div>
        
    </div>
  </div>
  <div class="controls">
    <button onclick="$('#flipbook').turn('previous')">Previous</button>
    <div id="pageInfo"></div>
    <button onclick="$('#flipbook').turn('next')">Next</button>
  </div>
  <script>
  $(document).ready(function() {
    var currentDisplay = null;
    var resizeTimer;
    // Store the original flipbook HTML to rebuild when needed.
    var originalFlipbookHTML = $("#flipbook").html();

    function getFlipbookDimensions() {
      var width = Math.floor(window.innerWidth * 0.9);
      var height = Math.floor(window.innerHeight * 0.8);
      console.log("Calculated dimensions: width = " + width + ", height = " + height);
      return { width: width, height: height };
    }

    function checkOrientation() {
      var mode = window.matchMedia("(orientation: portrait)").matches ? "single" : "double";
      console.log("Orientation check: " + mode);
      return mode;
    }

    function updatePageInfo() {
      var total = $("#flipbook").turn("pages");
      var view = $("#flipbook").turn("view");
      var infoText = "";
      if(currentDisplay === "double") {
        infoText = "Pages: " + view.join(" and ") + " of " + total;
      } else {
        infoText = "Page: " + view[0] + " of " + total;
      }
      $("#pageInfo").text(infoText);
      console.log("Updated page info: " + infoText);
    }

    function logDebugInfo() {
      var pagesCount = $("#flipbook").turn("pages");
      var view = $("#flipbook").turn("view");
      console.log("Debug Info:");
      console.log(" - Current display mode: " + currentDisplay);
      console.log(" - Total pages: " + pagesCount);
      console.log(" - Current view (visible pages): ", view);
    }

    function initFlipbook(displayType) {
      currentDisplay = displayType;
      var dims = getFlipbookDimensions();
      $("#flipbook").turn({
        width: dims.width,
        height: dims.height,
        autoCenter: true,
        display: displayType,
        elevation: 50,
        gradients: true,
        when: {
          turned: function(event, page) {
            console.log("Turned to page: " + page);
            logDebugInfo();
            updatePageInfo();
          }
        }
      });
      console.log("Initialized flipbook in " + displayType + " mode.");
      logDebugInfo();
      updatePageInfo();
    }

    function reinitFlipbook(newDisplay) {
      var currentPage = $("#flipbook").turn("page");
      console.log("Reinitializing flipbook. New display: " + newDisplay + ", current page: " + currentPage);
      try {
        $("#flipbook").turn("destroy");
        console.log("Destroyed current flipbook instance.");
      } catch (e) {
        console.log("Error destroying flipbook instance: " + e);
      }
      var $oldFlipbook = $("#flipbook");
      $oldFlipbook.replaceWith("<div id='flipbook'>" + originalFlipbookHTML + "</div>");
      setTimeout(function() {
        initFlipbook(newDisplay);
        var totalPages = $("#flipbook").turn("pages");
        if (currentPage > totalPages) {
          currentPage = totalPages;
        }
        $("#flipbook").turn("page", currentPage);
        console.log("Restored to page: " + currentPage);
      }, 300);
    }

    // Initial setup.
    initFlipbook(checkOrientation());

    function handleResize() {
      var newDisplay = checkOrientation();
      console.log("Handle resize: new display: " + newDisplay + ", current display: " + currentDisplay);
      if (newDisplay !== currentDisplay) {
        reinitFlipbook(newDisplay);
      } else {
        var dims = getFlipbookDimensions();
        $("#flipbook").turn("size", dims.width, dims.height);
        updatePageInfo();
      }
    }

    $(window).on("resize orientationchange", function() {
      clearTimeout(resizeTimer);
      resizeTimer = setTimeout(handleResize, 300);
    });
  });
  </script>
</body>
</html>
