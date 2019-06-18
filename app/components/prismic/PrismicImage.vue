<script>
export default {
  name: 'PrismicImage',
  props: {
    field: {
      default: null,
      required: true,
      validator: prop => typeof prop === 'object' || prop === null
    }
  },
  render(h) {
    if (this.field === null || this.field === undefined) return null
    return <img src={this.field.url} alt={this.field.alt || ''} copyright={this.field.copyright || ''} />
  }
}
</script>
