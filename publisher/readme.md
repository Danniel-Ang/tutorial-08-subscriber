## Understanding publisher and message broker.

1. How much data your publisher program will send to the message broker in one run?
Ada 5 message berbeda yang dikirimkan dan ini bisa kita lihat pada fn main. Dimana publisher melakukan publish_event 5 kali.

2. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber
program, what does it mean?

guest:guest@localhost:5672 adalah alamat koneksi (connection string) untuk mengakses server RabbitMQ.

- guest pertama adalah username untuk login ke RabbitMQ.
- guest kedua adalah password-nya. 

Ketika subscriber dan publisher mempunyai connection url yang sama berati program tersebut terhubung dengan instance RabbitMQ yang sama. Memungkinkan publisher mengirimkan pesan yang nantinya dapat diterima oleh subscriber.

## Running RabbitMQ as message broker
![alt text](<[IMG] RabbitMQ.png>)

## Sending and processing event
![alt text](<[IMG] Publisher&Consumer.png>)

Pada subscriber, fakta adanya 5 Message received pada terminal menandakan publisher sukses mengirimkan 5 pesan ke RabbitMQ broker. Subscriber sukses terhubung dengan broker yang sama dan menerima tiap message yang dikirimkan oleh publisher.

Pada publisher, kita tidak melihat banyak karena ketika kita menjalankan cargo run, kita mengirimkan 5 pesan ke RabbitMQ dan fakta consumer/subscriber mendapati 5 pesan itu sudah cukup untuk membuktikan pesan sukses di kirimkan dan di deserialized oleh subscriber.