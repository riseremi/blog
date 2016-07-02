# React Native
Записки будущему мне.

Стартовый набор:
* https://facebook.github.io/react-native/docs/getting-started.html
* https://github.com/react-native-material-design/react-native-material-design
* https://github.com/react-native-material-design/demo-app

 Большинство вопросов отлично гуглится в документации.
 
## Тонкие моменты
* Border можно задавать только каждый по отдельности. Чтобы сделать серый border сверху блока:
```js
postStyle: {
  borderTopWidth: 1,
  borderTopColor: '#d8d8d8'
}
```
* Нет блочной модели, используется flex. Чтобы расположить два элемента в ряд:
```jsx
<View style={style.container}>
  <Text>Previous</Text>
  <Text>Next</Text>
</View>

const styles = StyleSheet.create({
  container: {
    flexDirection: 'row',
  },
});
```
* Чтобы отключить iOS-like навигацию свайпами, в Navigator надо добавить `gestures: false`:
```
<Navigator
  configureScene={(route, stack) => {
    return {
      ...Navigator.SceneConfigs.HorizontalSwipeJump,
      gestures: false
    };
  }}
/>
```
* Чтобы убрать тень под тулбаром, нужно в его стили прописать `elevation: 0`
