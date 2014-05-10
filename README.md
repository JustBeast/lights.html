lights.html
===========
<!DOCTYPE html>
<html>
  <head>
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
    <script type="text/javascript" src="http://netdna.bootstrapcdn.com/bootstrap/3.0.3/js/bootstrap.min.js"></script>
    <script type="text/javascript" src="http://cdn.firebase.com/v0/firebase.js"></script>
    <link rel="stylesheet" href="http://netdna.bootstrapcdn.com/bootstrap/3.0.3/css/bootstrap.min.css">
    <link href="http://netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css" rel="stylesheet">
    <style>
    #off {
      background-color: #31B404;
      border-radius: 10px;
      border-color: white;
      font-size: 40px;
    }

    #on {
      background-color: #00BFFF;
      border-color: black;
      font-size: 40px;
    }
      
    </style>
    <script type="text/javascript">
    var firebase;

    function setup () {
      firebase= new Firebase('https://techlab-lights.firebaseio.com');
      $('#on').click(function(){
          turnOn()
        });
      $('#off').click(function(){
          turnOff(1);
          turnOff(2);
          turnOff(3);
          turnOff(4);
          turnOff(5);
          turnOff(6);
          turnOff(7);
          turnOff(8);
          turnOff(9);
          turnOff(10);
          turnOff(11);
          turnOff(12);
      });
    }

    function turnOff(light) {
      firebase.child(light).set(false);
    }
    function turnOn(light) {
      firebase.child(light).set(true)
    }

    $("#submit").click(function)
        var lightNumber=$('#light').val();
        turnOn(lightNumber)
    $(document).ready(setup);


    </script>
  </head>
  <body>
    <div class="container">
      <div class="row">
        <div class="col-md-4">
                <button id='off'>Off</button>

              <input type="text" id="light" class="form-control">
              <button id="submit">submit</button>
              
      </div>
  </div>
</div>


  </body>
</html>
