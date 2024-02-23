# React Component Layout

Bu README dosyası, React uygulamalarında Component Layout konseptini anlatan bir rehberdir. 

## Component Layout Nedir?

React uygulamalarında, Component Layout, kullanıcı arayüzünü oluşturan bileşenlerin düzenini ve ilişkilerini belirten bir konsepttir. Bu, uygulamanın genel yapısını oluşturur ve bileşenlerin birbirleriyle nasıl etkileşimde bulunacaklarını tanımlar.

## Componentleri Nasıl Kullanmalıyız?

React'te, bileşenleri kullanmak için önce onları oluşturmalı ve ardından uygulamanın farklı kısımlarında bu bileşenleri yerleştirmelisiniz. İşte basit bir örnek:

```jsx
import React from 'react';

const App = () => {
  return (
    <div>
      <Header />
      <MainContent />
      <Footer />
    </div>
  );
};

const Header = () => {
  return <header>Uygulama Başlığı</header>;
};

const MainContent = () => {
  return <main>Uygulama İçeriği</main>;
};

const Footer = () => {
  return <footer>Uygulama Alt Bilgi</footer>;
};
```
## Props Değerleri ve Avantajları
Component Layout içinde props değerleri kullanmak, bileşenler arasında veri iletişimini sağlar. Bu, bileşenlerin dinamik ve esnek olmasını sağlar. İşte basit bir örnek:

```javascript
import React from 'react';

const UserInfo = (props) => {
  return (
    <div>
      <p>Ad: {props.name}</p>
      <p>Email: {props.email}</p>
    </div>
  );
};

const App = () => {
  const user = {
    name: 'John Doe',
    email: 'john@example.com',
  };

  return <UserInfo {...user} />;
};
```
## Components Düzenlerinin Avantajları
### Modülerlik
React bileşenleri modülerdir, yani bağımsız olarak geliştirilebilir ve test edilebilirler. Bu, uygulamanın bölünmüş ve yönetilebilir parçalardan oluşmasını sağlar.

### Sürdürülebilirlik
Bileşen düzeni, uygulamanın büyümesi ve değişmesi sırasında daha sürdürülebilir bir kod tabanı oluşturur. Her bir bileşeni izole etmek, bakımını kolaylaştırır.

### Yeniden Kullanılabilirlik
Her bir bileşen, kendi içinde bir amaca hizmet eder ve bu, bu bileşenlerin başka yerlerde tekrar kullanılabilir olmasını sağlar. Bu, kodunuzu daha verimli ve etkili hale getirir.

### Tek Bir Komponent Tek Bir Amaca Hizmet Etmeli
Her bir bileşen, tek bir sorumluluğa odaklanmalıdır. Bu, kodun anlaşılabilirliğini artırır ve bakımı kolaylaştırır.

Bu avantajlar, React uygulamalarının daha sürdürülebilir ve yönetilebilir olmasını sağlar.


