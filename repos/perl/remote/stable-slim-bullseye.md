## `perl:stable-slim-bullseye`

```console
$ docker pull perl@sha256:19614362b1e78e06dadb5ff473c31770dac6ecd4894bc24c2bd256a4f2b850cd
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

### `perl:stable-slim-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:6ad4059adbd42bdcbda936caffa4a01ff46e67f6f034363eb6be0e454a016206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55800362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec79b54f03bb391cd4d678a1d4de5647a25a515dd72717c9e54254a668eb1e4`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc69cf4e72328fec9b62e4602f055e2ceda65ede9170b869c64badb4d2ed5892`  
		Last Modified: Tue, 14 May 2024 03:03:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4e95639e41a91d2d4c77e7317e7890d8dccce09b72b8f740b21c40018972ff`  
		Last Modified: Tue, 14 May 2024 03:03:14 GMT  
		Size: 24.4 MB (24366166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce14971246aa907c1ea77bb90e53742902f292ce50842390ffb296bb34045cb`  
		Last Modified: Tue, 14 May 2024 03:03:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:aff20cd6a8b46bd43cecbed2bfcf41c6488430f5b8b8ffdc2e1ce2277bc54a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3807a19a8508f5f1019b1650a46ebd1976844af54133b487776619cb81c3da20`

```dockerfile
```

-	Layers:
	-	`sha256:fcfb5957024cf8602dfa74792a20c4b0be6b6a9ee653b06a9cf6c2a750fede48`  
		Last Modified: Tue, 14 May 2024 03:03:13 GMT  
		Size: 3.9 MB (3912927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a7e5047b77812b692e9df8d2589448c3bf92636e9883dfd6c2d8b4e2c327d65`  
		Last Modified: Tue, 14 May 2024 03:03:13 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:8b2a97269c81e2bd15909ec3cff63a2ef8b331c5cf6663b839450c59f6ae5fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51322654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259ce29759733e91b038761406e49be9390c1205e4eb8d25bdc4516f81340b4f`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:7a63cf2b5d16adf102fbd2452be219224667c4ea55981247f398a4a867ef96c4 in / 
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
	-	`sha256:b6ea79e472ea80a508a2732ddeb0e19de51d3f0aaf8f0fd18c1cdd1c939d49de`  
		Last Modified: Tue, 14 May 2024 00:52:17 GMT  
		Size: 28.9 MB (28936721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbf414fcd8900093206ca0291e019fac973a1e907b2800308b58cc0d32a1eeb`  
		Last Modified: Tue, 14 May 2024 15:31:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c106ed62c520e63aefbec665b756e9a60ee7bcc2cf83738f039e0d1dc689ce`  
		Last Modified: Tue, 14 May 2024 15:31:11 GMT  
		Size: 22.4 MB (22385668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d5dc5bd5d40b92772ac3aa0468aef15fddaddd85a2a8560dbeaee7b0350928`  
		Last Modified: Tue, 14 May 2024 15:31:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:51b01e995818742205dc7950d56154fc49a77b8843621acb9944fdb69e20d305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3900428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18d2bb931dc1dca7634cd2fcf3dbb2c28c4600d23877c1289daf77220342122`

```dockerfile
```

-	Layers:
	-	`sha256:d30230fd7d8a66cf465fb360fb7d2d556dcf3126a9169c28daaa4e1f19f06909`  
		Last Modified: Tue, 14 May 2024 15:31:10 GMT  
		Size: 3.9 MB (3884140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7b4c61b8b419d603b0c9704993a567a3988726c5a87d985d592750991c9578b`  
		Last Modified: Tue, 14 May 2024 15:31:10 GMT  
		Size: 16.3 KB (16288 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:e6ca4fb294dd79dcd68b91ab153571c0d1a3a930621ee34deed8941ba559adb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48383259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55da576d3fb98a867a802edb97f864d9fbed20cd4e38dfba8a63e2b9a6a5926f`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
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
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac66be9478d777106d8a4a8bafb1865146b4c82924180a3e59b9b94683b39642`  
		Last Modified: Tue, 14 May 2024 14:29:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6aa7dfbf23ee350548aec94e9bec06bdd122306ddb1a0a9f43355bfa3b92a2`  
		Last Modified: Tue, 14 May 2024 14:29:12 GMT  
		Size: 21.8 MB (21788503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee47decddf85d16dcbcc8d7742db5376a900b889f4a6bfd9e529152bf563c90`  
		Last Modified: Tue, 14 May 2024 14:29:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:316800764178a472a3605bfcc986a8b2e82d011e3ebf1a101b6fa3838c10c4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3903146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca2b4d303a08f9aff1e832a04c2055d214749418d5f5e6fb9a27779cc042d9d`

```dockerfile
```

-	Layers:
	-	`sha256:19e23beebff680b07cc063a3e7b4297e49cdde94e6a33b1ead0d420e688c8214`  
		Last Modified: Tue, 14 May 2024 14:29:10 GMT  
		Size: 3.9 MB (3886858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e411846263f87180f84e32aa67080ba52db0291cdcde7f6c325a83997758f26`  
		Last Modified: Tue, 14 May 2024 14:29:10 GMT  
		Size: 16.3 KB (16288 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:c769b1857b6f1032538c576bece766b51819d0f0ed69bfe5842c856a8ca27147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53588823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f355b27ea4d0009a5d764a00cd6c9cba9a9eb2f85c0a8f20a84ca2abd3302a92`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dbb539b13bcec9b4a2118f4147996ebff04dd60087c6206f3fd1a8e4510829`  
		Last Modified: Thu, 25 Apr 2024 08:33:58 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5745a28ecd3c7a47742746bb34de76e6b406bef8c2ed3ddd1f923d5719e670`  
		Last Modified: Thu, 25 Apr 2024 08:33:59 GMT  
		Size: 23.5 MB (23501221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647da0899cab88a689b25023d73faea177d6c2095acbaee0fc8d859eaf8730d`  
		Last Modified: Thu, 25 Apr 2024 08:33:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e6550b8b0a3ef03b26b4a5e4c7e3deae2b68398ba8bcb29fcd0325e26eee40ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3903456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219ffa9508cc556807e55b58fea7d686f4fd7291e41a79f111b39fb2f263ab00`

```dockerfile
```

-	Layers:
	-	`sha256:23ec10c6fa5db5527c21aebb875ae8dc2370801820a12d931704451e923ff269`  
		Last Modified: Thu, 25 Apr 2024 08:33:58 GMT  
		Size: 3.9 MB (3887235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca48fd4b9ee9e7a678a45eb4822d8760f8e0cf2a6bb015afd6044fef72a6b7a3`  
		Last Modified: Thu, 25 Apr 2024 08:33:58 GMT  
		Size: 16.2 KB (16221 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:9433f1e09c8af31a2557f3e812afeeb4c019bd62c28243c9a05578289ecb8386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58214429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3a726f5b954be3d6eefc1869d8ff0787f2200b2f4fef14eb7378ce59fea7dd`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
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
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058b81d3dc385875a0b474f6d19e3a01310de4d325e8f671d0dac2c52fc3a0db`  
		Last Modified: Tue, 14 May 2024 02:01:24 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88903164564f19460162c52475e1cf258306ed701aa98481689fa7dc3712f2fd`  
		Last Modified: Tue, 14 May 2024 02:01:25 GMT  
		Size: 25.8 MB (25790121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387e6604ea518f404bdd7f15b58a8730d98ed485c60b2be751a5bdfeb8cc8911`  
		Last Modified: Tue, 14 May 2024 02:01:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:7c133dff11005082b30c2c236af82e0061f9ff6ba7f09aeb2daccb062a7ae556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3933521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b73dd17b802450fa52e1ccadaa04f9e87e41aea99341f4d8519a36c3aad1cb9`

```dockerfile
```

-	Layers:
	-	`sha256:1c689913017370357289a5a404add5f4ee7d1a7e3831c2ef6cd011c0316ed003`  
		Last Modified: Tue, 14 May 2024 02:01:24 GMT  
		Size: 3.9 MB (3917178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adb07015cac777d4c114ebd56f6217a79d6bf6a28395660f84e2f7787b183829`  
		Last Modified: Tue, 14 May 2024 02:01:24 GMT  
		Size: 16.3 KB (16343 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:97c14038950ecc461996efb84b67bb75edd0135e10da1528edb24e802cfc47e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52930394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873b1f905838f19be9c3fa58bdef87db7b4ea48b5203caf5d21780dde17da36a`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:87680940dfe26d5f4583964a639405d4e00c6a3f72863f7b7e18eca764a73c67 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:2d257022fa7c7f0c7879f59891b7e4277d67c9114b820f229207724d5e65d6cf`  
		Last Modified: Wed, 24 Apr 2024 03:26:43 GMT  
		Size: 29.7 MB (29652163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8258e1beb6e34ba884858fde8477e0ad3e23cd988398244bd20ec2cd663857`  
		Last Modified: Thu, 25 Apr 2024 02:44:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc742aeae37b46b95cf32416b1d80e0a8b7f367f663433764510d2317bb9889`  
		Last Modified: Thu, 25 Apr 2024 02:44:59 GMT  
		Size: 23.3 MB (23277965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef3cb4cc68630af01ba5c45f75cc26a8f67077923990a2cf084ceba64ebf6e0`  
		Last Modified: Thu, 25 Apr 2024 02:44:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a2738400287b1aed66c86b9a5b9726c66f3975121d947a0fad88541aa72caf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 KB (16057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e3de5941ea58295e5d2ca9bc8f5bbbe8d5ff7de6aaeba31b26fe88a2223ba1`

```dockerfile
```

-	Layers:
	-	`sha256:96ea510aa62cb8efe6353e8b27e292553947830d4ddbdc8e9d50fca7f8c5d776`  
		Last Modified: Thu, 25 Apr 2024 02:44:56 GMT  
		Size: 16.1 KB (16057 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:664883b3397d22d44dc3ca64acd6faba90b597f5800a1997e29ab7154d8cda04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59936048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c781c91a11770749c46b5612ff01042cc3f230fa791598bc80c43f721fafb8f3`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
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
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cf0bdb960b363821547c618b640d1b7844769c456af185e7f75402d45bbbd8`  
		Last Modified: Tue, 14 May 2024 14:02:01 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85adf6db9818e2f3117450b2f54e6960a162e300f8b2017e61447e54a1117c89`  
		Last Modified: Tue, 14 May 2024 14:02:02 GMT  
		Size: 24.6 MB (24624625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cf8f4510e072e8f865b9e7be91569fba88d1c1cfffe7316b56b95ae26e2627`  
		Last Modified: Tue, 14 May 2024 14:02:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:8ea59d024e51ac760e954df09ecfa3572b0fd02eb0d91cfa7310f310b8e57ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f305ffa6a0b1248237b3d9e485262d5d5e36890479f9705b99d6758953baa3c0`

```dockerfile
```

-	Layers:
	-	`sha256:732d74453e1ba1d5e7b1f7cb1fbd8f088df595aef5d96a29b9969e8fefe6e680`  
		Last Modified: Tue, 14 May 2024 14:02:01 GMT  
		Size: 3.9 MB (3901694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accc4515268a450cf52832dafaf14355a1be1d05a30722b46ddbf2555292835f`  
		Last Modified: Tue, 14 May 2024 14:02:01 GMT  
		Size: 16.3 KB (16254 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:cea778cea8301d33cca56603089e9b72621c41e3236403e9ef8c8beea5124f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53260225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb0113a26f9bc943b64a8687d7d2fceb4fc9d6076bb64189c373fbf8f02fd74`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:acaea4e054f1ab7ae5cbc8f02c73b546c367aebfcc48c7fb4f0dd9f3628bc25e in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:6f588995519e0e04ef4c150b91ad96c3c85667869db0ad72e5a78d4fab796e70`  
		Last Modified: Wed, 24 Apr 2024 03:49:47 GMT  
		Size: 29.7 MB (29673934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9a80240e29f2e5d48455f7f7ec669e99c757751c116b1b2b87ff5933d6b0e1`  
		Last Modified: Thu, 25 Apr 2024 03:25:05 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bdc9466eb80315c6d513adf89cba4c4bf93783fce92ea9d6b16409d855e818`  
		Last Modified: Thu, 25 Apr 2024 03:25:06 GMT  
		Size: 23.6 MB (23586027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9924623cbd5d46a00bb116d99213d0cce04c6456d8ee39a3f1a4f5a9ae1514a7`  
		Last Modified: Thu, 25 Apr 2024 03:25:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:20cfaacc710eecbb5b74d53048c33ff45a914417854110d66e905349c93b71f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007d5a835cf6e53aa4c92a5e747b1eedd517dc4e4180983cddce53833e1bab38`

```dockerfile
```

-	Layers:
	-	`sha256:6eda9cafd5cb6e14eb3ba6b545a447c43d88602e1568354ca797d70b165d6a4c`  
		Last Modified: Thu, 25 Apr 2024 03:25:05 GMT  
		Size: 3.9 MB (3901619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21fad4c874b1f16ba262a6ec81849cc5ddca79260f990a9e08d4b8a5f13fbdf4`  
		Last Modified: Thu, 25 Apr 2024 03:25:05 GMT  
		Size: 16.2 KB (16210 bytes)  
		MIME: application/vnd.in-toto+json
