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
	
#### 推荐继承方式

	function Person(name, age) {
		this.name = name;
		this.age = age;
	}

	Person.prototype.getName = function() {
		return this.name;
	};

	Person.prototype.setName = function(name) {
		this.name = name;
	};

	Person.prototype.getAge = function() {
		return this.age;
	};

	Person.prototype.setAge = function(age) {
		this.age = age;
	};

	function Student(name, age, score) {
		Person.call(this, name, age);
		this.score = score;
	}

	Student.prototype = new Person();

	Student.prototype.getScore = function() {
		return this.score;
	}

	Student.prototype.setScore = function(score) {
		this.score = score;
	}

	var s = new Student("zhangsan", 12, 99);
	s instanceof Person && s instanceof Student
