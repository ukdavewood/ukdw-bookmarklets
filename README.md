# ukdw-bookmarklets
Various Cruise related bookmarklets - tested againsts IgluCruise.co.uk - but may work on others with some modification

Instructions - drag bookmarklets to your bookmark bar to install dummy version, then edit the link with the text below

Bookmarklets
[Price per day](https://www.google.com)

```javascript:(function()%7Bvar%20%24div2%20%3D%20%24(%22div.ais-hits--item%22)%3Bconsole.log(%24div2.length)%3Bconst%20gratuities%20%3D%20%7B%20%22%2Fpo-cruises%22:%200%2C%22%2Fcelebrity-cruises%22:%2017.50%2C%22%2Fprincess-cruises%22:%2016%2C%22%2Froyal-caribbean-cruises%22:%2016%2C%22%2Fnorwegian-cruise-line-cruises%22:%2018%2C%22%2Fcunard-cruises%22:%2014.50%2C%22%2Fmarella-cruises%22:%200%2C%22%2Fholland-america-line-cruises%22:%2016%2C%22%2Fmsc-cruises%22:%200%20%7D%3Bexchange_rate%20%3D%200.8%3B%24(%24div2).each(function(%20index)%20%7Bvar%20days%20%3D%20parseFloat(%20%24(this).find('div.minimal-card__nights').find('span').text().split('%20')%5B0%5D)%20%3Bvar%20cost%20%3D%20parseFloat%20(%24(this).find(%22div.price-list__number%22).first().text().replace(%2F%5B%C2%A3%2C%5D%2B%2Fg%2C%22%22))%3B%24(this).find(%22ul.minimal-card__price-list--desktop%20li%22).first().clone().insertAfter(%24(this).find(%22ul.minimal-card__price-list--desktop%20li%22).first())%3Bvar%20costperday%20%3D%20Math.round(cost%2Fdays)%3Bvar%20%24href%20%3D%20%24(this).find('div.minimal-card__logo').find('a').first().attr('href')%3Bconsole.log('href:'%20%2B%20%24href)%3Bvar%20%24grat%20%3D%20gratuities%5B%24href%5D%3Bvar%20%24suff%20%3D%20%22%2Fd%22%3Bif%20(%24grat%20%3E%200)%20%7Bcostperday%20%3D%20costperday%20%2B%20Math.round(%24grat%20*%20exchange_rate)%3B%24suff%20%3D%20%22%2Fd*%22%20%3B%7D%24(this).find(%22div.price-list__number%22).first().html(%22%C2%A3%22%20%2B%20costperday.toString()%20%2B%20%22%20%22%20%2B%20%24suff)%3Bconsole.log(index%2C%20days%2Ccost%2Ccostperday%2C%24grat)%3B%7D)%3Bif%20(%24div2.length%20%3D%3D%20%200)%20%20alert(%22igloo%20table%20not%20found%22)%3Bif%20(%24div2.length%20%3E%200%20%26%26%20%24div2.length%20%3C%200)%20%20%7Bif%20(confirm(%24div2.length%20%2B%20%22%20values%20sorted%20-%20increase%20to%20100%3F%22))%20%7Bif%20(window.location.href.includes(%22hitsPerPage%3D%22))%20%7Bwindow.location.href%20%3D%20window.location.href.replace(%22hitsPerPage%3D%22%2C%22hitsPerPage%3D1%22)%7D%20else%20%7Bwindow.location.href%20%3D%20window.location.href%20%2B%20%22%26hitsPerPage%3D100%22%3B%7D%7D%7D%7D)()```


To edit them - such as adding / changing dates to the Overlap Bookmarklet - 
  1. Copy the bookmarklet
  2. Select the EncDec4 bookmarklet
  3. Select paste
  4. Select decode
  5. Edit code
  6. Select Encoude
  7. Select Copy
  8. Go back to bookmarklet, edit the address and paste the clipboard in.
  9. 
