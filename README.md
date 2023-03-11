# Rustand-React-Backend

Clone this repository to your local machine:

git clone
Navigate to the project directory:

cd <repository-name>
Install the project dependencies:

cd frontend
npm install
cd ..
cargo install --path .
Add The following depedencies to your cargo.toml file

[dependencies]
actix-cors = "0.6.4"
actix-files = "0.6.2"
actix-web = "4.3.0"
actix-web-actors = "4.2.0"
dotenv = "0.15.0"
serde = { version = "1.0.152", features = ["derive"] }
serde_json = "1.0.93"
sqlx = { version = "0.6.2", features = ["runtime-async-std-native-tls", "postgres"] }

Create a .env file in the project root directory and add the following variables:

DATABASE_URL=postgres://<username>:<password>@<host>:<port>/<database_name>
Replace <username>, <password>, <host>, <port> and <database_name> with appropriate values for your PostgreSQL database.

Create the database tables by running the following command:

create table users (
    id serial primary key,
    username varchar(255) not null unique,
    email varchar(255) not null unique,
    password varchar(255) not null
);
Start the project by running the following command:

cargo r -r
Navigate to http://localhost:3000 to see the React frontend.
