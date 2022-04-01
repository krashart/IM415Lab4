<script>
     export let text;
     export let checked;
     export let removeItem;
     export let toggleDone;
</script>

<li>
     <input bind:checked={checked} on:change={toggleDone} type="checkbox"> 
     <span class:checked={checked}>{text}</span>
     <button class="button1" type="button" on:click={removeItem} >Been There</button>
</li>

<style>
     .checked {
          text-decoration: line-through;
     }

     li {
          font-size: 22px;
          font-family: Georgia, 'Times New Roman', Times, serif;
          color: white;
          margin: 5px;
     }
     .button1 {
          background-color: white;
          color: black;
          border: 1px solid rgb(254, 0, 0);
          padding: 5px 10px;
          text-align: center;
          text-decoration: none;
          display: inline-block;
          font-size: 16px;
          transition-duration: 0.4s;
          margin-left: 20px;
     }
     .button1:hover {
          background-color: #555555;
          color: white;
}
</style>