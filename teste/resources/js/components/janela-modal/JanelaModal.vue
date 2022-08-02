<script>
export default {
    methods: {
        //Fecha o modal quando usuário clicar no X      
        closeClick() {
            myModal.style.display = "none";
        },
        //Fecha o modal quando usuário clicar em qualquer lugar na janela do browser
        janelaClick(event) {
            if (event.target == myModal) {
                myModal.style.display = "none";
            }
        }
    },
    created: function() {
        window.addEventListener('click',this.janelaClick);
    },
    destroyed: function() {
        window.removeEventListener('click', this.janelaClick);
    } 
}
</script>>