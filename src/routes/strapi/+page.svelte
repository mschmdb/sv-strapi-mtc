<script>
    import axios from 'axios';
    //Token needs to be put to .env
    const token = 'da144873ebe6a0b9dbff60c1fba7561740f0748f5364eae2c6fd209163c7142735ac5e2cbacfaec9b67182261acecb75e16483b048f1eac807ddba1b4ad5ca5014632401a7eba3c05a23f384c5feeef92a9a02052d516c0bf266bdf5fded5c60acead9cc3955ebfb6b2543385cb942dbc51713a0b88d0936b57d0db6e4da4d27';
    let collections = []
    // Request API.
    axios
    .get('https://strapi.mtc.berlin/api/collections', {
        headers: {
        Authorization: `Bearer ${token}`,
        },
    })
    .then(response => {
        // Handle success.
        console.log('Data: ', response.data);
        collections = response.data
    })
    .catch(error => {
        // Handle error.
        console.log('An error occurred:', error.response);
    });
   
</script>
<h1>Data from Strapi</h1>
{JSON.stringify(collections)}

   