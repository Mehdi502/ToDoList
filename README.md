# ToDoList

### 📌 **Backend : Spring Boot + PostgreSQL**  
#### 1️⃣ **Modélisation des entités**  
- **List** (`id`, `name`, `createdAt`)  
- **Task** (`id`, `title`, `description`, `dueDate`, `priority`, `status`, `listId`, `createdAt`)  

#### 2️⃣ **Endpoints REST API**  
🔹 **Listes** (`/lists`)  
- `GET /lists` → Récupérer toutes les listes  
- `POST /lists` → Créer une liste  
- `PUT /lists/{id}` → Modifier une liste  
- `DELETE /lists/{id}` → Supprimer une liste  

🔹 **Tâches** (`/tasks`)  
- `GET /tasks?listId={id}&sort={field}&filter={status}` → Récupérer et filtrer  
- `POST /tasks` → Ajouter une tâche  
- `PUT /tasks/{id}` → Modifier une tâche  
- `DELETE /tasks/{id}` → Supprimer une tâche  

### **Stack technique**  
- Spring Boot (Web, Data JPA)  
- PostgreSQL  
- Spring Security (si auth future)  


### 📌 **Frontend : Angular + Angular Material**  

#### 1️⃣ **Technologies**  
- **Framework** : Angular (TypeScript)  
- **UI** : Angular Material  
- **Gestion des états** : RxJS  
- **Communication avec l’API** : `HttpClientModule`  

#### 2️⃣ **Pages et Composants**  
🔹 **Page des listes**  
- Affichage des listes  
- Tri des listes  

🔹 **Page des tâches d’une liste**  
- Affichage des tâches d’une liste  
- Tri des tâches (par date, priorité)  
- Filtrage des tâches (statut : "à faire", "en cours", "terminée")  

#### 3️⃣ **Architecture des services**  
- `ListService` : Gestion des listes (CRUD)  
- `TaskService` : Gestion des tâches (CRUD + tri/filtrage)  
