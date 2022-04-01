<script>
     import Item from './Item.svelte';
     let newItem;
     let todoList = [];
     let count = [];

     function addToList() {
          if (!newItem) return;
          todoList = [...todoList, {
               text: newItem,
               checked: false,
          }]; 
          newItem = '';
     }
     function removeFromList(n) {
          todoList.splice(n, 1);
          todoList = todoList;
          console.log(todoList);
     }
     function toggleDone(index, v) {
          v = !v;
          todoList[index].checked = v;
          todoList = todoList;
     }
</script>

<!-- <form on:submit|preventDefault={addToList}>
     <input bind:value={newItem}>
</form> -->

<form on:submit|preventDefault={addToList}>
     <input bind:value={newItem} list="temples" name="temple">
     <datalist id="temples">
       <option value="Angkor Wat">
       <option value="Katas Raj">
       <option value="Bagan">
       <option value="Byodo-In">
       <option value="Khajuraho">
       <option value="Kukke">
     </datalist>
     <input type="submit" value="Choose Wisely!">
   </form>
<ul>
     {#each todoList as item, index}
          <Item 
          text={item.text}
          checked={item.checked} 
          toggleDone={() => toggleDone(index, item.checked)}
          removeItem={() => removeFromList(index)} />
     {/each}
</ul>


<style>
     ul {
          list-style: none;
          padding: 0;
          margin: 1rem 0 0 0;
     }
</style>