<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Điều chỉnh kích thước dòng in - HRPT_LP80</title>
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
        }
        
        @media print {
            body * {
                visibility: hidden;
            }
            .preview-section, .preview-section * {
                visibility: visible;
            }
            .preview-section {
                position: absolute;
                left: 0;
                top: 0;
                width: 100%;
                border: none;
                padding: 0;
                margin: 0;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Điều chỉnh kích thước dòng in</h1>
            <p class="description">Tùy chỉnh kích thước dòng và in trực tiếp đến máy in HRPT_LP80</p>
        </header>
        
        <div class="control-panel">
            <h2>Cài đặt in</h2>
            <div class="control-group">
                <span class="control-label">Kích thước chữ:</span>
                <input type="range" id="fontSize" min="12" max="24" value="16" step="1">
                <span id="fontSizeValue" class="value-display">16px</span>
            </div>
            <div class="control-group">
                <span class="control-label">Khoảng cách dòng:</span>
                <input type="range" id="lineHeight" min="1.2" max="2.5" value="1.5" step="0.1">
                <span id="lineHeightValue" class="value-display">1.5</span>
            </div>
            <div class="control-group">
                <span class="control-label">Căn lề trái:</span>
                <input type="range" id="paddingLeft" min="0" max="50" value="20" step="5">
                <span id="paddingLeftValue" class="value-display">20px</span>
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
                <h2>Xem trước khi in</h2>
            </div>
            <div id="preview" class="preview-content">Nội dung xem trước sẽ hiển thị ở đây...</div>
        </section>
        
        <div class="instructions">
            <h3><span class="icon">💡</span> Hướng dẫn sử dụng:</h3>
            <ul>
                <li><strong>Kích thước chữ</strong>: Điều chỉnh thanh trượt để thay đổi kích thước chữ trong bản in</li>
                <li><strong>Khoảng cách dòng</strong>: Tăng/giảm khoảng cách giữa các dòng để dễ đọc hơn</li>
                <li><strong>Căn lề trái</strong>: Điều chỉnh khoảng cách lề trái cho phù hợp</li>
                <li>Nhập văn bản bạn muốn in vào ô phía trên và xem trước ở phần bên dưới</li>
                <li>Nhấn nút "In đến HRPT_LP80" để in trực tiếp</li>
                <li>Đảm bảm máy in HRPT_LP80 đã được kết nối và bật</li>
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
                paddingLeftValue.textContent = `${this.value}px`;
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
                    preview.style.fontSize = '16px';
                    preview.style.lineHeight = '1.5';
                    preview.style.paddingLeft = '20px';
                    return;
                }
                
                preview.textContent = textInput.value;
                preview.style.fontSize = `${fontSize.value}px`;
                preview.style.lineHeight = lineHeight.value;
                preview.style.paddingLeft = `${paddingLeft.value}px`;
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
                        <title>In từ trang web HRPT_LP80</title>
                        <style>
                            body {
                                font-family: Arial, sans-serif;
                                font-size: ${printFontSize}px;
                                line-height: ${printLineHeight};
                                padding-left: ${printPaddingLeft}px;
                                padding-right: 20px;
                                white-space: pre-wrap;
                            }
                            @media print {
                                body {
                                    padding: 0;
                                    margin: 0;
                                }
                                @page {
                                    margin: 2cm;
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
