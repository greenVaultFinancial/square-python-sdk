## Catalog Query

A query composed of one or more different types of filters to narrow the scope of targeted objects when calling the `SearchCatalogObjects` endpoint.

Although a query can have multiple filters, only one query is allowed per call to [SearchCatalogObjects](#endpoint-Catalog-SearchCatalogObjects).

When a query filter is based on an attribute, the attribute must be searchable. 
Searchable attributes are listed as follows, along their parent types that can be searched for with applicable query filters. 

Searchable attribute and objects queryable by searchable attributes ** 
- `name`:  `CatalogItem`, `CatalogItemVariation`, `CatelogCatogry`, `CatalogTax`, `CatalogDiscount`, `CatalogModifier`, 'CatalogModifierList`, `CatalogItemOption`, `CatalogItemOptionValue` 
- `description`: `CatalogItem`, `CatalogItemOptionValue` 
- `abbreviation`: `CatalogItem` 
- `upc`: `CatalogItemVariation` 
- `sku`: `CatalogItemVariation` 
- `caption`: `CatalogImage` 
- `display_name`: `CatalogItemOption` 

For example, to search for [CatalogItem](#type-CatalogItem) objects by searchable attributes, you can use 
the `"name"`, `"description"`, or `"abbreviation"` attribute in an applicable query filter.

### Structure

`CatalogQuery`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sorted_attribute_query` | [`Catalog Query Sorted Attribute`](/doc/models/catalog-query-sorted-attribute.md) | Optional | The query expression to specify the key to sort search results. |
| `exact_query` | [`Catalog Query Exact`](/doc/models/catalog-query-exact.md) | Optional | The query filter to return the serch result by exact match of the specified attribute name and value. |
| `prefix_query` | [`Catalog Query Prefix`](/doc/models/catalog-query-prefix.md) | Optional | The query filter to return the search result whose named attribute values are prefixed by the specified attribute value. |
| `range_query` | [`Catalog Query Range`](/doc/models/catalog-query-range.md) | Optional | The query filter to return the search result whose named attribute values fall between the specified range. |
| `text_query` | [`Catalog Query Text`](/doc/models/catalog-query-text.md) | Optional | The query filter to return the search result whose searchable attribute values contain all of the specified keywords or tokens, independent of the token order or case. |
| `items_for_tax_query` | [`Catalog Query Items for Tax`](/doc/models/catalog-query-items-for-tax.md) | Optional | The query filter to return the items containing the specified tax IDs. |
| `items_for_modifier_list_query` | [`Catalog Query Items for Modifier List`](/doc/models/catalog-query-items-for-modifier-list.md) | Optional | The query filter to return the items containing the specified modifier list IDs. |
| `items_for_item_options_query` | [`Catalog Query Items for Item Options`](/doc/models/catalog-query-items-for-item-options.md) | Optional | The query filter to return the items containing the specified item option IDs. |
| `item_variations_for_item_option_values_query` | [`Catalog Query Item Variations for Item Option Values`](/doc/models/catalog-query-item-variations-for-item-option-values.md) | Optional | The query filter to return the item variations containing the specified item option value IDs. |

### Example (as JSON)

```json
{
  "sorted_attribute_query": null,
  "exact_query": null,
  "prefix_query": null,
  "range_query": null,
  "text_query": null,
  "items_for_tax_query": null,
  "items_for_modifier_list_query": null,
  "items_for_item_options_query": null,
  "item_variations_for_item_option_values_query": null
}
```

