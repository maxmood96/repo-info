## `perl:devel-slim-threaded`

```console
$ docker pull perl@sha256:cb75240217d3409e59fdc1fb771947d0c87d54eaafe6263249e0a443778999f4
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

### `perl:devel-slim-threaded` - linux; amd64

```console
$ docker pull perl@sha256:cb60177c842e4697b39d8cdf33fc9b721d1cf3a6d9e260fa7571fde2078c60cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57881288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce36abea11a6711bb493a6018408c6658e2a1887f7adfc7410127f6da8332db3`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d416e93462686471e15eac3bd33aee282bede6b53ca4133333917d07835e26`  
		Last Modified: Tue, 13 Feb 2024 02:06:41 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081291de456203eaa16061f623b6f5b54993230e6682155314eb308673efee61`  
		Last Modified: Tue, 13 Feb 2024 02:06:42 GMT  
		Size: 28.8 MB (28756932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b66b5b01b53b59d0fbb0687e945e4c0e297bc079242984ba0adf0cc1530d23`  
		Last Modified: Tue, 13 Feb 2024 02:06:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:97e7238a73efb14167afd31ba48e87e3e4b8135f7fec456ea7f5462d1a7920f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3248640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4cd87d5191ac03cfa56d970d9ab5f791822fef846d55c3af7ab6c9151ee991`

```dockerfile
```

-	Layers:
	-	`sha256:56abdfa4198501bfa7917176069b1e8b2e3200b47c40b85b444cfa66ff55a186`  
		Last Modified: Tue, 13 Feb 2024 02:06:42 GMT  
		Size: 3.2 MB (3231758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6211d2678c26d6fdc4452d0b3938557dd8cfc67fe0af235a38e5cfc203ff91ff`  
		Last Modified: Tue, 13 Feb 2024 02:06:41 GMT  
		Size: 16.9 KB (16882 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:9fdf351615cf221215ae628899489ff6cae1d5128d48b84d0552176507251c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52724619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147035e4929e6fb7471b115feb4ea09994c6f0a9d6b3e09ec1757da8ca931b0c`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98df6fbee44a8813274929f9059286a59af6adaf1c23945a1b0cdb4c26d832b`  
		Last Modified: Tue, 13 Feb 2024 18:53:39 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f036145980157004d17bac0a3fce29b40b76ba8d8839188af08bee018bfc635`  
		Last Modified: Tue, 13 Feb 2024 21:53:52 GMT  
		Size: 25.8 MB (25840451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93725ec55fa9ba81456e709b1043c716e8ee3a873770229f9034f4e36ec1e6ba`  
		Last Modified: Tue, 13 Feb 2024 21:53:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:8ad712c17ae3d6729adc453dc9dfeb8534371b248421a0a4bfe13bcc912b1842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3223274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84f260d4543d105699f29b45145a2d3b4fa35c4dffa78a7d3403ee98d94c80e`

```dockerfile
```

-	Layers:
	-	`sha256:00c175e3a779c833745ae8c332c9e2dc26f3a2e9759c1eea8a9fb2fa7a72f3e5`  
		Last Modified: Tue, 13 Feb 2024 21:53:51 GMT  
		Size: 3.2 MB (3206473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8160e0ef630eb977032baf5c767e461dba10017369ceab46debc433be68a6492`  
		Last Modified: Tue, 13 Feb 2024 21:53:50 GMT  
		Size: 16.8 KB (16801 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:d74dfcbf67c7edf44130083da021be8f527108300f94bea75b7ec0dc1a3c7ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49758425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70de93e684f8045fbac363e2b57c7e1c3b901953f4b82e545d6ffd21ad594bd3`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:7a5e2a926145215a27b5a8051ed294061243135af64539be80d4449e05f71f52`  
		Last Modified: Tue, 13 Feb 2024 01:26:50 GMT  
		Size: 24.7 MB (24716645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d06d24bc58aa34b3d9d3156ce5dbce83f016b0368889f35422c22b16d65c4e`  
		Last Modified: Thu, 15 Feb 2024 04:48:00 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40135b87a772360b6659d5d2236bea80987114ac620bcfde213cf3ebddc913b5`  
		Last Modified: Thu, 15 Feb 2024 19:12:46 GMT  
		Size: 25.0 MB (25041513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fdc09beed4cb7276c3a2dd3e8163834f9c5aff7371ff2ac0901b8e7f18b545`  
		Last Modified: Thu, 15 Feb 2024 19:12:45 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:356b69037d2ce0bafa9f60dda67fc75e8503236c79a8fc3d643bb8856e10595f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3223138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3934495d416e001eaa3e38d90d56c0167ab302c690a3a994f338c6301d88adc5`

```dockerfile
```

-	Layers:
	-	`sha256:cdb0aa738a75b6853856ee929acaadc46ac24d081262082c3bddc4fa65e93bd9`  
		Last Modified: Thu, 15 Feb 2024 19:12:45 GMT  
		Size: 3.2 MB (3206337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45180738272bd41181efdff0ae5f4f8c73bd09c82cb4e61d02f0f7a9c22c9e51`  
		Last Modified: Thu, 15 Feb 2024 19:12:45 GMT  
		Size: 16.8 KB (16801 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:ae484911b946ff3cf34489316eec458b8a1e0b178b0b53b517a517ecb5963977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56696122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d840826db556e9770b32ed6389cde0e0830f6e9938805302a687acc70c5e0f60`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce06e6fe7971d4300bd8297d02d5e4d11e37aff29a5cfff1defe35d995d3cdd7`  
		Last Modified: Wed, 14 Feb 2024 02:05:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfc3f7a7a965b94653fbe5b127e5a9d57ba680806b82bef8aa73840cba64a6d`  
		Last Modified: Wed, 14 Feb 2024 07:24:41 GMT  
		Size: 27.5 MB (27539494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b613255d9d7b6e8f699a22430f1cb05e9d7e50836854ab813088e7560a6866e1`  
		Last Modified: Wed, 14 Feb 2024 07:24:40 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:718c9c617ea5f00d9ede3e6628a2f8ec67cb70e606345c739b943dea6fceb3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3223673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66039384880a6a6d1bb0d26697e82c421416674dd2ef77e8c118650fda93610a`

```dockerfile
```

-	Layers:
	-	`sha256:39c898e639fa0e258ea330383e3f25a9c18534c9d1d4eeb331da3b031bad9061`  
		Last Modified: Wed, 14 Feb 2024 07:24:41 GMT  
		Size: 3.2 MB (3206944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d7e6dd6403745cd8171b5797eb56c7abe1e7ef9aef108882375f2d90868d381`  
		Last Modified: Wed, 14 Feb 2024 07:24:40 GMT  
		Size: 16.7 KB (16729 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; 386

```console
$ docker pull perl@sha256:fafd4f84c19297f7b14309ca777719173ac9bc1b02716a105c0b974e737c93ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57951508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a108dfcc79778bb0b5f74f48826d6eb59b6d3eaf1f6793de20d5cf4ea56c27ef`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c4266192aa9bfa49f9c4ecde7e98b1aca42e399f28ea7442f6a24e44653ad8`  
		Last Modified: Tue, 13 Feb 2024 02:07:20 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f23bfa28a8d2f18fdecd831987966a2d684879f295177b19b3a20c0856eebb`  
		Last Modified: Tue, 13 Feb 2024 02:07:21 GMT  
		Size: 27.8 MB (27809434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b878950b4624c5af1941677da73d266ba998b812fc80e70390701a6f125bf6`  
		Last Modified: Tue, 13 Feb 2024 02:07:20 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:d973812cc56c5ab3fa95c1e70b0340bc9157a5972ca22730158898db921958be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3242918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0340ad600073f602db5e107f3af3c5e34f6738dd5f0ae0d4410d3aa5288ae1`

```dockerfile
```

-	Layers:
	-	`sha256:c67969f15faafbb69e3970c09a9dd29ed348ff5c983d462c133ca998611c46c1`  
		Last Modified: Tue, 13 Feb 2024 02:07:20 GMT  
		Size: 3.2 MB (3226075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67e87030323762e1dd47f5868627d2d59af7614cb516dab593dc3d3d4f773edb`  
		Last Modified: Tue, 13 Feb 2024 02:07:20 GMT  
		Size: 16.8 KB (16843 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; mips64le

```console
$ docker pull perl@sha256:27a5859debc67d75ec0da6b560ef9e8c9e6c99042cec819933cad09085acbad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56040495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3896b833fafe1e0eace921ac97b944a8cc0add41c09e05293d0f01eb3331d9d1`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:7b0bbeed7888e49f58bdffd816596bc88b87bd4a3761c5a2590f3123c077899b in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:78ede1ea2c0b185708583060a40bd2aeddee7b533566b4df729e98e5e5de458b`  
		Last Modified: Tue, 13 Feb 2024 02:15:10 GMT  
		Size: 29.1 MB (29119092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea993ad695e1f5ad0d2f4acc84466547bd9dc5066c93eeca8259e36fe2a2b4f1`  
		Last Modified: Wed, 14 Feb 2024 06:20:43 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868d0dae024f65e4af619be0419bfd9e3f8c8fb0e5bdc4b87b23e2942fe76141`  
		Last Modified: Wed, 14 Feb 2024 17:15:10 GMT  
		Size: 26.9 MB (26921136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c02aa8837385694ecd2e9c2989402e7725a4dc5b9520a8e02f6c6c3705b47`  
		Last Modified: Wed, 14 Feb 2024 17:15:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:36e15037fec2c399cd4958b82ea2943d6797f268a0a4c5b94b5147b47a3d1a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 KB (16575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9629800f81ea2028615bb1840f8d9a93184bba27e41a309225f6c24f7caa27`

```dockerfile
```

-	Layers:
	-	`sha256:38ea2a5ec5c435aff43aecdeb7cb517fb81e4e5b344ce382ac6a1e2ddb377530`  
		Last Modified: Wed, 14 Feb 2024 17:15:07 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:90cd495c3b7b583bd15a434087f096bb00efc22632e86c6e8a1111db4074c6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62472548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61928bb7c833f5efbfacca39d12cc6fab9690e3f591781ac429dc8d7ce932f4a`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4c109e211fd15bf2d626ee178c7d10873a6aa86c952867704f46078db95610`  
		Last Modified: Tue, 13 Feb 2024 22:51:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a94dbf0922b8acda5b293580e795f143292184fed7571f104b4b94a4a97b51`  
		Last Modified: Wed, 14 Feb 2024 03:24:48 GMT  
		Size: 29.4 MB (29353375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f10c9408a23b6454d6783995cddc97022279c12afa9b7044c5bea8fd5cc0ea8`  
		Last Modified: Wed, 14 Feb 2024 03:24:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:85adca726bc24f6bd6726cb4a2ad8901158b4359119fefeb1331b9760f0bbd58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3237087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f52701b0610b5cecfe8e2645db0f4087c386dd0b3b8660ec079a090cd45ea8`

```dockerfile
```

-	Layers:
	-	`sha256:c4fea63a93ed74db2ea486faa916f5553abe00ebba31b0bd6bb6f0c2605e773c`  
		Last Modified: Wed, 14 Feb 2024 03:24:47 GMT  
		Size: 3.2 MB (3220323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e906ba1bf7effdcf6ba3b33614f0bae1e4eb355117ebb27f4033d490b44a1c8b`  
		Last Modified: Wed, 14 Feb 2024 03:24:46 GMT  
		Size: 16.8 KB (16764 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; s390x

```console
$ docker pull perl@sha256:20abaf2d168d2958f67a09ccdb055fbba084bf7fe281379a8eb1b5b818d9e2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54780684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ff6b12c565cf4d142d09248ae54cba78e20c19f82a3c54a639010a62911937`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe4cd4eb0306d8c8639424f378f0080906b98c08e0dd5238af056d92390fd8d`  
		Last Modified: Thu, 15 Feb 2024 06:31:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc7d65441be530e837465defca7ec9c3227bc3654145757c1e59f16ca87d1cc`  
		Last Modified: Thu, 15 Feb 2024 13:29:11 GMT  
		Size: 27.3 MB (27291830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d22841987ea649d63c9fa7f4015247c917a23b0b05f5d349fc28f89ebed2903`  
		Last Modified: Thu, 15 Feb 2024 13:29:11 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:202d2efb98ea6ac8bc18c771fd861c79cbfd3a0dbd8929e1289f3b43dabbc5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3238014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8592858dd3f6710e760d38bcfe8eb38b2021b164698c471eeb6abe7f927018`

```dockerfile
```

-	Layers:
	-	`sha256:860c4c9ab8629c48acce32245c457ba34413abfbe9685701ec2dc4a2df934e9a`  
		Last Modified: Thu, 15 Feb 2024 13:29:11 GMT  
		Size: 3.2 MB (3221300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68e40365b8e57683b566d0ff2041f696d5c8efddc7daab6066b274c7960e8491`  
		Last Modified: Thu, 15 Feb 2024 13:29:11 GMT  
		Size: 16.7 KB (16714 bytes)  
		MIME: application/vnd.in-toto+json
