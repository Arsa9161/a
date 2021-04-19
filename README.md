# airtamer-mn
## Requirements
- sass-loader v10.1.1
- npm v6.14.5
## CSS rule
Энэ төсөл дээр `css` бичихдээ дараах стандартаар бичье. 😄
- Өнгийг `rgba()` ашиглаагүй л бол ямагт **hex** бичиглэлээр **бүтэн** бичнэ. Энэ нь илүү найдвартай юм.
  ```css
  /* bad */
  color: #000;
  
  /* good */
  color: #000000;
  ```
- `rgba()` ашиглах бол өнгийг **rgb** бичиглэл эсвэл **хувьсагч**-аар авч болно.
  ```css
  /* bad */
  color: rgba(#000, 0.4);
  
  /* good */
  color: rgba(0, 0, 0, 0.4);
  color: rgba($var, 0.4);
  ```
- Spacing unit-дээ `px, %, vw, vh` ашиглана. 0 гэж тооцохдоо unit авалгүй дангаар нь бичнэ.
  ```css
  /* bad */
  margin: 2rem 0px;
  
  /* good */
  margin: 10px 0;
  ```
- `font-size` болон `line-height`-г `rem`-ээр, letter-spacing `px`-ээр тооцно.
  ```css
  /* bad */
  font-size: 10px;
  line-height: 10px;
  letter-spacing: 0.5em;
  
  /* good */
  font-size: 1rem;
  line-height: 1rem;
  letter-spacing: 0.5px;
  ```
 - `font-weight` тоогоор тооцно.
  ```css
  /* bad */
  font-weight: bold;
  
  /* good */
  font-weight: 700;
  ```
- Дараах нөхцлүүдэд шинэ мөр шилжүүлж бичнэ. 
  - Selector, pseudo class хооронд
  ```css
  /* bad */
    .selector {
      color: #000000;
        .title {
         color: #000000;
           &::after {
           ...
           }
        }
    }
    
  /* good */
    .selector {
      color: #000000;
      
      .title {
       color: #000000;
        
         &::after {
         ...
         }
      }
    }
  ```
  - mixin ашиглах үед. Хэрэв mixin нь `{` хаалтны дараа байвал шинэ мөр авах шаардлагагүй.
  ```css
  /* bad */
    .selector {
      @include mq('sm') {
        color: #000000;
      }
      @include mq('md') {
        color: #0000ff;
      }
    }
    
  /* good */
    .selector {
      @include mq('sm') {
        color: #000000;
      }
      
      @include mq('md') {
        color: #0000ff;
      }
    }
  ```
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
