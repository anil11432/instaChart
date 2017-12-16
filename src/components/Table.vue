<template>
    <div>
        <table class="table table-bordered">
            <thead>
                <tr>
                <th>Name</th>
                <th>Instagram Id</th>
                <th>Open Profile</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(item, index) in items" :key="index">
                    <th>{{item.name}}</th>
                    <th>({{item.instaId}})</th>
                    <th><button v-on:click="link(index)" class="btn btn-danger btn-xs">Open</button></th>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
export default {
    data(){
        return{
            items:[
                    {
                    name:'Rupesh',
                    instaId: 'cybersupernova'
                    },
                    {
                    name:'Anil',
                    instaId: 'anil_kumar11432'
                    }
            ]
        }
    },
    methods:{
        link : function(index){
            var lnk = this.items[index].instaId;
            console.log(lnk);
            window.open('https://www.instagram.com/'+lnk);
        }
    }
}
</script>

