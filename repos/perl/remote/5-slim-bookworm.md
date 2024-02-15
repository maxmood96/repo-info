## `perl:5-slim-bookworm`

```console
$ docker pull perl@sha256:9f9b34dacee2d7c9ae3f5d03cf74ab5c58258fbc8045beec4e49912734174f91
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

### `perl:5-slim-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:5e704735cb4f5d5d93d22c77b1e5b12b74da5c79d922c2727e1fdc981dbbd233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57610069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a8b61253eb33471cbefdd10f202f08843a4f90c4be24caa7c7043a966b895f`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f354fd9ba63b6da1511ed4a823ebf83d09b83f8b1d28d7105dee70fa5426904`  
		Last Modified: Tue, 13 Feb 2024 02:01:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a199853ff7bc05a700868a261525ae3b62ae70c6f5ed8b1d4eda6fdcf348035c`  
		Last Modified: Tue, 13 Feb 2024 02:01:15 GMT  
		Size: 28.5 MB (28485716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d234cac8e07b49fa684511a1d5c8fbc3fac5002a972d7713fc0c0e0ccfdb85`  
		Last Modified: Tue, 13 Feb 2024 02:01:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:7f4517be9e04a163e6ee4a1c12eb0bb62ce2a0e26f683d8b074125bebddb07fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3250723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e423ba6a8d111435934d621363198afaf60d766a1f3847cc7c1e417fdc9e6140`

```dockerfile
```

-	Layers:
	-	`sha256:4b1079a881a03da27a1d2482793adbad6507e884225e9074e9779a7a396ecbf6`  
		Last Modified: Tue, 13 Feb 2024 02:01:15 GMT  
		Size: 3.2 MB (3232858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:254f8e277fe954214286135ba4a8b7a459abef7b3168b369a868dd60f68609df`  
		Last Modified: Tue, 13 Feb 2024 02:01:15 GMT  
		Size: 17.9 KB (17865 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:318f7a058e4c9671e4dbbc05065edd4df6749572f247134c7b363788e4dcb807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52470421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8085bb2081006ddfe4a464b7f22d4111c603115d4c997683f7ae2e27e5d492`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:78e06c76116ddc9f0115170eed93b59e4b997aa794fd77f9cb938abde9c0c940`  
		Last Modified: Tue, 13 Feb 2024 18:53:40 GMT  
		Size: 25.6 MB (25586253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56aa1fd7c236ce5a58d3fba78aa27826c5f21f66c9857b4e9d4d0de8ee82db3a`  
		Last Modified: Tue, 13 Feb 2024 18:53:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:9007d78c49cf21e77a83ac06455d9d20c0b8b37e2d8bf180a1657d75020f4855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3225421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8108f3aa1ec5711378b7b8707865ee7bf2a9bf65c653adf3e6005e043296bd`

```dockerfile
```

-	Layers:
	-	`sha256:7bf20820345ea83dc26b5ca7fdc1f8f1996592682676029fce1e6c79242c6fae`  
		Last Modified: Tue, 13 Feb 2024 18:53:40 GMT  
		Size: 3.2 MB (3207605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:037c863b4810fb933a66d6c66373007fc7b18c94519d0d2e7bcea12da69fc753`  
		Last Modified: Tue, 13 Feb 2024 18:53:40 GMT  
		Size: 17.8 KB (17816 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:90c7fd9460900ca7e92af391d9d6d313442bce2cb8e4d269a698cda0206d758d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49526200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2dfc8bb1b99ed846447854262e46a82fa1c1722a18ae20ae9602abf0139abb4`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:2e216b573d46d187eadef5092f1199eaedd5fb380b317b2395e5dbfe74a7d760`  
		Last Modified: Thu, 15 Feb 2024 04:48:01 GMT  
		Size: 24.8 MB (24809288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b5f3317faf5514932e8aac3f94bfb8eeda91b05dcf10a4e5ba815e195cba7b`  
		Last Modified: Thu, 15 Feb 2024 04:48:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2572b8db0d3aa5a51099bfab829a44c4f7d771988d579b7ac587cf75d0d2c0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3225285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17bc0fd43f1e59bcd69a8197e7878caca74ac8f91dcbb88247edcdbf71fd85b2`

```dockerfile
```

-	Layers:
	-	`sha256:a1310cff1d8c1680ca094cd223d431656d2070c01b6fbf8b0d51e48beb69bf54`  
		Last Modified: Thu, 15 Feb 2024 04:48:01 GMT  
		Size: 3.2 MB (3207469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03d6113e9fdf8e83e45ae66174f92ba54fd6316c19c3bbae7461ef98be7311e2`  
		Last Modified: Thu, 15 Feb 2024 04:48:00 GMT  
		Size: 17.8 KB (17816 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:396672b190cdbb14ba525fbaddcfcde827c5cf3e8876d269b64886db83fb6b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56436182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed136edeef2827d1de41003a9ef45c85c2bd40fa93b36e41aea7ed0b3f03ec1f`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:20bf7205f3d2733d8087c01bd61e5b1f5a13fc2c76c57fc65938921b46090069`  
		Last Modified: Wed, 14 Feb 2024 02:05:05 GMT  
		Size: 27.3 MB (27279555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3a234ab11198489c3b29bb920f3e8371f98834b987f2bbac9e8f39b7233c0f`  
		Last Modified: Wed, 14 Feb 2024 02:05:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:cb746653c8b49d1db4285303f6d4b12f470f381a308b5275ae28aca9ae617fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3225772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1030b039bea58815a7029269c34e1bc6613cd242bc1afde783f00b94c38d9a98`

```dockerfile
```

-	Layers:
	-	`sha256:cc07ed5ac80182938fd565844cda411a61592165f5c8a650681bd1c7641a2025`  
		Last Modified: Wed, 14 Feb 2024 02:05:03 GMT  
		Size: 3.2 MB (3208052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0209d349556c30c7ff5a5e3ff0a1c1be8434f3bafd6feb9852dffba4a5f7883`  
		Last Modified: Wed, 14 Feb 2024 02:05:03 GMT  
		Size: 17.7 KB (17720 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; 386

```console
$ docker pull perl@sha256:a3126114c90b27a43770328208160aeb832f42bef2e79d477db520031a931e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57624437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca7a65bd4fb69e974f0f1516a0147b623cb92a92960cf081368b758a69de9a5`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d300f88c047987664b072f9de571796cb6f95e411c95700636180abc853e6e73`  
		Last Modified: Tue, 13 Feb 2024 02:00:51 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdfc9e4bb4f5c1a38dbac278a5b7d539f3408a4ec7da8c7cac6d10577066e7c`  
		Last Modified: Tue, 13 Feb 2024 02:02:08 GMT  
		Size: 27.5 MB (27482364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8aa8890fb33a93057f17937531c75e8ff20d25ce242bb50a627170f1f2cc0c`  
		Last Modified: Tue, 13 Feb 2024 02:02:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:5ad7789ebaa864586f1a06125c20e96d6235e789e9de37bab78c46af09498a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3244961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ab9442608c793802578946a0d27565f19b889fac9b93c9cc7417186b8d3130`

```dockerfile
```

-	Layers:
	-	`sha256:6d09337e017ac0011670f833db6c1df45c7a5f644dfa16ffdbdd92bbd8f0ccda`  
		Last Modified: Tue, 13 Feb 2024 02:02:07 GMT  
		Size: 3.2 MB (3227155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7390725209fa44dd62577a239179871cf9f3443fe9d711d68c3d6d5f3a89d35`  
		Last Modified: Tue, 13 Feb 2024 02:02:08 GMT  
		Size: 17.8 KB (17806 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:5847d33f56c08be16ea4311c129ab4d0e4bd4b34f222e690e3bc10d453e6b708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55766293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6c90e0793be76cfec3e2a13aa0cba6d306022bbbc18e392ceeca6ba6e2d35b`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:7b0bbeed7888e49f58bdffd816596bc88b87bd4a3761c5a2590f3123c077899b in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:586069f41d9459e06bcb8909b974014d9cac6b006197620ff58141f9c803d3d7`  
		Last Modified: Wed, 14 Feb 2024 06:20:46 GMT  
		Size: 26.6 MB (26646934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8217431f6c85d54e3a68ef463903775f01d7d63cd393f38f9bc84f14300086af`  
		Last Modified: Wed, 14 Feb 2024 06:20:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:ab9d502533b5cd807b6ef7d333cf769f0d65d0ed845c63bcbdc2ec9f901ce1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1559fff671fe3a7df3619c5b71889f7c77396102d94e1e941d568d51341fed95`

```dockerfile
```

-	Layers:
	-	`sha256:f8feeac450cfa455a318ed70716a7c35b4df3c633818f2c1b41c71fac1605e65`  
		Last Modified: Wed, 14 Feb 2024 06:20:43 GMT  
		Size: 17.6 KB (17594 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:cda600f2ddb37c89768d420f6c533fa7404f170e7b68be2ce6ffc6336387092e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62168201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0915f37a6a18560257d5be19dc01cd88a28fb4bb7a807fc293c40c53675e6d2c`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:9e57f3ec92ead8ae93d07d15736239df0e3c33909d67202c86a40da4c7db3aac`  
		Last Modified: Tue, 13 Feb 2024 22:51:15 GMT  
		Size: 29.0 MB (29049028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cca45bd34e75da98d4a6d27152e06dde44bb525d93cf813df6c0bb3c597cad`  
		Last Modified: Tue, 13 Feb 2024 22:51:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:da2419727443910c79afa61270f2e4b8e3adae36a5546a024c8253ab375a8c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3239219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370c5d1c4c340bcfc6a0e61e9a1c3798c37fbe935dfb88d0faac743b64838ccd`

```dockerfile
```

-	Layers:
	-	`sha256:9907b0314a38a72d680d96cab9e42a67594b4f76758dd079e5e3536933025aac`  
		Last Modified: Tue, 13 Feb 2024 22:51:14 GMT  
		Size: 3.2 MB (3221447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e85d5ec1d8e44d3da6dfa32c6afa33039537424058a9ee98b189c2eeb03f132`  
		Last Modified: Tue, 13 Feb 2024 22:51:13 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:c47b1ecdaaa6f1aad1b3f215356755d44ebf0e62354596ce45e5cf6a295caadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54518776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653d5f298973ab477976df80582d83e14682871e70701dd5e09a61688bf968da`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:6b553a460da397b3531cf77f96a4a4887fddc1af210716c22a58dbb876639493`  
		Last Modified: Thu, 15 Feb 2024 06:31:12 GMT  
		Size: 27.0 MB (27029922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb719fdd32f516c12df758410f7ef57c6f541bc0ab7ca399cd8c140f23a037c`  
		Last Modified: Thu, 15 Feb 2024 06:31:11 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:20322ab70dd9aa1a3c12ccf4f6c3882fa641461b913faac5531b67288df6c3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3240098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fb5e0a2e86ac3643f87cb00e10908393fa8e3af2bec522bfc53226f2c3d2e3`

```dockerfile
```

-	Layers:
	-	`sha256:3b96f6826184dd6440fa3cde5920ff9554471b2c1634e18e9d9544951b526f31`  
		Last Modified: Thu, 15 Feb 2024 06:31:11 GMT  
		Size: 3.2 MB (3222400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce19d9868c0a8883020444133066719bc37d76950f24e88980efb6d5fccb4f2f`  
		Last Modified: Thu, 15 Feb 2024 06:31:11 GMT  
		Size: 17.7 KB (17698 bytes)  
		MIME: application/vnd.in-toto+json
