<script context="module">
  export const sortByDate = (items, order) => {
    items.sort((a, b) => { 
      // Must have field named "date" in content source to work.
      let dateA = new Date(a?.fields?.publish?.date);
      let dateB = new Date(b?.fields?.publish?.date);
      return (order == "oldest") ? (dateA - dateB) : (dateB - dateA);
    });
    return items;
  };
</script>
