### Helpful commands

### Build Packages in workspaces
- #### For single package
> yarn workspace @medusajs/dashboard build

#### For all package 
> yarn workspaces foreach --all run  build

### Publish Packages 
- #### For single package
> yarn workspace @medusajs/dashboard npm publish

- #### For all package 
> yarn workspaces foreach -A npm publish --tolerate-republish --access public

### Unpublish packages
- #### For single package

> yarn workspace @medusajs/dashboard exec npm unpublish @medusajs/dashboard --force

- #### For all package 

> yarn workspaces foreach -pv exec 'npm unpublish $(node -p "require(\"./package.json\").name") --force'