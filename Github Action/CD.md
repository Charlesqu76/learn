```
name: Deploy site files

on:
  push:
    branches:
      - master

jobs:
  deploy:
    runs-on: ubuntu-latest

    strategy:
      matrix:
        node-version: [18.x]

    steps:
    - name: Checkout
      uses: actions/checkout@master

    - name: Upload files to deploy server
      uses: appleboy/scp-action@master
      with:
        host: ${{ secrets.SSH_HOST }}
        username: ${{ secrets.SSH_USERNAME }}
        password: ${{ secrets.SSH_PASSWORD }}
        port: ${{ secrets.SERVER_PORT }}
        source: "./*"
        target: "/home/ubuntu/portfolio/"
        rm: true

    - name: Deploy on server
      uses: appleboy/ssh-action@master
      with:
        host: ${{ secrets.SSH_HOST }}
        username: ${{ secrets.SSH_USERNAME }}
        password: ${{ secrets.SSH_PASSWORD }}
        port: ${{ secrets.SERVER_PORT }}
        script: |
          cd /home/ubuntu/portfolio
          sudo chmod +x deploy.sh
          sudo sh deploy.sh
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjA2MjEzNyw0NDA1ODk0NDFdfQ==
-->