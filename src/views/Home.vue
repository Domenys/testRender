<script>


export default {
  name: 'Home',
  data: () => ({
    name: 'Деном',
    level: '1'
  }),
  render(createElement) {
    return createElement('div', {
      attrs: {
        class: 'box'
      }
    }, [
      createElement(`h${this.level}`, {
        attrs: {
          class: 'box-title'
        }
      }, 'Добро пожаловать!'),
      createElement('span', {
        attrs: {
          class: 'box-text'
        },
      }, `Данная страница создана ${this.name}`)
    ])
  }
}
</script>


<style lang="less" scoped>
  .box {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 400px;
    height: 200px;
    margin: 10% auto;
    background: #c5c9c7;
    .box-title {
      color: red;
    }
    .box-text {
      color: blue;
    }
  }
</style>