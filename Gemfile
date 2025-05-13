source "https://rubygems.org"

# Jekyll 버전 지정
gem "jekyll", "~> 4.3.0"

# 기본 테마 (필요에 따라 변경 가능)
gem "minima", "~> 2.5"

# 플러그인
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-seo-tag", "~> 2.8"
end

# Windows와 JRuby는 이벤트 머신을 위한 특별한 gem이 필요함
# event-machine이 사용되는 경우에만 필요
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# 성능 향상 (http://www.rubydoc.info/gems/wdm/0.1.1)
# Windows에서만 필요
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# LockFile에서 상대 경로 사용
gem "webrick", "~> 1.8"
