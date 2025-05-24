
Per adesso ho deciso di levare la classe Wetlands.
Nella classe dataset ho calcolato ndvi e ndwi e inizialmente li avevo concatenati al canale RGB dell'immagine, ma veniva un canale di dimensione 5 e avevo problemi con DeepLabV3 perché
accetta canali RGB di dimensione 3, e quindi non sapevo come usare i dati di ndvi e ndwi
Per adesso ho problemi di overfitting
