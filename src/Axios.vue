<script>
const axios = require(axios)
    .get("https://jsonplaceholder.typicode.com/users/1")
    .then((response) => {
      displayOutput(response)
    })
    .catch((err) => console.log(err));
</script>