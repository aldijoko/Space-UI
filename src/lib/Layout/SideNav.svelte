<script>
    
</script>

<div class="side-bar">
    <div class="side-logo">
        <a href="">
            <h1>Xae</h1>
        </a>
    </div>
    <div class="side-sosmed">
        <ul>
            <li>
                <a href="#" >
                    <img style="width: 20px; height: 20px;" src="./img/IconSocialFacebook.svg" alt="" />
                </a>
            </li>
            <li>
                <a href="#" >
                    <img style="width: 20px; height: 20px;" src="./img/IconSocialInstagram.svg" alt="" />
                </a>
            </li>
            <li>
                <a href="#" >
                    <img style="width: 20px; height: 20px;" src="./img/IconSocialTwitter.svg" alt="" />
                </a>
            </li>
        </ul>
    </div>
</div>

<style>
    .side-bar {
        position: fixed;
        top: 0;
        z-index: 1;
        width: 161px;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        /* border: 1px solid #FFFFFF; */
        border-right: 1px solid var(--pure-white);
    }

    .side-logo a {
        text-decoration: none;
    }

    .side-logo h1 {
        font-family: 'Poppins', sans-serif;
        font-weight: 700;
        font-size: 48px;
        color: var(--pure-white);
        text-align: center;
        transition: all .5s ease-in-out;
    }

    .side-sosmed {
        width: 100%;
        color: var(--pure-white);
        padding: 25px;
    }

    .side-sosmed ul{
     list-style: none;
    }

    .side-sosmed ul li{
        margin: 2em 0;
    }

    .side-logo h1:hover{
        /* text-decoration: underline; */
        transform: scale(1.5);
    }

    .side-sosmed img:hover{
        transform: scale(1.5);
    }
</style>