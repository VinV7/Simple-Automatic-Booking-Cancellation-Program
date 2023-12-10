# Simple Automatic Booking Cancellation Program

Automatic Booking Cancellation Program is program made to automatically cancel bookings if certain requirements are not met. Such as the payment time exceeds more than the given time which is 15 minutes (Modifiable). First the program will connect to the database which is [PostgreSQL](https://www.postgresql.org/) (You can use other kinds of databases e.g [MySql](https://www.mysql.com/), [Oracle](https://www.oracle.com/uk/), Etc) using [Psycopg2](https://pypi.org/project/psycopg2/) module. Secondly after connecting to the database, the program will then continue to check if certain requirements are met such as the order is booked but the payment status is still unpaid and if it has been more than 15 minutes since the given time to transfer the payments. Third, the program then will send a PATCH (Update) request to the [YCBM](https://youcanbook.me/) API cancelling the booking session and making the booking session appear again in the website. This program is still very simple yet very useful. This program can also be upgraded making it automate the process using a [CRON](https://en.wikipedia.org/wiki/Cron) scheduler. In the future i will be updating this program adding a Cron scheduler using [Apache Airflow](https://airflow.apache.org/) 

## Installation : 

First clone the code

```bash
git clone https://github.com/VinV7/Simple-Automatic-Booking-Cancellation-Program.git
```

Install the modules used in the code using [pip](https://pip.pypa.io/en/stable/)

```bash
pip install psycopg2
pip install requests
```

## Modules and Database used : 

Database : 

[PostgreSQL](https://www.postgresql.org/)

Modules : 

[Psycopg2](https://pypi.org/project/psycopg2/)

[Requests](https://pypi.org/project/requests/)

[Python-dotenv](https://pypi.org/project/python-dotenv/)

## Features :

Connecting to a Database

Reading and Updating data inside the Database

Deleting and Updating booking sessions

## Technical Documentation References :
[https://api.youcanbook.me/docs/index.html](https://api.youcanbook.me/docs/index.html)

[https://www.psycopg.org/docs/](https://www.psycopg.org/docs/)

## Tutorial References :

[https://www.youtube.com/watch?v=KuQUNHCeKCk&ab_channel=BekBrace](https://www.youtube.com/watch?v=KuQUNHCeKCk&ab_channel=BekBrace)

[https://www.youtube.com/watch?v=Q8iYj2ypWss&ab_channel=BekBrace](https://www.youtube.com/watch?v=Q8iYj2ypWss&ab_channel=BekBrace)

[https://www.youtube.com/watch?v=8w3zHsEPFnQ&ab_channel=BekBrace](https://www.youtube.com/watch?v=8w3zHsEPFnQ&ab_channel=BekBrace)

[https://www.youtube.com/watch?v=a_1AEYxwLi8&ab_channel=BekBrace](https://www.youtube.com/watch?v=a_1AEYxwLi8&ab_channel=BekBrace)

[https://www.youtube.com/watch?v=8dlQ_nDE7dQ&t=359s&ab_channel=NeuralNine](https://www.youtube.com/watch?v=8dlQ_nDE7dQ&t=359s&ab_channel=NeuralNine)

## Licence

MIT License

Copyright (c) 2023 Albin Ivandito

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.