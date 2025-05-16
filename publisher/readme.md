## Understanding publisher and message broker.

1. How much data your publisher program will send to the message broker in one run?
Ada 5 message berbeda yang dikirimkan dan ini bisa kita lihat pada fn main. Dimana publisher melakukan publish_event 5 kali.

2. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber
program, what does it mean?

guest:guest@localhost:5672 adalah alamat koneksi (connection string) untuk mengakses server RabbitMQ.

- guest pertama adalah username untuk login ke RabbitMQ.
- guest kedua adalah password-nya. 

Ketika subscriber dan publisher mempunyai connection url yang sama berati program tersebut terhubung dengan instance RabbitMQ yang sama. Memungkinkan publisher mengirimkan pesan yang nantinya dapat diterima oleh subscriber.

