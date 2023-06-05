
<!DOCTYPE html>
<html>
<head>
    <title>List Example</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        
        .container {
            max-width: 400px;
            margin: 0 auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        
        h1 {
            text-align: center;
        }
        
        ul {
            list-style-type: none;
            padding: 0;
        }
        
        li {
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>My List</h1>
        <input type="text" id="itemInput" placeholder="Enter an item">
        <button id="addItemButton">Add Item</button>
        <ul id="itemList"></ul>
    </div>

    <script>
        var input = document.getElementById("itemInput");
        var button = document.getElementById("addItemButton");
        var ul = document.getElementById("itemList");

        button.addEventListener("click", function() {
            if (input.value !== "") {
                var li = document.createElement("li");
                li.appendChild(document.createTextNode(input.value));
                ul.appendChild(li);
                input.value = "";
            }
        });

        input.addEventListener("keypress", function(event) {
            if (input.value !== "" && event.keyCode === 13) {
                var li = document.createElement("li");
                li.appendChild(document.createTextNode(input.value));
                ul.appendChild(li);
                input.value = "";
            }
        });
    </script>
</body>
</html>
