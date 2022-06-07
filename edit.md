for css referencing before placing scss implementation


main{
    width: 100%;
    height: 80vh;
    display: flex;
    justify-content: center;
    align-items: center;
}
.main-container{
    width: 90%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
}
.section1{
    position: relative;
    height: 60%;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}
.section1 .img1,.img3,.img3{
    width: 100%;
    height: 100%;
    position:absolute;
    top: 0;
    left: 0;
}
.section2{
    color: #1DB954;
    animation: done 1s ease-out 12s 1 normal forwards ;
}    
.ball-slider{
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
    gap: 1vw;

}
.ball-slider span{
    width: 5%;
    height:40%;
    background-color: #9BADA2;
    border-radius: 50%;
}
.final-img{
    position: absolute;
    top: 0;
    display: flex;
    gap: 2vw;
    opacity: 0;
    animation: final 3s ease-in 12s 1 normal forwards;
}
.final-img img:hover{
    transition-duration: 0.2s;
    transition-timing-function: ease-in;
    transition-property: border;
    border-radius: 16px;
    border: 3px solid #1DB954;
}
.final-img :nth-child(2):hover{
    border: 3px solid #A52A2A;
}
.img1{
    opacity: 0;
    /* animation: name duration timing-function delay iteration-count direction fill-mode; */
    animation: slide1 3s ease-in 1 normal backwards;
}
.img2{
    opacity: 0;
    animation: slide 4s ease-in 3s 1 normal backwards;
}
.img3{
    opacity: 0;
    animation: slide 4s ease-in 7s 1 normal backwards;
}
.ball1{
    animation: ball 3s ease-in 1 normal forwards;
}
.ball2{
    animation: ball 4s ease-in 3s 1 normal forwards;
}
.ball3{
    animation: ball 4s ease-in 7s 1 normal forwards;
}

@keyframes slide1{
    0%{
        opacity: 1;
        transform: translateX(-20px);
    }
    50%{
        opacity: 1;
    }
    100%{
        opacity: 0;
        transform: translateX(20px);
    }
}

@keyframes slide{
    0%{
        opacity: 0;
        transform: translateX(-20px);
    }
    50%{
        opacity: 1;
        transition-duration: 1s;
    }
    100%{
        opacity: 0;
        transform: translateX(20px);
        transition-duration: 1s;

    }
}    
    @keyframes final{
        from{
            opacity: 0;
        }
        to{
            opacity: 1;
        }
        
    }

    @keyframes ball{
        0%{
            background-color: #9BADA2;
        }
        50%{
            background-color: #1DB954;
            box-shadow:0 0 3px #1DB954;
            transition-duration: 2s;
            transform: scale(1.2);
        }
        100%{
            background-color: #9BADA2;
            transform: scale(0.5);
            transition-duration: 1s;

        }
        
    }
    @keyframes done{
        to{
            opacity: 0;
            transition-duration: 2s;
        }
    }
    @media (max-width:600px){
        body{
            height: 100vh;
        }
        .final-img{
            flex-direction: column;
        }   
        .ball-slider{
            gap: 3vw;
        }    
    }