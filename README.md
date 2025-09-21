<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trang In Văn Bản - Khổ 52mmx70mm</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: #333;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1000px;
            margin: 0 auto;
            background-color: #fff;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #eee;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .logo-container {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 15px;
            gap: 15px;
        }
        
        .logo {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #2ecc71, #3498db);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            font-size: 24px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
        }
        
        .logo-text {
            font-size: 28px;
            font-weight: 700;
            background: linear-gradient(135deg, #2ecc71, #3498db);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
        }
        
        .description {
            color: #7f8c8d;
            font-size: 18px;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .control-panel {
            background-color: #f8f9fa;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 25px;
            border-left: 4px solid #3498db;
        }
        
        .control-group {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 15px;
            align-items: center;
        }
        
        .control-label {
            min-width: 150px;
            font-weight: 600;
            color: #2c3e50;
        }
        
        input[type="range"] {
            flex: 1;
            height: 8px;
            -webkit-appearance: none;
            background: #ddd;
            border-radius: 5px;
            outline: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #3498db;
            cursor: pointer;
        }
        
        .value-display {
            min-width: 60px;
            text-align: center;
            font-weight: 600;
            color: #3498db;
        }
        
        .input-section {
            margin-bottom: 30px;
        }
        
        textarea {
            width: 100%;
            height: 200px;
            padding: 15px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 16px;
            resize: vertical;
            transition: border 0.3s;
        }
        
        textarea:focus {
            border-color: #3498db;
            outline: none;
            box-shadow: 0 0 10px rgba(52, 152, 219, 0.3);
        }
        
        .button-group {
            display: flex;
            gap: 15px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
        button {
            padding: 14px 28px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
            font-weight: 600;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }
        
        #printBtn {
            background: linear-gradient(to right, #2ecc71, #27ae60);
            color: white;
            flex: 1;
        }
        
        #printBtn:hover {
            background: linear-gradient(to right, #27ae60, #219653);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(46, 204, 113, 0.4);
        }
        
        #clearBtn {
            background: linear-gradient(to right, #e74c3c, #c0392b);
            color: white;
        }
        
        #clearBtn:hover {
            background: linear-gradient(to right, #c0392b, #a93226);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(231, 76, 60, 0.4);
        }
        
        .preview-section {
            margin-top: 40px;
            padding-top: 20px;
            border-top: 2px solid #eee;
        }
        
        .preview-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .preview-content {
            background-color: #f9f9f9;
            border: 2px solid #ddd;
            border-radius: 8px;
            padding: 25px;
            min-height: 200px;
            white-space: pre-wrap;
            transition: all 0.3s;
        }
        
        .paper-size-info {
            background: #e8f4fc;
            border-left: 4px solid #3498db;
            padding: 15px;
            margin: 20px 0;
            border-radius: 0 8px 8px 0;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .instructions {
            background-color: #e8f4fc;
            border-left: 4px solid #3498db;
            padding: 20px;
            margin-top: 30px;
            border-radius: 0 8px 8px 0;
        }
        
        .instructions h3 {
            margin-bottom: 15px;
            color: #2c3e50;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .instructions ul {
            padding-left: 20px;
        }
        
        .instructions li {
            margin-bottom: 10px;
            line-height: 1.5;
        }
        
        .icon {
            font-size: 20px;
        }
        
        @media (max-width: 768px) {
            .button-group {
                flex-direction: column;
            }
            
            button {
                width: 100%;
            }
            
            .control-group {
                flex-direction: column;
                align-items: flex-start;
                gap: 10px;
            }
            
            input[type="range"] {
                width: 100%;
            }
            
            .logo-container {
                flex-direction: column;
                text-align: center;
            }
        }
        
        /* Thiết lập in cho khổ giấy 52mm x 70mm */
        @media print {
            body * {
                visibility: hidden;
                margin: 0;
                padding: 0;
            }
            
            .preview-section, .preview-section * {
                visibility: visible;
            }
            
            .preview-section {
                position: absolute;
                left: 0;
                top: 0;
                width: 52mm;
                height: 70mm;
                border: none;
                padding: 2mm;
                margin: 0;
                overflow: hidden;
                font-size: 10px;
                line-height: 1.2;
            }
            
            .preview-content {
                width: 100%;
                height: 100%;
                padding: 2mm;
                border: none;
                margin: 0;
                background: white;
                overflow: hidden;
            }
            
            @page {
                size: 52mm 70mm;
                margin: 0;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="logo-container">
                <div class="logo">GHN</div>
                <div class="logo-text">Giao Hàng Nhanh</div>
            </div>
            <h1>Trang In Văn Bản</h1>
            <p class="description">In trực tiếp đến máy in HRPT_LP80 - Khổ giấy 52mm x 70mm</p>
        </header>
        
        <div class="paper-size-info">
            <i class="fas fa-info-circle"></i>
            <span>Trang web đã được thiết lập để in trên khổ giấy 52mm x 70mm</span>
        </div>
        
        <div class="control-panel">
            <h2>Cài đặt in</h2>
            <div class="control-group">
                <span class="control-label">Kích thước chữ:</span>
                <input type="range" id="fontSize" min="8" max="16" value="10" step="1">
                <span id="fontSizeValue" class="value-display">10px</span>
            </div>
            <div class="control-group">
                <span class="control-label">Khoảng cách dòng:</span>
                <input type="range" id="lineHeight" min="1.0" max="1.5" value="1.2" step="0.1">
                <span id="lineHeightValue" class="value-display">1.2</span>
            </div>
            <div class="control-group">
                <span class="control-label">Căn lề trái:</span>
                <input type="range" id="paddingLeft" min="0" max="10" value="2" step="1">
                <span id="paddingLeftValue" class="value-display">2mm</span>
            </div>
        </div>
        
        <section class="input-section">
            <h2>Nhập văn bản cần in</h2>
            <textarea id="textInput" placeholder="Nhập nội dung văn bản bạn muốn in tại đây..."></textarea>
            
            <div class="button-group">
                <button id="printBtn"><span class="icon">🖨️</span> In đến HRPT_LP80</button>
                <button id="clearBtn"><span class="icon">🗑️</span> Xóa nội dung</button>
            </div>
        </section>
        
        <section class="preview-section">
            <div class="preview-header">
                <h2>Xem trước khi in (Tỷ lệ 1:1)</h2>
                <span class="paper-size">52mm × 70mm</span>
            </div>
            <div id="preview" class="preview-content">Nội dung xem trước sẽ hiển thị ở đây...</div>
        </section>
        
        <div class="instructions">
            <h3><span class="icon">💡</span> Hướng dẫn sử dụng:</h3>
            <ul>
                <li><strong>Kích thước chữ</strong>: Điều chỉnh thanh trượt để thay đổi kích thước chữ trong bản in (từ 8px đến 16px)</li>
                <li><strong>Khoảng cách dòng</strong>: Tăng/giảm khoảng cách giữa các dòng để phù hợp với khổ giấy 52mmx70mm</li>
                <li><strong>Căn lề trái</strong>: Điều chỉnh khoảng cách lề trái (từ 0mm đến 10mm)</li>
                <li>Nhập văn bản bạn muốn in vào ô phía trên và xem trước ở phần bên dưới</li>
                <li>Nhấn nút "In đến HRPT_LP80" để in trực tiếp</li>
                <li>Đảm bảm máy in HRPT_LP80 đã được kết nối và có giấy khổ 52mmx70mm</li>
            </ul>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const textInput = document.getElementById('textInput');
            const printBtn = document.getElementById('printBtn');
            const clearBtn = document.getElementById('clearBtn');
            const preview = document.getElementById('preview');
            
            // Controls
            const fontSize = document.getElementById('fontSize');
            const fontSizeValue = document.getElementById('fontSizeValue');
            const lineHeight = document.getElementById('lineHeight');
            const lineHeightValue = document.getElementById('lineHeightValue');
            const paddingLeft = document.getElementById('paddingLeft');
            const paddingLeftValue = document.getElementById('paddingLeftValue');
            
            // Cập nhật giá trị controls
            fontSize.addEventListener('input', updatePreview);
            lineHeight.addEventListener('input', updatePreview);
            paddingLeft.addEventListener('input', updatePreview);
            
            // Cập nhật preview khi người dùng nhập
            textInput.addEventListener('input', updatePreview);
            
            // Hiển thị giá trị controls
            fontSize.addEventListener('input', function() {
                fontSizeValue.textContent = `${this.value}px`;
            });
            
            lineHeight.addEventListener('input', function() {
                lineHeightValue.textContent = this.value;
            });
            
            paddingLeft.addEventListener('input', function() {
                paddingLeftValue.textContent = `${this.value}mm`;
            });
            
            // Xóa nội dung
            clearBtn.addEventListener('click', function() {
                textInput.value = '';
                updatePreview();
            });
            
            // Cập nhật preview
            function updatePreview() {
                if (!textInput.value.trim()) {
                    preview.textContent = 'Nội dung xem trước sẽ hiển thị ở đây...';
                    preview.style.fontSize = '10px';
                    preview.style.lineHeight = '1.2';
                    preview.style.paddingLeft = '2mm';
                    return;
                }
                
                preview.textContent = textInput.value;
                preview.style.fontSize = `${fontSize.value}px`;
                preview.style.lineHeight = lineHeight.value;
                preview.style.paddingLeft = `${paddingLeft.value}mm`;
            }
            
            // Chức năng in
            printBtn.addEventListener('click', function() {
                if (!textInput.value.trim()) {
                    alert('Vui lòng nhập nội dung trước khi in!');
                    return;
                }
                
                // Tạo một iframe ẩn để in
                const printContent = textInput.value;
                const printWindow = window.open('', '_blank');
                
                // Áp dụng các thiết lập từ controls
                const printFontSize = fontSize.value;
                const printLineHeight = lineHeight.value;
                const printPaddingLeft = paddingLeft.value;
                
                printWindow.document.write(`
                    <!DOCTYPE html>
                    <html>
                    <head>
                        <title>In từ trang web - GHN</title>
                        <style>
                            body {
                                font-family: Arial, sans-serif;
                                font-size: ${printFontSize}px;
                                line-height: ${printLineHeight};
                                padding: 2mm;
                                padding-left: ${printPaddingLeft}mm;
                                margin: 0;
                                width: 52mm;
                                height: 70mm;
                                overflow: hidden;
                                background: white;
                            }
                            @page {
                                size: 52mm 70mm;
                                margin: 0;
                            }
                            @media print {
                                body {
                                    margin: 0;
                                    padding: 2mm;
                                    padding-left: ${printPaddingLeft}mm;
                                    width: 52mm;
                                    height: 70mm;
                                    overflow: hidden;
                                }
                            }
                        </style>
                    </head>
                    <body>
                        ${printContent}
                    </body>
                    </html>
                `);
                printWindow.document.close();
                
                // Sau khi nội dung được tải, thực hiện in
                printWindow.onload = function() {
                    printWindow.focus();
                    printWindow.print();
                    // printWindow.close(); // Bạn có thể bỏ comment dòng này nếu muốn tự động đóng cửa sổ in
                };
            });
            
            // Khởi tạo preview
            updatePreview();
        });
    </script>
</body>
</html>
