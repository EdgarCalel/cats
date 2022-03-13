<script>
  export let name;
  export let nickname;
</script>
<style>
    .Profile-content {
      display: flex;
      align-items: center;
    }
    .Profile-avatar img {
      width: 42px;
      height: 42px;
      border-radius: 50%;
    }
    .Profile-info {
      margin: 0 0 0 0.5em;
    }
    .Profile-info h2 {
      font-size: 14px;
      color: black;
      margin: 0;
      padding: 0;
    }
    .Profile-info span {
      font-size: 12px;
      font-weight: normal;
    }
  </style>
<div class="Profile">
    <div class="Profile-content">
        <div class="Profile-avatar">
            <img src="https://scontent.fgua3-4.fna.fbcdn.net/v/t1.6435-9/123120989_3675657519151447_6278233892572714214_n.jpg?_nc_cat=100&ccb=1-5&_nc_sid=8bfeb9&_nc_ohc=7CSn1WhrxHAAX8DNg7G&_nc_oc=AQnWpV2lSLmANgfiaZN0dLK2hhZlF7bUefoV2OcClISAL1TFSPxTmlipXk1EqRll8f2o4-DgD94tXnvIt3IaFe9q&_nc_ht=scontent.fgua3-4.fna&oh=00_AT-osppsoF3CQ9iVzkpWMQ5tM-YnMUVrCMRVrwFwiz8LJw&oe=6252CD00" alt="" />
        </div>
        <div class="Profile-info">
            <h2>{nickname}</h2>
            <span>{name}</span>
        </div>

    </div>
</div>