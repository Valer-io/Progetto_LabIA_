Ho fatto vari train tra le 20-25-30 epoche: sono partito da un train normale senza bilanciamento della loss con i class weights, poi li ho aggiunti ed ho notato che la MiOu si è alzata.
Ho provato aggiugendo un'altra augmentation (A.GridDistortion(p=0.2)) ed ho provato a tenere la size attuale delle immagini (1024) e anche con 512 e 256.
Volevo usare altre backbone come ResNet50 (Troppo pesante), Resnet18 o EfficientNet, ma l'ho trovate pesanti e mi ci sarebbe voluto troppo tempo.
L'ultima prova che ho fatto è stata un lo scheduler con parametri step_size=5, gamma=0.5.
In generale ho ottenuto una MiOu finale di 0.4.
Dentro la cartella "prove" ci stanno le 5 prove in ordine, del notebook
Nel progetto vecchio avevo messo "max_pixel_value=1.0" perché così ottenevo dei valori di mean e std migliore, adesso l'ho levato ed ho usato "image = self.normalize(image)" direttamente nel __getitem__
