<script>
    export let text;
    </script>
    <style>
        button{
          width: 50px;
          height: 50px;
          font-size: 2rem;
          background-color: rgba(177, 160, 136, 0.568);
          border-radius: 50%;
        }
    </style>
    <div class="BtnDark"> 
    <button  on:click >{text}</button>
    </div>