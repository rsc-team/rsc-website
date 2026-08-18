<script lang="ts">
    let {
        label = 'NavLabel',
        link = '',
        newtab = false,
        textcolor = "white"
    } = $props()
</script>


<a href={link} 
   target={newtab ? "_blank" : undefined}
   rel={newtab ? "noopener noreferrer" : undefined}
   class={"flex justify-center items-center text-center pl-3 pr-3"}

>
<p class={`text-${textcolor} text-xl
           text-shadow-lg/45
           font-sweetsquare
           font-bold
           `}>
{label}
</p>

</a>