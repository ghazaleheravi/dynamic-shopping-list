# dynamic-shopping-list
<!doctype html>
<html lang="en-us" dir="ltr">
    <head>
        <meta charset="utf-8">
        <title>my shopping list</title>

        <style>
           body {
               border: solid;
               font-size: 20px;
           } 
           li {
             margin-bottom: 10px;  
           }
           li button {
               color:cornflowerblue;
               margin-left: 20px;
               border-radius: 60px;
           }


        </style>
    </head>

    <body>
        <h1>My shopping list</h1>

        <div>
            <label for="input">Enter a new item: </label>
            <input id="input" type="text">
            <button>Add item</button>
        </div>

        <ul>

        </ul>

        <script>

            let button = document.querySelector('button');
            let item = document.querySelector('#input');
            let list = document.querySelector('ul');

            button.addEventListener('click',addItem);

            function addItem(){
               
                let li = document.createElement('li');
                li.textContent = item.value;
                list.appendChild(li);

                let dltBtn = document.createElement('button');
                dltBtn.textContent = 'Delete';
                li.appendChild(dltBtn);

                dltBtn.addEventListener('click',function(){
                    list.removeChild(li);

                });

                

                item.value = '';
                item.focus();


            }

            

        </script>

    </body>



</html>
