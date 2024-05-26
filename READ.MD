# Mono Repo


## Absulute Path configs


tsconfig.json
```json
{
	"compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "@*": ["./src/*"],
      "@components/*": ["./src/*", "./dist/*", ""],
      "@pages/*": ["./src/pages/*"],
      "@routes/*": ["./src/routes/*"],
      "@hooks/*": ["./src/hooks/*"],
      "@api/*": ["./src/api/*"],
      "@utils/*": ["./src/utils/*"],
      "@types/*": ["./src/types/*"]
    }
	}
}
```
vite.config.ts
```ts
  resolve: {
    alias: {
      '@': path.resolve(__dirname, './src/'),
      '@components': path.resolve(__dirname, './src/components/'),
      '@pages': path.resolve(__dirname, './src/pages/'),
      '@hooks': path.resolve(__dirname, './src/hooks/'),
      '@api': path.resolve(__dirname, './src/api/'),
      '@utils': path.resolve(__dirname, './src/utils/'),
      '@routes': path.resolve(__dirname, './src/routes/'),
      '@types': path.resolve(__dirname, './src/types/'),
    }
  }
```