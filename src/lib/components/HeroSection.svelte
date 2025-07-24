<script>
    import bookCover from "$assets/book_cover.png";
    import phoneCover from "$assets/phone_cover.png";
    import {Button} from "$components";
</script>
<section class="hero">
    <div class="hero-showcase text-center bold">
        <h1 class="purple">MOVE TO</h1>
        <h1 class="purple mb-xs">SPAIN</h1>
        <h4 class="italic semi-bold">
            There's no need to make the same mistakes I made
        </h4>
        <img class="book-cover" src={bookCover} alt="">
        <img class="phone-cover" src={phoneCover} alt="">
    </div>

    <div class="hero-text white text-center">
        <h1 class>THIS EBOOK WILL</h1>
        <h1>SAVE YOU MONEY</h1>
        <h1 class="mb-m">TIME & NERES</h1>
        <p class="light-grey mb-l">
            Move to Spain is a practical and inspiring guide for anyone dreaming of starting a new life under the 
            Spanish sun. Whether you're relocating for work, retirement, or simply seeking a lifestyle change,
            this book walks you through everything from visa requirements and finding a home 
            culture and learning the language. With personal stories and expert tip.
           
        </p>
        <Button> Purchase E-book for 10$</Button>
    </div>
</section>

<style>
    .hero{
        display: flex;
        height: 100vh;
        overflow-y: hidden;
    }
    .hero-showcase{
        position: relative;
        width: 50%;
        padding: 100px 16px 0 16px;
        background: linear-gradient(
            135deg,
            #e2cbff,
            #e2cbff 25%,
            #deeaff 50%,
            #deeaff 75%,
            #927bce
        );
    }
    .hero-text{
        padding: 100px 5%;
        width: 50%;
        background-color:black;
    }
    .book-cover{
        position: absolute;
        right: 2%;
        bottom: 0%;
        width: 65%;
        transform: translateY(30%);
    }
    .phone-cover{
        position: absolute;
        width: 35%;
        bottom: 0;
        right: 52%;
        transform: translateY(25%);
    }
</style>