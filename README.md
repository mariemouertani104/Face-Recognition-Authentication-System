# Face Recognition Authentication System

Un système d'authentification par reconnaissance faciale avec détection de vivacité (Liveness Detection) développé dans le cadre d'un projet personnel.

## 🎯 Objectif
Reconnaître une personne pour autoriser l'accès en utilisant des **face embeddings** et détecter si c'est un vrai humain ou une photo/écran (Liveness Detection via Eye Aspect Ratio).

## 🛠️ Technologies utilisées
- **face_recognition** (basé sur FaceNet + dlib)
- OpenCV
- dlib (pour les landmarks faciaux)
- Google Colab (développement)
- Python

## ✨ Fonctionnalités
- Enregistrement des embeddings faciaux
- Reconnaissance faciale en temps réel
- Liveness Detection (détection de clignement des yeux)
- Interface simple via webcam ou image uploadée

## ⚠️ Limitations importantes

- **Sensibilité à l'angle et à la pose** : Le système fonctionne bien uniquement lorsque le visage est présenté dans un angle proche de celui de la photo d'enregistrement. Des variations importantes d'angle, d'éclairage ou d'expression réduisent fortement la précision de reconnaissance.
- **Une seule photo par utilisateur** : Contrairement aux systèmes professionnels qui utilisent plusieurs photos par personne, ce projet utilise actuellement une seule photo d'enregistrement. Cela limite la robustesse.
- **Liveness Detection** : Fonctionne correctement uniquement lorsque l'utilisateur cligne volontairement des yeux pendant la capture. Sur des photos statiques, le système peut souvent détecter "Fake".
- Performance dépendante de l'éclairage et de la qualité de la caméra.


## 🚀 Comment utiliser

### Sur Google Colab
1. Ouvrir le notebook `Face_Recognition_Colab.ipynb`
2. Exécuter les cellules dans l'ordre
3. Ajouter votre photo dans la base
4. Tester avec la webcam (cligner des yeux pendant la capture)

### En local
```bash
pip install -r requirements.txt
python face_auth.py

###Made with ❤️ using face_recognition

