<template>     
        <div class="nivelcontacto">
            <div class="cuadroTxt">
                <h1>Contactanos</h1>
                <article> <br>
                    Somos una empresa familiar 100% mexicana, con experiencia en la confección de prendas de vestir para dama, caballero y niña. 
                    <br> <br> Con textiles de la más alta calidad, elaborados especialmente en manta, lino o combinada con otras texturas que puede ser algodón, en sus diferentes presentaciones.    
                    <br><br> <h2>Pagina de facebook</h2>  
                    <a  class="contactw" href="https://www.facebook.com/share/1BGRPAc49i/" target="_blank">
                        <img id="insta" src="./kubyhe/faceboock.svg.webp" alt="" />
                         facebook.com/CreacionesKubyHe 
                         <img id="insta" src="./kubyhe/faceboock.svg.webp" alt="" />
                    </a>
                    <br>
                    <h2>Teléfonos</h2> 
                    TEL. 22-82-09-32-57   y   22-88-43-82-94 <br>  XALAPA, VER. 
                    <br><br>  Whatsapp 
                    <a  class="" :href="'https://wa.me/522282093257/?text=Hola,%20quiero%20saber%20más%20sobre%20la%20ropa%20de%20manta'" target="_blank">
                       22 82 09 32 57 <br> <img id="insta" src="./kubyhe/whatsp.png" alt="" />
                        </a>
                    <h2> Correo Electrónico </h2> E-mail: <a href="mailto:kubota_pintor@hotmail.com"  target="_blank">kubota_pintor@hotmail.com</a>   y <a href="mailto:kubyhe@hotmail.com"  target="_blank">kubyhe@hotmail.com</a> 
                </article>
            </div>

        
            <div class="contactw">
            <a  class="contactw" href="mailto:kubyhe@hotmail.com" target="_blank"> <img id="insta" src="./kubyhe/gmail.svg" alt="" /></a>
            <a  class="contactw" href="https://www.facebook.com/share/1YAXtry3qM/" target="_blank"> <img id="insta" src="./kubyhe/faceboock.svg.webp" alt="" /></a>
            <a  class="contactw" :href="'https://wa.me/522282093257/?text=Hola,%20quiero%20saber%20más%20sobre%20la%20ropa%20de%20manta'" target="_blank"> <img id="insta" src="./kubyhe/whatsp.png" alt="" /></a>
            </div>
        </div>
</template>

<script>
export default{
    name: 'contactoK',
    };

</script>


<style scoped>
    #whatsappn {
        width: auto;
        height: 25px;
    }

    #insta {
        width: auto;
        height: 45px;
    }

    .contactw {
        display: flex;
        flex-wrap: wrap;
        padding: 5px;
        justify-content: center;
        align-content: center;
        align-items: center;
        color: #fff !important;
        font-size: 20px;
        font-weight: 500;
        border-radius: 0.5em 1.2em;
        background: #318aac;
        position: relative;
        border: 2px solid #318aac;
        outline: 2px solid;
        outline-color: rgba(49, 138, 172, 0.4);
        transition: all 1s cubic-bezier(0.19, 1, 0.22, 1);
       }
    
       .contactw:hover{
        box-shadow: inset 0 0 20px rgba(49, 138, 172, 0.5), 0 0 20px rgba(49, 138, 172, 0.4);
        outline-color: rgba(49, 138, 172, 0);
        outline-offset: 80px;
        text-shadow: 1px 1px 6px #fff;
        }

.nivelcontacto {
    display: flex;
    flex-direction: column;
    justify-content: center;
}
.cuadroTxt {
  border: solid 1px;
  border-radius: 0.8em;
  background:rgba(201, 201, 201, 0.56);
  padding: 15px;
}

</style>