<html>
    <body>
        <style>
            
            body {
                margin: 0;    
            }
            #controls {
                z-index: 10;
                position: absolute;
            }
            #pulser {
                position: absolute;
                width: 100%;
                height: 100%;
                background: red;
                animation-name: pulser;
                animation-duration: 0.0s;
                animation-iteration-count: infinite;
                animation-direction: alternate;
            }
            @keyframes pulser {
                0%   {background-color: red;}
                37%   {background-color: red;}
                37.5%   {background-color: white;}
                100%   {background-color: white;}
            }
        </style>


        <div id="controls">
            <span id="BPM"> &ensp; 10</span>BPM
            <input value="10" min="1" max="200" oninput="setHertz(this)" type="range" step="1">
            <br>
            <br>
            <span id="A"> &ensp; 10</span>
            <input value="10" min="1" max="200" oninput="setA(this)" type="range" step="1">
            <input value = "10" min="1" max="200" oninput = "setA(this)" type = "number" step= "1"><br>
            <span id="B"> &ensp; 10</span>
            
            <input value="10" min="1" max="200" oninput="setB(this)" type="range" step="1"><input value = "10" min="1" max="200" oninput = "setB(this)" type = "number" step= "1"><br><span id="C"> &ensp; 10</span>
            <input value="10" min="1" max="200" oninput="setC(this)" type="range" step="1"><input value = "10" min="1" max="200" oninput = "setC(this)" type = "number" step= "1"><br><span id="D"> &ensp; 10</span>
            <input value="10" min="1" max="200" oninput="setD(this)" type="range" step="1"><input value = "10" min="1" max="200" oninput = "setF(this)" type = "number" step= "1"><br><span id="E"> &ensp; 10</span>
            <input value="10" min="1" max="200" oninput="setE(this)" type="range" step="1"><input value = "10" min="1" max="200" oninput = "setE(this)" type = "number" step= "1"><br><span id="F"> &ensp; 10</span>
            <input value="10" min="1" max="200" oninput="setF(this)" type="range" step="1"><input value = "10" min="1" max="200" oninput = "setF(this)" type = "number" step= "1"><br>
            <button name="run" onclick="routine()" >run</button>
        <br>

            <button name ="idk" onclick = "findAllVariables()" > debugg</button>
            <pre><p style="font-family:courier new;font-size:15px">
            To set the routine use the sliders to set your middle value
            </pre></p>
            
        </div>
        <div id="pulser"></div>
        <script>
            function routine() {
                var value = document.getElementById("A").value;
                var value = document.getElementById("B").value;
                var value = document.getElementById("C").value;
                var value = document.getElementById("D").value;
                var value = document.getElementById("E").value;
                var value = document.getElementById("F").value;

            }
            function setA(ele) {
                var A = ele.value;
                document.getElementById('A').innerText = A;
            }
            function setB(ele) {
                var A = ele.value;
                document.getElementById('B').innerText = A;
            }
            function setC(ele) {
                var A = ele.value;
                document.getElementById('C').innerText = A;
            }
            function setD(ele) {
                var A = ele.value;
                document.getElementById('D').innerText = A;
            }
            function setE(ele) {
                var A = ele.value;
                document.getElementById('E').innerText = A;
            }
            function setF(ele) {
                var A = ele.value;
                document.getElementById('F').innerText = A;
            }
            function setHertz(ele) {
                var BPM = ele.value;
                document.getElementById('BPM').innerText = BPM;
                var seconds = 1 / ((parseInt(BPM))/60) / 2;
                
                console.log(seconds)
               document.getElementById('pulser').style.animationDuration = seconds + 's'
            }
        
        </script>
        
        
    </body>
</html>
