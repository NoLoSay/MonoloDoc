#  Create a page


1. Clone another folder within `src/pages` and name the new folder the same as your page name
2. Edit each of the tsx pages to reflect the logic your page
3. In the `src/App.tsx`:
    - Locate where the following blocks exist for other pages
    - Duplicate them
    - Enter your page values instead

```TSX
        {
            name: "items",
            list: "/items",
            create: "/items/create",
            edit: "/items/edit/:id",
            show: "/items/show/:id",
            meta: {
                canDelete: true, // Is the item deletable, you might want to disable it on enums, types and other critical items
            },
        },
```

```TSX
        <Route path="/items">
            <Route index element={<ItemList />} />
            <Route path="create" element={<ItemCreate />} />
            <Route path="edit/:id" element={<ItemEdit />} />
            <Route path="show/:id" element={<ItemShow />} />
        </Route>
```



