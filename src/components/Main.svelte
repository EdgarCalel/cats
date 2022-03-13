
<style>
    .Main {
      display: grid;
      grid-template-columns: minmax(auto, 936px);
      justify-content: center;
     
    }
    .Main-container {
      display: grid;
      grid-template-columns: 3fr 1fr;
      grid-gap: 2em;
      padding: 2em 0;
    }
    @media only screen and (max-width: 375) {
 .Main{
 margin: 0;
 background-color: green;
 }
}
  </style>
<div class="Main">
    <div class="Main-container">
        <slot  />
    </div>
</div>