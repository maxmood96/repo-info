## `perl:5-slim`

```console
$ docker pull perl@sha256:78fa2213768daa6e432ec4e07f832a2968614b0511a671046cd29a685bd6cdd2
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

### `perl:5-slim` - linux; amd64

```console
$ docker pull perl@sha256:9cf7df62e70b10b3a840992587152f06126e00f1c14d54a86b245b0ba2942bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57447607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382982be9a78901432cca0841ec90ea906828e6348cc17bb1367714cfc5f0f8c`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:e7d85e6c641c82a190457a1011f5a59d84b9acbebe5f4519252fee095849eb30`  
		Last Modified: Tue, 14 May 2024 03:03:34 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678398aceb0dac676b1a26fa8805073dd230492d8042842e055a17135e58deb`  
		Last Modified: Tue, 14 May 2024 03:03:34 GMT  
		Size: 28.3 MB (28296931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6de1a27ef21620bae90a256c3f53c2edf262d602154699122d540919c858c7f`  
		Last Modified: Tue, 14 May 2024 03:03:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:13a8411013048dfb61aea812584bbc8a6d7d1e8b13fb4f1408237fb1795b0848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4626bc90dfae162618de5145ed3382d66e054943f5135f93e4bd674884e0b521`

```dockerfile
```

-	Layers:
	-	`sha256:2d9c752d2768fbf1e7db34d1c0625fc9b1c53769eac03a288805c70a3fc0f220`  
		Last Modified: Tue, 14 May 2024 03:03:34 GMT  
		Size: 3.7 MB (3720454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a15f9e1454fdd9faa7a4092f76030940b0ef2a38cb744b7c6fa7a04add00b2`  
		Last Modified: Tue, 14 May 2024 03:03:34 GMT  
		Size: 17.9 KB (17868 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:8920acaa10bcbfba18c2fb753d95913ac96550b6777325be00ea34f9604280f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52618676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f62f0b9b40a37fdef74d12a8868bd1ecc16d92666bf4bbf86d1ec43bcf566c`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:2340232946e78c042e7eb7357bf8e9477d676282991f12fac0c8e91babe40837`  
		Last Modified: Mon, 10 Jun 2024 21:24:01 GMT  
		Size: 25.7 MB (25708487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7a62a95560976bde5d4bcdb40e0ed53574daef21a64de15ca8b9373b98dfd8`  
		Last Modified: Mon, 10 Jun 2024 21:24:00 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:b5249b7008f4e22bbfb6a1b5673ab1a94715fedcc3c5a1a78869488934d50952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3708616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e0250b3ec9915bba1f9d93f88d5506c30d22648d0e5b1dc94465a410e7ff09`

```dockerfile
```

-	Layers:
	-	`sha256:2db1f855600fface06e8815da112193f49276e0a15cb6c014bdd67f39a5149fb`  
		Last Modified: Mon, 10 Jun 2024 21:24:00 GMT  
		Size: 3.7 MB (3690748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b06424f921a9298a3f20884d39abfedcd879b47a7d9e272bde2b4aa28a75df`  
		Last Modified: Mon, 10 Jun 2024 21:23:59 GMT  
		Size: 17.9 KB (17868 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:8b0ddcae290f5f9deb152a344001e80332d884bae9a6aba8fc58ec8b3933ec53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49660731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da9013aebc27e8676ccbd24c1c7865f6ca573087181486accf8144a522d35e9`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:5b4a81aa71d5866a6d593b68dde3ddc85f63c2834279b9c64f68ac14cdf0c99d`  
		Last Modified: Mon, 10 Jun 2024 21:22:49 GMT  
		Size: 24.9 MB (24920258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5248d83f8802619722d30ebf5a4d60af00ee3ac099b3ebb49cc70888d05eaecc`  
		Last Modified: Mon, 10 Jun 2024 21:22:48 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:d4e16b5e4004dec3d6c57f1492c6785df7de54faad0f23dfa0e30c9baff8df8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3708373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec42e4f107cd1b5401228fabc45ff160ddfd69c8c97281ee3399860032517676`

```dockerfile
```

-	Layers:
	-	`sha256:c38a9b78afdf2261f8df69b1c5ac56842e6b78256c59015053c34e6e7804c084`  
		Last Modified: Mon, 10 Jun 2024 21:22:48 GMT  
		Size: 3.7 MB (3690506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:929f84aa483095c9cd03ce75802e8b74fc28a39bb4bd0dc0b0b0887248cf4dc1`  
		Last Modified: Mon, 10 Jun 2024 21:22:48 GMT  
		Size: 17.9 KB (17867 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:0ed90cfefb2c702a077849cc2fac31bab2f1cd68823c4a3aec30cf9fcfb5aa85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56273066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8fd0106697a4e93bafa5993ad473f53b8318d741f74165478d2f84fd7a7ca7`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:28520dda232dbeda47383d6615aa1572fb0e88df370255d2d2d016e41dc10fd7`  
		Last Modified: Tue, 14 May 2024 18:19:16 GMT  
		Size: 27.1 MB (27093300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac305d32b50e6ae9de71677dd10a6991001295aaac17ec254861359155e00ad`  
		Last Modified: Tue, 14 May 2024 18:19:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:8680df0d9baa1b77ee6a1c4024f9aea39c7389310d05a4f55db80ce0c56338da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1418f04df44fd280d89a80ad4c10d71e2e2a254d18aa19786619fa7d76ffc67b`

```dockerfile
```

-	Layers:
	-	`sha256:ae12c098bfaf32c92c4ba04b4e9634bfc12d3829c2bd2880fdeffde937f53a6d`  
		Last Modified: Tue, 14 May 2024 18:19:15 GMT  
		Size: 3.7 MB (3691620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce76e5abbe00c808e4cd109a97e61c570b8051b7106e67085b99b9a7db0da513`  
		Last Modified: Tue, 14 May 2024 18:19:14 GMT  
		Size: 17.7 KB (17724 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; 386

```console
$ docker pull perl@sha256:434a3e472eab38cc519733bf4e3d5ad1d690e9965bdddfed8b2fe050dcbc6aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57756346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595b951c990c41417bcb14ebfa6449e7985295e496065b17f5d6ff5a039cdc1d`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:2b330048a73f1a3d76faa826937cdb777aed77ac42693f620794d297765daf48`  
		Last Modified: Mon, 10 Jun 2024 21:03:03 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024091cd128daa9388d3c78dafc7c3c93a73480108da2772c1f94318372a7980`  
		Last Modified: Mon, 10 Jun 2024 21:04:04 GMT  
		Size: 27.6 MB (27593440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6bd9a763869614a2ac20b554beaa232da8876b6f29eccdb07ef1496a68e9bd`  
		Last Modified: Mon, 10 Jun 2024 21:04:03 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:40f9ded9c8fba036241529fe8a4fc3f7edb331539afa9666309a700abfc303f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c4658b88d93f9b0872af882efc383f38eecdb3dd3f33b509adfb62d5963a05`

```dockerfile
```

-	Layers:
	-	`sha256:19b76b70dd488805e3826c2589a2120ce8bad91f92eb77cb14c329d1b50c3a07`  
		Last Modified: Mon, 10 Jun 2024 21:04:04 GMT  
		Size: 3.7 MB (3714326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f7e7b74297b8dea0a61060b1bda11465a1ffaa442439e8ab9ae1c49165b13a`  
		Last Modified: Mon, 10 Jun 2024 21:04:03 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; mips64le

```console
$ docker pull perl@sha256:470e7a11eab77f8fbf94d28f14c811484e5e0171ab811ea0c0aea348deb9b98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55602371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3108da5d98bf2a07e20afaa1754b7fca4d18d15c964597f02cab74195b60585f`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:e53ccd24d1ec04162f3ebaedffe2e4f20a2e4e0e65461ada289a2ccd0245666a`  
		Last Modified: Tue, 14 May 2024 23:00:08 GMT  
		Size: 26.5 MB (26458416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fbbe8f907518f3116e6fc5be8ad8cd4dce11f4d58d6bff3cb510d45a245af0`  
		Last Modified: Tue, 14 May 2024 23:00:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:54a35f024784c69e09fd1c6435d2f1d0b301f937bd4b942dcaf96878761b0768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93ba2052c602dc678bc72ccfeab11af28ebafbc2d938ffbe89d2a468b9a852b`

```dockerfile
```

-	Layers:
	-	`sha256:018bfdb7c63e22db7e887d1b4f61f09bb0afbf056c3f60e950a859712ce0b744`  
		Last Modified: Tue, 14 May 2024 23:00:05 GMT  
		Size: 17.6 KB (17594 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; ppc64le

```console
$ docker pull perl@sha256:af84c2faba2e1bda161aa764a39817c1be77e423b1ddf49f03e48b2906dc20c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62298398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2652d3fb2e8a1fcd5dc9afbb8b61dedae30c701ec6f38e0ce4777abaf083809e`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:4434e7973260b4d43df4a07347535e2734ac699b270c3bfda5e0a2bd357e6606`  
		Last Modified: Mon, 10 Jun 2024 21:16:47 GMT  
		Size: 29.2 MB (29156972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f4f6f40fc8c27970f568c41607021aa355b65a872e6f9f236dd2573e8c5a68`  
		Last Modified: Mon, 10 Jun 2024 21:16:46 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:c52d8ef050b7a35f35a39eb072e5a8917d6ec31562990158da1605c135a7f1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08507f2421b17b0a668837218967b685455de76aab47651356c3c70711c19b7`

```dockerfile
```

-	Layers:
	-	`sha256:ff9e0b76a42997bb8d8f230ef47ae520a71826d266ffc103fa3cc341f40acd59`  
		Last Modified: Mon, 10 Jun 2024 21:16:46 GMT  
		Size: 3.7 MB (3706180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7cb451a7c07c1ed8fc3396fc10741dfb3f00fe80844161013440acd90e05d4e`  
		Last Modified: Mon, 10 Jun 2024 21:16:46 GMT  
		Size: 17.8 KB (17824 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; s390x

```console
$ docker pull perl@sha256:2c2868ae0b502fbf73b7d8f59c14b092d6b96662e3d12a635bca988c831664e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54659462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c58724f845e0a42a9f03dc1937618c5916ed4a971cc42de67f0d7360d752fc5`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:7dc7d6bf7453f42d9d043340d920ad98a6edfa6c3a056ec7ad7d5ab40e05622d`  
		Last Modified: Mon, 10 Jun 2024 21:25:42 GMT  
		Size: 27.1 MB (27146797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60706afa8db1fae323de3727586f1d37b2f4d3171249d0ebe7756f6605b280ee`  
		Last Modified: Mon, 10 Jun 2024 21:25:41 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:cc21b24c8d4d913cd2bfdf99fb9b907409d24352bc2576702b89289beb156379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d94dd34d253231da47a839408fb48d671cd9f00bc9723b1c6d6a93ebd3fdc8`

```dockerfile
```

-	Layers:
	-	`sha256:7e929453c1f97413ace3e147907a848119fae038ec89c7ef7a409e876b3c7ea4`  
		Last Modified: Mon, 10 Jun 2024 21:25:41 GMT  
		Size: 3.7 MB (3708723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea3c509efa1f988e922fa3ed9569aa198f48cdd674ec6290fd92cbd56c1e91df`  
		Last Modified: Mon, 10 Jun 2024 21:25:41 GMT  
		Size: 17.8 KB (17750 bytes)  
		MIME: application/vnd.in-toto+json
