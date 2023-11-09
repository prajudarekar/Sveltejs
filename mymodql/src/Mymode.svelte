<script>
  function toggle() {
    window.document.body.classList.toggle('dark-mode')
  }
  </script>
 <!-- <button class="btn" on:click={toggle}>-->
    
     <!-- <div class="dark-light" on:click={toggle}>
          <i class='bx bx-moon moon'></i>
          <i class='bx bx-sun sun'></i>
      </div>-->
      <label class="switch">
        <input type="checkbox"  on:click={toggle}>
        <span class="slider round"></span>
      </label>
      
  
  <style>
.switch {
  position: relative;
  display: inline-block;
  margin-top: 15%;
  width: 35px;
  height: 14px;
}

.switch input { 
  opacity: 0;
  width: 0;
  height: 0;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #2196F3;
  -webkit-transition: .4s;
  transition: .4s;
}

.slider:before {
  position: absolute;
  content: "";
  height: 6px;
  width: 6px;
  left: 4px;
  bottom: 4px;
  background-color: white;
  -webkit-transition: .4s;
  transition: .4s;
}

input:checked + .slider {
  background-color: #ccc;
}

input:focus + .slider {
  box-shadow: 0 0 1px #ccc;
}

input:checked + .slider:before {
  -webkit-transform: translateX(22px);
  -ms-transform: translateX(22px);
  transform: translateX(22px);
}

/* Rounded sliders */
.slider.round {
  border-radius: 34px;
  border:1px solid gainsboro;

}

.slider.round:before {
  border-radius: 50%;
  border:1px solid gainsboro;

}

    :global(body.dark-mode) button {
      background-color: #0084f6;
      color: white;
    }
  </style>