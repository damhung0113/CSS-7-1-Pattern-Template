# Abstracts
Thư mục `abstracts/` tập hợp tất cả các tools và helpers Sass được sử dụng trong toàn bộ dự án. 
Mọi global variable, function, mixin và placeholder phải được đưa vào đây.

Quy tắc chung cho thư mục này là nó không được xuất ra một dòng CSS khi tự biên dịch. Đây không phải là những Sass helpers.

EXAMPLE

.avatar-status {
  &:before {
    content: '';
    position: absolute;
    bottom: 5%;
    right: 5%;
    width: 20%;
    height: 20%;
    border-radius: 50rem;
    border: 1px solid #fff;
  }
}

.avatar-online {
  @extend .avatar-status;
  &:before {
    background-color: green;
  }
}

.avatar-busy {
  @extend .avatar-status;
  &:before {
    background-color: red;
  }
}
