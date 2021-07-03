### Vòng đời của một component 

sử dụng hook useEffect();

nếu ko có đối số thứ 2 truyền vào thì là componentDidMount, componentDidUpdate,

nếu truyền vào mảng đối số là [] => componentDidMount.

nếu truyền mảng có các đối số [agr1, agr2] => componentDidUpdate (update khi các đối số truyền vào thay đổi)

nếu truyền vào một return hàm ở cuối thì nó sẽ là componentWillUnMount;
useEffect(()=> {
    console.log('componentDidMount');
    return () => {
      console.log('component WillUnMount');
    }
  }, []);