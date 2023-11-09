
<script>
    import Profile from '../assets/images/profile.jpg'
    let city='<b>Delhi</b>'
    let user=
    [
        {
        img:Profile,
        name:"Sonali More",
        email:"Sonali.more@gmail.com"
    },
    {
        img:"https://cdn.imgbin.com/0/4/8/imgbin-computer-icons-user-profile-encapsulated-postscript-young-zw13f7LRFRB0d8qpK53VMFcGX.jpg",
        name:"Sonali kale",
        email:"Sonali.kale@gmail.com"
    },
    {
        img:"https://w7.pngwing.com/pngs/517/749/png-transparent-computer-icons-user-profile-avatar-woman-young-child-face-black-hair.png",
        name:"Poojsa More",
        email:"Pooasa.kale@gmail.com"
    },
    {
        img:"https://e7.pngegg.com/pngimages/694/639/png-clipart-computer-icons-user-profile-female-symbol-miscellaneous-purple.png",
        name:"SonKunalali More",
        email:"Kunal.kale@gmail.com"
    }
    ];
    </script>
    
    <div>
        {#each user as user1}
        <p>new loop</p>
    <img src="{user1.img}"/>
    <h1>Name: {user1.name}</h1>
    <p>Email:: {user1.email}</p>
  <p>{@html city}</p>
    {/each}
    
    </div>

    export default Users;