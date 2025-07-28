<!DOCTYPE html>
<html lang="el">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ΓΩΝΙΑΔΗΣ Ο.Ε | Επαγγελματικά Έπιπλα</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }

        header {
            background-color: #333;
            color: white;
            padding: 20px;
            text-align: center;
        }

        .company-name {
            font-size: 2em;
            margin: 0;
        }

        /* Hamburger Menu */
        .menu-btn {
            position: fixed;
            top: 20px;
            left: 20px;
            cursor: pointer;
            z-index: 1001;
        }

        .menu-btn div {
            width: 30px;
            height: 3px;
            background: white;
            margin: 6px 0;
            transition: 0.4s;
        }

        /* Animation για το X */
        .menu-btn.open div:nth-child(1) {
            transform: rotate(45deg) translate(5px, 5px);
        }

        .menu-btn.open div:nth-child(2) {
            opacity: 0;
        }

        .menu-btn.open div:nth-child(3) {
            transform: rotate(-45deg) translate(6px, -6px);
        }

        /* Sidebar Menu */
        nav.sidebar {
            height: 100%;
            width: 0;
            position: fixed;
            top: 0;
            left: 0;
            background-color: #222;
            overflow-x: hidden;
            transition: 0.5s;
            padding-top: 80px;
            z-index: 1000;
        }

        nav.sidebar.open {
            width: 250px;
        }

        nav.sidebar a {
            padding: 10px 20px;
            text-decoration: none;
            font-size: 1.2em;
            color: white;
            display: block;
            transition: 0.3s;
        }

        nav.sidebar a:hover {
            background-color: #444;
        }

        .content {
            padding: 20px;
            transition: margin-left 0.5s;
        }

        .content.shift {
            margin-left: 250px;
        }

        @media (max-width: 768px) {
            .company-name {
                font-size: 1.5em;
            }
        }
    </style>
</head>
<body>
    <!-- Hamburger Menu -->
    <div class="menu-btn" onclick="toggleMenu()" aria-label="Εναλλαγή μενού" role="button">
        <div></div>
        <div></div>
        <div></div>
    </div>

    <!-- Sidebar Menu -->
    <nav class="sidebar" id="sidebar">
        <a href="#colors">Χρωματολόγιο</a>
        <a href="#interior">Εσωτερικές</a>
        <a href="#exterior">Εξωτερικές</a>
        <a href="#kitchen">Επίπλα Κουζίνας</a>
        <a href="#bathroom">Επίπλα Μπάνιου</a>
        <a href="#living">Επίπλα Σαλονιού</a>
        <a href="#bedroom">Επίπλα Δωματίου</a>
        <a href="#contact">Επικοινωνία</a>
    </nav>

    <!-- Κύριο Περιεχόμενο -->
    <div class="content" id="content">
        <header>
            <h1 class="company-name">ΓΩΝΙΑΔΗΣ Ο.Ε</h1>
        </header>

        <main>
            <section id="about">
                <h2>Σχετικά με εμάς</h2>
                <p>Εδώ μπορείτε να προσθέσετε πληροφορίες για την εταιρεία σας.</p>
                <!-- <img src="foto1.jpg" alt="Εταιρεία ΓΩΝΙΑΔΗΣ Ο.Ε" width="300"> -->
            </section>
        </main>
    </div>

    <script>
        function toggleMenu() {
            document.getElementById('sidebar').classList.toggle('open');
            document.getElementById('content').classList.toggle('shift');
            document.querySelector('.menu-btn').classList.toggle('open');
        }
    </script>
</body>
</html>
