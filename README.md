<!DOCTYPE html>
<html lang="tg">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Профили Instagram</title>
    <style>
        /* CSS-и умумӣ барои саҳифа */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #fafafa;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        /* Контейнери асосии профил */
        .profile-container {
            max-width: 600px;
            width: 100%;
            background-color: #ffffff;
            border: 1px solid #dbdbdb;
            border-radius: 12px;
            padding: 30px 25px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
        }

        /* Сарлавҳаи профил - қисми болоӣ */
        .profile-header {
            display: flex;
            align-items: center;
            gap: 25px;
            margin-bottom: 25px;
        }

        /* Рамзи профил (аватар) */
        .profile-avatar {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            background: linear-gradient(135deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888);
            display: flex;
            justify-content: center;
            align-items: center;
            flex-shrink: 0;
        }

        .profile-avatar img {
            width: 92px;
            height: 92px;
            border-radius: 50%;
            border: 3px solid white;
            object-fit: cover;
        }

        /* Барои вақте ки расм нест, инициалҳо нишон дода мешаванд */
        .avatar-placeholder {
            width: 92px;
            height: 92px;
            border-radius: 50%;
            background-color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 40px;
            font-weight: bold;
            color: #bc1888;
        }

        .profile-info {
            flex: 1;
        }

        .profile-username {
            font-size: 22px;
            font-weight: 600;
            color: #262626;
            margin-bottom: 8px;
        }

        .profile-name {
            font-size: 16px;
            color: #8e8e8e;
            margin-bottom: 5px;
        }

        .profile-bio {
            font-size: 14px;
            color: #262626;
            line-height: 1.5;
        }

        /* Статистика - постҳо, фолловерҳо, фоллоуинг */
        .profile-stats {
            display: flex;
            justify-content: space-around;
            border-top: 1px solid #efefef;
            border-bottom: 1px solid #efefef;
            padding: 15px 0;
            margin-bottom: 20px;
        }

        .stat-item {
            text-align: center;
        }

        .stat-number {
            font-size: 18px;
            font-weight: 700;
            color: #262626;
        }

        .stat-label {
            font-size: 13px;
            color: #8e8e8e;
        }

        /* Тугмаҳои амал */
        .profile-actions {
            display: flex;
            gap: 10px;
            margin-bottom: 25px;
        }

        .btn {
            flex: 1;
            padding: 8px 0;
            border: none;
            border-radius: 8px;
            font-size: 15px;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.2s;
        }

        .btn-follow {
            background-color: #0095f6;
            color: white;
        }

        .btn-follow:hover {
            background-color: #0077cc;
        }

        .btn-message {
            background-color: #efefef;
            color: #262626;
        }

        .btn-message:hover {
            background-color: #dbdbdb;
        }

        /* Шабакаи постҳо (GRID) */
        .post-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 4px;
        }

        .post-item {
            aspect-ratio: 1 / 1;
            background-color: #efefef;
            border-radius: 4px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 12px;
            color: #8e8e8e;
            overflow: hidden;
            position: relative;
        }

        .post-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* Агар расм набошад, рангҳои гуногун */
        .post-placeholder {
            background: linear-gradient(145deg, #e0e0e0, #f5f5f5);
            font-weight: 500;
        }

        /* Барои посухгӯӣ дар дастгоҳҳои хурд */
        @media (max-width: 500px) {
            .profile-header {
                flex-direction: column;
                text-align: center;
                gap: 15px;
            }

            .profile-avatar {
                width: 80px;
                height: 80px;
            }

            .avatar-placeholder {
                width: 74px;
                height: 74px;
                font-size: 30px;
            }
        }
    </style>
</head>
<body>
    <div class="profile-container">

        <!-- Сарлавҳаи профил -->
        <div class="profile-header">
            <div class="profile-avatar">
                <!-- Агар шумо расм дошта бошед, инро иваз кунед: -->
                <!-- <img src="rasmi_shumo.jpg" alt="Аватар"> -->
                <div class="avatar-placeholder">💫</div>
            </div>
            <div class="profile-info">
                <div class="profile-username">@nargis_offical</div>
                <div class="profile-name">Наргис Раҳимова</div>
                <div class="profile-bio">🌿 Табиат | сафар | ҳаёти солим<br>📍 Душанбе, Тоҷикистон</div>
            </div>
        </div>

        <!-- Статистика -->
        <div class="profile-stats">
            <div class="stat-item">
                <div class="stat-number">48</div>
                <div class="stat-label">постҳо</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">1,234</div>
                <div class="stat-label">фолловерҳо</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">567</div>
                <div class="stat-label">фоллоуинг</div>
            </div>
        </div>

        <!-- Тугмаҳо -->
        <div class="profile-actions">
            <button class="btn btn-follow">Фоллоу</button>
            <button class="btn btn-message">Паём</button>
        </div>

        <!-- Шабакаи постҳо -->
        <div class="post-grid">
            <div class="post-item post-placeholder">📸 1</div>
            <div class="post-item post-placeholder">📸 2</div>
            <div class="post-item post-placeholder">📸 3</div>
            <div class="post-item post-placeholder">📸 4</div>
            <div class="post-item post-placeholder">📸 5</div>
            <div class="post-item post-placeholder">📸 6</div>
            <!-- Барои расмҳои воқеӣ, инро истифода баред: -->
            <!-- <div class="post-item"><img src="post1.jpg" alt="Пост 1"></div> -->
        </div>

        <!-- Эзоҳ: Ин танҳо як намуна аст -->
        <p style="text-align: center; margin-top: 20px; font-size: 12px; color: #c7c7c7;">Instagram профили намунавӣ</p>
    </div>
</body>
</html>
