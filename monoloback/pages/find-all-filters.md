Keys for **ALL ROUTES**

```YML
_start: first element to take
_end: last element to take
_sort: key used to sort (see routes)
_order: 'asc' | 'desc'
```

---

**Addresses**

__Sort__ _(default: 'id')_

```Rust
['id', 'zip', 'cityId', 'street', 'houseNumber', 'longitude', 'latitude', 'createdAt']
```

__Filters__

```YML
city_id: number
zip_start: string (will take all zips beginning by this value)
createdAt_gte: everything create after this
createdAt_lte: everything created before this
```

---

**Cities**

__Sort__ _(default: 'id')_

```Rust
['id', 'zip', 'name', 'departmentId', 'longitude', 'latitude', 'createdAt']
```

__Filters__
```YML

department_id: number
zip_start: string (will take all zips beginning by this value)
name_start: string (will take all names beginning by this value)
createdAt_gte: everything create after this
createdAt_lte: everything created before this
```

---

**Countries**

__Sort__ _(default: 'id')_

```Rust
['id', 'name', 'code', 'longitude', 'latitude', 'createdAt']
```

__Filters__

```YML
name_start: string (will take all names beginning by this value)
code_start: string (will take all codes beginning by this value)
createdAt_gte: everything create after this
createdAt_lte: everything created before this
```

---

**Departments**

__Sort__ _(default: 'id')_

```Rust
['id', 'name', 'code', 'countryId', 'longitude', 'latitude', 'createdAt']
```

__Filters__

```YML
country_id: number
name_start: string (will take all names beginning by this value)
code_start: string (will take all codes beginning by this value)
createdAt_gte: everything create after this
createdAt_lte: everything created before this
```

---

**Exhibitions**

__Sort__ _(default: 'id')_

```Rust
['id', 'name', 'siteId', 'longitude', 'latitude', 'createdAt']
```

__Filters__

```YML
site_id: number
name_start: string (will take all names beginning by this value)
createdAt_gte: everything create after this
createdAt_lte: everything created before this
```

---

**ItemCategories**

__Sort__ _(default: 'id')_

```Rust
['id', 'name', 'createdAt']
```

__Filters__

```YML
name_start: string (will take all names beginning by this value)
createdAt_gte: everything create after this
createdAt_lte: everything created before this
```

---

**ItemTypes**

__Sort__ _(default: 'id')_

```Rust
['id', 'categoryId', 'name', 'createdAt']
```

__Filters__

```YML
item_category_id: number
name_start: string (will take all names beginning by this value)
createdAt_gte: everything create after this
createdAt_lte: everything created before this
```

---

**Items**

__Sort__ _(default: 'id')_

```Rust
['id', 'name', 'description', 'itemType', 'createdAt']
```

__Filters__

```YML
type_id: number
category_id: number
name_contains: string (will take all names containing this value)
createdAt_gte: everything created after this
createdAt_lte: everything created before this
```

---

**Persons**

__Sort__ _(default: 'id')_

```Rust
['id', 'type', 'name', 'birthDate', 'deathDate', 'createdAt']
```

__Filters__

```YML
person_type: PersonType
name_start: string (will take everything starting by this value)
birth_start: string (will take everything starting by this value)
death_start: string (will take everything starting by this value)
createdAt_gte: everything created after this
createdAt_lte: everything created before this
```

---

**Profiles**

```
Unsupported
```

---

**Sanctions**
> deletedAt and related are only accessible from 'Admin' profiles

__Sort__ _(default: 'id')_

```Rust
['id', 'userId', 'issuerId', 'reason', 'sanctionType', 'sanctionStart', 'sanctionEnd', 'createdAt', 'updatedAt']
```

__Filters__

```YML
reason_contains: string (will take everything containing this value)
target_user: number (id of the target user)
issuer: number (id of the issuer profile id)
issuer_user: number (id of the issuer user id)
sanction_type: string ('BAN' | 'BLOCK_UPLOAD')
sanctionStartAt_gte: every sanction starting after this
sanctionStartAt_lte: every sanction starting before this
sanctionEndAt_gte: every sanction ending after this
sanctionEndAt_lte: every sanction ending before this
createdAt_gte: everything created after this
createdAt_lte: everything created before this
deletedAt_gte: everything deleted after this
deletedAt_lte: everything deleted before this
```

---

**Sites**

__Sort__ _(default: 'id')_

```Rust
['id', 'type', 'name', 'telNumber', 'email', 'website', 'price', 'type', 'addressId', 'createdAt']
```

__Filters__

```YML
name_start: string (will take everything starting by this value)
tel_start: string (will take everything starting by this value)
email_start: string (will take everything starting by this value)
website_contains: string (will take everything containing this value)
price: number
site_type: SiteType
address_id: number
createdAt_gte: everything created after this
createdAt_lte: everything created before this
```

---

**Users**
> deletedAt and related are only accessible from 'Admin' profiles

__Sort__ _(default: 'id')_

```Rust
['id', 'username', 'telNumber', 'email', 'emailVerified', 'type', 'addressId', 'createdAt', 'deletedAt']
```

__Filters__
```YML
name_start: string (will take everything starting by this value)
tel_start: string (will take everything starting by this value)
email_start: string (will take everything starting by this value)
email_verified: boolean
createdAt_gte: everything created after this
createdAt_lte: everything created before this
deletedAt_gte: everything deleted after this
deletedAt_lte: everything deleted before this
```

---

**Videos**
> deletedAt and related are only accessible from 'Admin' profiles

__Sort__ _(default: 'id')_

```Rust
['id', 'validationStatus', 'createdAt'],
```

__Filters__
```YML
validationStatus: string ('VALIDATED' | 'REFUSED' | 'PENDING'),
item: number (the id of the item the video is related to),
user: number (the id of the user that posted the videos),
createdAt_gte: everything created after this
createdAt_lte: everything created before this
deletedAt_gte: everything deleted after this
deletedAt_lte: everything deleted before this
```
