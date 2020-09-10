---
description: Para crear el proyecto y otorgar permisos
---

# Configurar Proyecto Firebase

{% embed url="https://www.loom.com/share/e0c7c50b100746e28c929c39f96d72d1" %}

## Create Realtime DB

{% embed url="https://www.loom.com/share/31fdd113b0304124979277c22b267991" %}

#### Código para ingresar en REAL TIME DATABASE

```text
{  
  "rules": {  
    ".read": true,  
     ".write": "auth !== null"  
  }  
}
```

## Crear  Base de dato Firestore

{% embed url="https://www.loom.com/share/fef572a8964340d1a23f77f85b4a8191" %}

#### Copiar esta regla en la base de dato Firestore

```text
rules_version = '2'; 
service cloud.firestore { 
  match /databases/{database}/documents {
    match /{document=**} {
      allow  read: if true;
      allow  write: if request.auth.uid != null;
    }
  }
}
```

