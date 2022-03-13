<script>
    import { onMount} from 'svelte'
import Header from '../components/Header.svelte'
import TimeLine from '../components/TimeLine.svelte'
import Sidebar from '../components/Sidebar.svelte'
import Main from '../components/Main.svelte'
import About from '../../../svelte/src/components/About.svelte'
import App from '../../../svelte/src/App.svelte'

let data=[];
//const API2='https://rickandmortyapi.com/api/character'
const API='https://kittygram-api.vercel.app'
onMount(async ()=>{
   const toto =  await fetch(API)
     const result=  toto.json();
     data= await result
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
  :global(body){
background-color: #fafafa;
color: rgba(38, 38, 38, 0.7);
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
        <TimeLine posts={data.posts} />
        <Sidebar {...data.user} />
    </Main>
