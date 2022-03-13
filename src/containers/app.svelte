<script>
    import { onMount} from 'svelte'
import Header from '../components/Header.svelte'
import TimeLine from '../components/TimeLine.svelte'
import Sidebar from '../components/Sidebar.svelte'
import Main from '../components/Main.svelte'

let data=[];
const API='https://rickandmortyapi.com/api/character'
//const API='https://kittygram-api.vercel.app'
onMount(async ()=>{
   const toto =  await fetch(API)
     const result=  toto.json();
     const  dataPre = await result
     data= await dataPre.results
     
//    const  DataAfter = await result.results
//     const data2 = await DataAfter.map(el=>{
//         return{
//         name: el.name,
//         nickname: el.name.split(' ')[0].trim(),
//         username: el.species,
//         location: el.location.name,
//         avatar: el.image,
//         photo: el.image,
//         like: false,
//         bookmark: false,
//         postComment: 'Episodios',
//         comments:el.episode.map(el=>{return{name:el}})
//         }
//     })
//   console.log(DataAfter)
//   console.log(data)
 })

</script>


<style>
  @import url('https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;1,900&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');
  :global(body.dark-mode){
          background-color: #1d3040 ;
          color: #0559e9
      }
  :global(body.Main){

color: rgba(153, 0, 0, 0.7);
font-family: 'Lato', sans-serif;
margin: 0;
padding: 0;
}
:global(h1,h2,h3){
    margin: 0;
    padding: 0;
}
</style>

<Header />
    <Main>
        <TimeLine posts={data} />
        <Sidebar {...data} />
    </Main>
