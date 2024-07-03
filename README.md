# Firebase Go CRUD Documentation
The firebase-go-crud.go file provides an interface for interacting with Firebase Firestore to perform CRUD (Create, Read, Update, Delete) operations on documents.

## Structure
The file defines a FirebaseClient structure that encapsulates a Firebase client and an execution context. This structure provides methods to interact with Firestore.

## Methods
### NewFirebaseClient
Creates a new Firebase client.

```go

func NewFirebaseClient(ctx context.Context, projectID string, secretsJSON []byte) (*FirebaseClient, error)
```

- `ctx`: The execution context.
- `projectID`: The Firebase project ID.
- `secretsJSON`: The JSON credentials.


### GetDocument
Retrieves a document from a specified collection.

```go
func (f *FirebaseClient) GetDocument(collection string, document string) (map[string]interface{}, error)
```

- `collection`: The name of the collection.
- `document`: The ID of the document to retrieve.

## DeleteDocument
Deletes a document from a specified collection.

```go
func (f *FirebaseClient) DeleteDocument(collection string, document string) error
collection: The name of the collection.
```

- `document`: The ID of the document to delete.

## UpsertDocument
Inserts or updates a document in a specified collection with the provided data.

```go
func (f *FirebaseClient) UpsertDocument(collection string, document string, data map[string]interface{}) error
```

- `collection`: The name of the collection.
- `document`: The ID of the document to insert or update.
- `data`: The data to insert or update in the document.


# Dependencies
This file depends on the following libraries:

- `cloud.google.com/go/firestore`
- `firebase.google.com/go`
- `google.golang.org/api/option`

Ensure you have these dependencies in your go.mod file to use the Firebase client.

#
For more details on the methods and their usage, refer to the source code in [`firebase-go-crud.go`](firebase-go-crud.go).