# LabelImg – Installation Guide

## 1. Yêu cầu hệ thống
- OS: Windows 10 / 11
- Python: **3.8 – 3.9 (khuyến nghị)**  
  ⚠️ Python 3.10+ dễ gặp bug
- Git đã cài sẵn

### Repo chính thức: `https://github.com/HumanSignal/labelImg.git`

---

## 2. Clone repository chính thức
```bash
git clone https://github.com/tzutalin/labelImg.git
cd labelImg
```

## 3. Cài thư viện

```bash
pip install PyQt5 lxml
```

## 4. Tạo `resources.qrc`

```bash
pyrcc5 -o libs/resources.py resources.qrc
```

## 5. Thay hàm đổi `show_bounding_box_from_annotation_file` trong file `labelImg.py` (nếu lỗi thì mới cần thay)

```python
def show_bounding_box_from_annotation_file(self, file_path):
    if file_path is None:
        return
```

## 6. Chạy `labelImg.py`

```python
python labelImg.py
```
