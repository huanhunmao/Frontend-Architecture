├── app/
|   # Application composition layer
|   # Only contains abstract initialization logic and static assets, and thus mustn't contain any Slices
|
├── processes/
|   # Slices implementing page-independent workflows or workflows involving multiple pages
|   ├── auth
|   ├── payment
|   ├── quick-tour
|
|
├── pages/
|   # Slices implementing complete application views
|   ├── feed
|   |
|   ├── profile
|   |   # Due to routing specifics, this layer can contain nested structures
|   |   ├── edit
|   |   └── stats
|   |
|   ├── sign-up
|
|
├── widgets/
|   # Slices implementing various combinations of abstract and / or business units from lower layers,
|   # to deliver isolated atomic User Interface fragments
|   ├── chat-window
|   ├── header
|   ├── feed
|
|
├── features/
|   # Sliced implementing user scenarios, which usually operate on business entities
|   ├── auth-by-phone
|   ├── create-post
|   ├── write-message
|
|
├── entities/
|   # Slices implementing business units in terms of which application business logic works
|   ├── account
|   ├── conversation
|   ├── post
|   ├── wallet
|
|
├── shared/
|   # This layer is a set of abstract Segments
|   # It means that it must not contain any business units or business-related logic