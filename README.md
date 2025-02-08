# 🚀 Data_Flow_2025
## 📖 Tài liệu
- [NHẬP MÔN HỌC MÁY VÀ KHAI PHÁ DỮ LIỆU](https://users.soict.hust.edu.vn/khoattq/ml-dm-course/IT3190-Tai-lieu-doc.pdf)
## 🛠️ Tóm tắt kiến thức
### 1. Python cơ bản
Đây là kiến thức về Python tóm tắt [Click]{}
### 2. Data Science
- **Mục đích DS:** 
  - Các mục tiêu cuối cùng của khoa học dữ liệu có thể được gom thành:

    - Mô tả (Descriptive tasks)
  
    - Dự đoán(Predictive tasks)
  
  - Để đạt được mục tiêu này đòi hỏi phải thực hiện qua các bước:

    - Thu thập dữ liệu(Data scraping)
  
    - Làm sạch(Data cleaning), tiền xử lý(pre-processing) và tích hợp dữ liệu(integration).

    - Học máy
  
    - Trực quan hóa(Visualization)

- **Khoa học dữ liệu có thể áp dụng với nhiều loại(kiểu) dữ liệu khác nhau :**

    - Dữ liệu thô(số)
  
    - Dữ liệu văn bản

    - Dữ liệu ảnh, video

    - Dữ liệu đồ thị
 
- **Quy trình :** hướng tìm kiếm tri thức
  ![image](https://github.com/user-attachments/assets/c0a557cf-f9db-426b-8fcb-4f9f605bb2b6)

- Mô tả dữ liệu(Data description)
  
  - Mô tả dữ liệu: tóm tắt dữ liệu theo cách “có thể hiểu được“:
    
    - Thông qua **phân tích dữ liệu thăm dò(EDA -Exploratory Data Analysis)**
      
      - Hầu hết là các mô tả thống kê: average, standard deviation, median, PCA...
        
    - Thông qua trực quan hóa dữ liệu (data visualization)
   
- **Phân nhóm dữ liệu(Data segmentation)**
  
  - Phân nhóm dữ liệu: nhóm các bản ghi dữ liệu giống nhau thành các nhóm đồng nhất(tạo ra các cụm dữ liệu).
    
    - Các bản ghi trong một nhóm có các giá trị thuộc tính tương tự nhau
      
    - Mục tiêu học ra một thuộc tính (nhóm) “mới” từ các thuộc tính ở các bản ghi.
      
    - Có thể sử dụng các phương pháp học không giám sát (Unsupervised machine learning)
   
- **Luật kết hợp (Associationrules)**

  - Khám phá các quy tắc liên kết giữa các bản ghi dữ liệu dựa trên các tiêu chí được xác định trước

    - Vd: các sản phẩm thường được mua cùng nhau trong môt lần mua sắm
   
    - Học ra thông tin “mới” (các quy tắc) dựa trên các thuộc tính của dữ liệu
   
    - Có thể sử dụng các phương pháp học không giám sát (Unsupervised machine learning)
   
- **Dự đoán (Prediction)**

  - Dự đoán hoặc ước lượng các giá trị của một thuộc tính cho một tập các bản ghi(điểm) dữ liệu.
 
    - Thuộc tính được biết bởi các bản ghi khác
   
    - Tri thức mới sẽ được dùng để dự đoán các giá trị của thuộc tính này trên một tập các bản ghi
   
    - Có thể sử dụng các phương pháp học có giám sát (Supervised machine learning)


![image](https://github.com/user-attachments/assets/287cd8e1-d4b3-4be1-a074-f95ab1d8b863)
  
**2.1. Thu thập và tiền xử lý dữ liệu** (Phần này BTC sẽ cung cấp data, nên không cần thu nhập data)

**2.2. Làm sạch và tích hợp dữ liệu**

**2.2.1. Tích hợp dữ liệu - Data integration** (Phần này sẽ không có)

**2.2.2. Tiền xử lý dữ liệu - Data preprocessing** 

<p><b>Quá trình khai thác dữ liệu</b></p> <br>

![image](https://github.com/user-attachments/assets/b7c1cf53-bf71-4d4a-9088-8d6e5cc3e840)

- Tiền xử lý dữ liệu thật sự rất tốn kém

  - Trích xuất, làm sạch và biến đổi dữ liệu chiếm phần lớn khối lượng công việc khi xây dựng kho dữ liệu cũng như làm khoa học dữ liệu

- Dữ liệu không có chất lượng, rất khó để phân tích ra kết quả có ý nghĩa

  - Các quyết định tốt cần được đúc rút từ dữ liệu có chất lượng

    -  Vd., dữ liệu thiếu, mâu thuẫn lẫn nhau có thể đưa ra kết quả phân tích không đúng
   
- Phân loại các vấn đề về chất lượng dữ liệu

  - **Mức giá trị đơn lẻ - Value-level**
 
    - Giá trị thiếu: Một trường thuộc tính cần phải có nhưng lại không có giá trị
      
      - *Vd.:birthdate=‘’*
        
    - Vi phạm cú pháp: giá trị gi nhận không thỏa mãn luật về cú pháp định nghĩa cho giá trị trường thuộc tính
      
      - *Vd.:zipcode=27655-175;syntacticalrule:xxxx-xxx*
        
    - Lỗi chính tả

      - *Vd.:city=‘Lsboa’, thay vì giá trị đúng ‘Lisbon’* 

    - Vi phạm miền xác định: giá trị không thuộc về tập các giá trị có thể có
      
      - *Vd.:age=240; trong khi age:{0,120}* 
  
  - **Mức tập giá trị - Value-set (attribute/column) level**
    
    - Tồn tại các giá trị đồng nghĩa: thuộc tính có giá trị khác nhau nhưng có cùng ngữ nghĩa
   
      - *Vd.: emprego = ‘futebolista’; emprego = ‘jogador futebol’*

    - Tồn tại các từ đồng âm khác nghĩa

      - *Vd: Cùng một tên nhưng thuộc về nhiều tác giả khác nhau*
     
    - Tồn tại vi phạm tính đơn nhất:

      - *Vd.: hai khách hàng có cùng ID*
     
    - Tồn tại các vi phạm về rằng buộc toàn vẹn (Integrity contraint):
   
      - *Vd.: Tổng các % thành phần vượt quá 100*
  
  - **Mức bản ghi - Record level**

    - Vi phạm rằng buộc toàn vẹn
      
      - *Vd.: giá bán cuối cùng không bằng tổng giá + thuế VAT* 
  
  - **Mức quan hệ - Relation level**
    
    - Nhiều dạng biểu diễn khác nhau của dữ liệu: đây là vấn đề rất bình thường trong thực tế

      - *Vd.: name = ‘John Smith’; name = ‘Smith, John’*
        
    - Vi phạm ràng buộc phụ thuộc hàm
    
      - *Vd.: (2765-175, ‘Estoril’) và (2765-175, ‘Oeiras’)*
      
    - Sự tồn tại của các bản ghi gần như bị trùng lặp

      - *Vd.: (1, André Fialho, 12634268) và (2, André Pereira Fialho, 12634268)!* 

    - Vi phạm ràng buộc toàn vẹn
    
      - *Vd.: Tổng lương của nhân viên lớn hơn tổng ngân quỹ lương*
  
  - **Mức giữa các quan hệ với nhau - Multiple relations level** 

    - Nhiều dạng biểu diễn khác nhau của dữ liệu

      - *Vd.: một bảng lưu trữ số đo theo đơn vị metter, một bảng theo đơn vị inch*
     
    - Tồn tại các đồng nghĩa
    
    - Tồn tại các đồng âm khác nghĩa
    
    - Sự khác nhau về đơn vị phân mức (granularity level):

      - *Vd.: age:{0-30,31-60,>60};age:{0-25,26-40, 40-65, >65}*
    - Vi phạm ràng buộc tham chiếu
      
    - Tồn tại các bản ghi gần như trùng lặp
    
    - Vi phạm ràng buộc toàn vẹn
   
**Các tác vụ chính của tiền xử lý dữ liệu**

- Làm sạch dữ liệu - Data cleaning
  
  - Điền đầy các giá trị thiếu, làm mịn nhiễu, xác định và loại bỏ các ngoại lệ, phân giải sự không nhất quán trong dữ liệu
    
- Tích hợp dữ liệu - Data integration (bỏ)

  - Tích hợp nhiều cơ sở dữ liệu, nhiều nguồn dữ liệu khác nhau
    
- Chuyển đổi dữ liệu - Data transformation
  
  - Chuẩn hóa dữ liệu (quy chiếu dữ liệu theo phạm vi xác định) 
 
  - Kết tập dữ liệu – aggregation 

- Giảm nhẹ dữ liệu - Data reduction

  - Tìm một biểu diễn của dữ liệu nhỏ hơn về khối lượng nhưng vẫn đảm bảo kết quả phân tích 
 
  - Rời rạc hóa dữ liệu - Data discretization: đặc biệt quan trọng với dữ liệu số
    
  - Kết tập dữ liệu, giảm chiều dữ liệu, nén dữ liệu, khái quát hóa dữ liệu

**Xử lý dữ liệu thiếu**

- *Bỏ qua các bản ghi này:* nếu số lượng bản ghi có dữ liệu thiếu không quá nhiều, có thể xem xét bỏ đi
  
- *Xem xét từng giá trị bị thiếu và thêm vào:* tốn kém và không khả thi?
  
- *Sử dụng giá trị hằng toàn cục cho mọi giá trị thiếu:* Vd., “unknown”, “NULL”?!
  
- Sử dụng giá trị trung vị median để điền các giá trị thiếu
  
- Sử dụng giá trị bình quân (mean) của từng phân lớp cho giá trị thiếu của bản ghi ứng với phân lớp đó
  
- *Sử dụng giá trị có xác xuất cao nhất cho giá trị thiếu:* dựa vào học suy diễn như hồi quy, công thức 
Bayesian, cây quyết định

Chúng tôi gọi đây là giá trị sentinel: khi có mặt, nó chỉ ra một giá trị bị thiếu (hoặc rỗng):

```bash
In [14]: float_data = pd.Series([1.2, -3.5, np.nan, 0])

In [15]: float_data
Out[15]: 
0    1.2
1   -3.5
2    NaN
3    0.0
dtype: float64
```
Phương pháp này cung cấp cho chúng ta một chuỗi Boolean với các giá trị là ```bash null:isnaTrue```

```bash
In [16]: float_data.isna()
Out[16]: 
0    False
1    False
2     True
3    False
dtype: bool
```

Có một số cách để lọc ra dữ liệu bị thiếu. Mặc dù bạn luôn có tùy chọn để làm điều đó bằng tay, sử dụng và lập chỉ mục Boolean, nhưng có thể hữu ích. Trên một Series, nó trả về Series chỉ với dữ liệu không rỗng và các giá trị chỉ mục:```bash pandas.isnadropna```

```bash
In [23]: data = pd.Series([1, np.nan, 3.5, np.nan, 7])

In [24]: data.dropna()
Out[24]: 
0    1.0
2    3.5
4    7.0
dtype: float64
```
Điều này cũng giống như làm:

```bash
In [25]: data[data.notna()]
Out[25]: 
0    1.0
2    3.5
4    7.0
dtype: float64
```
Với các đối tượng DataFrame, có nhiều cách khác nhau để loại bỏ dữ liệu bị thiếu. Bạn có thể muốn bỏ các hàng hoặc cột đều là NA hoặc chỉ những hàng hoặc cột chứa bất kỳ NA nào. theo mặc định sẽ loại bỏ bất kỳ hàng nào chứa giá trị bị thiếu:```bash dropna```

```bash
In [26]: data = pd.DataFrame([[1., 6.5, 3.], [1., np.nan, np.nan],
   ....:                      [np.nan, np.nan, np.nan], [np.nan, 6.5, 3.]])

In [27]: data
Out[27]: 
     0    1    2
0  1.0  6.5  3.0
1  1.0  NaN  NaN
2  NaN  NaN  NaN
3  NaN  6.5  3.0

In [28]: data.dropna()
Out[28]: 
     0    1    2
0  1.0  6.5  3.0
```
Vượt qua sẽ chỉ bỏ các hàng đều là NA:```bash how="all"```

```bash
In [29]: data.dropna(how="all")
Out[29]: 
     0    1    2
0  1.0  6.5  3.0
1  1.0  NaN  NaN
3  NaN  6.5  3.0
```
*Điền vào dữ liệu bị thiếu*

Thay vì lọc ra dữ liệu bị thiếu (và có khả năng loại bỏ dữ liệu khác cùng với nó), bạn có thể muốn điền vào "lỗ hổng" theo bất kỳ cách nào. Đối với hầu hết các mục đích, phương pháp này là chức năng làm việc để sử dụng. Gọi bằng một hằng số sẽ thay thế các giá trị bị thiếu bằng giá trị đó:```bash fillna```

```bash
In [33]: df = pd.DataFrame(np.random.standard_normal((7, 3)))

In [34]: df.iloc[:4, 1] = np.nan

In [35]: df.iloc[:2, 2] = np.nan

In [36]: df
Out[36]: 
          0         1         2
0 -0.204708       NaN       NaN
1 -0.555730       NaN       NaN
2  0.092908       NaN  0.769023
3  1.246435       NaN -1.296221
4  0.274992  0.228913  1.352917
5  0.886429 -2.001637 -0.371843
6  1.669025 -0.438570 -0.539741

In [37]: df.dropna()
Out[37]: 
          0         1         2
4  0.274992  0.228913  1.352917
5  0.886429 -2.001637 -0.371843
6  1.669025 -0.438570 -0.539741

In [38]: df.dropna(thresh=2)
Out[38]: 
          0         1         2
2  0.092908       NaN  0.769023
3  1.246435       NaN -1.296221
4  0.274992  0.228913  1.352917
5  0.886429 -2.001637 -0.371843
6  1.669025 -0.438570 -0.539741

In [39]: df.fillna(0)
Out[39]: 
          0         1         2
0 -0.204708  0.000000  0.000000
1 -0.555730  0.000000  0.000000
2  0.092908  0.000000  0.769023
3  1.246435  0.000000 -1.296221
4  0.274992  0.228913  1.352917
5  0.886429 -2.001637 -0.371843
6  1.669025 -0.438570 -0.539741
```


**Xử lý dữ liệu nhiễu**

- Phương pháp tạo cột - Binning:
  
  - Sắp xếp dữ liệu và phân rã thành các cột có độ dầy bằng nhau
    
  - Làm mịn dữ liệu bằng cách sử dụng trung vị (median), số bình quân (mean) của các cột này, giá trị biên của các cột này
    
- Gom cụm - Clustering:
  
  - Nhận định và loại bỏ các ngoại lệ
    
- Hồi quy - Regression
  
  - Sử dụng các hàm hổi quy
    
- Bán tự động
  
  - Kết hợp mô hình và con người để xử lý dữ liệu nhiễu
 
**Xử lý dữ liệu không nhất quán**

- Xử lý bằng sức người, sử dụng các tài liệu tham chiếu bên ngoài (external references)
  
- Bán tự động sử dụng công cụ
  
  - Phát hiện các vi phạm ràng buộc phụ thuộc hàm và các ràng buộc khác của dữ liệu
    
  - Chỉnh sửa lại dữ liệu dư thừa
 
**Phương pháp luận cho làm sạch dữ liệu**

- Trích chọn các trường thuộc tính đơn mà có liên quan lẫn nhau

- Chuẩn hóa các trường bản ghi

- Chỉnh sửa lại dữ liệu ở mức giá trị đơn 

- Chỉnh sửa lại dữ liệu ở mức tập giá trị và mức bản ghi 

- Chỉnh sửa lại dữ liệu ở mức quan hệ 

- Chỉnh sửa lại dữ liệu ở mức đa quan hệ
  
- Xem xét đến feedback của người sử dụng
   
  - Để giải quyết các vấn đề của dữ liệu mà không thể làm bằng các phương pháp chuẩn và tự động
  
- *Tính hiệu quả của làm sạch dữ liệu và biến đổi dữ liệu cần được đánh giá cho cùng 1 tập dữ liệu*

**Tích hợp dữ liệu - Data integration**

- Là bài toán kết hợp dữ liệu từ nhiều nguồn thành một hệ dữ liệu nhất quán, chặt chẽ 

- Xây dựng lược đồ trung gian : 

  - Vd. Chuẩn hóa các trường thuộc tính vd., A.cust-id = B.cust-#

- Định danh các thực thể bản ghi dữ liệu từ nhiều nguồn

  - Vd., Bill Clinton = William Clinton
    
- Phát hiện và giải quyết các xung đột dữ liệu khi tích hợp từ nhiều nguồn 

  - Biểu diễn dữ liệu khác nhau, phạm vi dữ liệu khác nhau (scales)

 **Biến đổi dữ liệu - Data transformation**

- Làm mịn - Smoothing: khử nhiễu từ dữ liệu 

- Kết tập - Aggregation: tổng kết, thống kê về dữ liệu 

- Khái quát hóa - Generalization

- Chuẩn hóa - Normalization: co kéo dữ liệu theo phạm vi phù hợp
  
  - Chuẩn hóa min-max

  - Chuẩn hóa z-score 

  - Chuẩn hóa theo thang thập phân - decimal scaling

- Kỹ nghệ xây dựng các đặc trưng - Attribute/feature engineering

**Ví dụ về chuẩn hóa**

- Chuẩn hóa Min-Max là phương pháp ánh xạ dữ liệu về khoảng **[NewMin, NewMax]** theo công thức:

$$
x'_i = \frac{x_i - \text{OriginalMin}}{\text{OriginalMax} - \text{OriginalMin}} \times (\text{NewMax} - \text{NewMin}) + \text{NewMin}
$$

```bash
import numpy as np

def min_max_scaling(data, new_min, new_max):
    """
    Chuẩn hóa Min-Max dữ liệu về khoảng [new_min, new_max]
    
    Parameters:
    - data (list hoặc numpy array): Dữ liệu đầu vào
    - new_min (float): Giá trị Min mới sau khi chuẩn hóa
    - new_max (float): Giá trị Max mới sau khi chuẩn hóa
    
    Returns:
    - Numpy array chứa dữ liệu đã được chuẩn hóa
    """
    original_min = np.min(data)
    original_max = np.max(data)
    
    scaled_data = (data - original_min) / (original_max - original_min) * (new_max - new_min) + new_min
    return scaled_data

# Ví dụ dữ liệu ban đầu
data = np.array([5, 10, 15, 20, 25])
new_min, new_max = 0, 1

# Chuẩn hóa dữ liệu
normalized_data = min_max_scaling(data, new_min, new_max)

# In kết quả
print("Dữ liệu gốc:", data)
print("Dữ liệu sau khi chuẩn hóa:", normalized_data)

>>> Dữ liệu gốc: [ 5 10 15 20 25]
>>> Dữ liệu sau khi chuẩn hóa: [0.   0.25 0.5  0.75 1.  ]
```
- Chuẩn hóa Z-score : (μ: mean, σ: standard deviation):

$$
v' = \frac{v - μ_A}{σ_A}
$$

```bash
import numpy as np

def z_score_normalization(data):
    """
    Chuẩn hóa dữ liệu bằng phương pháp Z-score.
    
    data: Danh sách hoặc mảng numpy chứa dữ liệu đầu vào.
    return: Mảng numpy chứa dữ liệu đã được chuẩn hóa.
    """
    mean = np.mean(data)  # Tính giá trị trung bình (μ)
    std_dev = np.std(data)  # Tính độ lệch chuẩn (σ)
    
    z_scores = (data - mean) / std_dev  # Áp dụng công thức Z-score
    return z_scores

# Dữ liệu ví dụ
data = np.array([10, 20, 30, 40, 50])

# Áp dụng chuẩn hóa Z-score
normalized_data = z_score_normalization(data)

# In kết quả
print("Dữ liệu gốc:", data)
print("Dữ liệu sau khi chuẩn hóa Z-score:", normalized_data)

>>> Dữ liệu gốc: [10 20 30 40 50]
>>> Dữ liệu sau khi chuẩn hóa Z-score: [-1.414 -0.707 0. 0.707 1.414]
```
- Chuẩn hóa theo thang thập phân: Đảm bảo dữ liệu được kéo về khoảng 1 và −1 (Cách này thường ít dùng)
 - Với điều kiện n là số chữ số của giá trị lớn nhất

 $$
 x'_i = \frac{x_i}{10^n}
 $$

**Giảm nhẹ dữ liệu - Data reduction**

- Tìm một biểu diễn của dữ liệu nhỏ hơn về khối lượng nhưng vẫn đảm. bảo kết quả phân tích 

  - Giảm chiều dữ liệu - Dimensionality reduction

    - Lựa chọn đặc trưng 

    - Trích rút đặc trưng (vd. Phân tích PCA)

  - Nén dữ liệu - Data Compression

    - Chuyển đổi dữ liệu văn bản thành dữ liệu số
    
    - Phân cụm dữ liệu 

  - Rời rạc hóa dữ liệu - Discretization

    - Biến đổi dữ liệu liên tục về dữ liệu phân lớp
   
**2.2.3. Phân tích và khám phá dữ liệu**

**Mục tiêu**
- Hiểu các vẫn đề cốt lõi trong phân tích thăm dò dữ liệu (EDA)
  
- Diễn giải và sử dụng các công cụ thống kê cho EDA
  
- Biểu diễn và diễn giải các đồ thị và biểu đồ cho EDA

**Đặt vấn đề** 

- Muốn khai thác được dữ liệu, trước hết cần phải hiểu dữ liệu đang có
  
- Tại sao ?
  
  - Nhận biết các sai sót trong dữ liệu
  
  - Nhận biết các đặc trưng pattern của dữ liệu
  
  - Nhận biết nếu các giả định thống kê hiện tại không phù hợp với dữ liệu 

  - Có căn cứ để đưa ra các giả thiết về dữ liệu 
  
  -… nếu không hiểu dữ liệu, sẽ gặp nhất nhiều khó khăn để khai thác được giá trị từ dữ liệu

**Trọng tâm của EDA**

-  EDA quan tâm tới cấu trúc, các ngoại lệ, và các mô hình từ dữ liệu 

- EDA quan tâm tới tất cả các điểm dữ liệu trong tập dữ liệu
  
  - Các thống kê 

  - Trực quan hóa 

  - Phân cụm và phát hiện bất thường 

  - Giảm chiều dữ liệu
 
EDA không phải là một tập các kỹ thuật, mà là một triết lý về cách mà chúng ta nên làm khi muốn hiểu về dữ liệu

- Hỗ trợ lựa chọn đúng đắn các công cụ để tiền xử lý và phân tích dữ liệu
  
- Cho phép sử dụng kinh nghiệm con người trong việc phát hiện và nhìn nhận các đặc trưng pattern của dữ liệu

**Các câu hỏi chính khi phân tích EDA**

-  Giá trị tiêu chuẩn trong dữ liệu là bao nhiêu?
-
-  Tính nhiễu của dữ liệu như thế nào?
-
-  Dữ liệu có tuân theo phân bố nào không?
-
-  Đặc trưng nào trong dữ liệu quan trọng với bài toán cần 
phân tích?

- Đặc trưng này của dữ liệu có quan trọng với bài toán cần 
phân tích không?

- Có thể mô tả mối tương quan giữa đặc trưng của dữ liệu và bài toán phân tích như thế nào?

- Có thể phân rã tín hiệu đúng và nhiễu trong dữ liệu hay 
không?

- Có thể trích xuất cấu trúc từ dữ liệu hay không?

- Dữ liệu có ngoại lệ outliers hay không? 

**EDA là một quá trình lặp**

- Repeat...

  - Nhận diện và ưu tiên các câu hỏi liên quan theo thứ tự giảm dần độ quan trọng

  - Đặt câu hỏi
• Xây dựng các đồ thị, biểu đồ để có thể trả lời câu hỏi đặt ra 
• Xem xét các kết quả và đặt ra các câu hỏi mớ

```bash
# Clone repo
git clone https://github.com/user/repo.git

# Cài đặt thư viện cần thiết
pip install -r requirements.txt

# Chạy chương trình
python main.py
```

