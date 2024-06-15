# Sobat Tani Backend Documentation
# Prerequisites
# Installation
# Configuration
# Database Schema
# Documentation API 
API Backend App Sobat Tani (Auth User, Bookmark, Status, Detail Plant)
# 📁 Folder: root 
## End-point: root
### Method: GET
>```
>/
>```

⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
# 📁 Folder: User Auth 
## Register User Information

Retrieves information about a specific user.

### Request

- Method: `POST`
    
- URL: `/register`
    
- Headers:
    
    - `Authorization: Bearer`
      
### Body (**raw**)

```json
{
    "name": " C241-PS007",
    "email": "sobattani@gmail.com",
    "password": "securepassword01234"
}
```

### Response: 200
```json
{
    "message": "Success"
}
```

### Response: 400
```json
{
    "message": "Masukkan Email dengan benar"
}
```

### Response: 400
```json
{
    "message": "Masukkan Password"
}
```

### Response: 400
```json
{
    "message": "Email telah terdaftar"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
# Login

Retrieves a JWT token and user information for an authenticated user

### Request

- Method: `POST`
    
- URL: `/auth/login`
    
- Headers:
    
    - `Authorization`: `Bearer`
      
### Body (**raw**)

```json
{
    "email": "sobattani@gmail.com",
    "password": ""
}
```

### Response: 200
```json
{
    "message": "Success",
    "data": {
        "uid": "3AH1fnwLBXNjibPkon1EcWor9mG2",
        "name": " C241-PS007",
        "email": "sobattani@gmail.com"
    },
    "token": "<your-example-key>"
}
```

### Response: 400
```json
{
    "message": "Password salah"
}
```

### Response: 400
```json
{
    "message": "Masukkan Email dengan benar"
}
```

### Response: 400
```json
{
    "message": "Password is required"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
# Update User Information

Updates the profile information of an authenticated user  

Request

- Method: `PUT`
    
- URL: `/auth/user`
    
- Headers:
    
    - `Authorization`: `Bearer`

### Body (**raw**)

```json
{
   "name": " C241-PS007new",
    "password": "securepassword01234"
}
```

### Response: 200
```json
{
    "message": "Success",
    "data": {
        "uid": "2aoGXnj8OETqgCTa3B6J3LWdaaU2",
        "email": "SobatTaniTest23@gmail.com",
        "name": " C241-PS007"
    }
}
```

### Response: 200
```json
{
    "message": "Success",
    "data": {
        "uid": "2aoGXnj8OETqgCTa3B6J3LWdaaU2",
        "email": "SobatTaniTest23@gmail.com",
        "name": " C241-PS007new"
    }
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
# Get User Details

Retrieves detailed information of the authenticated user

### Request

- Method: `GET`
    
- URL: `/auth/user`
    
- Headers:
    
    - `Authorization`: `Bearer`

### Response: 200
```json
{
    "message": "success",
    "data": {
        "uid": "3AH1fnwLBXNjibPkon1EcWor9mG2",
        "name": " C241-PS007",
        "email": "sobattani@gmail.com"
    }
}
```

### Response: 400
```json
{
    "message": "Invalid token!"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
# 📁 Folder: Bookmark 

# Add Bookmark

Uploads an image and creates a bookmark entry for a plant disease

### Request

- Method: `POST`
    
- URL: `/bookmark`
    
- Headers:
    
    - `Authorization`: `Bearer`
        
    - `Content-Type : multipart/form-data`

### Body formdata

|Param|value|Type|
|---|---|---|
|nama_tanaman|penyakit jagung|text|
|jenis_penyakit|ini adalah description|text|
|image|/C:/Users/Fanissa Azzahra/Downloads/data-test-submissions/bad-request.jpg|file|
|||text|


### Response: 201
```json
{
    "message": "Succcess",
    "data": {
        "id": "7g7gqdIHrMWdGm3y2p9S",
        "userId": "2aoGXnj8OETqgCTa3B6J3LWdaaU2",
        "nama_tanaman": "penyakit jagung",
        "jenis_penyakit": "ini adalah description",
        "imageUrl": "https://storage.googleapis.com/sobat-tani-project-425607.appspot.com/bookmark-image/6f0f35e3-8481-4c38-a1cf-72f1ab870c28.jpg",
        "timestamp": {}
    }
}
```

### Response: 400
```json
{
    "message": "Nama Tanaman tidak ditemukan"
}
```

### Response: 400
```json
{
    "message": "Penyakit Tanaman tidak ditemukan"
}
```

### Response: 400
```json
{
    "message": "Gambar tidak ditemukan"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

# Get All Bookmarks

Retrieves all bookmark entries for the authenticated user

Request

- Method: `GET`
    
- URL: `/bookmark/`
    
- Headers:
    
    - `Authorization`: `Bearer`

### Response: 404
```json
{
    "message": "BookMark tidak ditemukan!"
}
```

### Response: 200
```json
{
    "message": "Succecss",
    "data": [
        {
            "id": "2aGYVzhYJ9Gd0uMjfhZ0",
            "nama_tanaman": "penyakit jagung",
            "jenis_penyakit": "ini adalah description",
            "imageUrl": "https://storage.googleapis.com/sobat-tani-project-425607.appspot.com/bookmark-image/ef6695c6-c5a1-485c-82d2-cb9accc1ffaa.jpg",
            "userId": "2aoGXnj8OETqgCTa3B6J3LWdaaU2",
            "timestamp": "2024-06-09 15:20:30"
        },
        {
            "id": "2ovGUXcOgS2Cy8rSK3xA",
            "nama_tanaman": "Bambu Terbang",
            "jenis_penyakit": "demam bambu",
            "imageUrl": "https://storage.googleapis.com/sobat-tani-project-425607.appspot.com/bookmark-image/83fbecb1-76c7-4a05-b9a9-fb6bab37f6cf.jpg",
            "userId": "2aoGXnj8OETqgCTa3B6J3LWdaaU2",
            "timestamp": "2024-06-09 13:51:27"
        },
        {
            "id": "7g7gqdIHrMWdGm3y2p9S",
            "nama_tanaman": "penyakit jagung",
            "jenis_penyakit": "ini adalah description",
            "imageUrl": "https://storage.googleapis.com/sobat-tani-project-425607.appspot.com/bookmark-image/6f0f35e3-8481-4c38-a1cf-72f1ab870c28.jpg",
            "userId": "2aoGXnj8OETqgCTa3B6J3LWdaaU2",
            "timestamp": "2024-06-09 15:16:06"
        }
    ]
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

# Get Bookmark By ID

### Retrieves a specific bookmark entry by its ID  
  
Request

- Method: `GET`
    
- URL: `/bookmark/:id`
    
- Headers:
    
    - `Authorization`: `Bearer`

### Response: 200
```json
{
    "message": "Success",
    "data": {
        "id": "7g7gqdIHrMWdGm3y2p9S",
        "nama_tanaman": "penyakit jagung",
        "jenis_penyakit": "ini adalah description",
        "imageUrl": "https://storage.googleapis.com/sobat-tani-project-425607.appspot.com/bookmark-image/6f0f35e3-8481-4c38-a1cf-72f1ab870c28.jpg",
        "userId": "2aoGXnj8OETqgCTa3B6J3LWdaaU2",
        "timestamp": "2024-06-09 08:16:06"
    }
}
```

### Response: 404
```json
{
    "message": "Bookmark tidak ditemukan!"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

# Delete Bookmark By ID

Deletes a specific bookmark entry by its ID

### Request

- Method: `DELETE`
    
- URL: `/bookmark/delete/:id`
    
- Headers:
    
    - `Authorization`: `Bearer`

### Response: 200
```json
{
    "message": "Bookmark berhasil dihapus"
}
```

### Response: 404
```json
{
    "message": "Bookmark tidak ditemukan!"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
# 📁 Folder: Status 


## End-point: addStatus
# Add Status

Uploads an image and creates a status entry for a plant disease

### Request

- Method: POST
    
- URL: `/status`
    
- Headers:
    
    - `Authorization`: `Bearer`
        
    - `Content-Type : multipart/form-data`
### Method: POST
>```
>https://sobat-tani-witgb3votq-et.a.run.app/status
>```
### Headers

|Content-Type|Value|
|---|---|
|Authorization|Bearer <your-example-key>|


### Headers

|Content-Type|Value|
|---|---|
|Content-Type|multipart/form-data|


### Body formdata

|Param|value|Type|
|---|---|---|
|nama_tanaman|Singkong
|text|
|jenis_penyakit|Mosaik|text|
|image|/C:/Users/Fanissa Azzahra/Downloads/data-test-submissions/cancer-2.png|file|


### Response: 201
```json
{
    "message": "Success",
    "data": {
        "id": "J1KySoQ6sePsN2ntoE7R",
        "userId": "2aoGXnj8OETqgCTa3B6J3LWdaaU2",
        "nama_tanaman": "Singkong\n",
        "jenis_penyakit": "Mosaik",
        "imageUrl": "https://storage.googleapis.com/sobat-tani-project-425607.appspot.com/status-image/6ebfe922-4d17-46c6-aa77-0edf65fa1c73.jpg",
        "timestamp": {}
    }
}
```

### Response: 400
```json
{
    "message": "Masukkan Nama Tanaman!"
}
```

### Response: 400
```json
{
    "message": "Masukkan Jenis Penyakit!"
}
```

### Response: 400
```json
{
    "message": "Masukkan gambar Tanaman!"
}
```

### Response: 400
```json
{
    "message": "Invalid token!"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: getAllStatus
# Get All Statuses

Retrieves all status entries

### Request

- Method: GET
    
- URL: `/status`
    
- Headers:
    
    - `Authorization`: `Bearer`
### Method: GET
>```
>https://sobat-tani-witgb3votq-et.a.run.app/status
>```
### Headers

|Content-Type|Value|
|---|---|
|Authorization|Bearer <your-example-key>|


### Body formdata

|Param|value|Type|
|---|---|---|


### Response: 200
```json
{
    "message": "Succecss",
    "data": [
        {
            "id": "J1KySoQ6sePsN2ntoE7R",
            "userId": "2aoGXnj8OETqgCTa3B6J3LWdaaU2",
            "imageUrl": "https://storage.googleapis.com/sobat-tani-project-425607.appspot.com/status-image/6ebfe922-4d17-46c6-aa77-0edf65fa1c73.jpg",
            "nama_tanaman": "Singkong\n",
            "jenis_penyakit": "Mosaik",
            "timestamp": "2024-06-09 08:28:24"
        },
        {
            "id": "QsKIDYj1srBBs0dKJkOA",
            "userId": "SaP0QYo5EgZjBqPew2IReZQUWPD3",
            "imageUrl": "https://storage.googleapis.com/sobat-tani-project-425607.appspot.com/status-image/0c5c5013-129a-45fb-a863-f65707693297.jpg",
            "nama_tanaman": "Rekomendasi obat Penyakit Garis-Garis Coklat (Brown Streak Disease)",
            "jenis_penyakit": "Berikan tanaman nutrisi yang cukup untuk meningkatkan sistem kekebalan tanaman terhadap penyakit. Namun, hindari pemupukan yang berlebihan karena dapat membuat tanaman lebih rentan terhadap serangan penyakit.",
            "timestamp": "2024-06-08 17:34:03"
        },
        {
            "id": "yysaMbE1pLytCL8RFxH4",
            "userId": "SaP0QYo5EgZjBqPew2IReZQUWPD3",
            "imageUrl": "https://storage.googleapis.com/sobat-tani-project-425607.appspot.com/status-image/c1b58a6c-a71f-42c8-90c1-43900eaaabed.jpg",
            "nama_tanaman": "Rekomendasi obat Penyakit Garis-Garis Coklat (Brown Streak Disease)",
            "jenis_penyakit": "Berikan tanaman nutrisi yang cukup untuk meningkatkan sistem kekebalan tanaman terhadap penyakit. Namun, hindari pemupukan yang berlebihan karena dapat membuat tanaman lebih rentan terhadap serangan penyakit.",
            "timestamp": "2024-06-08 17:53:42"
        }
    ]
}
```

### Response: 400
```json
{
    "message": "Invalid token!"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: getStatusById
# Get Status By ID

Retreieves a specific status entry by its ID

### Request

- Method: GET
    
- URL: `/status/:id`
    
- Headers:
    
    - `Authorization`: `Bearer`
### Method: GET
>```
>https://sobat-tani-witgb3votq-et.a.run.app/status/:id
>```
### Headers

|Content-Type|Value|
|---|---|
|Authorization|Bearer <your-example-key>|


### Body formdata

|Param|value|Type|
|---|---|---|


### Response: 404
```json
{
    "message": "status tidak ditemukan!"
}
```

### Response: 200
```json
{
    "message": "Success",
    "data": {
        "id": "J1KySoQ6sePsN2ntoE7R",
        "userId": "2aoGXnj8OETqgCTa3B6J3LWdaaU2",
        "nama_tanaman": "Singkong\n",
        "jenis_penyakit": "Mosaik",
        "imageUrl": "https://storage.googleapis.com/sobat-tani-project-425607.appspot.com/status-image/6ebfe922-4d17-46c6-aa77-0edf65fa1c73.jpg",
        "timestamp": "2024-06-09 08:28:24"
    }
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: deleteStatus
# Delete Status

Deletes a specific status entry by its ID, including the associated image

### Request

- Method: `DELETE`
    
- URL: `/status/:id`
    
- Headers:
    
    - `Authorization`: `Bearer`
### Method: DELETE
>```
>https://sobat-tani-witgb3votq-et.a.run.app/status/:id
>```
### Headers

|Content-Type|Value|
|---|---|
|Authorization|Bearer <your-example-key>|


### Body formdata

|Param|value|Type|
|---|---|---|


### Response: 404
```json
{
    "message": "Status not found"
}
```

### Response: 200
```json
{
    "message": "Success"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
# 📁 Folder: detail-plants 


## End-point: getDetailsPlant
# Get Plant Details

Retrieves details of a plant based on the provided name and disease type

### Request

- Method: `GET`
    
- URL: `/plant-detail`
    
- Headers:
    
    - `Authorization`: `Bearer`
        

### Query Parameters

- `nama_tanaman`: (string) Name of the plant.
    
- `jenis_penyakit`: (string) Type of the disease.
### Method: GET
>```
>https://sobat-tani-witgb3votq-et.a.run.app/plant?nama_tanaman=Singkong&jenis_penyakit=Hawar Bakteri
>```
### Headers

|Content-Type|Value|
|---|---|
|Authorization|Bearer <your-example-key>|


### Query Params

|Param|value|
|---|---|
|nama_tanaman|Singkong|
|jenis_penyakit|Hawar Bakteri|


### Response: 400
```json
{
    "message": "Invalid token!"
}
```

### Response: 400
```json
{
    "message": "Invalid token!"
}
```

### Response: 400
```json
{
    "message": "Invalid token!"
}
```

### Response: 200
```json
{
    "message": "Success",
    "data": [
        {
            "id": "WDTguSlPf6gipOWf8q7H",
            "ciri_ciri": {
                "0": "Daun menguning dan menggulung.",
                "1": "Bercak coklat pada daun yang bisa menyebar ke batang.",
                "2": "Luka pada batang yang mengeluarkan lendir bakteri."
            },
            "nama_tanaman": "Singkong",
            "jenis_penyakit": "Hawar Bakteri",
            "cara_pengobatan": {
                "0": "Penggunaan Bakterisida: Aplikasi bakterisida berbasis tembaga seperti tembaga oksiklorida dapat mengurangi infeksi bakteri.",
                "1": "Sanitasi Lapangan: Menghapus dan membakar bagian tanaman yang terinfeksi untuk mencegah penyebaran.",
                "2": "Penggunaan Benih Bebas Penyakit: Menanam benih yang telah disertifikasi bebas dari bakteri."
            },
            "deskripsi": "Penyakit hawar bakteri pada singkong disebabkan oleh bakteri Xanthomonas axonopodis pv. manihotis. Penyakit ini menyebabkan kerusakan pada daun, batang, dan akar singkong, mengakibatkan daun menguning dan menggulung, serta munculnya bercak-bercak coklat pada daun.",
            "cara_pengobatan_alami": {
                "0": "Penyemprotan Ekstrak Bawang Putih: Bawang putih memiliki sifat antibakteri yang dapat membantu mengurangi populasi bakteri.",
                "1": "Penanaman Varietas Tahan: Memilih varietas singkong yang lebih tahan terhadap hawar bakteri."
            }
        }
    ]
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

# Running the Application
