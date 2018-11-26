# php-template

Simple PHP template class.

## Create template file
[Example](https://github.com/isRuslan/php-template/blob/master/tpl.html) <br>
Template variables:<br>
- `{var}` - single variable <br>
- `{loop items} {name} {end loop}` - loop for items array <br>
- `{%index%}` - index of item in items loop

## Create index.php file
[Example](https://github.com/isRuslan/php-template/blob/master/index.php) <br>
- Include template class:<br>
`include 'template.php';`
- Create an object:<br>
`$template = new Template();`
- Set template variables, single:<br>
`$template->assign( 'my_var', 'test' );`
- Set template variables, loops:<br>
`$template->assign( 'items', array( array( 'name' => 'First' ), array( 'name' => 'Second' ) ) );`
- Parse template (eval()):<br>
`$template->parse( 'tpl.html' );`
- Parse template (return str):<br>
`$template->parse2string( 'tpl.html' );`
