<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Online Book Hub</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@700;400&display=swap" rel="stylesheet">
    <style>
        body {
            margin: 0;
            font-family: 'Montserrat', Arial, sans-serif;
            background: linear-gradient(135deg, #f8fafc 0%, #e0e7ff 100%);
            color: #22223b;
        }
        header {
            background: linear-gradient(90deg, #4f46e5 60%, #a5b4fc 100%);
            color: #fff;
            padding: 30px 0 15px 0;
            text-align: center;
            box-shadow: 0 2px 8px rgba(79,70,229,0.1);
        }
        header h1 {
            margin: 0;
            font-size: 2.5rem;
            letter-spacing: 2px;
        }
        nav ul {
            list-style: none;
            padding: 0;
            margin: 20px 0 0 0;
            display: flex;
            justify-content: center;
            gap: 30px;
        }
        nav a {
            color: #fff;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1rem;
            transition: color 0.2s;
        }
        nav a:hover {
            color: #fbbf24;
        }
        .hero {
            background: url('https://images.unsplash.com/photo-1512820790803-83ca734da794?auto=format&fit=crop&w=1200&q=80') center/cover no-repeat;
            color: #fff;
            text-align: center;
            padding: 80px 20px 60px 20px;
            border-radius: 0 0 40px 40px;
            box-shadow: 0 4px 24px rgba(79,70,229,0.08);
            margin-bottom: 40px;
        }
        .hero h2 {
            font-size: 2.2rem;
            margin-bottom: 18px;
            text-shadow: 0 2px 8px rgba(0,0,0,0.15);
        }
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            text-shadow: 0 1px 4px rgba(0,0,0,0.10);
        }
        .hero button {
            background: #fbbf24;
            color: #22223b;
            border: none;
            padding: 14px 36px;
            font-size: 1.1rem;
            border-radius: 30px;
            font-weight: 700;
            cursor: pointer;
            box-shadow: 0 2px 8px rgba(251,191,36,0.15);
            transition: background 0.2s, color 0.2s;
        }
        .hero button:hover {
            background: #fff;
            color: #4f46e5;
        }
        .book-section {
            max-width: 1100px;
            margin: 0 auto 50px auto;
            padding: 0 20px;
        }
        .book-section h2 {
            text-align: center;
            font-size: 2rem;
            margin-bottom: 28px;
            color: #4f46e5;
        }
        .book-list {
            display: flex;
            flex-wrap: wrap;
            gap: 32px;
            justify-content: center;
        }
        .book-card {
            background: #fff;
            border-radius: 18px;
            box-shadow: 0 4px 16px rgba(79,70,229,0.08);
            padding: 22px 18px 18px 18px;
            width: 240px;
            text-align: center;
            transition: transform 0.18s, box-shadow 0.18s;
        }
        .book-card:hover {
            transform: translateY(-8px) scale(1.04);
            box-shadow: 0 8px 32px rgba(79,70,229,0.16);
        }
        .book-card img {
            width: 120px;
            height: 170px;
            object-fit: cover;
            border-radius: 10px;
            margin-bottom: 16px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.10);
        }
        .book-card h3 {
            margin: 0 0 8px 0;
            font-size: 1.15rem;
            color: #22223b;
        }
        .book-card p {
            margin: 0;
            color: #6366f1;
            font-weight: 500;
        }
        #categories {
            background: #f1f5f9;
            padding: 50px 0 40px 0;
            border-radius: 40px;
            margin: 0 0 40px 0;
        }
        #categories h2 {
            text-align: center;
            color: #4f46e5;
            font-size: 2rem;
            margin-bottom: 28px;
        }
        .categories-list {
            display: flex;
            justify-content: center;
            gap: 24px;
            flex-wrap: wrap;
        }
        .categories-list button {
            background: #4f46e5;
            color: #fff;
            border: none;
            padding: 14px 32px;
            border-radius: 30px;
            font-size: 1.1rem;
            font-weight: 700;
            cursor: pointer;
            box-shadow: 0 2px 8px rgba(79,70,229,0.10);
            transition: background 0.2s, color 0.2s;
        }
        .categories-list button:hover {
            background: #fbbf24;
            color: #22223b;
        }
        footer {
            background: #4f46e5;
            color: #fff;
            text-align: center;
            padding: 36px 10px 24px 10px;
            border-radius: 40px 40px 0 0;
            margin-top: 40px;
        }
        footer h2 {
            margin-top: 0;
            font-size: 1.3rem;
            letter-spacing: 1px;
        }
        footer p {
            margin: 8px 0;
            font-size: 1rem;
        }
        @media (max-width: 800px) {
            .book-list {
                flex-direction: column;
                align-items: center;
            }
            .book-card {
                width: 90%;
            }
            .categories-list {
                flex-direction: column;
                gap: 18px;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Online Book Hub</h1>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#books">Books</a></li>
                <li><a href="#categories">Categories</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <h2>Welcome to the Largest Online Book Collection</h2>
        <p>Explore thousands of books from various genres. Read, review, and share your favorite books.</p>
        <button onclick="alert('Feature coming soon!')">Explore Now</button>
    </section>

    <section id="books" class="book-section">
        <h2>Featured Books</h2>
        <div class="book-list">
            <div class="book-card">
                <img src="https://tse3.mm.bing.net/th/id/OIP.5DR6ZkXNRi-iB8EFtMgITQHaLM?pid=Api&P=0&h=180" alt="Book Cover" />
                
   <a href="https://drive.google.com/file/d/1ATFgC-ic-L2M4dLIsRnRFHJqn_kxklvb/view?usp=drivesdk" target="_blank" rel="noopener noreferrer"><h3>Wings of fire</h3> </a>
    <p>Author: A. P. J. Abdul Kalam and Arun Tiwari</p>
            </div>
            <div class="book-card">
                <img src="https://miro.medium.com/v2/resize:fit:1200/1*yPTgWvFZ_jy7rsscgNrTkA.jpeg" alt="Book Cover" />
                <a href="https://drive.google.com/file/d/1eqlhRzFhA0shQHUiGir31_rpgkbMOXdF/view?usp=drivesdk" target="_blank" rel="noopener noreferrer"><h3>Atomic habits</h3> </a>
                <p>Author: James Clear</p>
            </div>
            <div class="book-card">
                <img src="https://m.media-amazon.com/images/I/81QENBkoqYL.SL1500.jpg" alt="Book Cover" />
                 <a href="https://drive.google.com/file/d/1eqlhRzFhA0shQHUiGir31_rpgkbMOXdF/view?usp=drivesdk" target="_blank" rel="noopener noreferrer"><h3>Change Your Diet</h3> </a>
                <p>Author: Alan Turing</p>
            </div>
        </div>
    </section>

    <section id="categories">
        <h2>Categories</h2>
        <div class="categories-list">
            <button onclick="alert('Fiction books coming soon!')">Fiction</button>
            <button onclick="alert('Science books coming soon!')">Science</button>
            <button onclick="alert('History books coming soon!')">History</button>
            <button onclick="alert('Technology books coming soon!')">Technology</button>
        </div>
    </section>

    <footer id="contact">
        <h2>Contact Us</h2>
        <p>Email: support@onlinebookhub.com</p>
        <p>Phone: 9555220312</p>
        <p>&copy; 2025 Online Book Hub</p>
    </footer>
</body>
</html></footer></div></section>
