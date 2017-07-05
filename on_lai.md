## Menu với thẻ ul,li, thuộc tính relative, absolute, z-index, display: none
## Lựa chọn option với checkbox, radio, label.
## sử dụng jquery để thêm sản phẩm vào giỏ hàng.
https://stackoverflow.com/questions/24126819/jquery-sum-of-multiple-input-fields-if-same-class-in-one-input
* key word tìm kiếm:
https://www.google.com.vn/search?q=how+to+add+1+value+without+all+in+the+same+class+jquery&oq=how+to+add+1+value+without+all+in+the+same+class+jquery+&aqs=chrome..69i57.59417j0j9&sourceid=chrome&ie=UTF-8
* Sử dụng  CSS :focus Selector trong css:
```css
    .product-group:focus, .sub-group:focus {
        outline: none;
    }
```
* sử dụng jquery để thay đổi các element, css:
  * Tạo ra scroll menu: add thêm class rồi css.
     ```javascript
         $(window).bind('scroll', function () {
                 if ($(window).scrollTop() > 460) {
                     $('header').addClass('fixed');
                     $('button#menu-scroll.navbar-toggle').css('display', 'block');
                     $('header').css('height', '71px');
                 } else {
                     $('header').removeClass('fixed');
                     $('button#menu-scroll.navbar-toggle').css('display', 'none');
                     $('header').css('height', '151px');
                 }

             });
     ```
    * https://stackoverflow.com/questions/13274592/leave-menu-bar-fixed-on-top-when-scrolled
    * https://www.google.com.vn/search?q=scroll+menu&oq=scroll+menu+&aqs=chrome..69i57j0l5.15855j0j7&sourceid=chrome&ie=UTF-8#q=jquery+menu+scroll+100+stackoverflow
  * Khi gặp phải bài toán có sự lặp giữa 2 lựa chọn => sử dụng tính chất hoán vị giữa 2 lựa chọn:
      * Click vào nút thì button thì hiện ra menu, click ngược lại thì ẩn đi:
        * sử dụng if else
          ```javascript
            var click = 'onclicked'
            $(".form-search button").click(function () {
                    if (click === 'onclicked') {
                        $('header').css('height', '151px');
                        $('header .navbar').css('display', 'flex');
                        click = 'clicked again'
                    } else if (click === 'clicked again') {
                        $('header').css('height', '71px');
                        $('header .navbar').css('display', 'none');
                        click = 'onclicked';
                    }
                }
          ```
         * sử dụng switch ... case:
            ```javascript
                var temp = 1
                switch (temp) {
                            case (1): {
                                $('header').css('height', '151px');
                                $('header .navbar').css('display', 'flex');
                                console.log(temp);
                                temp++
                            }
                                break
                            case(2): {
                                $('header').css('height', '71px');
                                $('header .navbar').css('display', 'none');
                                console.log(temp);
                                temp--
                            }
                                break
                            default:
                        }
            ```

* Kiểm tra đã click hay chưa:
   https://stackoverflow.com/questions/6081608/jquery-check-if-it-is-clicked-or-not
   https://stackoverflow.com/questions/15404890/jquery-check-if-button-is-clicked

* Sử dụng ```javascript javascript:void(0) ```
