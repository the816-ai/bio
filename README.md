
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Fashion Store - Link Bio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);
            min-height: 100vh;
            color: #333;
        }

        .container {
            max-width: 400px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.95);
            min-height: 100vh;
            position: relative;
            overflow: hidden;
        }

        .header {
            text-align: center;
            padding: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            position: relative;
        }

        .profile-img {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background: #fff;
            margin: 0 auto 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            border: 3px solid rgba(255,255,255,0.3);
        }

        .store-name {
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .store-desc {
            font-size: 14px;
            opacity: 0.9;
            margin-bottom: 15px;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 10px;
        }

        .social-btn {
            width: 35px;
            height: 35px;
            border-radius: 50%;
            background: rgba(255,255,255,0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: transform 0.3s ease;
        }

        .social-btn:hover {
            transform: scale(1.1);
            background: rgba(255,255,255,0.3);
        }

        .content {
            padding: 20px;
        }

        .search-bar {
            width: 100%;
            padding: 12px 16px;
            border: 1px solid #ddd;
            border-radius: 25px;
            margin-bottom: 20px;
            font-size: 14px;
            background: #f8f9fa;
        }

        .tabs {
            display: flex;
            border-bottom: 1px solid #eee;
            margin-bottom: 20px;
        }

        .tab {
            flex: 1;
            text-align: center;
            padding: 12px;
            background: none;
            border: none;
            font-size: 14px;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
        }

        .tab.active {
            color: #667eea;
            font-weight: bold;
        }

        .tab.active::after {
            content: '';
            position: absolute;
            bottom: -1px;
            left: 0;
            right: 0;
            height: 2px;
            background: #667eea;
        }

        .section {
            margin-bottom: 30px;
        }

        .section-title {
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 15px;
            color: #333;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
            margin-bottom: 20px;
        }

        .product-item {
            aspect-ratio: 1;
            background: #f8f9fa;
            border-radius: 12px;
            overflow: hidden;
            position: relative;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .product-item:hover {
            transform: scale(1.05);
        }

        .product-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .product-item .overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(transparent, rgba(0,0,0,0.7));
            color: white;
            padding: 8px;
            font-size: 11px;
            text-align: center;
        }

        .featured-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
            margin-bottom: 20px;
        }

        .featured-item {
            background: #f8f9fa;
            border-radius: 15px;
            overflow: hidden;
            position: relative;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .featured-item:hover {
            transform: translateY(-5px);
        }

        .featured-item img {
            width: 100%;
            height: 120px;
            object-fit: cover;
        }

        .featured-info {
            padding: 12px;
        }

        .featured-title {
            font-size: 13px;
            font-weight: bold;
            margin-bottom: 4px;
        }

        .featured-desc {
            font-size: 11px;
            color: #666;
            line-height: 1.3;
        }

        .shop-links {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
            margin-bottom: 20px;
        }

        .shop-link {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 15px;
            border-radius: 15px;
            text-decoration: none;
            text-align: center;
            font-weight: bold;
            transition: transform 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .shop-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        .category-showcase {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            margin-bottom: 20px;
        }

        .category-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
            cursor: pointer;
        }

        .category-card:hover {
            transform: translateY(-5px);
        }

        .category-card img {
            width: 100%;
            height: 100px;
            object-fit: cover;
        }

        .category-info {
            padding: 12px;
            text-align: center;
        }

        .category-name {
            font-size: 13px;
            font-weight: bold;
            margin-bottom: 4px;
        }

        .category-count {
            font-size: 11px;
            color: #666;
        }

        .see-more {
            background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 100%);
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 25px;
            font-weight: bold;
            width: 100%;
            margin-bottom: 15px;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .see-more:hover {
            transform: translateY(-2px);
        }

        .footer {
            background: #f8f9fa;
            padding: 20px;
            text-align: center;
            margin-top: 30px;
        }

        .footer-text {
            font-size: 12px;
            color: #666;
            margin-bottom: 10px;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .contact-item {
            font-size: 11px;
            color: #888;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        .price-tag {
            position: absolute;
            top: 8px;
            right: 8px;
            background: #ff4757;
            color: white;
            padding: 4px 8px;
            border-radius: 12px;
            font-size: 10px;
            font-weight: bold;
        }

        .badge {
            position: absolute;
            top: 8px;
            left: 8px;
            background: #2ed573;
            color: white;
            padding: 4px 8px;
            border-radius: 12px;
            font-size: 10px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="profile-img">👗</div>
            <div class="store-name">My Fashion Store</div>
            <div class="store-desc">Thời trang nữ hiện đại • Chất lượng cao • Giá tốt nhất</div>
            <div class="social-links">
                <a href="#" class="social-btn">📘</a>
                <a href="#" class="social-btn">📷</a>
                <a href="#" class="social-btn">🎵</a>
                <a href="#" class="social-btn">📞</a>
            </div>
        </div>

        <div class="content">
            <input type="text" class="search-bar" placeholder="🔍 Tìm kiếm sản phẩm theo tên...">
            
            <div class="tabs">
                <button class="tab active" onclick="switchTab('new')">Mới nhất</button>
                <button class="tab" onclick="switchTab('shops')">Cửa hàng</button>
                <button class="tab" onclick="switchTab('categories')">Danh mục</button>
            </div>

            <div id="new" class="tab-content active">
                <div class="section">
                    <div class="section-title">🔥 Sản phẩm nổi bật</div>
                    <div class="featured-grid">
                        <div class="featured-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='120' viewBox='0 0 200 120'%3E%3Crect width='200' height='120' fill='%23ffeaa7'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='16' fill='%23636e72'%3EÁo dài%3C/text%3E%3C/svg%3E" alt="Áo dài">
                            <div class="price-tag">899K</div>
                            <div class="featured-info">
                                <div class="featured-title">Set Áo Dài Cách Tân</div>
                                <div class="featured-desc">Thiết kế hiện đại, chất liệu cao cấp</div>
                            </div>
                        </div>
                        <div class="featured-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='120' viewBox='0 0 200 120'%3E%3Crect width='200' height='120' fill='%23fd79a8'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='16' fill='white'%3EBikini%3C/text%3E%3C/svg%3E" alt="Bikini">
                            <div class="badge">Hot</div>
                            <div class="featured-info">
                                <div class="featured-title">Bikini Đồ Bơi</div>
                                <div class="featured-desc">Nhiều màu sắc, form dáng đẹp</div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="section">
                    <div class="section-title">👚 Set đồ cực xinh</div>
                    <div class="product-grid">
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23fab1a0'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='12' fill='white'%3EÁo khoác%3C/text%3E%3C/svg%3E" alt="Áo khoác">
                            <div class="overlay">Áo khoác nữ</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%2374b9ff'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='12' fill='white'%3EÁo tweed%3C/text%3E%3C/svg%3E" alt="Áo tweed">
                            <div class="overlay">Set tweed</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%2355a3ff'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='12' fill='white'%3EVáy đen%3C/text%3E%3C/svg%3E" alt="Váy đen">
                            <div class="overlay">Váy đen</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23a29bfe'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='12' fill='white'%3ESet nữ%3C/text%3E%3C/svg%3E" alt="Set nữ">
                            <div class="overlay">Set nữ</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23fd79a8'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='12' fill='white'%3EJump suit%3C/text%3E%3C/svg%3E" alt="Jump suit">
                            <div class="overlay">Jump suit</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23fdcb6e'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='12' fill='white'%3ECardigan%3C/text%3E%3C/svg%3E" alt="Cardigan">
                            <div class="overlay">Cardigan</div>
                        </div>
                    </div>
                    <button class="see-more">Xem thêm</button>
                </div>

                <div class="section">
                    <div class="section-title">👠 Giày dép thời trang</div>
                    <div class="product-grid">
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%236c5ce7'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3ESneaker%3C/text%3E%3C/svg%3E" alt="Sneaker">
                            <div class="overlay">Sneaker</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23ff7675'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3ESandal%3C/text%3E%3C/svg%3E" alt="Sandal">
                            <div class="overlay">Sandal</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%2300b894'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3EGiày cao gót%3C/text%3E%3C/svg%3E" alt="Giày cao gót">
                            <div class="overlay">Giày cao gót</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23e17055'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3EGiày bệt%3C/text%3E%3C/svg%3E" alt="Giày bệt">
                            <div class="overlay">Giày bệt</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%232d3436'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3EBooties%3C/text%3E%3C/svg%3E" alt="Booties">
                            <div class="overlay">Booties</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23ffeaa7'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='%23636e72'%3ESlippers%3C/text%3E%3C/svg%3E" alt="Slippers">
                            <div class="overlay">Slippers</div>
                        </div>
                    </div>
                    <button class="see-more">Xem thêm</button>
                </div>

                <div class="section">
                    <div class="section-title">👜 Túi xách thời trang</div>
                    <div class="product-grid">
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23a29bfe'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3ETúi xách%3C/text%3E%3C/svg%3E" alt="Túi xách">
                            <div class="overlay">Túi xách da</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23fd79a8'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3EHandbag%3C/text%3E%3C/svg%3E" alt="Handbag">
                            <div class="overlay">Handbag</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%2300b894'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3EClutch%3C/text%3E%3C/svg%3E" alt="Clutch">
                            <div class="overlay">Clutch bag</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23636e72'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3EBackpack%3C/text%3E%3C/svg%3E" alt="Backpack">
                            <div class="overlay">Backpack</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23e17055'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3EShoulder%3C/text%3E%3C/svg%3E" alt="Shoulder bag">
                            <div class="overlay">Shoulder bag</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23ffeaa7'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='%23636e72'%3ETote bag%3C/text%3E%3C/svg%3E" alt="Tote bag">
                            <div class="overlay">Tote bag</div>
                        </div>
                    </div>
                    <button class="see-more">Xem thêm</button>
                </div>

                <div class="section">
                    <div class="section-title">💄 Mỹ phẩm & Phụ kiện</div>
                    <div class="product-grid">
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23ff7675'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3ESon môi%3C/text%3E%3C/svg%3E" alt="Son môi">
                            <div class="overlay">Son môi</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23fdcb6e'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3EPudder%3C/text%3E%3C/svg%3E" alt="Pudder">
                            <div class="overlay">Phấn trang điểm</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23fab1a0'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3EBông tai%3C/text%3E%3C/svg%3E" alt="Bông tai">
                            <div class="overlay">Bông tai</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%236c5ce7'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3EKhuyên tai%3C/text%3E%3C/svg%3E" alt="Khuyên tai">
                            <div class="overlay">Khuyên tai</div>
                        </div>
                        <div class="product-item">
                            <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' fill='%23a29bfe'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='10' fill='white'%3EKính%3C/text%3E%3C/svg%3E" alt="Kính">
<!-- CỬA HÀNG -->
<div id="shops" class="tab-content">
  <div class="section">
    <div class="section-title">🏬 Cửa hàng yêu thích</div>
    <div class="shop-links">
      <a href="https://shopee.vn/mystore" class="shop-link" target="_blank">
        <i class="fab fa-shopee"></i> Shopee Store
      </a>
      <a href="https://tiktok.com/@mystore" class="shop-link" target="_blank">
        <i class="fab fa-tiktok"></i> TikTok Store
      </a>
    </div>
  </div>
</div>

<!-- DANH MỤC -->
<div id="categories" class="tab-content">
  <div class="section">
    <div class="section-title">🗂️ Danh mục sản phẩm</div>
    <div class="category-showcase">
      <div class="category-card">
        <img src="https://via.placeholder.com/200x100?text=Áo+dài" alt="Áo dài">
        <div class="category-info">
          <div class="category-name">Áo dài</div>
          <div class="category-count">332 sản phẩm</div>
        </div>
      </div>
      <div class="category-card">
        <img src="https://via.placeholder.com/200x100?text=Váy" alt="Váy">
        <div class="category-info">
          <div class="category-name">Váy</div>
          <div class="category-count">185 sản phẩm</div>
        </div>
      </div>
      <div class="category-card">
        <img src="https://via.placeholder.com/200x100?text=Set+đồ" alt="Set đồ">
        <div class="category-info">
          <div class="category-name">Set đồ</div>
          <div class="category-count">122 sản phẩm</div>
        </div>
      </div>
    </div>
  </div>
</div>
<script>
function switchTab(tab) {
  document.querySelectorAll('.tab').forEach(btn => btn.classList.remove('active'));
  event.target.classList.add('active');

  document.querySelectorAll('.tab-content').forEach(section => {
    section.classList.remove('active');
  });

  const target = document.getElementById(tab);
  if (target) target.classList.add('active');
}
</script>
