<template>
    <div class="item">
       <input 
            type="checkbox"
            @change="updateCheck()"
            
        />
        <span>{{item.name}}</span>
       <button @click="removeItem()" class="trashcan">
           <font-awesome-icon icon="trash" />
       </button>
    </div>
</template>
<script>
export default {
    props:['item'],
    created(){
        console.log(this.item);
    }
}
</script> 
<style scoped>
    .completed{
        text-decoration: line-through;
        color: #999999;
    }
    .itemText{
        width: 100%;
        margin-left: 20px;
    }
    .item{
        display: flex;
        justify-content: center;
        align-items: center;

    }
    .trashcan{
       background: #e6e6e6;
       border: none;
       color:#FF0000;
       outline:none;
    }
</style>