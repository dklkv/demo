<h2>Базовий (необхідний) рівень:</h2>
<ul>
    <li>створені основні акаунти в системах та сервісах, наведених у матеріалах кодінг-сесії;</li>
    <li>налаштоване працююче середовище розробки VSCode;</li>
    <li>створено початковий код виконання практичного завдання;</li>
    <li>
        <p>код компілюється та запускається локально.</p>
        <p><code>go build -o bin/app src/main.go</code> <small>компіляція коду в бінарний файл</small></p>
    </li>
</ul>

<h2>Розширений рівень:</h2>
<ul>
    <li>
        <p>створено образ контейнера за допомогою docker;</p>
        <p><code>go mod init "project name"</code> <small>файл залежностей</small></p>
        <p><code>docker build .</code></p>
    </li>
    <li>контейнер успішно запускається локально;</li>
    <p><code>docker run -p 8080:8080 sha256:"image id"</code></p>
    <li>образ контейнеру залитий на docker hub.</li>
    <p><code>docker tag "image id" dkulikov/demo:v1.0.0</code></p>
    <p><code>docker push dkulikov/demo:v1.0.0</code></p>
</ul>

<h2>Топовий рівень:</h2>
<ul>
    <li>встановлено версію kubernetes k3s;</li>
    <p><code>k3d cluster create demo</code></p>
    <li>контейнер запущено у kubernetes;</li>
    <p><code>kubectl create deploy demo dkulikov/demo:v1.0.0</code></p>
    <p><code>kubectl port-forward deploy/demo 8080</code></p>
    <li>сервіс працює.</li>
</ul>
