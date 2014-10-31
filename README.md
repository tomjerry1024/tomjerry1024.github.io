tomjerry1024.github.io
======================

js对象中私有变量和原型变量的理解1

function Obj()
{
	//this.a = {v:0};
	this.a.v++;	
	this.b = 1;
	this.b++;
}
Obj.prototype.a = {v:1};
Obj.prototype.get = function(k){
	return this[k];	
};

var myOby1 = new Obj();
var myOby2 = new Obj();
console.log(myOby1.get("a").v);
console.log(myOby1.get("b"));




