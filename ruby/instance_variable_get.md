
#### instance_variable_get 
>取得并返回对象的实例变量的值.可以使用字符串或者Symbol来向var指定实例变量名.
若实例变量尚未定义,则返回nil.


```ruby
class Foo
  def initialize
    @foo = 1
  end
end
 
obj = Foo.new
p obj.instance_variable_get("@foo")     # => 1
p obj.instance_variable_get(:@foo)      # => 1
p obj.instance_variable_get(:@bar)      # => nil

```
### instance_variable_set(var, val)
>将val的值赋值给对象的实例变量并返回该值.可以使用字符串或Symbol来向var设定实例变量名.若实例变量尚未定义,则重新定义.

```ruby
obj = Object.new
p obj.instance_variable_set("@foo", 1)  # => 1
p obj.instance_variable_set(:@foo, 2)   # => 2
p obj.instance_variable_get(:@foo)      # => 2
```




#### 其他
```ruby
  # 定义
  def row_result_status
    self.instance_variable_get(:@result_status)
  end

  # 赋值
  ...
  self.instance_variable_set(:@result_status, 1)
  ...

  #调用  返回@result_status值 返回1
  self.row_result_status

```