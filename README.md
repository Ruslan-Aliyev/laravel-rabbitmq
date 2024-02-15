# Intro

This is a continuation from Async PHP/Laravel Queues: https://github.com/Ruslan-Aliyev/PHP_Async/tree/master?tab=readme-ov-file#laravel-1

## Important steps

1/ Good easy intro: https://www.youtube.com/watch?v=deG25y_r6OY

2/ Install and setup RabbitMQ (on Windows): https://www.youtube.com/watch?v=KhYiaEOrw7Q

3/ Admin panel: http://localhost:15672 . Credentials `guest`/`guest`

4/ Usage with Laravel: https://www.youtube.com/watch?v=K-xzRM6EKHg

- Need this library: https://github.com/vyuldashev/laravel-queue-rabbitmq `composer require vladimir-yuldashev/laravel-queue-rabbitmq`
- In `config/queue.php`: change `connections` > `sync` > `driver` to `rabbitmq` & add the `rabbitmq` block into `connections` https://github.com/vyuldashev/laravel-queue-rabbitmq?tab=readme-ov-file#configuration
- Make a job `php artisan make:job DummyJob`
	- Do something in the `handle` part of `DummyJob`, in this example "Hello World" is printed.
- Dispatch this job from routes or command. In this example the job is dispatched from the web route.
- Serve the Laravel app: `php artisan serve`
- Visit the route, run `php artisan queue:work` in another terminal, and then see the results in RabbitMQ admin panel

## Further Tutorials

- https://dev.to/dendihandian/rabbitmq-queue-driver-for-laravel-3ng4
- https://www.youtube.com/watch?v=Cie5v59mrTg
- https://www.youtube.com/watch?v=m-hNL87-lFo&list=PLcjapmjyX17hJZ-shzRMxTus0aMw0EVVB&index=8
- https://laravel-news.com/laravel-rabbitmq-queue-driver
- https://laravel-news.com/laravel-jobs-queues-101
- https://www.youtube.com/watch?app=desktop&v=bj4GFsv3_Yc
- https://www.youtube.com/watch?v=GMmRtSFQ5Z0
- https://github.com/atabegruslan/chat#rabbit-mq