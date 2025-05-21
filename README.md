problemi che ho avuto:
Nella classe del dataset ho fatto img_data = img.read().astype(np.float32) / 10000
per portare i valori di img_data.min(), img_data.max() tra 0 e 1 e poi ho usato la funzione def compute_mean_std(dataset)
per calcolare i mean e std. Poi quando utilizzo questi valori nella Normalizzazione, purtroppo mi vengono Mean per channel after transform: tensor([-2.4104, -2.8151, -2.3245])
Std per channel after transform: tensor([0.0077, 0.0064, 0.0059]).
Per adesso ho deciso di levare la classe Wetlands.
Nella classe dataset ho calcolato ndvi e ndwi e inizialmente li avevo concatenati al canale RGB dell'immagine, ma veniva un canale di dimensione 5 e avevo problemi con DeepLabV3 perché
accetta canali RGB di dimensione 3, e quindi non sapevo come usare i dati di ndvi e ndwi
