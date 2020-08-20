<template>
    <div>
        <p>HP Player {{randomDamage(1,3)}} 
                {{ player[randomDamage(0,3)-1].name}}</p> +รูป
        <p>HP Monster 150 </p> +รูป
        <button @click="start()">Start</button>
        <button @click="attack()">Attack</button>
        <hr />
            name = {{aPlayer.name}}
            HP = {{aPlayer.HP}}
            image = {{aPlayer.image}}
        <hr />
     </div>
</template>

   
    <script>
    export default {
        data:function(){
            return{
                aPlayer{ name: '', HP :  ,image: ''
                }
                //ชื่อ player[1].name
                Player : [{name:'Suneo',HP : 100, image: 'a' },
                    {name:'Jaian',HP : 150, image: 'd'  },
                    {name:'Nobita',HP : 120, image: 'c'  },
                    {name:'Doraemon',HP : 160, image: 'a'  },
                    {name:'Shizuka',HP : 80, image: 'a'  }],

                Monster : [{name:'ชื่อมอน1',HP : 50, image: 'a' },
                    {name:'ชื่อมอน2',HP : 60, image: 'a' },
                    {name:'ชื่อมอน2',HP : 100, image: 'a' }]
            }
        }
    },
    methods:{
        randomDamage: function(min, max) {
            return Math.max(Math.floor(Math.random() * max) + 1, min);
        },
        start:function(){
            // 1. random player 1-5 -->ชื่อ HP รูป
            thisaPlayer=this.player[this.randomDamage(1, 3) - 1] // {...}

            // 2. random Monster 1-3 -->ชื่อ HP รูป
        }
        attack:function(){
            // 1.player --> monster
            // 2.player <-- monster
            // 3.player.HP <=0  ===>?
            // 4.monster.HP <=0  ===>?
            // 5. END GAME
        }
    }
    
    
    </script>



