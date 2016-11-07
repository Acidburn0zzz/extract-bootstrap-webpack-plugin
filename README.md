# extract-bootstrap-webpack-plugin

Extract the webpack bootstrap into its own file. This supports some use cases related to sharing a webpack bootstrap to decrease file size of a large group of entries. This could be use with a package of components where each component is an entry. Then using those components in an application, the application's webpack config doesn't need to worry about the specific webpack config needed for the components. This plugin for such a use case then provides some optimization by reducing the duplication of the bootstrap in each output bundle. If the application used 20 unique components from the component package, the bootstrap for those components would appear once in your application bundle instead of 20 times.
