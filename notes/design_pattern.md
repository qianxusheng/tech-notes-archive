# 单例模式：
  private constructor不让外部创建新的instance，public一个static方法（不依赖于instance）getInstance获取instance --只有一个instance
# 观察者模式：
  创建subject和observer抽象类，具体实现subject和observer，subject（agency）需要observer作为输入，一旦触发subject的某个方法，可以通知订阅的所有observer
# 工厂模式：
  const myDrink = DrinkFactory.createDrink("cola"); const myDrink = new CocaCola(); decoupled，第二种方式如果cocacola改成百事需要把每一行都改了，但是第一种可以在drinkFactory里面改
