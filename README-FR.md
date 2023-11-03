## API ChatGPT Gratuit

### Introduction
Cette API ChatGPT Gratuit permet d'utiliser le modèle de génération de texte de manière interactive. Vous pouvez l'utiliser pour créer des chatbots, des assistants virtuels ou d'autres applications de génération de texte.

### Endpoint
Le point de terminaison de cette API est :
```
https://gpt-api-laza.onrender.com/v1/completions
```

### Requête
La requête doit être de type `POST` et doit inclure les paramètres suivants :

1. `type`: Ce paramètre spécifie le type de conversation. Dans cet exemple, le type est défini sur "chat".

2. `content`: Ce paramètre correspond au contenu de la conversation. Il doit être un tableau d'objets avec les paires clé-valeur `from` et `content`. Dans cet exemple, il y a un seul objet avec les valeurs `from: "you"` et `content: "Hello, ceci est un test"`.

#### Exemple de Requête
```
curl -X POST -H "Content-Type: application/json" -d '{
    "type": "chat",
    "content": [
        {
            "from": "you",
            "content": "Hello, ceci est une teste"
        }
    ]
}' https://gpt-api-laza.onrender.com/v1/completions
```

### Génération d'Image

Pour générer une image, vous pouvez passer les paramètres suivants :

1. `type`: Ce paramètre doit être défini sur "image" pour générer une image spécifique.

2. `content`: Ce paramètre correspond au contenu de la conversation pour la génération de l'image. Il doit être un objet avec les paires clé-valeur `from` et `content`. Dans cet exemple, il y a un seul objet avec les valeurs `from: "you"` et `content: "Elon musk"`.

3. `messages`: Ce paramètre spécifie les messages qui accompagnent la génération d'image. Dans cet exemple, le message est "Elon musk".

#### Exemple de Requête pour la Génération d'Image
```
curl -X POST -H "Content-Type: application/json" -d '{
    "type": "image",
    "content": [
        {
            "from": "you",
            "content": "Elon musk"
        }
    ],
    "messages": "Elon musk"
}' https://gpt-api-laza.onrender.com/v1/completions
```

### Réponse
La réponse de l'API sera un objet JSON

### Auteur
Email: <a href="mailto:lazaniaina13@gmail.com">Laza</a>
