# jQuery - ajax
## 这是一个关于使用 jQuery 实现 ajax 的 Demo
## 包含以下几种用法
### 回顾 原生JS ajax 的用法
```JavaScript
  var xhr = new XMLHttpRequest()
  xhr.open('GET','https://www.easy-mock.com/mock/5b7238fdf22b3d63d2d67b28/jQuery-mock-test',true)
  xhr.send()
  xhr.addEventListener('load',function(){
    console.log(xhr.status)
    if((xhr.status >= 200 && xhr.status < 300)|| xhr.status === 304){
      var data = xhr.responseText
      console.log(data)
    }else{
      console.log('error')
    }
  })
  xhr.onerror = function(){
    console.log('error')
  }
```

### jQuery - $.ajax 用法
```JavaScript
  $.ajax({
    url: 'https://www.easy-mock.com/mock/5b7238fdf22b3d63d2d67b28/jQuery-mock-test',
    method: 'GET'
  }).done(function(result){
    console.log(result)
  }).fail(function(){
    console.log('error')
  })
```

### jQuery - $.get 用法
```JavaScript
  $.get('https://www.easy-mock.com/mock/5b7238fdf22b3d63d2d67b28/jQuery-mock-test').done(function(result){
    console.log(result)
  })
```

### jQuery - $.getJSON 用法
```JavaScript
  $.getJSON('https://www.easy-mock.com/mock/5b7238fdf22b3d63d2d67b28/jQuery-mock-test',function(result){
    console.log(result)
  })
```
