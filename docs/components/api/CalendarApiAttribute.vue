<template>
<b-table
  :data='props'>
  <template scope='props'>
    <b-table-column label='Property'>
      <span v-html='props.row.propertyName'></span>
    </b-table-column>
    <b-table-column label='Description'>
      <span v-html='props.row.description'></span>
    </b-table-column>
    <b-table-column label='Default'>
      <span v-html='props.row.default'></span>
    </b-table-column>
  </template>
</b-table>
</template>

<script>
export default {
  data() {
    const props = [
      {
        propertyName: '<code>key: String</code>',
        description: 'Attribute keys may affect how animations are applied when they appear or disappear.',
        default: '<code><i>index</i></code>',
      },
      {
        propertyName: '<code>highlight: Object</code>',
        description: 'Highlight to associate with the attribute.',
        default: '<code>undefined</code>',
      },
      {
        propertyName: '<code>dot: Object</code>',
        description: 'Dot to associate with the attribute.',
        default: '<code>undefined</code>',
      },
      {
        propertyName: '<code>bar: Object</code>',
        description: 'Bar to associate with the attribute.',
        default: '<code>undefined</code>',
      },
      {
        propertyName: '<code>contentStyle: Object</code>',
        description: 'Day cell content style to associate with the attribute.',
        default: '<code>undefined</code>',
      },
      {
        propertyName: '<code>contentHoverStyle: Object</code>',
        description: 'This style is merged with the <code>contentStyle</code> property when the content is hovered.',
        default: '<code>undefined</code>',
      },
      {
        propertyName: '<code>dates: Array[Date, Object]</code>',
        description: 'List of dates or date range objects for the attribute. Date ranges must specify <code>start</code> and <code>end</code> dates.',
        default: '<code>[]</code>',
      },
      {
        propertyName: '<code>order: Number</code>',
        description: 'By default, attributes are ordered to display the most information possible. For example, when attributes overlap, single date attributes appear above/before date range attributes, and date range attributes with a later start date appear above/before those with an earlier start date. If you would like to force an attribute to prioritize above all others (overriding these rules), assign an <code>order</code> value greater than 0.',
        default: '<code>0</code>',
      },
    ];
    return {
      props,
    };
  },
};
</script>
