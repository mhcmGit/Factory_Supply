<!-- markdownlint-disable-next-line -->
<div align="center">

  <!-- markdownlint-disable-next-line -->
  # Factory Supply

  Trang tin chia sẻ kinh nghiệm, thông tin, kiến thức về logistics và cung ứng vật tư cho nhà máy.

  [![GitHub license][badge-license]][license]&nbsp;
  [![Gem Version][badge-gem]][gem]&nbsp;
  [![Build & Deploy][badge-pages]][pages]

  [![Devices Mockup](https://chirpy-img.netlify.app/commons/devices-mockup.png)][demo]

</div>

## Giới Thiệu

**Factory Supply** là một nền tảng chia sẻ chuyên sâu về lĩnh vực:

- 🚚 **Logistics & Vận chuyển**: Chiến lược vận chuyển, tối ưu lộ trình giao hàng.
- 📦 **Quản lý tồn kho**: Phương pháp 5S, ABC Analysis, tối ưu chi phí kho.
- 🛒 **Mua sắm & Cung ứng**: Xây dựng kế hoạch mua sắm, đánh giá nhà cung cấp.
- 🏭 **Cung ứng vật tư nhà máy**: Hệ thống cấp 4 cấp, quản lý nguyên liệu.

Trang được xây dựng trên nền tảng **Chirpy Jekyll Theme** — một theme Jekyll hiện đại, đáp ứng yêu cầu responsive, hỗ trợ tiếng Việt.

## Cài Đặt & Chạy Local

### Yêu cầu

- Ruby >= 3.1
- Node.js >= 18

### Các bước

1. Cài đặt dependencies:

   ```bash
   bundle install
   npm install
   ```

2. Build assets (CSS & JS):

   ```bash
   npm run build
   ```

3. Chạy server phát triển:

   ```bash
   bundle exec jekyll serve --livereload
   ```

   Truy cập [http://localhost:4000](http://localhost:4000) để xem trang.

## Đóng Góp

Bạn muốn chia sẻ kinh nghiệm hoặc bài viết mới? Vui lòng:

1. Fork repo này
2. Tạo nhánh mới: `git checkout -b feature/ten-bai-viet`
3. Thêm bài viết vào thư mục `_posts/`
4. Commit và đẩy lên nhánh
5. Tạo Pull Request

## License

This project is licensed under the [MIT License][license].

[badge-license]: https://img.shields.io/github/license/factosupply/FactoSupply?color=goldenrod
[badge-gem]: https://img.shields.io/gem/v/jekyll-theme-chirpy?&logo=RubyGems&logoColor=ghostwhite&label=gem&color=orange
[badge-pages]: https://img.shields.io/github/actions/workflow/status/factosupply/FactoSupply/pages-deploy.yml?logo=github
[license]: https://github.com/factosupply/FactoSupply/blob/main/LICENSE
[gem]: https://rubygems.org/gems/jekyll-theme-chirpy
[pages]: https://factosupply.github.io/FactoSupply/
[demo]: https://factosupply.github.io/FactoSupply/
