<h1 align="center"> Library API </h1>

## KELOMPOK 2
#### Adam Gumilang
#### Sahrul Mahdi Muhammad
#### Puput Handayani

# Database : perpustakaan
## Tabel :
- books : id, title, author, genre, published_date
- loans : id, user_id, book_id, loan_date, return_date 
- reviews : id, user_id, book_id, rating, comment, created_at
- users : id, name, email, password, phone, created_at

# Relasi antar tabel:
- Users dapat meminjam Books melalui tabel Loans.
- Users dapat memberikan ulasan pada Books melalui tabel Reviews.
- Books dapat memiliki banyak ulasan (Reviews) dan banyak peminjaman (Loans).

# Endpoint:
### Yang hanya bisa diakses oleh admin:
- GET /api/users
- DELETE /api/users/:user_id
- POST /api/books
- PUT /api/books/:book_id
- DELETE /api/books/:book_id
- GET /api/loans

# Bisa diakses admin dan user:
- POST /api/auth/register
- POST /api/auth/login
- GET /api/users/:user_id
- GET /api/books
- GET /api/books/:book_id
- GET /api/books?genre=:genre
- POST /api/loans
- PUT /api/loans/:loan_id/return
- GET /api/loans/user/:user_id
- POST /api/reviews
- GET /api/reviews/:book_id
- DELETE /api/reviews/:review_id
- PUT /api/reviews/:review_id
- GET /api/external?query=:query
