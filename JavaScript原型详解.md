#### 经典方式

    function Person(name, age) {
		this.name = name;
		this.age = age;
	}
	
	Person.prototype.getInfo = function() {
		return this.name + ", " + this.password;
	};
	
	var p = new Person("zhangsan", "123");
	var p2 = new Person("lisi", "456");

	p.getInfo();
	p2.getInfo();

#### 动态原型方式

	function Person(username, password) {
		this.username = username;
		this.password = password;

		if(!Person.prototype.getInfo) {
			Person.prototype.getInfo = function() {
				return this.name + ", " + this.password;
			};
		}
	}

	var p = new Person("zhangsan", "123");
	var p2 = new Person("lisi", "456");

	p.getInfo();
	p2.getInfo();
