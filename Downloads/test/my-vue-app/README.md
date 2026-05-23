# my-vue-app

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

* Chuyển trang trong vue 
### Cài đặt thư viện
``` npm i vue-router ```
### Tạo các file giao diện (views)
### Tạo file cấu hình định tuyến (src/router/index.js)
```
- Tạo thư mục router và file index.js
- Import createRouter và createWebHistory từ thư viện vue-router
- import 2 file views vừa tạo
- khai báo mảng routes chứa object trang gồm: path(url), name(tên định danh duy nhất), component(views)
- khởi tạo đối tượng router(truyền cấu hình history và routes vào): router biến đại diện bộ điều hướng, function createRouter kích hoạt bộ điều hướng, history cấu hình làm sạch, routes nạp danh sách các trang 
- export default router
```
### Kích hoạt router trên toàn app (src/main.js)
```
- import router 
- thêm .use(router) vào trước dòng app.mount
```
### Tạo mennu và cửa sổ hiển thị (src/App.vue)
```
- Dùng thẻ <router-link to="/"> để hiên thị nút bấm
- Đặt thẻ <router-view/> tại nơi muốn hiển thị nội dung trang con hiển thị ra 
```