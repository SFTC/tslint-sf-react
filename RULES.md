# Rules

- `jsx-alignment`
  - 属性对齐，jsx的属性，或者在同一行，或者每行一个；

  ```ts
  // Good:
  const element = <div
      className="foo"
      tabIndex={1}
  >
      {children}
  </div>;

  // Also Good:
  <Button
      appearance="pretty"
      disabled
      label="Click Me"
      size={size}
  />

  // Also Good:
  <Col span={7} style={{ textAlign: "right" }}>

  // Bad
  <Select style={{ width: 130 }}
      onChange={this.handleSelectProvince}
      defaultValue={select.station_province || ""}
    >
  ```

- `jsx-boolean-value`
  - 对于布尔值的属性，不能够省略.

  ```ts
  // Bad:
  const element = <div
      className="foo"
      tabIndex={1}
      disabled
  >
      {children}
  </div>;

   // Good:
  const element = <div
      className="foo"
      tabIndex={1}
      disabled={true}
  >
      {children}
  </div>;
  ```

- `jsx-curly-spacing`
  - 在大括号的属性值中，要求在括号内填充空格，在tslint-react中设置的'never'，这里升级为'always'

- `jsx-equals-spacing`
  - 在属性的等号前后填充空格，在tslint-react中设置的'never'，这里升级为'always'.

  ```ts
  // Bad:
  const element = <div
      className="foo"
      tabIndex={1}
      disabled
  >
      {children}
  </div>;

   // Good:
  const element = <div
      className = "foo"
      tabIndex = { 1 }
  >
      {children}
  </div>;
  ```

- `jsx-key`
  - 在`Array.prototype.map`函数中，提示缺少key值；

- `jsx-no-bind`
  - 禁止在JSX中使用bind函数，也是出于减少重复渲染的考虑；

- `jsx-no-lambda`
  - 禁止在JSX中使用箭头函数，也是出于减少重复渲染的考虑；

- `jsx-no-string-ref`
  - 禁止使用字符串，作为ref的赋值；

  ``` ts
  // Bad;
  <div ref="container"></div>

  // Good;
  this.myRef = React.createRef();
  ...
  <div ref={this.myRef}></div>
  ```

- `jsx-self-close`
  - 没有子元素时，请使用自闭合的方式；

  ```ts
  // Bad;
  <div className="foo"></div>

  // Good;
  <div className="foo" />
  ```

- `jsx-space-before-trailing-slash`
  - 自闭合的标签，需要在'/>'前面有一个空格.


- `jsx-wrap-multiline`
  - 强制要求JSX值被括号包裹，且左括号、右括号各自独立一行；

  ```ts
  // bad
  const button = <button type="submit">
      Submit
  </button>;

  // good
  const button = (
      <button type="submit">
          Submit
      </button>
  );
  ```

--------------

- `adjacent-overload-signatures`
  - 重载要挨着；

- `align`
  - {options: ["parameters", "statements"]}
  - 参数与代码块均需对齐；

- `"array-type": [true, "array-simple"]`
  - 对于数组，使用T[]方式进行类型声明，T是简单类型；

- `arrow-parens`
  - 箭头函数的参数，必须使用括号包裹；

- `arrow-return-shorthand`
  - 箭头函数在直接return的情形下，需省略return；

- `ban-types`
  - ["Object", "Avoid using the `Object` type. Did you mean `object`?"],
  - ["Function","Avoid using the `Function` type. Prefer a specific function type, like `() => void`.",],
  - ["Boolean", "Avoid using the `Boolean` type. Did you mean `boolean`?"],
  - ["Number", "Avoid using the `Number` type. Did you mean `number`?"],
  - ["String", "Avoid using the `String` type. Did you mean `string`?"],
  - ["Symbol", "Avoid using the `Symbol` type. Did you mean `symbol`?"],

- `callable-types`
  - An interface or literal type with just a call signature can be written as a function type.

- `class-name`
  - 强制使用大驼峰式为类命名；

- `comment-format`
  - options: ["check-space"]
  - 单行注释，// 后必须以一个空格为开始；

- `curly`
  - 要求 if/for/do/while 代码片段使用大括号包裹；

- `eofline`
  - 确保每个文件最后一行为空行

- `forin`
  - 在for in循环内部，强制要求使用if对属性进行过滤

  ``` ts
  for (let key in someObject) {
    if (someObject.hasOwnProperty(key)) {
        // code here
    }
  }
  ```

- `indent: [true, "spaces", 2]`
  - 使用两个空格做代码缩进

- 54 https://github.com/palantir/tslint/blob/master/src/configs/recommended.ts