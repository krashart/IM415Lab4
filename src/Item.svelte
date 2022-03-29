<script>
     export let text;
     export let checked;
     export let removeItem;
     export let toggleDone;
</script>

<li>
     <input bind:checked={checked} on:change={toggleDone} type="checkbox"> 
     <span class:checked={checked}>{text}</span>
     <button class="button1" type="button" on:click={removeItem} >Delete</button>
</li>

<style>
     .checked {
          text-decoration: line-through;
     }
     .button1 {
          background-color: white;
          color: black;
          border: 1px solid rgb(254, 0, 0);
          padding: 10px 15px;
          text-align: center;
          text-decoration: none;
          display: inline-block;
          font-size: 12px;
          transition-duration: 0.4s;
     }
     .button1:hover {
          background-color: #555555;
          color: white;
}
</style>