> Person.js

    function Person(name, age) {
		this.name = name;
		this.age = age;
	}

	Person.prototype.defaults = {
		username: "zhangsan",
		password: "123456"
	};

	Person.prototype.getName = function() {
		return this.name;
	};

	Person.prototype.getAge = function() {
		return this.age;
	};

	Person.prototype.setName = function(name) {
		this.name = name;
	};

	Person.prototype.setAge = function(age) {
		this.age = age;
	};

	Person.prototype.getInfo = function() {
		return this.name + ", " + this.age;
	};
