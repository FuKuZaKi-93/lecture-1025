# テクノロジー（藤原）10/25授業

```
fukuzaki93:~/workspace $ pry
[1] pry(main)> puts "こんにちは"
こんにちは
=> nil
[2] pry(main)> print "こんにちは"
こんにちは=> nil
[3] pry(main)> p "こんにちは"
"こんにちは"
=> "こんにちは"
[4] pry(main)> message = "こんにちは"
=> "こんにちは"
[5] pry(main)> puts message
こんにちは
=> nil
[6] pry(main)> num = 123
=> 123
[7] pry(main)> outs num
NoMethodError: undefined method `outs' for main:Object
from (pry):7:in `__pry__'
[8] pry(main)> puts num
123
=> nil
[9] pry(main)> puts message.length
5
=> nil
[10] pry(main)> 1234   # Integer (整数，Ruby2.4以降の場合)
=> 1234
[11] pry(main)> 1234.class
=> Integer
[12] pry(main)> 3.14159  # Float (少数)
=> 3.14159
[13] pry(main)> (3.14159).class
=> Float
[14] pry(main)> Math::PI # より正確な円周率
=> 3.141592653589793
[15] pry(main)> 'こんにちは'
=> "こんにちは"
[16] pry(main)> "さようなら"
=> "さようなら"
[17] pry(main)> 'ぐり'+'と'+'ぐら'   # +で文字列を連結
=> "ぐりとぐら"
[18] pry(main)> name =
[18] pry(main)* 
[18] pry(main)* 
[18] pry(main)* 'ふじわら'　# 決まった文字列は一重引用符がベター
/usr/local/rvm/gems/ruby-2.4.0@global/gems/method_source-0.9.0/lib/method_source/code_helpers.rb:140:in `===': invalid byte sequence in UTF-8 (ArgumentError)
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/method_source-0.9.0/lib/method_source/code_helpers.rb:140:in `==='
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/method_source-0.9.0/lib/method_source/code_helpers.rb:76:in `rescue in complete_expression?'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/method_source-0.9.0/lib/method_source/code_helpers.rb:80:in `complete_expression?'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/pry_instance.rb:290:in `handle_line'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/pry_instance.rb:243:in `block (2 levels) in eval'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/pry_instance.rb:242:in `catch'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/pry_instance.rb:242:in `block in eval'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/pry_instance.rb:241:in `catch'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/pry_instance.rb:241:in `eval'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/repl.rb:77:in `block in repl'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/repl.rb:67:in `loop'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/repl.rb:67:in `repl'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/repl.rb:38:in `block in start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/input_lock.rb:61:in `__with_ownership'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/input_lock.rb:79:in `with_ownership'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/repl.rb:38:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/repl.rb:13:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/pry_class.rb:192:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/lib/pry/cli.rb:116:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/pry-0.11.2/bin/pry:12:in `<top (required)>'
        from /usr/local/rvm/rubies/ruby-2.4.0/bin/pry:22:in `load'
        from /usr/local/rvm/rubies/ruby-2.4.0/bin/pry:22:in `<main>'
        from /usr/local/rvm/gems/ruby-2.4.0/bin/ruby_executable_hooks:15:in `eval'
        from /usr/local/rvm/gems/ruby-2.4.0/bin/ruby_executable_hooks:15:in `<main>'
fukuzaki93:~/workspace $ pry
[1] pry(main)> name = 'ふじわら' # 決まった文字列は一重引用符がベター
=> "ふじわら"
[2] pry(main)> puts "#{name}さん、こんにちは"   # 式展開（二重引用符の [2] pry(main)> puts "#{name}さん、こんにちは"   # 式展開（二重引用符の ふじわらさん、こんにちは
=> nil
[3] pry(main)> puts "\nさようなら\n"  # 改行は\n（二重引用符の中のみ）

さようなら
=> nil
[4] pry(main)> a=4;b="9"
=> "9"
[5] pry(main)> a+b
TypeError: String can't be coerced into Integer
from (pry):5:in `+'
[6] pry(main)> a.to_s + b
=> "49"
[7] pry(main)> (a.to_s + b)                                            
=> "49"
[8] pry(main)> (a.to_s + b).class
=> String
[9] pry(main)> a + b.to_i
=> 13
[10] pry(main)> (a + b.to_i).class                                     
=> Integer
[11] pry(main)> animals = ["いぬ", "ねこ", "ぞう"]                     
=> ["いぬ", "ねこ", "ぞう"]
[12] pry(main)> animals
=> ["いぬ", "ねこ", "ぞう"]
[13] pry(main)> animals[0]
=> "いぬ"
[14] pry(main)> animals[1] = "こうもり"
=> "こうもり"
[15] pry(main)> animals
=> ["いぬ", "こうもり", "ぞう"]
[16] pry(main)> animals[3]
=> nil
[17] pry(main)> animals.push("くじら")
=> ["いぬ", "こうもり", "ぞう", "くじら"]
[18] pry(main)> animals
=> ["いぬ", "こうもり", "ぞう", "くじら"]
[19] pry(main)> animals.pop
=> "くじら"
[20] pry(main)> animals
=> ["いぬ", "こうもり", "ぞう"]
[21] pry(main)> colors = []
=> []
[22] pry(main)> colors.empty?
=> true
[23] pry(main)> colors.length
=> 0
[24] pry(main)> colors = ["赤", "青", "黄", "ピンク"]                  
=> ["赤", "青", "黄", "ピンク"]
[25] pry(main)> colors.empty?
=> false
[26] pry(main)> colors.length
=> 4
[27] pry(main)> 5.time {|i| puts i}
NoMethodError: undefined method `time' for 5:Integer
Did you mean?  times
from (pry):27:in `__pry__'
[28] pry(main)> 5
=> 5
[29] pry(main)> 5.time {|i| puts i}
NoMethodError: undefined method `time' for 5:Integer
Did you mean?  times
from (pry):29:in `__pry__'
[30] pry(main)> 5.times {|i| puts i}                                   
0
1
2
3
4
=> 5
[31] pry(main)> 5.class
=> Integer
[32] pry(main)> a = true
=> true
[33] pry(main)> b = 1
=> 1
[34] pry(main)> c = "a" 
=> "a"
[35] pry(main)> d = if true
[35] pry(main)*   "a"
[35] pry(main)* end  
=> "a"
[36] pry(main)> exit
```