# Set up cho dự án nttStore

## Dirrctory

### Cài đặt FE với Vite

Cú pháp, tạo thư mục dự án

```CMD
mkdir nttStore
```

Tạo frontend: 
Tạo ra folder frontend và sau đó cài đặt dự án react bằng vite, sau đó install tailwindcss vào dự án react
```CMD
npm create vite@latest frontend -- --template react
cd frontend
npm i


npm i -D tailwindcss postcss autoprefixer
npx tailwindcss init -p

```
Để vào file index.css
```CSS
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Test thử có tailwindcss chưa

```JSX
export default function App() {
  return (
    <h1 className="text-3xl font-bold underline">
      Hello world!
    </h1>
  )
}
```
Tạo dự án cài đặt npm init -y, sau đó cài đặt thư viện

```cmd
npm init -y
```
Các thư viện cài đặc cho backend

**nodemon**

Nó giúp tự động khởi động lại ứng dụng Node.js mỗi khi bạn lưu thay đổi trong mã nguồn của ứng dụng. Điều này giúp bạn tiết kiệm thời gian và công sức khi phát triển, vì bạn không cần phải thủ công khởi động lại ứng dụng sau mỗi lần thay đổi mã nguồn.

**multer**
Là một middleware sử dụng trong ứng dụng web Node.js để xử lý tải tệp lên máy chủ Đặc biệt, "multer" thường được sử dụng để quản lý tệp đính kèm (file uploads) trong các ứng dụng web, như khi người dùng tải lên hình ảnh, video, tài liệu, và các tệp khác.

Các tính năng chính của "multer" bao gồm:
1. Xử lý tải lên: "multer" cho phép bạn xử lý tệp được tải lên từ các yêu cầu HTTP POST. Bạn có thể chỉ định nơi lưu trữ các tệp tải lên trên máy chủ.

2. Quản lý tệp: "multer" giúp bạn đặt ra các quy tắc về loại tệp được chấp nhận, kích thước tối đa, định dạng tên tệp, và các tham số tùy chỉnh khác để kiểm soát việc tải lên tệp.

3. Xử lý nhiều tệp: "multer" cho phép tải lên nhiều tệp trong cùng một yêu cầu HTTP và cung cấp thông tin về từng tệp.

4. Tích hợp dễ dàng: "multer" tích hợp dễ dàng với các framework web phổ biến như Express.js và hỗ trợ cho việc xử lý tệp đính kèm dễ dàng và hiệu quả.

**mongoose** 
một công cụ được sử dụng chủ yếu cho việc tương tác với cơ sở dữ liệu MongoDB khi bạn phát triển ứng dụng Node.js.

1. Định nghĩa mô hình dữ liệu: Mongoose cho phép bạn định nghĩa cấu trúc dữ liệu của các tài liệu (document) trong cơ sở dữ liệu MongoDB bằng cách sử dụng các Schema. Mô hình dữ liệu này giúp xác định các trường, kiểu dữ liệu, và quy tắc cho dữ liệu được lưu trữ trong MongoDB.

2. Tạo và truy vấn cơ sở dữ liệu: Mongoose cung cấp các phương thức dễ sử dụng để thêm, cập nhật, xóa và truy vấn dữ liệu trong cơ sở dữ liệu MongoDB. Điều này giúp bạn tương tác với cơ sở dữ liệu MongoDB một cách tiện lợi và linh hoạt.

3. Validation: Mongoose cho phép bạn xác thực dữ liệu trước khi lưu trữ nó trong cơ sở dữ liệu, đảm bảo tính nhất quán và an toàn của dữ liệu.

4. Middleware: Bạn có thể sử dụng middleware trong Mongoose để thực hiện các chức năng tùy chỉnh trước hoặc sau khi lưu trữ hoặc truy vấn dữ liệu.

5. Tương tác với các tính năng nâng cao: Mongoose hỗ trợ nhiều tính năng nâng cao như quan hệ,

**jsonwebtoken**
jsonwebtoken là một công cụ phổ biến được sử dụng để tạo và xác minh các token JSON Web Token (JWT) trong các ứng dụng web và dịch vụ web. JWT là một tiêu chuẩn mở được sử dụng để đại diện cho thông tin trong một đối tượng JSON có chữ ký số để đảm bảo tính toàn vẹn và xác thực.

1. Tạo JWT: Thư viện "jsonwebtoken" cho phép bạn tạo các JWT bằng cách cung cấp dữ liệu và một khóa bí mật. JWT có thể chứa thông tin như người dùng, quyền truy cập, thời gian hết hạn, và các thông tin tùy chỉnh khác.

2. Xác minh JWT: Bạn có thể sử dụng "jsonwebtoken" để kiểm tra tính hợp lệ của JWT bằng cách kiểm tra chữ ký số bằng khóa bí mật. Điều này đảm bảo rằng JWT không bị sửa đổi và đến từ nguồn tin cậy.

3. Phân tích JWT: Thư viện cung cấp cách dễ dàng để trích xuất thông tin từ JWT, như người dùng đã xác thực, quyền truy cập, và thông tin tùy chỉnh khác.

4. Hỗ trợ cho các thuật toán chữ ký: "jsonwebtoken" hỗ trợ nhiều thuật toán chữ ký, bao gồm HS256 (HMAC SHA-256) và RS256 (RSA SHA-256). Điều này cho phép bạn lựa chọn thuật toán tùy chỉnh cho việc tạo và xác minh JWT.

Thư viện "jsonwebtoken" thường được sử dụng trong các ứng dụng web để quản lý xác thực người dùng, quản lý phiên làm việc (session), và bảo mật các API. JWT thường được truyền qua các tiêu đề HTTP hoặc trong phần thân của yêu cầu HTTP để xác thực người dùng hoặc quyền truy cập.


**express-formidable**

Thư viện "express-formidable" là một middleware dành cho framework web Node.js Express, được sử dụng để xử lý các yêu cầu HTTP chứa dữ liệu biểu mẫu (form data), đặc biệt là tập tin đính kèm (file uploads) trong các biểu mẫu HTML. Nó giúp bạn dễ dàng xử lý dữ liệu gửi từ biểu mẫu và tệp tải lên trong ứng dụng Express.

Dưới đây là một số tính năng chính và cách sử dụng "express-formidable":

1. Xử lý dữ liệu biểu mẫu: "express-formidable" cho phép bạn trích xuất các trường dữ liệu từ biểu mẫu HTML gửi lên qua yêu cầu HTTP. Bạn có thể dễ dàng truy cập các giá trị được gửi từ các trường input trong biểu mẫu.

2. Xử lý tệp tải lên: Thư viện này cung cấp tích hợp cho việc xử lý tệp tải lên. Bạn có thể truy cập các tệp đính kèm, lưu chúng trên máy chủ hoặc thực hiện các thao tác tùy chỉnh với tệp tải lên.

3. Tùy chỉnh xử lý tệp: "express-formidable" cho phép bạn cấu hình các tùy chọn như nơi lưu trữ các tệp tải lên, kiểu tệp được chấp nhận, kích thước tối đa, và nhiều tùy chọn khác để kiểm soát cách tệp tải lên được xử lý.

**express-async-handler**

"express-async-handler" là một middleware cho framework web Node.js Express được sử dụng để xử lý lỗi trong các hàm xử lý tài liệu (route handlers) khi sử dụng JavaScript async/await. Nó giúp quản lý các lỗi trong các hàm xử lý tài liệu một cách dễ dàng và hiệu quả bằng cách tự động xử lý các lỗi được ném ra từ các hàm async và chuyển chúng đến middleware xử lý lỗi của Express.

Trong Express, khi một lỗi xảy ra trong một hàm xử lý tài liệu, bạn có thể sử dụng next để truyền lỗi đó đến middleware xử lý lỗi chung. Tuy nhiên, khi bạn sử dụng async/await trong các hàm xử lý tài liệu, việc quản lý lỗi có thể trở nên phức tạp hơn. "express-async-handler" giúp giải quyết vấn đề này bằng cách tự động xử lý các lỗi được ném ra từ các hàm async và chuyển chúng đến middleware xử lý lỗi của Express.

**Express**

Express.js, thường được gọi là Express, là một framework web Node.js phổ biến và mạnh mẽ được sử dụng để xây dựng ứng dụng web và API. Nó cung cấp một tập hợp các tính năng và công cụ giúp bạn dễ dàng xây dựng ứng dụng web hiệu quả và nhanh chóng.

Dưới đây là một số điểm quan trọng về Express:

1. Minh bạch và tối giản: Express được thiết kế để làm cho việc phát triển ứng dụng web Node.js dễ dàng hơn. Nó cung cấp một cơ sở cho xây dựng các ứng dụng web mà không cần nhiều cấu hình phức tạp.

2. Routing: Express cho phép bạn xác định các tuyến đường (routes) để định rõ cách yêu cầu HTTP cụ thể nên được xử lý. Điều này giúp bạn xây dựng các ứng dụng đáp ứng các yêu cầu GET, POST, PUT, DELETE, và nhiều loại yêu cầu khác.

3. Middleware: Express sử dụng kiến trúc middleware, cho phép bạn thêm các chức năng trung gian vào xử lý yêu cầu. Middleware có thể thực hiện nhiều chức năng, như xác thực, xử lý lỗi, ghi nhật ký, nén dữ liệu, và nhiều chức năng tùy chỉnh khác.

4. Xử lý tệp tải lên: Express cho phép bạn dễ dàng xử lý tệp tải lên từ yêu cầu HTTP, giúp bạn quản lý các trường hợp tải lên tệp dễ dàng.

5. Cơ sở dữ liệu: Express không bắt buộc bạn sử dụng một loại cơ sở dữ liệu cụ thể nào, nhưng nó tương thích tốt với nhiều cơ sở dữ liệu phổ biến và có thư viện hỗ trợ cho MongoDB, MySQL, PostgreSQL, và nhiều hệ thống cơ sở dữ liệu khác.

6. Hỗ trợ template engine: Express cho phép bạn sử dụng các template engine như EJS, Pug (formerly Jade), Handlebars, và nhiều loại khác để tạo các trang web động.

7. Phát triển dự án lớn: Express thích hợp cho cả ứng dụng nhỏ và lớn. Nó không áp đặt quy tắc cụ thể nào và cho phép bạn tự do thiết kế cấu trúc ứng dụng theo cách bạn muốn.

Express là một trong những framework web phổ biến nhất trong cộng đồng Node.js và rất thích hợp cho việc phát triển các ứng dụng web và API hiệu quả và linh hoạt.

**dotenv**

"dotenv" là một thư viện Node.js được sử dụng để quản lý biến môi trường trong ứng dụng Node.js. Biến môi trường (environment variables) thường được sử dụng để lưu trữ cấu hình ứng dụng, thông tin kết nối đến cơ sở dữ liệu, khóa bí mật, và các giá trị cấu hình khác mà bạn không muốn lưu trực tiếp trong mã nguồn ứng dụng. Thay vì lưu trữ cứng trong mã nguồn, bạn có thể đọc các biến môi trường từ một tệp .env hoặc từ môi trường máy chủ.

"dotenv" giúp bạn đọc và quản lý biến môi trường từ tệp .env. Thư viện này cung cấp một cách đơn giản để tải các biến môi trường từ tệp .env vào quá trình của ứng dụng Node.js. Bạn có thể sử dụng biến môi trường trong mã nguồn của mình giống như bất kỳ biến nào khác.

**cors**

CORS là viết tắt của "Cross-Origin Resource Sharing," một cơ chế trong web development cho phép trình duyệt web yêu cầu tài nguyên từ một tên miền khác nơi trang web gốc đang chạy. Nó là một cơ chế bảo mật giúp ngăn chặn các cuộc tấn công từ các trang web không đáng tin cậy và bảo vệ tài nguyên trên máy chủ của bạn.

Khi một trình duyệt web cố gắng tải một tài nguyên từ một tên miền khác, trình duyệt sẽ gửi một yêu cầu HTTP OPTIONS gọi là "preflight request" để xác minh xem tài nguyên đó có thể được truy cập từ tên miền hiện tại không. Nếu máy chủ phản hồi với các đầu mục (headers) phù hợp, trình duyệt sẽ cho phép tải tài nguyên đó.

CORS hoạt động dựa trên cơ chế "same-origin policy," một nguyên tắc bảo mật trong web development. Nguyên tắc này đòi hỏi rằng một trang web chỉ có thể tải tài nguyên từ cùng một tên miền mà trang web đó đang chạy. CORS cho phép bạn mở rộng sự truy cập để cho phép các trang web khác nơi tên miền khác có thể truy cập tài nguyên từ máy chủ của bạn.

CORS cung cấp một cách để cấu hình máy chủ web để xác định các tên miền nào được phép truy cập tài nguyên. Bạn có thể cấu hình máy chủ để cho phép truy cập từ một danh sách cụ thể các tên miền hoặc để cho phép truy cập từ tất cả các tên miền. Bạn có thể cấu hình các đầu mục (headers) để kiểm soát các loại yêu cầu và phản hồi được phép. CORS giúp bảo vệ tài nguyên và dữ liệu trên máy chủ của bạn, đồng thời cho phép tích hợp dữ liệu từ các nguồn khác nhau trong ứng dụng web của bạn.

**cookie-parser**

"cookie-parser" là một middleware cho framework web Node.js Express, được sử dụng để xử lý và quản lý các cookie trong ứng dụng web. Cookie là một cách để lưu trữ thông tin trên máy khách (trình duyệt) và truyền nó lại cho máy chủ mỗi khi trình duyệt gửi yêu cầu HTTP. Cookie thường được sử dụng để lưu trạng thái phiên (session state), thông tin đăng nhập, và các dữ liệu khác mà máy chủ cần theo dõi.

Middleware "cookie-parser" cho phép bạn dễ dàng đọc và ghi cookie từ và đến trình duyệt của người dùng. Điều này giúp bạn quản lý phiên làm việc của người dùng và lưu trạng thái trên máy khách. Bạn có thể sử dụng "cookie-parser" để:

1. Đọc giá trị của cookie từ yêu cầu HTTP và sử dụng nó trong xử lý yêu cầu.

2. Ghi dữ liệu vào cookie và gửi nó về trình duyệt của người dùng.

**concurrently**

"concurrently" là một công cụ dòng lệnh (command-line tool) trong ngữ cảnh của Node.js và JavaScript, được sử dụng để thực thi nhiều lệnh hoặc tác vụ (scripts) cùng một lúc từ một tệp cấu hình. Điều này hữu ích khi bạn cần chạy nhiều tiến trình, ứng dụng hoặc tác vụ đồng thời, chẳng hạn như khởi động nhiều máy chủ, ứng dụng hoặc dịch vụ trong quá trình phát triển hoặc triển khai ứng dụng.

Cách sử dụng "concurrently" thường là thông qua một tệp cấu hình hoặc lệnh dòng lệnh. Thông qua cấu hình, bạn có thể định rõ danh sách các lệnh hoặc tác vụ cần thực hiện đồng thời và "concurrently" sẽ quản lý việc thực thi chúng. Điều này giúp tăng hiệu suất và tiết kiệm thời gian khi phát triển hoặc triển khai các ứng dụng phức tạp.

Dưới đây là một ví dụ cách sử dụng "concurrently" để khởi động hai máy chủ web cùng một lúc, ví dụ một máy chủ API và một máy chủ giao diện người dùng:

Vừa chạy cả frontend và backend

```JS
{
  "scripts": {
    "start": "concurrently \"npm run server\" \"npm run client\"",
    "server": "node server.js",
    "client": "npm start --prefix client"
  }
}

```
**bcryptjs**

"bcryptjs" là một thư viện JavaScript được sử dụng để mã hóa mật khẩu (password hashing) và kiểm tra tính đúng đắn của mật khẩu trong ứng dụng web hoặc bất kỳ ứng dụng nào cần xác thực người dùng. Mục tiêu chính của "bcryptjs" là bảo mật mật khẩu người dùng bằng cách lưu trữ chúng dưới dạng băm một cách an toàn.

"bcryptjs" là một phiên bản JavaScript của "bcrypt," một thư viện mã hóa mật khẩu phổ biến được sử dụng trong nhiều ngôn ngữ lập trình. Thư viện này sử dụng một thuật toán băm mạnh mẽ và đáng tin cậy để biến đổi mật khẩu thành một chuỗi băm (hash) không thể đảo ngược. Băm mật khẩu là một quá trình không thể đảo ngược, điều này đảm bảo rằng người quản trị hệ thống không thể dễ dàng xem mật khẩu thật của người dùng.

Cách sử dụng "bcryptjs" bao gồm:

1. Mã hóa mật khẩu: Khi người dùng đăng ký hoặc thay đổi mật khẩu, "bcryptjs" sẽ được sử dụng để băm mật khẩu thật thành một chuỗi băm và lưu trữ chuỗi băm này trong cơ sở dữ liệu.

2. Kiểm tra mật khẩu: Khi người dùng đăng nhập, "bcryptjs" kiểm tra xem mật khẩu đã nhập có khớp với chuỗi băm trong cơ sở dữ liệu hay không. Nếu khớp, người dùng được xác thực.

Lưu ý rằng việc sử dụng "bcryptjs" giúp bảo mật mật khẩu của người dùng bằng cách lưu trữ chúng dưới dạng băm mạnh mẽ và đặng tin cậy, ngăn chặn việc hiển thị mật khẩu thật trong cơ sở dữ liệu.

```CMD
npm i nodemon multer mongoose jsonwebtoken express-formidable express-async-handler express dotenv cors cookie-parser concurrently bcryptjs
```


```CMD
mkdir backend
```

Chỉnh sửa file package.json

package.json
```json
"scripts": {
    "backend": "nodemon backend/index.js",
    "frontend": "npm run dev --prefix frontend",
    "dev": "concurrently \"npm run frontend\" \"npm run backend"
},
```

Tạo file .env để lưu trữ các connect đến các ứng dụng thứ 3 như Database chẳng hạn

```JS
PORT=5000
MONGO_URI='mongodb://127.0.0.1:27017/test'
```



## Frontend

Các thư viện cài đặt cho dự án Frontend

**slick-carousel**

"Slick Carousel" là một thư viện JavaScript được sử dụng để tạo các slideshow (carousel) hấp dẫn và linh hoạt trong các ứng dụng web. Nó cung cấp một cách dễ dàng để tạo và tùy chỉnh các carousel hiển thị ảnh, nội dung, hoặc bất kỳ loại dữ liệu nào bạn muốn hiển thị theo kiểu trượt qua.

Slick Carousel được phát triển dựa trên thư viện jQuery, và nó đã trở thành một trong những giải pháp phổ biến nhất để tạo carousel trong thế giới phát triển web. 

**react-slick**

"react-slick" là một gói mở rộng cho thư viện React.js, được sử dụng để tạo và tùy chỉnh các slideshow (carousel) trong ứng dụng web sử dụng React. Nó là một thành phần React cho phép bạn dễ dàng tạo các carousel linh hoạt và tùy chỉnh chúng để hiển thị nội dung bất kỳ bạn muốn, chẳng hạn như hình ảnh, video, tin tức, sản phẩm, hoặc bất kỳ loại dữ liệu nào.

"react-slick" là một giao diện cho thư viện Slick Carousel mà tôi đã đề cập trong câu trả lời trước. Nó cung cấp một tích hợp dễ dàng cho Slick Carousel trong môi trường React, giúp bạn sử dụng tính năng tạo carousel của Slick Carousel một cách dễ dàng trong các ứng dụng React. 

**react-toastify**

"react-toastify" là một thư viện JavaScript React được sử dụng để tạo thông báo (toast notifications) dễ dàng và linh hoạt trong ứng dụng web React. Thông báo là các thông điệp ngắn dạng pop-up thường xuất hiện ở góc trên hoặc dưới cùng của trang web để thông báo cho người dùng về các sự kiện quan trọng hoặc cung cấp thông tin liên quan đến tương tác của họ với ứng dụng.

"react-toastify" giúp bạn dễ dàng tạo và quản lý các thông báo trong ứng dụng React. Nó cung cấp một API đơn giản cho việc hiển thị thông báo và cho phép bạn tùy chỉnh các thông báo theo nhu cầu của bạn.

**react-router and react-router-dom**
"react-router" và "react-router-dom" là hai gói liên quan được sử dụng để quản lý định tuyến (routing) trong ứng dụng React. Chúng giúp bạn tạo và quản lý các định tuyến trong ứng dụng, cho phép người dùng điều hướng giữa các trang và hiển thị nội dung khác nhau dựa trên URL hiện tại.

**react-router**:

- "react-router" là gói chính của thư viện định tuyến React.
- Nó là bản cơ sở và không cung cấp các thành phần giao diện người dùng như Link, Route, và BrowserRouter.
- Được sử dụng trong các ứng dụng React Native, hoặc trong bất kỳ ngữ cảnh nào cần quản lý định tuyến mà không sử dụng DOM truyền thống (như ứng dụng desktop bằng Electron).

**react-router-dom**:

- "react-router-dom" là một phần mở rộng của "react-router" được thiết kế để sử dụng trong ứng dụng React web.
- Nó cung cấp các thành phần giao diện người dùng quan trọng như BrowserRouter, Route, Link, và nhiều thành phần khác để tạo và quản lý định tuyến trong ứng dụng React dựa trên trình duyệt web.
- "react-router-dom" cung cấp một cách thuận tiện để tạo các liên kết (links) trong ứng dụng và xác định các Route để hiển thị nội dung tương ứng.

**react-redux**

"react-redux" là một thư viện JavaScript được sử dụng trong ứng dụng React để quản lý trạng thái ứng dụng và tạo liên kết giữa trạng thái ứng dụng và giao diện người dùng. Nó là một phần của hệ sinh thái Redux và giúp bạn quản lý trạng thái của ứng dụng một cách hiệu quả và dễ dàng sử dụng.

Các thành phần chính của "react-redux" bao gồm:

1. **Provider**: "react-redux" cung cấp một thành phần gọi là Provider, mà bạn bọc xung quanh toàn bộ ứng dụng React. Provider làm cho các thành phần con của ứng dụng có thể truy cập vào trạng thái Redux mà nó quản lý.

2. **connect()**: "react-redux" cung cấp hàm connect(), mà bạn sử dụng để kết nối các thành phần React với trạng thái Redux. Bằng cách sử dụng connect(), bạn có thể lấy dữ liệu từ trạng thái Redux và cập nhật nó thông qua các props của các thành phần React.

3. **Action creators và Reducers**: "react-redux" hoạt động chặt chẽ với Redux, vì vậy bạn sử dụng action creators để gửi các hành động (actions) đến Redux Store và reducers để xác định cách thay đổi trạng thái của ứng dụng dựa trên các hành động đó.

4. **Store**: Redux Store là nơi lưu trữ trạng thái ứng dụng. "react-redux" giúp bạn truy cập và sử dụng dữ liệu từ Store trong các thành phần React.

Sử dụng "react-redux" giúp bạn quản lý trạng thái của ứng dụng một cách dễ dàng và giúp tạo ra các ứng dụng React có trạng thái phức tạp mà có thể dễ dàng duyệt qua các trang, tương tác với dữ liệu và hiển thị giao diện người dùng dựa trên trạng thái ứng dụng.

**react-icons**

"react-icons" là một thư viện JavaScript React được sử dụng để hiển thị các biểu tượng (icons) trong ứng dụng React. Thư viện này cung cấp một bộ sưu tập lớn các biểu tượng đa dạng từ nhiều nguồn khác nhau như Font Awesome, Material Icons, và nhiều nguồn icons khác. Với "react-icons," bạn có thể dễ dàng thêm biểu tượng vào ứng dụng của mình và tùy chỉnh chúng theo nhu cầu.

**apexcharts**

ApexCharts là một thư viện JavaScript mã nguồn mở được sử dụng để tạo biểu đồ tương tác và đa dạng trong ứng dụng web. Thư viện này cung cấp một cách mạnh mẽ để hiển thị dữ liệu dưới dạng biểu đồ với nhiều loại biểu đồ khác nhau như biểu đồ đường, biểu đồ cột, biểu đồ hình bánh, biểu đồ radar, và nhiều loại biểu đồ khác. ApexCharts là một công cụ phổ biến trong phát triển ứng dụng web và quản lý dữ liệu.

**react-apexcharts**

react-apexcharts là một gói mở rộng cho thư viện ApexCharts, được sử dụng để tích hợp ApexCharts với ứng dụng React. Thư viện này giúp bạn tạo và hiển thị các biểu đồ sử dụng ApexCharts một cách dễ dàng trong ứng dụng React.

react-apexcharts cung cấp các thành phần React cho các loại biểu đồ khác nhau như biểu đồ đường, biểu đồ cột, biểu đồ hình bánh, biểu đồ radar và nhiều loại biểu đồ khác, và cho phép bạn tùy chỉnh và tương tác với biểu đồ theo nhu cầu của bạn.

**moment**

Thư viện có tên "moment.js," thường được gọi là "moment," là một thư viện JavaScript được sử dụng để xử lý và quản lý thời gian và ngày tháng trong ứng dụng React và các ứng dụng web khác. "moment" giúp bạn thực hiện nhiều tác vụ liên quan đến thời gian và ngày tháng, bao gồm:

- **Hiển thị và định dạng thời gian**: "moment" cho phép bạn hiển thị thời gian và ngày tháng dưới dạng chuỗi văn bản theo các định dạng tùy chỉnh.

- **Tính toán khoảng cách thời gian**: Bạn có thể sử dụng "moment" để tính toán khoảng cách giữa hai ngày hoặc thời điểm, chẳng hạn như số ngày, số giờ, số phút, và số giây.

- **Xác định thời gian hiện tại**: "moment" cho phép bạn xác định thời gian và ngày tháng hiện tại, đồng thời hỗ trợ múi giờ (time zones).

- **Phân tích và cắt dữ liệu thời gian**: Bạn có thể sử dụng "moment" để phân tích và cắt chuỗi văn bản chứa thông tin thời gian và ngày tháng thành các thành phần riêng lẻ như ngày, tháng, năm, giờ, phút, giây, và nhiều thuộc tính khác.

- **Tạo và thay đổi thời gian và ngày tháng**: "moment" cho phép bạn tạo các đối tượng thời gian mới và thay đổi các giá trị của chúng.

- **Hỗ trợ định dạng ngôn ngữ:** "moment" hỗ trợ định dạng ngôn ngữ và localizations, cho phép hiển thị thời gian và ngày tháng theo ngôn ngữ cụ thể.

Mặc dù "moment" đã từng là một thư viện phổ biến để xử lý thời gian trong JavaScript, nhưng hiện tại, người ta khuyên dùng sử dụng các thư viện khác như "date-fns" hoặc "luxon" để xử lý thời gian trong các dự án React mới hơn. Các thư viện này cung cấp cách tiếp cận tốt hơn cho xử lý thời gian và có hiệu suất tốt hơn so với "moment."

**flowbite**


**axios**
Axios là một thư viện JavaScript phía máy khách (client-side) được sử dụng để tạo các yêu cầu HTTP và xử lý phản hồi từ máy chủ trong ứng dụng web. Axios cung cấp một giao diện dễ sử dụng để tương tác với các API và dịch vụ web từ phía máy khách.

Một số đặc điểm quan trọng của Axios bao gồm:

1. **Gửi yêu cầu HTTP**: Axios cho phép bạn gửi các yêu cầu HTTP như GET, POST, PUT, DELETE và nhiều loại yêu cầu khác đến máy chủ.

2. **Hỗ trợ Promise**: Axios sử dụng Promises để xử lý yêu cầu và phản hồi, giúp viết mã xử lý yêu cầu và xử lý phản hồi theo cách dễ đọc và tuân thủ hơn.

3. **Tùy chỉnh dễ dàng**: Bạn có thể tùy chỉnh các yêu cầu HTTP bằng cách thêm tiêu đề (headers), tham số (parameters), và thực hiện các xác thực cần thiết.

4. **Xử lý lỗi**: Axios cung cấp cách xử lý lỗi và các trạng thái phản hồi khác nhau một cách thuận tiện, cho phép bạn xử lý các trường hợp ngoại lệ như lỗi mạng hoặc lỗi máy chủ.

5. **Interceptors**: Bạn có thể sử dụng interceptors để can thiệp vào quá trình gửi yêu cầu hoặc nhận phản hồi, chẳng hạn như thêm các tiêu đề (headers) tự động vào mỗi yêu cầu.

6. **Hỗ trợ JSON và FormData**: Axios hỗ trợ gửi dữ liệu dưới dạng JSON và FormData một cách dễ dàng.

**@reduxjs/toolkit**

@reduxjs/toolkit là một thư viện của Redux, được tạo ra để giúp đơn giản hóa quá trình quản lý trạng thái ứng dụng trong ứng dụng React và các ứng dụng JavaScript khác sử dụng Redux.

Redux là một thư viện quản lý trạng thái phía máy khách phổ biến trong cộng đồng React. Nó giúp quản lý trạng thái ứng dụng một cách hiệu quả và dễ dàng theo dõi các thay đổi trạng thái. Tuy nhiên, việc cấu hình Redux và viết các reducers, actions có thể gây ra khá nhiều công đoạn mã. Đó là lý do tạo ra **@reduxjs/toolkit**.

Một số tính năng quan trọng của **@reduxjs/toolkit** bao gồm:

1. **Tạo reducers và actions một cách dễ dàng**: Nó cung cấp một API đơn giản để tạo reducers và actions mà không cần viết nhiều mã boilerplate.

2. **Hỗ trợ tự động lưu trạng thái**: @reduxjs/toolkit hỗ trợ tự động lưu trạng thái ứng dụng bằng cách sử dụng Redux Persist, giúp bạn duy trì trạng thái ngay cả khi trình duyệt làm mới.

3. **Hỗ trợ thực thi gọi hàm bất đồng bộ**: Bạn có thể dễ dàng thực hiện các gọi hàm bất đồng bộ và xử lý chúng trong reducers bằng sử dụng Redux Toolkit.

4. **Hỗ trợ tạo nhiều slices**: Bạn có thể tạo nhiều "slices" cho ứng dụng của mình, mỗi slice tương ứng với một phần của trạng thái.

5. **Giúp tối ưu hóa hiệu suất**: Redux Toolkit cung cấp các tiện ích để giúp bạn tối ưu hóa hiệu suất ứng dụng.

6. **Hỗ trợ tiêu đề "immer" cho immutable updates**: Immer giúp bạn làm việc với trạng thái ứng dụng một cách dễ dàng mà không cần lo lắng về việc sao chép và cập nhật immutable.

Tạo reducers và actions một cách dễ dàng: Nó cung cấp một API đơn giản để tạo reducers và actions mà không cần viết nhiều mã boilerplate.

Hỗ trợ tự động lưu trạng thái: **@reduxjs/toolkit** hỗ trợ tự động lưu trạng thái ứng dụng bằng cách sử dụng Redux Persist, giúp bạn duy trì trạng thái ngay cả khi trình duyệt làm mới.

Hỗ trợ thực thi gọi hàm bất đồng bộ: Bạn có thể dễ dàng thực hiện các gọi hàm bất đồng bộ và xử lý chúng trong reducers bằng sử dụng Redux Toolkit.

Hỗ trợ tạo nhiều slices: Bạn có thể tạo nhiều "slices" cho ứng dụng của mình, mỗi slice tương ứng với một phần của trạng thái.

Giúp tối ưu hóa hiệu suất: Redux Toolkit cung cấp các tiện ích để giúp bạn tối ưu hóa hiệu suất ứng dụng.

Hỗ trợ tiêu đề "immer" cho immutable updates: Immer giúp bạn làm việc với trạng thái ứng dụng một cách dễ dàng mà không cần lo lắng về việc sao chép và cập nhật immutable.

**@paypal/react-paypal-js**

là một thư viện JavaScript được sử dụng để tích hợp tính năng thanh toán trực tuyến bằng cổng thanh toán PayPal vào ứng dụng web hoặc ứng dụng React. Thư viện này là một giao diện dễ sử dụng cho PayPal JavaScript SDK, cho phép bạn tích hợp thanh toán PayPal một cách dễ dàng và an toàn.

Các tính năng chính của **@paypal/react-paypal-js** bao gồm:

1. **Tích hợp thanh toán PayPal**: Thư viện này cho phép bạn tích hợp tính năng thanh toán PayPal vào ứng dụng của mình mà không cần viết mã nguyên thủy của PayPal SDK.

2. **Hỗ trợ các chức năng thanh toán đa dạng**: Bạn có thể tùy chỉnh cách thanh toán bằng cách sử dụng các tính năng như thanh toán một lần (one-time payment), thanh toán theo gói (subscriptions), và các tùy chọn thanh toán khác.

3. **Hỗ trợ xác thực và quản lý tài khoản người dùng**: Thư viện này cung cấp cách xác thực và quản lý tài khoản người dùng thông qua tích hợp với PayPal.

4. **Tích hợp các tùy chỉnh giao diện**: Bạn có thể tùy chỉnh giao diện và trải nghiệm thanh toán PayPal để phù hợp với giao diện ứng dụng của bạn.

5. **Hỗ trợ Promise**: @paypal/react-paypal-js sử dụng Promise để xử lý các yêu cầu thanh toán và cung cấp cách dễ dàng xử lý phản hồi từ PayPal.

Sau đó, bạn có thể import nó vào mã nguồn của bạn và sử dụng để tích hợp tính năng thanh toán PayPal vào ứng dụng của bạn, bao gồm việc thiết lập và cấu hình các nút thanh toán PayPal và xử lý kết quả thanh toán.


```CMD
npm i slick-carousel react-slick react-toastify react-router react-router-dom react-redux react-icons apexcharts react-apexcharts moment flowbite axios @reduxjs/toolkit @paypal/react-paypal-js
```

Loại bỏ bớt các file có sẵn không cần thiết của Frontend đi:

+ Loại bỏ thư mục public

Trong src:

+ Loại bỏ thư mục assets
+ App.css

Trả cho file App.jsx về như sau
```JS
function App() {
  
  return (
    <h1 className="text-3xl font-bold underline">
      Hello world!
    </h1>
  )
}

export default App
```

Trả cho file main.jsx về như sau:

```JS
import React from 'react'
import ReactDOM from 'react-dom/client'
import App from './App.jsx'

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
)

```

## Backend

### Tạo thư mục config

+ Cấu hình đến Database: tạo thư mục db.js

```JS
import mongoose from "mongoose"; // Chúng ta cần thư viện này để hiểu được MongoDB.

// Đây giống như bạn đang chuẩn bị một cái kẹp để gắp sách từ kệ sách. Hàm này sẽ giúp chúng ta kết nối với cơ sở dữ liệu MongoDB.
const connectDB = async () => {
    try {
        await mongoose.connect(process.env.MONGO_URI)
        // Đoạn này giống như việc bạn đặt kẹp của mình vào sách. Chúng ta đang kết nối với MongoDB bằng cách sử dụng địa chỉ (URI) đặc biệt. Địa chỉ này được lấy từ môi trường (nơi chúng ta lưu các thông tin quan trọng).
        console.log(`Successfully connected to mongoDB`);
    } catch (error) {
        console.log(`ERROR: ${error.message}`);
        process.exit(1);
    }
}

export default connectDB;
// Đoạn này giống như bạn gắp sách ra khỏi kệ và cho ai đó mượn sách. Chúng ta đang đóng gói hàm kết nối MongoDB và cho phép nó được sử dụng ở những nơi khác trong ứng dụng.
```

```TXT
const connectDB = async () => : Dòng này bắt đầu định nghĩa một hàm tên là connectDB. Hàm này dùng để kết nối ứng dụng với cơ sở dữ liệu MongoDB. Chúng ta sử dụng async trước () => {...} để cho phép sử dụng await trong hàm này, điều này cho phép đợi cho các hoạt động không đồng bộ như kết nối cơ sở dữ liệu.

try : Dòng này bắt đầu khối mã mà chúng ta muốn thử nghiệm, nghĩa là khối mã bên trong try là nơi chúng ta cố gắng thực hiện kết nối cơ sở dữ liệu.

await mongoose.connect(process.env.MONGO_URI): Dòng này sử dụng mongoose.connect để thực hiện kết nối đến cơ sở dữ liệu MongoDB. process.env.MONGO_URI là một biến môi trường, chứa chuỗi kết nối đến cơ sở dữ liệu MongoDB. Bằng cách sử dụng await, chúng ta đợi cho đến khi quá trình kết nối hoàn thành.

catch (error) : Dòng này bắt đầu khối mã mà chúng ta sẽ thực hiện nếu có lỗi xảy ra trong khối try.
```

Thư mục "config" trong một ứng dụng Node.js thường được sử dụng để chứa các tệp cấu hình (configuration files) hoặc các biến môi trường (environment variables) để quản lý các cài đặt, tùy chỉnh, và thông tin cấu hình của ứng dụng. Thư mục này giúp bạn tách biệt thông tin cấu hình khỏi mã nguồn chính của ứng dụng, giúp bạn dễ dàng cấu hình và điều chỉnh ứng dụng mà không cần thay đổi mã nguồn.

Các tệp cấu hình thông thường có thể bao gồm:

1. Tệp cấu hình JSON: Một tệp JSON có thể chứa thông tin cấu hình như cổng (port) mà máy chủ lắng nghe, địa chỉ cơ sở dữ liệu, khóa bí mật, và các tùy chọn cấu hình khác.

2. Tệp cấu hình JavaScript: Một tệp JavaScript cho phép bạn viết mã để cấu hình ứng dụng. Điều này có thể hữu ích khi bạn cần logic phức tạp để xây dựng cấu hình.

3. Tệp .env (environment variables): Một tệp .env có thể chứa các biến môi trường, chẳng hạn như các khóa bí mật hoặc thông tin môi trường khác. Thường thì bạn sử dụng một thư viện như "dotenv" để tải các biến này vào quá trình ứng dụng Node.js.

Thư mục "config" cũng có thể chứa các tệp chia sẻ thông tin cấu hình cho môi trường phát triển (development), môi trường sản phẩm (production), và môi trường thử nghiệm (test). Điều này cho phép bạn cấu hình ứng dụng dựa trên môi trường nơi ứng dụng đang chạy.

Việc sử dụng thư mục "config" giúp tăng tính linh hoạt và bảo mật của ứng dụng bằng cách ngăn chặn việc lưu trữ thông tin cấu hình quan trọng trong mã nguồn và cho phép dễ dàng cấu hình ứng dụng cho môi trường khác nhau mà không cần thay đổi mã nguồn.

### Tạo thư mục controllers

Thư mục "controllers" trong một ứng dụng backend Node.js thường được sử dụng để chứa các tệp mã nguồn (JavaScript) chứa logic điều khiển (controller logic) của ứng dụng. Logic điều khiển (controller logic) được sử dụng để xử lý các yêu cầu HTTP từ máy khách (client) và quản lý việc gửi và nhận dữ liệu giữa máy khách và máy chủ.

Các chức năng chính của thư mục "controllers" trong ứng dụng Node.js bao gồm:

1. **Xử lý yêu cầu HTTP**: Controllers xác định cách ứng dụng phản ứng với các yêu cầu HTTP từ máy khách. Chúng kiểm tra và xác thực yêu cầu, sau đó thực hiện các xử lý cần thiết và gửi phản hồi đến máy khách.

2. **Tách biệt logic ứng dụng**: Việc đặt logic điều khiển trong thư mục "controllers" giúp tách biệt logic ứng dụng (business logic) khỏi logic xử lý yêu cầu HTTP. Điều này giúp mã nguồn trở nên dễ quản lý, dễ kiểm tra và dễ bảo trì.

3. **Sử dụng middleware**: Controllers thường sử dụng middleware để thực hiện các chức năng như xác thực, quyền truy cập, và kiểm tra dữ liệu trước khi xử lý yêu cầu chính. Middleware có thể được áp dụng trước hoặc sau logic điều khiển.

4. **Gửi và nhận dữ liệu**: Controllers gửi yêu cầu đến cơ sở dữ liệu hoặc các dịch vụ bên ngoài và nhận dữ liệu từ họ. Sau đó, họ định dạng và trả về dữ liệu cho máy khách.

5. **Xử lý lỗi**: Controllers xử lý các lỗi liên quan đến yêu cầu và phản hồi. Họ có thể gửi mã trạng thái và thông báo lỗi cho máy khách khi có lỗi xảy ra.

Dưới đây là một ví dụ về cách bạn có thể tổ chức một thư mục "controllers" trong ứng dụng Node.js:

```TXT
- controllers/
  - userController.js
  - postController.js
  - authController.js
```

Trong ví dụ này, có ba tệp "userController.js," "postController.js," và "authController.js," mỗi tệp chứa logic điều khiển liên quan đến việc quản lý người dùng, bài đăng, và xác thực trong ứng dụng. Controllers này có thể được sử dụng để xử lý các yêu cầu liên quan đến người dùng, bài đăng và xác thực.

### Tạo thư mục middlewares

Thư mục "middlewares" trong một ứng dụng Node.js thường được sử dụng để chứa các middleware functions, đây là các phần mềm (software components) đoạn mã JavaScript dùng để xử lý yêu cầu HTTP trước khi chúng đến đích (controllers hoặc routes). Middleware thường thực hiện các công việc như xác thực, kiểm tra quyền truy cập, xử lý dữ liệu, ghi nhật ký (logging), và nhiều tác vụ khác liên quan đến xử lý yêu cầu HTTP.

Các chức năng chính của thư mục "middlewares" trong ứng dụng Node.js bao gồm:

1. **Xác thực và quyền truy cập**: Middleware có thể thực hiện xác thực người dùng (authentication) và kiểm tra quyền truy cập (authorization). Ví dụ, bạn có thể có một middleware để đảm bảo rằng người dùng đã đăng nhập trước khi truy cập các tài nguyên bảo mật.

2. **Xử lý dữ liệu**: Middleware có thể kiểm tra và xử lý dữ liệu được gửi trong yêu cầu, đảm bảo tính toàn vẹn của dữ liệu và chuẩn hóa nó trước khi nó được sử dụng trong logic điều khiển.

3. **Ghi nhật ký (logging)**: Middleware có thể ghi lại thông tin về các yêu cầu và hoạt động của ứng dụng vào tệp nhật ký để giúp theo dõi và gỡ lỗi.

4. **Xử lý lỗi**: Middleware có thể xử lý lỗi xảy ra trong quá trình xử lý yêu cầu và gửi phản hồi lỗi cho máy khách.

5. **Nén dữ liệu và tối ưu hóa**: Middleware có thể nén dữ liệu gửi đi để tối ưu hóa băng thông và tăng tốc độ truyền tải.

6. **Xử lý CORS (Cross-Origin Resource Sharing)**: Middleware có thể được sử dụng để xử lý các vấn đề liên quan đến chia sẻ tài nguyên giữa các nguồn gốc khác nhau trên web.

Thư mục "middlewares" thường chứa nhiều tệp hoặc modul riêng lẻ, mỗi tệp tương ứng với một middleware cụ thể. Ví dụ:

```TXT
- middlewares/
  - authenticationMiddleware.js
  - authorizationMiddleware.js
  - loggingMiddleware.js
  - errorHandlingMiddleware.js
  - compressionMiddleware.js

```

Các tệp middleware có thể được sử dụng trong routes hoặc controllers để xử lý các yêu cầu HTTP. Middleware thường được sử dụng bằng cách áp dụng chúng cho một hoặc nhiều tuyến đường (routes) cụ thể, cho phép bạn quản lý quá trình xử lý yêu cầu một cách linh hoạt.



### Tạo thư mục models

Thư mục "models" trong ứng dụng Node.js thường được sử dụng để chứa các tệp mã nguồn (JavaScript hoặc TypeScript) mô hình (models) để tương tác với cơ sở dữ liệu hoặc đại diện cho các đối tượng dữ liệu trong ứng dụng. Mô hình thường định nghĩa cấu trúc dữ liệu và quy tắc liên quan đến việc truy xuất và xử lý dữ liệu từ cơ sở dữ liệu hoặc các nguồn dữ liệu khác.

Các chức năng chính của thư mục "models" trong ứng dụng Node.js bao gồm:

1. **Định nghĩa cấu trúc dữ liệu**: Mô hình định nghĩa cấu trúc dữ liệu cho các loại đối tượng hoặc bảng trong cơ sở dữ liệu. Ví dụ, nếu bạn có một ứng dụng quản lý người dùng, mô hình người dùng (user model) có thể định nghĩa các trường như tên, email, mật khẩu, v.v.

2. **Tương tác với cơ sở dữ liệu**: Mô hình thường chứa logic để tạo, đọc, cập nhật và xóa (CRUD) dữ liệu từ cơ sở dữ liệu. Điều này giúp tách biệt logic truy vấn cơ sở dữ liệu khỏi mã nguồn chính của ứng dụng.

3. **Kiểm tra dữ liệu và xử lý**: Mô hình có thể chứa các phương thức để kiểm tra tính toàn vẹn của dữ liệu trước khi ghi vào cơ sở dữ liệu hoặc trước khi hiển thị cho người dùng.

4. **Tạo quan hệ giữa các mô hình**: Trong một ứng dụng có nhiều loại dữ liệu, mô hình có thể được sử dụng để xác định các quan hệ giữa chúng. Ví dụ, một mô hình bài viết có thể liên quan đến mô hình người dùng thông qua trường người đăng (author).

5. **Xử lý logic ứng dụng cụ thể**: Mô hình cũng có thể chứa logic ứng dụng cụ thể liên quan đến đối tượng mô hình đó. Ví dụ, trong mô hình người dùng, bạn có thể định nghĩa phương thức để đăng nhập người dùng hoặc tạo người dùng mới.

Thường thì mô hình sẽ thực hiện các thao tác tương tác với cơ sở dữ liệu thông qua một thư viện ORM (Object-Relational Mapping) hoặc một thư viện tương tác với cơ sở dữ liệu như Mongoose (cho MongoDB) hoặc Sequelize (cho SQL databases).

Dưới đây là một ví dụ về cách bạn có thể tổ chức thư mục "models" trong ứng dụng Node.js:

```JS
- models/
  - user.js
  - post.js
  - comment.js
```

Trong ví dụ này, có ba tệp "user.js," "post.js," và "comment.js," mỗi tệp đại diện cho một mô hình riêng biệt (người dùng, bài viết, và bình luận) và chứa logic để định nghĩa cấu trúc dữ liệu và tương tác với cơ sở dữ liệu.

### Tạo thư mục routes

Thư mục "routes" trong một ứng dụng Node.js thường được sử dụng để chứa các tệp mã nguồn (JavaScript hoặc TypeScript) định nghĩa và quản lý các tuyến đường (routes) của ứng dụng. Tuyến đường (route) đại diện cho các URI (Uniform Resource Identifier) cụ thể và cách xử lý yêu cầu HTTP mà ứng dụng phải thực hiện khi nhận được yêu cầu đến URI đó.

Các chức năng chính của thư mục "routes" trong ứng dụng Node.js bao gồm:

1. **Định nghĩa tuyến đường (route definitions)**: Tuyến đường là nơi bạn xác định các URI và phương thức HTTP (GET, POST, PUT, DELETE, v.v.) mà ứng dụng của bạn sẽ hỗ trợ. Đây là nơi bạn liên kết các tuyến đường với các xử lý (controllers) tương ứng.

2. **Xử lý yêu cầu HTTP**: Thư mục "routes" chứa mã nguồn để xử lý yêu cầu HTTP tới các URI cụ thể. Bạn có thể gọi các hàm điều khiển (controllers) từ đây để xử lý yêu cầu và gửi phản hồi cho máy khách.

3. **Xác định middleware**: Bạn có thể áp dụng middleware cho tuyến đường cụ thể. Middleware có thể thực hiện các chức năng như xác thực, kiểm tra quyền truy cập, và xử lý dữ liệu trước khi đến đối tượng điều khiển.

4. **Phân chia mã nguồn**: Thư mục "routes" giúp bạn phân chia mã nguồn thành các phần tương ứng với từng tuyến đường hoặc tài nguyên cụ thể, giúp mã nguồn trở nên dễ quản lý và dễ bảo trì.

Dưới đây là một ví dụ về cách bạn có thể tổ chức thư mục "routes" trong ứng dụng Node.js:

```md
- routes/
  - index.js
  - users.js
  - posts.js

```

Trong ví dụ này:

- Tệp "index.js" có thể định nghĩa tuyến đường gốc (root route) của ứng dụng.
- Tệp "users.js" có thể định nghĩa các tuyến đường liên quan đến người dùng (user routes).
- Tệp "posts.js" có thể định nghĩa các tuyến đường liên quan đến bài viết (post routes).

### Tạo thư mục utils

Thư mục "utils" trong một ứng dụng Node.js thường được sử dụng để chứa các tệp mã nguồn (JavaScript hoặc TypeScript) chứa các tiện ích (utilities) hoặc hàm hỗ trợ (helper functions) mà bạn sử dụng trong toàn bộ ứng dụng. Các tiện ích này thường là các chức năng hoặc lớp giúp bạn thực hiện các nhiệm vụ phổ biến và lặp lại trong ứng dụng.

Các chức năng chính của thư mục "utils" trong ứng dụng Node.js bao gồm:

1. **Chứa các hàm hỗ trợ**: Thư mục "utils" là nơi bạn có thể định nghĩa và tổ chức các hàm hỗ trợ chung mà bạn sử dụng trong nhiều phần của ứng dụng. Ví dụ, bạn có thể có một hàm để định dạng ngày tháng, một hàm để mã hóa mật khẩu, hoặc một hàm để thực hiện tính toán phức tạp.

2. **Tách biệt logic phụ trợ**: Bằng cách đặt các hàm hỗ trợ vào thư mục "utils," bạn giúp tách biệt logic phụ trợ khỏi mã nguồn chính của ứng dụng. Điều này làm cho mã nguồn trở nên dễ đọc hơn và dễ bảo trì hơn.

3. **Tích hợp với các thư viện bên ngoài**: Thư mục "utils" cũng có thể chứa các tệp kết nối và tích hợp với các thư viện và dịch vụ bên ngoài, chẳng hạn như thư viện gửi email, thư viện xử lý hình ảnh, hoặc các API bên ngoài.

4. **Sử dụng lại mã nguồn**: Bạn có thể sử dụng các hàm hỗ trợ từ thư mục "utils" trong nhiều phần của ứng dụng mà không cần viết lại mã.

5. **Kiểm tra đơn vị (unit testing)**: Việc đặt các hàm hỗ trợ trong thư mục "utils" giúp bạn dễ dàng thực hiện kiểm tra đơn vị (unit tests) trên các hàm này để đảm bảo tính đúng đắn và hoạt động như mong đợi.

Dưới đây là một ví dụ về cách bạn có thể tổ chức thư mục "utils" trong ứng dụng Node.js:

```JS
- utils/
  - dateUtils.js
  - encryptionUtils.js
  - emailUtils.js
  - imageProcessingUtils.js

```

Trong ví dụ này:

- Tệp **"dateUtils.js"** có thể chứa các hàm để định dạng và xử lý ngày tháng.
- Tệp **"encryptionUtils.js"** có thể chứa các hàm để mã hóa và giải mã dữ liệu, chẳng hạn như mật khẩu.
- Tệp **"emailUtils.js"** có thể chứa các hàm liên quan đến gửi và nhận email trong ứng dụng.
- Tệp **"imageProcessingUtils.js"** có thể chứa các hàm để xử lý hình ảnh, chẳng hạn như chuyển đổi kích thước hoặc cắt ảnh.

Bằng cách tổ chức thư mục "utils" một cách có tổ chức và sáng sủa, bạn có thể dễ dàng quản lý các tiện ích và hàm hỗ trợ của ứng dụng của mình.

### Tạo file index.js
+ Kết nối đến DB:
```JS
console.log("Hello world!");

// package
import path from 'path';
import express from 'express';
import dotenv from 'dotenv';
import cookieParser from 'cookie-parser';

//utils
import connectDB from './config/db.js';

dotenv.config();
/*
// Dòng này sử dụng thư viện dotenv để cấu hình ứng dụng từ các biến môi trường (environment variables) được lưu trong tệp .env.
// Điều này cho phép bạn đặt cấu hình ứng dụng, chẳng hạn như cổng máy chủ, một cách linh hoạt. 
*/

const port = process.env.PORT || 5000;

// Dòng này thiết lập biến port dựa trên biến môi trường PORT. Nếu không có PORT được đặt, nó sẽ sử dụng cổng mặc định là 5000.


connectDB();

// Dòng này gọi hàm connectDB, được nhập từ tệp './config/db.js'. Hàm này kết nối ứng dụng với cơ sở dữ liệu MongoDB.


const app = express();

// Dòng này tạo một ứng dụng Express. Express là một framework web cho Node.js giúp bạn xây dựng các ứng dụng web và API dễ dàng.


app.use(express.json());

// Dòng này thêm một middleware cho ứng dụng để xử lý dữ liệu JSON gửi đến từ client. Nó cho phép ứng dụng hiểu và xử lý JSON dễ dàng.


app.use(express.urlencoded({ extended: true }));

// Dòng này thêm một middleware (urlencoded là 1 loại middleware) để xử lý dữ liệu gửi dưới dạng dữ liệu form. Tùy chọn `{ extended: true }` cho phép bạn sử dụng thư viện nâng cao để xử lý dữ liệu form.


app.use(cookieParser());

// Dòng này thêm một middleware để xử lý cookie. CookieParser giúp ứng dụng đọc và ghi dữ liệu từ cookies trên trình duyệt của người dùng.


app.get("/", (req, res) => {
    res.send("Hello, world!");
});

// Dòng này xác định một tuyến đường (route) cho URL chính ("/"). Khi bạn truy cập URL chính, ứng dụng sẽ gửi lại một thông điệp "Hello, world!".

// res: là response gửi yêu cầu được xử lý xong về cho client, ở đây res.send("Hello, world!"); là gửi đoạn chuỗi này về phía client nếu như callbacks này được thực hiện


app.listen(port, () => console.log(`Server running on port: ${port}`));

// Dòng này bắt đầu máy chủ Express lắng nghe trên cổng được đặt (thông qua biến `port`).
// Khi máy chủ được khởi động, nó in ra thông báo trên bảng điều khiển cho biết máy chủ đang chạy trên cổng nào.

```

## Database sử dụng NoSQL MongoDB: localhost

Đường dẫn này là kết nối tới MongoDB compass, được đặt ở file .env

```JS
MONGO_URI='mongodb://127.0.0.1:27017/test'
```

Tóm tắt:

Bạn đã gọi Express và gán nó cho biến app bằng dòng này: const app = express();. Điều này tạo ra một ứng dụng Express mà bạn có thể sử dụng để xây dựng các tuyến đường và thêm middleware.

Bạn sử dụng các hàm như use, get, và listen để cấu hình và điều khiển ứng dụng Express của bạn:

app.use(...) là để thêm các middleware cho ứng dụng. Middleware là các chức năng được thực hiện trước khi yêu cầu HTTP tiếp tục vào các tuyến đường. Middleware có thể thực hiện các công việc như xử lý dữ liệu JSON, dữ liệu form, xử lý cookie, kiểm tra xác thực, và nhiều công việc khác.

app.get(...) là để xác định một tuyến đường (route) cho ứng dụng. Khi một yêu cầu HTTP với phương thức GET được gửi đến tuyến đường này, mã được cung cấp trong hàm callback (được định nghĩa bởi (req, res) => { ... }) sẽ được thực thi. Điều này cho phép bạn xử lý yêu cầu và gửi phản hồi về client.

app.listen(...) là để bắt đầu máy chủ Express lắng nghe trên một cổng cụ thể. Khi máy chủ được khởi chạy, nó sẽ lắng nghe các yêu cầu từ trình duyệt và xử lý chúng dựa trên các tuyến đường và middleware bạn đã định nghĩa.

### Ví dụ về middleware urlencoded

Cho 1 đoạn sau

```txt
name=John&email=john@example.com&age=30
```

Middleware urlencoded trong Express.js giúp bạn giải mã và phân tích chuỗi này thành một đối tượng dễ quản lý trong mã nguồn của bạn. Bạn có thể sử dụng req.body để truy cập các giá trị của các trường trong biểu mẫu và thực hiện các xử lý dữ liệu cần thiết.

sử dụng middleware urlencoded

```JS
// Sử dụng middleware urlencoded để xử lý dữ liệu từ biểu mẫu
app.use(express.urlencoded({ extended: true }));

app.post('/submit', (req, res) => {
  // Dữ liệu từ biểu mẫu sẽ được lưu trong req.body
  const name = req.body.name;
  const email = req.body.email;
  // Thực hiện xử lý với dữ liệu từ biểu mẫu
});
```


### Ví dụ về cookies

```js

// Sử dụng cookieParser để xử lý cookie
app.use(cookieParser());

// Tạo một tuyến đường để đặt cookie
app.get('/set-cookie', (req, res) => {
  // Đặt một cookie với tên "user" và giá trị "John"
  res.cookie('user', 'John');

  res.send('Cookie đã được đặt.');
});

// Tạo một tuyến đường để đọc cookie
app.get('/get-cookie', (req, res) => {
  // Đọc giá trị của cookie "user"
  const userName = req.cookies.user;

  if (userName) {
    res.send(`Xin chào, ${userName}!`);
  } else {
    res.send('Cookie "user" không tồn tại.');
  }
});

app.listen(3000, () => {
  console.log('Server is running on port 3000');
});
```

Trong ví dụ trên:

Chúng ta sử dụng cookieParser thông qua app.use(cookieParser()) để kích hoạt middleware xử lý cookie trong ứng dụng Express.

Chúng ta tạo hai tuyến đường:

/set-cookie để đặt một cookie có tên "user" với giá trị "John".
/get-cookie để đọc và hiển thị giá trị của cookie "user" nếu tồn tại.
Khi bạn truy cập /set-cookie, ứng dụng sẽ đặt một cookie trên trình duyệt của bạn.

Khi bạn truy cập /get-cookie, ứng dụng sẽ đọc giá trị của cookie "user" và hiển thị thông điệp chào mừng nếu cookie tồn tại, hoặc thông báo nếu cookie không tồn tại.

Điều này cho thấy cách cookieParser giúp bạn dễ dàng xử lý cookie trong ứng dụng Express và làm việc với dữ liệu liên quan đến trạng thái của người dùng.

