# 🧪 Selenium WebDriver Automation Tests

![Tests](https://github.com/Thuan-fe004/selenium-automation-tests/actions/workflows/selenium-tests.yml/badge.svg)
![Python Version](https://img.shields.io/badge/python-3.9%20%7C%203.10%20%7C%203.11-blue)
![Selenium](https://img.shields.io/badge/selenium-4.15.0-green)

Bộ test automation hoàn chỉnh cho các chức năng web phổ biến sử dụng Selenium WebDriver với Python.

## 📋 Mục lục

- [Giới thiệu](#giới-thiệu)
- [Test Cases](#test-cases)
- [Công nghệ](#công-nghệ)
- [Cài đặt](#cài-đặt)
- [Chạy Tests](#chạy-tests)
- [CI/CD](#cicd)
- [Kết quả](#kết-quả)
- [Cấu trúc dự án](#cấu-trúc-dự-án)

## 🎯 Giới thiệu

Dự án này cung cấp một bộ test automation đầy đủ cho các tính năng web phổ biến:
- Xử lý JavaScript Popups
- Drag and Drop
- Multiple Windows/Tabs
- iFrames
- Dynamic Controls

Tất cả tests được tự động hóa với **GitHub Actions CI/CD**, chạy tự động khi có code mới.

## 📝 Test Cases

### Bài 1: Xử lý JavaScript Popup
**URL**: https://the-internet.herokuapp.com/javascript_alerts

| ID | Test Case | Mô tả |
|----|-----------|-------|
| TC_01_01 | Click button JS Alert | Xử lý alert popup |
| TC_01_02 | Xác minh text Alert | Kiểm tra nội dung alert |
| TC_01_03 | JS Confirm - Dismiss | Nhấn Cancel trên confirm |
| TC_01_04 | JS Confirm - Accept | Nhấn OK trên confirm |
| TC_01_05 | Nhập text vào Prompt | Input dữ liệu vào prompt |
| TC_01_06 | Xác minh kết quả Prompt | Kiểm tra text đã nhập |

**Tổng: 6 test cases**

### Bài 2: Kéo và Thả (Drag and Drop)
**URL**: https://the-internet.herokuapp.com/drag_and_drop

| ID | Test Case | Mô tả |
|----|-----------|-------|
| TC_02_01 | Vị trí ban đầu | Kiểm tra vị trí khởi tạo |
| TC_02_02 | Thực hiện Drag and Drop | Kéo thả element |
| TC_02_03 | Xác minh hoán đổi vị trí | Verify swap thành công |

**Tổng: 3 test cases**

### Bài 3: Chuyển đổi giữa nhiều cửa sổ
**URL**: https://the-internet.herokuapp.com/windows

| ID | Test Case | Mô tả |
|----|-----------|-------|
| TC_03_01 | Lấy window handle chính | Get main window |
| TC_03_02 | Mở cửa sổ mới | Open new window |
| TC_03_03 | Chuyển sang cửa sổ mới | Switch to new window |
| TC_03_04 | Xác minh nội dung | Verify window content |
| TC_03_05 | Quay về cửa sổ chính | Return to main window |

**Tổng: 5 test cases**

### Bài 4: Tương tác với iFrame
**URL**: https://the-internet.herokuapp.com/iframe

| ID | Test Case | Mô tả |
|----|-----------|-------|
| TC_04_01 | Chuyển vào iframe | Switch to iframe |
| TC_04_02 | Xóa nội dung cũ | Clear editor content |
| TC_04_03 | Nhập nội dung mới | Input new text |
| TC_04_04 | Xác minh nội dung | Verify text input |
| TC_04_05 | Quay về trang chính | Switch to default |

**Tổng: 5 test cases**

### Bài 5: Kiểm thử với dữ liệu động
**URL**: https://the-internet.herokuapp.com/dynamic_controls

| ID | Test Case | Mô tả |
|----|-----------|-------|
| TC_05_01 | Checkbox hiển thị ban đầu | Check initial state |
| TC_05_02 | Click button Remove | Remove checkbox |
| TC_05_03 | Message sau khi remove | Verify message |
| TC_05_04 | Checkbox đã biến mất | Verify invisibility |
| TC_05_05 | Click button Add | Add checkbox back |
| TC_05_06 | Checkbox xuất hiện lại | Verify visibility |
| TC_05_07 | Enable input field | Enable input |
| TC_05_08 | Nhập dữ liệu vào input | Input text |

**Tổng: 8 test cases**

## 🎉 Tổng kết

**27 test cases** được tự động hóa hoàn toàn với:
- ✅ Explicit Waits
- ✅ Proper Assertions
- ✅ Exception Handling
- ✅ Excel Reports
- ✅ CI/CD Integration

## 🛠️ Công nghệ

- **Python**: 3.9, 3.10, 3.11
- **Selenium WebDriver**: 4.15.0
- **Chrome Browser**: Latest stable
- **Excel**: openpyxl 3.1.2
- **Data**: pandas 2.1.3
- **CI/CD**: GitHub Actions

## 📦 Cài đặt

### Prerequisites
- Python 3.9 trở lên
- Chrome Browser

### Bước 1: Clone repository
```bash
git clone https://github.com/Thuan-fe004/selenium-automation-tests.git
cd selenium-automation-tests
```

### Bước 2: Cài đặt dependencies
```bash
pip install -r requirements.txt
```

## 🚀 Chạy Tests

### Chạy local
```bash
cd tests
python selenium_test_suite.py
```

### Chạy với headless mode
```bash
export CI=true
python selenium_test_suite.py
```

### Xem kết quả
Kết quả được xuất ra file: `Selenium_Test_Results.xlsx` với 2 sheet:
- **Test Results**: Chi tiết từng test case
- **Summary**: Tổng hợp kết quả

## 🔄 CI/CD

### Tự động chạy khi:
1. ✅ **Push code** lên branch `main` hoặc `develop`
2. ✅ **Tạo Pull Request**
3. ✅ **Schedule**: Mỗi ngày lúc 9:00 AM UTC
4. ✅ **Manual**: Click "Run workflow" trong Actions tab

### Xem kết quả CI/CD:
1. Vào tab **Actions** trên GitHub
2. Click vào workflow run mới nhất
3. Download **artifacts** để xem Excel report

### Matrix Testing:
Tests chạy trên nhiều Python versions:
- Python 3.9
- Python 3.10
- Python 3.11

## 📊 Kết quả

### Console Output
```
================================================================================
SELENIUM WEBDRIVER - BỘ KIỂM THỬ TỰ ĐỘNG
================================================================================
Thời gian bắt đầu: 2025-01-12 14:30:45
✓ WebDriver đã khởi tạo thành công!

================================================================================
BÀI 1: XỬ LÝ JAVASCRIPT POPUP
================================================================================

Test Case 1: JS Alert
   ✓ TC_01_01: Click button JS Alert - PASSED
   ✓ TC_01_02: Xác minh text Alert - PASSED
...
```

### Excel Report
File Excel chứa:
- Chi tiết tất cả test cases
- Status với màu sắc (PASSED = xanh, FAILED = đỏ)
- Expected vs Actual results
- Execution time
- Notes cho failed tests

## 📁 Cấu trúc dự án

```
selenium-automation-tests/
├── .github/
│   └── workflows/
│       └── selenium-tests.yml       # GitHub Actions workflow
├── tests/
│   └── selenium_test_suite.py       # Main test file
├── reports/
│   └── .gitkeep                     # Keep folder
├── requirements.txt                 # Python dependencies
├── .gitignore                       # Git ignore rules
└── README.md                        # Documentation
```

## 🔧 Cấu hình

### Chrome Options (CI/CD)
```python
chrome_options.add_argument('--headless=new')
chrome_options.add_argument('--no-sandbox')
chrome_options.add_argument('--disable-dev-shm-usage')
chrome_options.add_argument('--disable-gpu')
```

### Timeout Settings
- Default wait: 10 seconds
- Workflow timeout: 15 minutes

## 🐛 Troubleshooting

### Lỗi: ChromeDriver not found
```bash
pip install webdriver-manager --upgrade
```

### Lỗi: Tests timeout
Tăng timeout trong workflow:
```yaml
timeout-minutes: 20
```

### Lỗi: Element not found
Kiểm tra explicit waits trong code

## 📈 Roadmap

- [ ] Thêm HTML test report
- [ ] Screenshot khi test fail
- [ ] Slack/Email notifications
- [ ] Parallel test execution
- [ ] Cross-browser testing (Firefox, Edge)
- [ ] Performance metrics

## 🤝 Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create feature branch
3. Commit changes
4. Push to branch
5. Create Pull Request

## 📝 License

MIT License - see LICENSE file

## 👤 Author

**Thuận Đỗ**
- GitHub: [@Thuan-fe004](https://github.com/Thuan-fe004)

## 🙏 Acknowledgments

- [Selenium](https://www.selenium.dev/)
- [The Internet - Herokuapp](https://the-internet.herokuapp.com/)
- [GitHub Actions](https://github.com/features/actions)

---

**⭐ Nếu project hữu ích, hãy cho một star!**