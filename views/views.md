# View Snippets (.html.erb files)

## Links

This list assumes you have done `rake routes`

>Without controller

```ruby
<%= link_to 'Link', {controller: 'your_controller'}, class: "your_class" %>
```

>With controller

```ruby
<%= link_to 'Link', rake_routes_path, class: "your_class" %>
```

## Image Tag

## Iterating

```ruby
<% @list.each do |item| %>
        <%= item.column_name %>
        <%= image_tag item.img %>
        <%= link_to 'View', rake_routes_path(item), class: "your_class" %>
        <%= link_to 'Edit', edit_rake_routes(item), class: "your_class" %>
        <%= link_to 'Destroy',  rake_routes_path(item),
                                method: :delete, 
                                data: { confirm: 'Are you sure?' }, 
                                class: "your_class"
        %>
    <% end %>
```