Ho fatto vari train tra le 20-25-30 epoche: sono partito da un train normale senza bilanciamento della loss con i class weights, poi li ho aggiunti ed ho notato che la MiOu si è alzata.
Ho provato aggiugendo un'altra augmentation (A.GridDistortion(p=0.2)) ed ho provato a tenere la size attuale delle immagini (1024) e anche con 512 e 256.
Volevo usare altre backbone come ResNet50 (Troppo pesante), Resnet18 o EfficientNet, ma l'ho trovate pesanti e mi ci sarebbe voluto troppo tempo.
L'ultima prova che ho fatto è stata un lo scheduler con parametri step_size=5, gamma=0.5.
In generale ho ottenuto una MiOu finale di 0.4.
