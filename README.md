# GET-DESCRIPTION-FROM-README-ACTION

GitHub Action to get description from README.

## README Format

The first paragraph of the first header is considered the description.

## Usage

``` yaml
steps:
  -
    name: Checkout repository
    uses: actions/checkout@v4
  -
    name: Get README description
    id: get-description
    uses: rtvu/get-description-from-readme-action@v1.0.0
  -
    name: Echo description
    run: echo ${{ steps.get-description.outputs.description }}
```

## Inputs

| Name     | Description                  | Default     |
| -------- | ---------------------------- | ----------- |
| `readme` | Path to repository's README. | `README.md` |

## Outputs

| Name          | Description           |
| ------------- | --------------------- |
| `description` | README's description. |
