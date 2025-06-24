// Office data - combining both sets of numbers
const offices = [
    // KM Express numbers
    { name: "UK Main Office", phone: "+44 775 254 3300", type: "uk" },
    { name: "Baghdad", phone: "+964 772 358 0202", type: "iraq" },
    { name: "Hawler (Erbil)", phone: "+964 750 509 8484", type: "iraq" },
    { name: "Slemani", phone: "+964 770 509 4242", type: "iraq" },
    { name: "Duhok", phone: "+964 750 509 7272", type: "iraq" },
    { name: "Kirkuk", phone: "+964 770 034 0505", type: "iraq" },
    { name: "Halabja Shahid", phone: "+964 770 822 8989", type: "iraq" },
    { name: "Raniya", phone: "+964 770 508 6464", type: "iraq" },
    { name: "Kalar", phone: "+964 772 358 0303", type: "iraq" },
    { name: "IRAQ Main Office", phone: "+964 772 358 0101", type: "iraq" },
    { name: "Koya", phone: "+964 776 442 2018", type: "iraq" },
    { name: "Soran", phone: "+964 776 442 2017", type: "iraq" },
    { name: "Said Sadiq", phone: "+964 771 166 7272", type: "iraq" },
    { name: "Zakho", phone: "+964 750 119 1473", type: "iraq" },
    { name: "Chamchamal", phone: "+964 773 600 5757", type: "iraq" },
    { name: "Halabja Taza", phone: "+964 770 822 8181", type: "iraq" },
    { name: "Qaladze", phone: "+964 773 300 6464", type: "iraq" },
    { name: "Darbandikhan", phone: "+964 770 822 8585", type: "iraq" },
    
    // Iraq Distribution Offices numbers
    { name: "Baghdad Distribution", phone: "+964 773 034 0505", type: "iraq" },
    { name: "Hawler (Erbil) Distribution", phone: "+964 751 543 0090", type: "iraq" },
    { name: "Slemani Distribution", phone: "+964 771 233 0049", type: "iraq" },
    { name: "Duhok Distribution", phone: "+964 750 119 1473", type: "iraq" },
    { name: "Kirkuk Distribution", phone: "+964 770 034 0505", type: "iraq" },
    { name: "Halabja Shahid Distribution", phone: "+964 770 822 8989", type: "iraq" },
    { name: "Raniya Distribution", phone: "+964 750 034 0505", type: "iraq" },
    { name: "Kalar Distribution", phone: "+964 772 358 0303", type: "iraq" },
    { name: "IRAQ Main Distribution", phone: "+964 770 509 4242", type: "iraq" },
    { name: "Koya Distribution", phone: "+964 776 442 2018", type: "iraq" },
    { name: "Soran Distribution", phone: "+964 776 442 2017", type: "iraq" },
    { name: "Said Sadiq Distribution", phone: "+964 771 166 7272", type: "iraq" },
    { name: "Zakho Distribution", phone: "+964 750 119 1473", type: "iraq" },
    { name: "Chamchamal Distribution", phone: "+964 773 600 5757", type: "iraq" },
    { name: "Halabja Taza Distribution", phone: "+964 770 822 8181", type: "iraq" },
    { name: "Qaladze Distribution", phone: "+964 773 300 6464", type: "iraq" },
    { name: "Darbandikhan Distribution", phone: "+964 770 822 8585", type: "iraq" }
];

// Generate office cards
function generateOfficeCards(filteredOffices = offices) {
    const container = document.getElementById('officesContainer');
    container.innerHTML = '';
    
    if (filteredOffices.length === 0) {
        container.innerHTML = '<div class="no-results">No offices found matching your search. Please try another term.</div>';
        return;
    }
    
    filteredOffices.forEach(office => {
        const card = document.createElement('div');
        card.className = 'office-card';
        
        // Clean phone number for WhatsApp link
        const cleanedPhone = office.phone.replace(/[^0-9+]/g, '');
        const whatsappLink = `https://wa.me/${cleanedPhone}`;
        
        // Determine icon based on location type
        const iconClass = office.type === 'uk' ? 'fas fa-flag-uk' : 'fas fa-flag';
        
        card.innerHTML = `
            <div class="card-header">
                <i class="${iconClass}"></i>
                ${office.name}
            </div>
            <div class="card-body">
                <a href="${whatsappLink}" class="phone-link" target="_blank">
                    <i class="fab fa-whatsapp"></i> ${office.phone}
                </a>
            </div>
        `;
        
        container.appendChild(card);
    });
}

// Search function
function searchOffices() {
    const searchTerm = document.getElementById('searchInput').value.toLowerCase();
    const filtered = offices.filter(office => 
        office.name.toLowerCase().includes(searchTerm) || 
        office.phone.includes(searchTerm)
    );
    generateOfficeCards(filtered);
}

// Initialize on page load
document.addEventListener('DOMContentLoaded', () => {
    generateOfficeCards();
    
    // Live search as user types
    document.getElementById('searchInput').addEventListener('input', searchOffices);
    
    // Also search on Enter key
    document.getElementById('searchInput').addEventListener('keyup', (e) => {
        if (e.key === 'Enter') {
            searchOffices();
        }
    });
});
