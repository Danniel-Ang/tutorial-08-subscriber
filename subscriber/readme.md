## Understanding subscriber and message broker
1. What is AMQP?
AMQP atau Advance Message Queuing Protocol adalah protokol komunikasi yang memungkinkan aplikasi bertukar pesan melewati sebuah perantara yang memiliki queue based.

Analogi dari protokol ini cukup mirip dengan kotak pos dimana kita mengirim pesan ke dalam antrian daripada menggunakan REST API yang membutuhkan kedua service hidup.

2. What does it mean? guest:guest@localhost:5672, what is the first guest, and what
is the second guest, and what is localhost:5672 is for?

guest:guest@localhost:5672 adalah alamat koneksi (connection string) untuk mengakses server RabbitMQ.

- guest pertama adalah username untuk login ke RabbitMQ.
- guest kedua adalah password-nya. 
- localhost:5672 menunjukkan bahwa RabbitMQ berjalan di komputer lokal (localhost) pada port 5672, yang merupakan port default untuk protokol AMQP.


## Simulation slow subscriber
![subscriber/\[IMG\] Slow Subs.png](<[IMG] Slow Subs.png>)

Total (Highest): 21
Because i run it like five times, i guess what happen is the first four messages doesnt get into queue but direct to subscriber. But the rest is going to the queue because it is delayed for 1s each message. 

## Reflection and Running at least three subscribers
![alt text](<[IMG] Multiple Subs.png>)