document.addEventListener('DOMContentLoaded', () => {
    const gameBoard = document.getElementById('game-board');

    // Crear cartas
    for (let i = 0; i < 12; i++) {
        const card = document.createElement('div');
        card.classList.add('card');
        card.textContent = '🂠'; // Puedes reemplazar esto con imágenes de cartas
        gameBoard.appendChild(card);

        // Agregar evento para mover la carta
        card.addEventListener('click', () => {
            card.style.position = 'absolute';
            card.style.top = `${Math.random() * 350}px`;
            card.style.left = `${Math.random() * 550}px`;
        });
    }
});
