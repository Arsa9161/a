# airtamer-mn
## Requirements
- sass-loader v10.1.1
- npm 6.14.5
## CSS rule
- Өнгийг hex бичиглэлээр бүтэн бичнэ.
  ```css
  // bad
  color: #000
  // good
  color: #000000
  ```
- rg1ba() ашиглах бол өнгийг rgb бичиглэл эсвэл хувьсагчаар авч болно.
- Spacing unit-дээ `px, %, vw, vh` ашиглана. 0 гэж тооцохдоо unit авалгүй дангаар нь бичнэ.
- Font-size болон line-height-г `rem`-ээр тооцно. letter-spacing `px`-ээр тооцно.
- Дараах нөхцлүүдэд шинэ мөр шилжүүлж бичнэ. 
  - Selector, pseudo class хооронд
  - mixin ашиглах үед. Хэрэв mixin нь `{` хаалтны дараа байвал шинэ мөр авах шаардлагагүй.
## Git rule
- Тухайн task-ын хүрээндэх branch дотроо л өөрчлөлтийг хийнэ
- 1 task 1 commit дүрэм-г баримтлана
- Task дууссан бол pull request develop branch-руу явуулах
- Pull request-ын description-д шинээр нэмсэн болон өөрчилсөн хэсгүүдийг тодорхой бичих
- Task дууссан гэж үзэж байгаа бол PR-ын link-г явуулах
- PR-с авсан comment-уудыг засварыг шинэ commit үүсгэн явуулна
## Build Setup



```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
