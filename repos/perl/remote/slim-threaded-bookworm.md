## `perl:slim-threaded-bookworm`

```console
$ docker pull perl@sha256:131fee52e511ab431249fb3dc91e5e78a52a722e54857a0fe871834c33a912d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `perl:slim-threaded-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:d7c2abdb676f3158a03fe7186c773af321712fc81038a94cfdfffd3c0d0a1241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57503547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e4e6aa94bb02d5ec1dc39f563e0435dad7b53e38e22677cda5e62aad675246`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc31ac81663f7b7afd520b5ecb7aefa76f75da4b8afc2df1123eb5d1f72d1e4`  
		Last Modified: Tue, 14 May 2024 03:04:38 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039ee0253ce61d4bffb7029513992fa905374046fa9d7b46ccb1d8e9bc2d3dd9`  
		Last Modified: Tue, 14 May 2024 03:04:38 GMT  
		Size: 28.4 MB (28352871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12f9cb178b0ccbe986413f98ab5fa9be49352e5ef3e02fcfbc4c251cf756c0`  
		Last Modified: Tue, 14 May 2024 03:04:38 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:ae755afb33e99c07238fea97f83b14c6d4b597e2bf655b2c3bb316d3367791ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aaba611601e9aa186c0a0ea972418f98eb16d4e5f53b7de02f0588c002fc2a8`

```dockerfile
```

-	Layers:
	-	`sha256:5308f07a594d50d08c9203e0d8dec76decc29984887ceffd40cffd0e1d9b576c`  
		Last Modified: Tue, 14 May 2024 03:04:38 GMT  
		Size: 3.7 MB (3720634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ae879d0edf4d3dfaa137385472709e2ec9c3d6189eb63f97e215299613f3cbf`  
		Last Modified: Tue, 14 May 2024 03:04:38 GMT  
		Size: 18.1 KB (18096 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:4d089bf3ac46d2e2ad36b59a94cda4e9363779c2c82b03c0972b7fe0d38fe0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52643681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b8dcb683ccd0323d0d4ac6a3e941e2e54775c011fde9968a304da97c8452af`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1926652acea8fe80008535c9ebd1e47df0d546dce6e2c93afebcab0822019221`  
		Last Modified: Mon, 10 Jun 2024 21:24:00 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d5b11410d3abbe15b46e4d8a4428ddcdf2054e122a01f00962d5e194c5b165`  
		Last Modified: Mon, 10 Jun 2024 21:53:17 GMT  
		Size: 25.7 MB (25733492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb25723a54188f3088ef2d2139269f35421021242bb77dff9c7fa30d8e49ed44`  
		Last Modified: Mon, 10 Jun 2024 21:53:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:faa7571fcc25bf316ed8197e0e7c2d36b2c278f454922bb6d6c8e1261d2bd544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae3ed9b41a6833ef5ad589196cda76242603691fea172389ee5df8b41597d15`

```dockerfile
```

-	Layers:
	-	`sha256:c6074e46affe244f18f3d6abc788ac9e6b4ef736fbe3a7c6417c7df17b04a8bc`  
		Last Modified: Mon, 10 Jun 2024 21:53:16 GMT  
		Size: 3.7 MB (3690928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57629da39aa1dd7ba3bdf667d7ca02af0593383c9615bb51499a5e6bcc280db`  
		Last Modified: Mon, 10 Jun 2024 21:53:16 GMT  
		Size: 18.1 KB (18095 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:3547fa10e25be5f39cc7fbbf5556302f0065b285d1e1c67dc3ef6271eb0fa55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49686060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802592455990dfa4e00ffd5e8267f6f6b194e376dae664dcaa1fe92bff6717bd`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f16d34ffad4fba8abfddb20dc48754ec8865fbe493cb2f59ffcc0adb2c7aabb`  
		Last Modified: Mon, 10 Jun 2024 21:22:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8898a6f5adc8ad52df7bde81d73cdc8dbc2f8905fd0dbdabc454675e639df51`  
		Last Modified: Mon, 10 Jun 2024 22:04:38 GMT  
		Size: 24.9 MB (24945588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545bbc2c3b1e754ecffc54c15afe926f708c1acec93fc9d12bc85e0c2dfcc687`  
		Last Modified: Mon, 10 Jun 2024 22:04:36 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:fb29f3884ec13bd6480dc04c72cf709bac008ad5013a161a9949c8f5b3fca84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3708781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6614c4c18e9f5dea70651f9389a39600f7bbe0f14cff99de31d2253f1e50ae`

```dockerfile
```

-	Layers:
	-	`sha256:1cd309fafb5b4827960104fa3577533aed1feffddd0d0f5edc975dd5fd6d3079`  
		Last Modified: Mon, 10 Jun 2024 22:04:37 GMT  
		Size: 3.7 MB (3690686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c72edbcd0f1a00efc3b15b33abcd88610026d1f1c0dc56fb0a8a8e8c533c41bc`  
		Last Modified: Mon, 10 Jun 2024 22:04:36 GMT  
		Size: 18.1 KB (18095 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:c1ac3a949bc81c763b3e5635db4393bd1230d0bec9044c6a2b7b3678c231bff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56316186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc00588ff9e4b88b0c53ef7d58db5554ac69ce22aada90c872c5f70e866b4d9a`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b25813b847d8069cde0d8793f64218d5606dbd0973a1cefa64632f24e7c988`  
		Last Modified: Tue, 14 May 2024 18:19:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d40af95b7f585c9b715bf443bdc1aec402ecbdd48356f8d93c742e799cfd135`  
		Last Modified: Tue, 14 May 2024 18:35:19 GMT  
		Size: 27.1 MB (27136420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b2185d8c098cbbb4945f8ed3f6987e13c5b4025fc231ec23b0dff7d341853a`  
		Last Modified: Tue, 14 May 2024 18:35:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:5b3bf2dd397e8ca6bbdcda53f41a77617d6c6ab590c564f1bcb58f6a6651f853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c287f7767c37d148bafdaf3649788fc2dc82deb33459aa420209a583f431c859`

```dockerfile
```

-	Layers:
	-	`sha256:46262372d77ea2afc2629ae663dbabbadfe0e8bcb0cb45bd950fb42cc97d4b44`  
		Last Modified: Tue, 14 May 2024 18:35:18 GMT  
		Size: 3.7 MB (3691800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e5f27fc72b1c01b62bbc5a9cfe739527898e31c8b6285d969ecc9f90eeab8c`  
		Last Modified: Tue, 14 May 2024 18:35:18 GMT  
		Size: 18.0 KB (17951 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:171ed6ff0be6863862e6d5872ce3939db46b9de40a45105f86c93123eba878e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57865562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f854ae839f42ab1ef9ee2063134c969930299659570b87abd77aab30efc59347`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73403137d5ad1600755898b6992342647deb8e5e8fe8eebbe484b05a897d6a6a`  
		Last Modified: Mon, 10 Jun 2024 21:03:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050782db89ae8f70e446e270caf516e8325511ab9472e627750dd19adf8baef0`  
		Last Modified: Mon, 10 Jun 2024 21:05:18 GMT  
		Size: 27.7 MB (27702656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303c9a4ad16f8e3a6e0f4fbd3442f9063695e8aaa93145ecffccfa70f29c86bc`  
		Last Modified: Mon, 10 Jun 2024 21:05:17 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:b043a0080c768f00ff59af4433bba520a3e44899e03b45c5ab3177c3c8be846a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8a571d1f96b7c04967973f2c134d98eafa54e64315e48bd5a13a0d8bef1854`

```dockerfile
```

-	Layers:
	-	`sha256:f131b6bf767ea70db3a936f22b0d2cb4a747a35541c1829737ca20cc0ab592a1`  
		Last Modified: Mon, 10 Jun 2024 21:05:17 GMT  
		Size: 3.7 MB (3714506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25be51f6e607a38187f8c24bdf751ad3e39e2726748c52ed44c5dfd52a2baca`  
		Last Modified: Mon, 10 Jun 2024 21:05:17 GMT  
		Size: 17.9 KB (17918 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:a467d04cf308dddb5dd6db05e333364c313f547f24ef1656504643e1a9525d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55657646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4decbe71edd755a665012fd66f95260cc6adf79ff596629f69106f8087a81055`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a435867010d15f84cd8b8957e96e620a25c5ce1b07cfe581559c04bd2ef9e86`  
		Last Modified: Tue, 14 May 2024 23:00:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff91e005178d6e2d407ba16197d35945a21ad72e5fa07bc08cd33eea24bd2b10`  
		Last Modified: Tue, 14 May 2024 23:54:50 GMT  
		Size: 26.5 MB (26513692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd30df70e684917e8e21154ad12568ef77b1915e6a8e10defea4c6808dce209`  
		Last Modified: Tue, 14 May 2024 23:54:47 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:6731ee335ecc17d5f6fe9196e14cdfe46437c64ac7d533d5b345d38a16055960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 KB (17821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3264d6e302c4e17b332bf04813e27c0e94d52812593f3ea05a4af31467e0f42c`

```dockerfile
```

-	Layers:
	-	`sha256:3177d229cffcd6cc62cbb7911a7822c3cc456f8aff99ec066c20ababfbaaa81a`  
		Last Modified: Tue, 14 May 2024 23:54:47 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:9b221cb5ddcd0fd1a3eeeb50fff8996179448a2a64e6d4f66e439c258f06f174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62388636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5508b8f27673e75cfa50b06fe8ce9187dfc2510e34c51200a5d0346097a86257`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ff8df256974417a0d39f7365cd1284542d5bf2c3f3385a7b3a7e084857ab4c`  
		Last Modified: Mon, 10 Jun 2024 21:16:45 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011e638074277df43cfe9c85ca69fdb8ef1e12b6b2225f73798006bbeda743de`  
		Last Modified: Mon, 10 Jun 2024 21:43:58 GMT  
		Size: 29.2 MB (29247210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc811d487294ff77379dbdd3367bcfdf25808ab2b63441b97c29bcf614c6d669`  
		Last Modified: Mon, 10 Jun 2024 21:43:57 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:42ba5fab9b9e6a10f34ca366d189824e32a0799e08d6fe035bcc19aa69936a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22caf232ab64e4016f1033d2356f402c85121b5c258ffb26a7abe6bbcfa9267b`

```dockerfile
```

-	Layers:
	-	`sha256:7f6623a2e95dd5ebffd1a6306b7e83c29dfcaf16aa3b84d00764825a5ce48d12`  
		Last Modified: Mon, 10 Jun 2024 21:43:57 GMT  
		Size: 3.7 MB (3706360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa05c7440b46b2d47cb3031b70d1dc643a2cf8fbeb1cc1860df63a34630c35a`  
		Last Modified: Mon, 10 Jun 2024 21:43:57 GMT  
		Size: 18.1 KB (18051 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:0724bf9fe2a0c9e4b72f8266d0ecf436761db84e58eb3e4c3d746e8203a49182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54701938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff48826d1dc5e839c76848f7b10e89aae1a1b351bee3620fafa0400740173269`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c76854954dfb8f363230b4322ad5f1044a004d5ffa7e1b4cd95d97ef8a86241`  
		Last Modified: Mon, 10 Jun 2024 21:25:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748b6642f4f0808663596248a3611d039658a28b385c9c15f0dfbdc060baf78e`  
		Last Modified: Mon, 10 Jun 2024 21:59:12 GMT  
		Size: 27.2 MB (27189273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44563432009e2adab8d84f72434ac2dd46493e83c7c974c0d55e8e4be1b3b84`  
		Last Modified: Mon, 10 Jun 2024 21:59:11 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:be9486ebfc7a0893bc7fad1754ee131c7a3e40ed3d8e7d04de961a1e32d07d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d9d49750f901de5e2e473a53c325d1188f8c1ffdc15fb043220d69357097d2`

```dockerfile
```

-	Layers:
	-	`sha256:df92612b23cb32c9f0a0a2b145e55e432ff1f9a184d69f71496d916e57a6f150`  
		Last Modified: Mon, 10 Jun 2024 21:59:11 GMT  
		Size: 3.7 MB (3708903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8186d925283aed536d49d01094360e359f3b8df8b2b9868d473fa7ed99b99ab0`  
		Last Modified: Mon, 10 Jun 2024 21:59:11 GMT  
		Size: 18.0 KB (17977 bytes)  
		MIME: application/vnd.in-toto+json
