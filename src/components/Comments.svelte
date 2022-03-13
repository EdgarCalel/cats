<script>
  export let comments=[]

  function addComment(e) {
    const msg = e.target.text.value;
    if (msg.length > 3) {
      const message = {
        id: Date.now(),
        text: msg,
        username: "Edgar Calel",
      };
      comments = [...comments, message];
      e.target.text.value = "";
    }
  }
</script>
<style>
    .Comments h3 {
      font-size: 14px;
      color: black;
      font-weight: bold;
      margin: 0;
      padding: 0;
    }
    .Comments span {
      font-size: 14px;
      margin: 0 0 0 0.5em;
      font-weight: bold;
      color: rgba(109, 82, 185, 0.404);
    }
    .Comments-add {
      padding: 1em 1em 1em 1em;
      border-top: 1px solid rgba(219, 219, 219, 0);
    }
    .Comments-add form {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .Comments-content {
      padding: 0 1em 0.5em 1em;
    }
    .Comments-users {
      margin: 0 0 0.5em 0;
      display: flex;
    }
  
    input {
      border: solid 1px #e9e9e9;
      border-radius: 5px;
      color: #696969;
      border: 1px solid transparent;
      font-size: 12px;
      outline: none;
      width: 100%;
      display: flex;
    }
    button {
      border: none;
      color: #3897f0;
      font-size: 12px;
      outline: none;
      cursor: pointer;
    }
    label {
      display: none;
    }
  </style>
  
<div class="Comments">
    <div class="Comments-content">
      {#each comments as comment (comment.id)}
      <div class="Comments-users">
        <h3>{comment.username}</h3>
        <span>{comment.text}</span>
      </div>
{:else}
<div><p>loading-...</p></div>
      {/each}


        <div class="Comments-users">
<label for="">holaaaa</label>
</div>
        <div class="Comments-add">
            <form on:submit|preventDefault={addComment} >
                <input 
                type="text" 
                class="Comments-input" 
                placeholder="agregar comentario"
                id="text" />
                <button type="submit">Enviar</button>   
            </form>
        </div>
    </div>
</div>