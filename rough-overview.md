##### Seems like the base of React is component

```
class Game extends React.Component {
  render() {
    return(<a href="https://google.com">Hello</a>)
  }
}
```

Each component has a render() function ;
     which must return a view 
     and that view can be another component or simple html tags
     
like the following

```
class SimpleView extends React.Component{
  render(){
      return (<b>This is SimpleView</b>);
  }
}
class Game extends React.Component {
  render() {
    return (<SimpleView />);
  }
}
```
     
Q) What is React Component?
Q) How does rendering happens in React?
Q) How does compiling works in React?
        
When our data changes, React will efficiently update and re-render our components.
    
Q) How does react know that the data has been changed? What is the monitoring thing of react
    
#### Props of the component

Seems like each component acts a class which can have their own properties
Just like we describe the class in following manner

```java
class MyView(){
   public int width;
   public int height;
   public Person(){
   }
}
```

So, each component we can define our own properties as well
```
class MyView extends React.Component{
   render(){
     return(
       <b>My width ={this.props.width} height = {this.props.height} </b>
     );
   }
}
//and while calling this view we can do
class Game extends React.Component {
  render() {
    return (
          <MyView width="20" height="30"/>
    );
  }
}

```