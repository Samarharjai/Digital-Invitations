<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>wedinvities</title>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Playball&display=swap"
      rel="stylesheet"
    />
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-4bw+/aepP/YC94hEpVNVgiZdgIC5+VKNBQNGCHeKRQN+PtmoHDEXuppvnDJzQIu9"
      crossorigin="anonymous"
    />
    <link rel="stylesheet" href="style.css" />
  </head>

  <body>
    <script
      src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js"
      integrity="sha384-HwwvtgBNo3bZJJLYd8oVXjrBZt8cqVSpeBNS5n7C8IVInixGAoxmnlMuBnhbgrkm"
      crossorigin="anonymous"
    ></script>
    <div class="cont">
      <h1 class="text-center">SHADI MUBARAKH</h1>
      <div class="row">
        <div class="col-md-6">
          <div class="image">
            <img
              class="show"
              src="https://indianweddingtoolkit.com/wp-content/uploads/2015/11/holdinghands-775x450.jpg"
            />
            <div class="companyname1">WELCOME</div>
            <div class="companyname2">TO</div>
            <div class="companyname3">WEDINVITIES</div>
          </div>
        </div>

        <div class="col-md-6 text" id="part2">
          <hr />
          <div class="form-group my-3">
            <label for="namefield">Groom name</label>
          </div>
          <input
            type="text"
            id="gname"
            placeholder="enter groom name"
            class="text-center"
          />
          <hr />
          <div class="form-group my-3">
            <label for="namefield">Bride name</label>
          </div>
          <input
            type="text"
            id="bname"
            placeholder="enter bride name"
            class="inputwali"
          />
          <hr />
          <div class="form-group my-3">
            <label for="namefield">location</label>
          </div>
          <input
            type="text"
            id="loc"
            placeholder="enter location"
            class="text-center"
          />
          <hr />
          <div class="form-group my-3">
            <label for="namefield">date&time</label>
          </div>
          <input
            type="datetime"
            id="date&time"
            placeholder="enter date"
            class="text-center"
          />
          <hr />
          <div class="form-group">
            <label for="">Image</label>
            <input
              type="file"
              class="form-control"
              style="margin: 10px"
              id="profile"
            />
          </div>
        </div>
      </div>
      <button id="button" onclick="generatedcard()" class="btn1">Submit</button>
    </div>
      <div id="bookmarks">
        <div class="bookmark">
            <img id="renderImage" style="width: 650px; height: 433px;" />
    </div>
    <div class="container2">
        <h1 class="text-center">save the date</h1>
        <h1 class="text-center" id="gnames">Groom</h1>
        <h1 class="text-center">weds</h1>
        <h1 class="text-center" id="bnames">Bridge</h1>
        <h2 class="text-center">INVITE YOU TO CELEBRATE</h2>
        <h2 class="text-center">THEIR MARRIAGE</h2>
        <hr />
        <h1 class="text-center" id="dates">date</h1>
        <hr />
        <h1 class="text-center" id="locs">address</h1>
      </div>
    </div>
    <button onclick="generateddesign()">Change design</button>
    <script>
      function generatedcard() {
        let b = document.getElementById("gname").value;
        document.getElementById("gnames").innerHTML = b;
        let c = document.getElementById("bname").value;
        document.getElementById("bnames").innerHTML = c;
        let d = document.getElementById("date&time").value;
        document.getElementById("dates").innerHTML = d;
        let e = document.getElementById("loc").value;
        document.getElementById("locs").innerHTML = e;

        const inputPhoto = document.getElementById("profile");
        const outputPhoto = document.getElementById("renderImage");
        console.log(inputPhoto, inputPhoto.files);
        const file = inputPhoto.files[0];
        console.log(file);
        const src = URL.createObjectURL(file);
        console.log(src);
        outputPhoto.src = src;
      }
      function generateddesign(){
        var f = document.getElementById("bookmarks");
        Element.classlist.add("mystyle");
      }
    </script>
  </body>
</html>
