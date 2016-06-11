# A very quick intro to Ruby and ERB

This short and snappy chapter is a reference for those who are encountering Ruby and ERB for the first time or need a refresher.

This chapter is not extensive, and if you feel you need more, [you can find a list of tutorials/books I found useful myself learning Ruby](#further_resources)

## Ruby

## Erb

Erb is short for "embedded Ruby". Erb is a syntax that should be pretty familiar to experienced developers as most languages seems to have a version.

In erb you mix your HTML/JS with template tags that output the value of your Ruby code.

The tags look like a variation of ```<% ruby_code_in_here %>```.

The three major variations of these brackets - the ```<%``` bits - are the following:

### Print code tag <%= %>

Percentage brackets followed directly by an equal sign prints out the result of your ruby code.

So the following code:

```erb
<h1><%= title %></h1>
```

Results in the title variable being printed into your HTML. So if our title variable was "Hello world!" we'd see:

```html
<h1>Hello world!</h1>
```

### Non-printing code tag <% %>

In order to run code, but not print it out, you don't include the equal sign "=". So the following:

```erb
<h1><% title %></h1>
```

Wouldn't print anything between the `<h1>` tags. The title code would be run, but nothing would be printed out into your HTML.

Naturally there are plenty of times we need to execute code without printing something. We could be declaring a variable before using it elsewhere. Running some calculations or grabbing some external resources.

Another major reason to use the executing code tag is for logic. When we want to start an if loop we don't want to print our logic because that would create an error. We use the executing code tag like below:

```erb
<% if true %>

<% end %>
```
Here our if/end block is executed and, as expected, not printed out (if we try to print it out an if we get an error).

If you are wondering how we bring this together to actually make an if block print something out, we either place our HTML inside the blow or include an output tag inside the if block like so:

```erb
<% if true %>
  <h1>Raw html that prints if true</h1>
  <%= some_variable_which_will_print_out_if_true? %>
<% end %>
```

### Comment tag <%# %>

> If you're used to PHP you may have noticed that with Ruby you don't need to constantly `echo` things as Ruby automatically returns the result of the last statement

### Non-printing, Remove trialing whitespace tag <% -%>

You may find the need, or notice in the wild, the use of a tag with a minus tag at the end of the ```%>```. This is about removing the trailing whitespace from any executed code.

## Further resources