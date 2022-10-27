# tag-exists-action

A Github action that determines if a tag exists

## Inputs

### `tag`

**Required** The tag to search for.

## Outputs

### `exists`

a string value of 'true' or 'false'

## Example usage

```yaml
- uses: uruz-7/tag-exists-action@v2
  id: checkTag
  with:
    tag: "v1"
  env:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

- run: echo ${{ steps.checkTag.outputs.exists }}
```
