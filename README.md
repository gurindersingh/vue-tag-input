# @gurinder/vue-tag-input

### Usage

```html
<vue-tag-input tag-rest-url="http://example.com/tags" :data-selected-tags="selectedTags"></vue-tag-input>
```

JS
```js
import VueTagInput from '@gurinder/vue-tag-input';
Vue.component('vue-tag-input', VueTagInput);
```

SCSS
```scss
.tag-wrap {
  position: relative;
}

.tag-box {
  display: flex;
  flex-wrap: wrap;

  > .tag {
    background: $primary; // Color
    margin: 0 5px 5px 0;
    border-radius: 5px;
    color: white;
    display: flex;
    align-content: center;
    overflow: hidden;

    .tag-label {
      padding: 0 0 0 10px;
    }

    .delete {
      display: flex;
      align-content: center;
      background: darken($primary, 5%);
      padding: 5px;
      margin: 0 0 0 10px;
    }

  }

  > input {
    border: none;
    height: 26px;
    flex-grow: 1;

    &:focus {
      box-shadow: none !important;
      border: none !important;
      outline: none;
    }
  }

}

.tag-suggections {
  position: absolute;
  width: 100%;
  background: white;
  z-index: $zindex-popover;
  left: 0;

  li.active {
    background: #efefef;
  }

}
```