# jquery-levelup
Simple +1/-1 Animation similar to point accumulation in a video game.

[on npm](https://www.npmjs.com/package/jquery-levelup)

[![Latest release](https://img.shields.io/github/release/pstrinkle/jquery-levelup.svg)](https://github.com/pstrinkle/jquery-levelup/releases/latest)
[![npm](https://img.shields.io/npm/v/jquery-levelup.svg)](https://www.npmjs.com/package/jquery-levelup)

Plans
-----

See issues.

Usage
-----
```html
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
<script src="/libs/jquery-levelup/jquery.levelup.min.js"></script>

<span>counter <span style="font-weight: bold;" id='the_cnt'>0</span></span>

<script>
    var $tc = $('#the_cnt');
    $tc.levelup({'start' : 0});

    $('#incrementBtn').on('click', function(event) {
        $tc.levelup('increment', 1);
        $(this).blur();
    });
    $('#decrementBtn').on('click', function(event) {
        $tc.levelup('decrement', 1);
        $(this).blur();
    });
</script>
```

Options
-------
You should specify options like in usage example above.

| Name | Type | Default | Description |
| ---- | ---- | ---- | ---- |
| start | integer | `0` | Start value for span. |
| incrementer/decrementer.bold | boolean | true | Whether the incrementer|decrementer is bold |
| incrementer/decrementer.color | CSS color string | null | Change the incrementer|decrementer's text color |
| incrementer/decrementer.class | string | null | Add a class to the incrementer|decrementer element |
| showThousands | boolean | false | Whether to use a thousands separate everywhere |
| thousandSep | string | "," | The thousand separator to use |

| Methods  | Params |
| ---- | ---- | ---- |
| `increment` | integer by which to increment |
| `decrement` | absolute value of integer by which to decrement (always positive) |
| `reset` | |
| `get` | | Returns the current value after all pending animations are completed.

License
-------
[Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0)
