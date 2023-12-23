<template>
    <div>
        <div class="tables">
            <table> 
                <tr v-for="col in grid" class="tables__column">
                    <td v-for="cell in col" class="tables__cell">{{ cell }}</td>
                </tr>
            </table>
        </div>
    </div>
</template>

<script>
    export default{
        props: ['grid']
    }
</script>

<style>

    .tables{
        margin: 3vh 0  ; 
        border: 2px solid ; 
        width: fit-content ; 
    }

</style>