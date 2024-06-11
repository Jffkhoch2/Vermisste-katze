document.getElementById('cat-form').addEventListener('submit', function(event) {
    event.preventDefault();

    const name = document.getElementById('name').value;
    const date = document.getElementById('date').value;
    const location = document.getElementById('location').value;
    const description = document.getElementById('description').value;

    const catCard = document.createElement('div');
    catCard.className = 'cat-card';
    catCard.innerHTML = `
        <h2>${name}</h2>
        <p><strong>Vermisst seit:</strong> ${date}</p>
        <p><strong>Ort:</strong> ${location}</p>
        <p><strong>Beschreibung:</strong> ${description}</p>
    `;

    document.getElementById('cat-list').appendChild(catCard);

    document.getElementById('cat-form').reset();
});
