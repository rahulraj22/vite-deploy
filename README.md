### Deploy Vite React App on Github
1. Make changes to `vite.config.js` by including `base: "/<repo-name>/` as shown in below code
```js
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
  base: "/vite-deploy/" // this is we are reffering to.
})
```

2. Create new folder `.github` and inside it create another folder `workflows` and inside it create file `deploy.yml`.
3. Copy paste the code of `deploy.yml` from [here](https://github.com/ErickKS/vite-deploy/blob/main/.github/workflows/deploy.yml) to your own `deploy.yml` file.
4. Then upload your project to github by creating repository.
5. Then go to `settings` -> `Actions` -> `general` -> Change `Workflow Permissions` to `Read and Write permissions` -> then click `SAVE`.
6. Go to `Actions` tab and see the `deployments` performed in action.
