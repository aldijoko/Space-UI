<script>

</script>

<footer>
    <div class="cont-foot">
        <div class="footer-photo">
            <img class="img-footer" src="./img/astronout.png" alt="">
        </div>
        <div class="content-footer">
            <h1>Exploration</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Placerat id potenti faucibus nec, rhoncus, vulputate</p>
            <img class="vector" src="./img/vector2.svg" alt="">
        </div>
        <div class="foot-footer">
            <h1>Footprint</h1>
            <p>
                Lorem ipsum dolor sit amet, consectetur 
            </p>
        </div>
    </div>
    <div class="cont-foot">
        <div class="footer-photo">
            <img class="img-footer" src="./img/astronout.png" alt="">
        </div>
        <div class="content-footer">
            <h1>Exploration</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Placerat id potenti faucibus nec, rhoncus, vulputate</p>
            <img class="vector" src="./img/vector2.svg" alt="">
        </div>
        <div class="foot-footer">
            <h1>Footprint</h1>
            <p>
                Lorem ipsum dolor sit amet, consectetur 
            </p>
        </div>
    </div>
    
    

    
</footer>
<div class="footer-mobile">
    <img class="img-mobile" src="./img/astronout.png" alt="">
    <div class="content-mobile">
        <h1>Exploration</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing </p>
        <img class="vector" src="./img/vector2.svg" alt="">
    </div>
   
</div>

<style>
    footer {
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        background-color: black;
        height: auto;
        /* padding: 30px; */
    }

    .cont-foot {
        display: flex;
    }

    h1{
        font-size: 24px;
        line-height: 36px;
        font-weight: 700;
    }

    p{
        font-weight: 500;
        font-size: 18px;
        line-height: 31.5px;
    }

    .footer-photo {
        height: 100%;
        width: 30%;
        display: flex;
        justify-content: center;
        align-items: center;
        padding-left: 50px;
    }

    .img-footer{
        height: 255px;
        width: 100%;
        padding-left: 50px;
    }

    .content-footer {
        position: relative;
        color: var(--pure-white);
        width: 40%;
        padding: 0px 100px;
        /* background-color: aqua; */
    }
    
    .vector {
        position: absolute;
        top: 160px;
        right: 0px;
        cursor: pointer;
        transition: all .2s ease-in-out;
    }

    .vector:hover{
        transform: scale(1.5);
    }


    .foot-footer {
        color: var(--pure-white);
        width: 30%;
        margin-left: 50px;

    }

    .footer-mobile {
        display: none;
    }

    cont-foot {
        display: none;
    }

    .content-mobile {
        display: none;
    }

    @media screen and (max-width: 768px) {

        footer {
            display: none;
        }
		.footer-photo, .content-footer, .foot-footer {
            display: none;
        }
        
        .footer-mobile {
            display: flex;
            width: 100%;
            height: 187px;
            background-color: black;
            color: var(--pure-white);
        }

        .footer-mobile h1 {
            font-size: 16px;

        }

        .content-mobile {
            position: relative;
            padding: 10px;
            display: flex;
            flex-direction: column;
        }

        .img-mobile {
            margin-left: 20px;
            width: 238px;
            height: 187px;
        }

	}
</style>