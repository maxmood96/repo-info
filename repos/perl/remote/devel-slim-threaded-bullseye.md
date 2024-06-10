## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:01db2d8366d048d0cd18e29d50bea8143285576f0e59a97cce432b8890f5cc13
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

### `perl:devel-slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:271ca05110c503f18b8837b4d12fb81019432a865862ebeb6aeff7ddcbaba08f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56127999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e727563855467b11416edfcb452dc815a9c3462cd18cadaf6059a6c37b286c53`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81aeeb26e7ac2e281803198d521870f4fb120952df2df4ccfe0c323ed6a6eb`  
		Last Modified: Tue, 14 May 2024 03:05:44 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e53e924b38a86a9a0bbeec5654b9538a15fb57f542d6ee7eafe18f0ac125976`  
		Last Modified: Tue, 14 May 2024 03:05:44 GMT  
		Size: 24.7 MB (24693804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b411a6b7a08b0d073956969307d18d2799d6b3b7161ead9f13e35c5c4f2f54a`  
		Last Modified: Tue, 14 May 2024 03:05:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:d30771d5ab3b2307d6cc3edcc2f69a7eb0db1badb5621c67e8778922cd1e0b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf5ae47b370a0c5f0e965f569f02726a5b688ada65efdd4fd4c1fbc025ddb7c`

```dockerfile
```

-	Layers:
	-	`sha256:8ada72840f9bf3df3faf634885f3afe921475133df07d71f7bf9a0d046b617d6`  
		Last Modified: Tue, 14 May 2024 03:05:44 GMT  
		Size: 3.9 MB (3912363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af51d19a1aca1c4e2ffd6e003da6f0906aa001859d1bc88a3ff044546ee96ff8`  
		Last Modified: Tue, 14 May 2024 03:05:44 GMT  
		Size: 15.9 KB (15941 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:fd2c3b9d9084b8eca04c37244eb939745a4698d997400eb5276b0fe16464b605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51626340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516e4b63715d01e31db392363ffcba6189d0079161e27c0ed3dd6e5330e35de7`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:7a63cf2b5d16adf102fbd2452be219224667c4ea55981247f398a4a867ef96c4 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
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
	-	`sha256:f5f8cac79ac87a93ae5167b2b8ab413bccb97c5fe9fef80faabb710288df1a67`  
		Last Modified: Tue, 14 May 2024 18:21:58 GMT  
		Size: 22.7 MB (22689355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5b62d7f44c8dc0b7a4b8841fc873f40807af1b95a7d4380fb523684fdd05bb`  
		Last Modified: Tue, 14 May 2024 18:21:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:4116b8d3818b811832d62a6f3aa66ed1785038421a0aa40c5ad1165eea3c9d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3899396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca72f8b661b274b5e349e00c4c5511d1f0f07cca13aec0ab9a0d03e12630c7`

```dockerfile
```

-	Layers:
	-	`sha256:5fa4b93dcadf2a02a4b0438d6003beda2545301476cba01731862e83eedc38eb`  
		Last Modified: Tue, 14 May 2024 18:21:57 GMT  
		Size: 3.9 MB (3883560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c153dc54c4e37d1156563b0ed2ca3f46743084c161098f4bfeed4e104f07617`  
		Last Modified: Tue, 14 May 2024 18:21:57 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:cffd402f27bba74d9530d25167f05c2ce348b68c2a85962e5c9155953b3f6518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48671451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d7e479e54def300c7071133ea14200a864c343ce91c371dadbf1cd3e43818d`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
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
	-	`sha256:7243dd1963a5d369cf35f09a51db259cbc8c81380d034890ab4379d39ff45275`  
		Last Modified: Tue, 14 May 2024 16:45:34 GMT  
		Size: 22.1 MB (22076693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a88ef4a4eae3613ff3d9f61f59ffe935a66e4499bbb20d1e8fc4af781de155e`  
		Last Modified: Tue, 14 May 2024 16:45:33 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:deee42645baf21a26b22419f32e5c4c3b1b417ee88016327ee239d1dc05fbcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3902114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbc4020f5f642475e1ba7a0d2baea54130eeecbbe9b089242f2d99495e2a2b4`

```dockerfile
```

-	Layers:
	-	`sha256:211049a0d265d826c4b867ec71622a667c996e58fe883712d8615242eceef164`  
		Last Modified: Tue, 14 May 2024 16:45:33 GMT  
		Size: 3.9 MB (3886278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18d768bcc609963dd1053b7f6298481948c3cc8bdade51c5bdbc73ac79c630ff`  
		Last Modified: Tue, 14 May 2024 16:45:33 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:200d885d6f46141f9feb4fb3578713ebfe1f53dc41daef8d39c47df5b6f2dd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53894130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638e6f2a40c3917f5d16e5748f9e1d8cbb8d890d70b6e39adbf80b44b2d280c4`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacccfa947f9296f4e60b6b2eaa847fb68e0cc89210a0c5cff7436cbd685f18b`  
		Last Modified: Tue, 14 May 2024 18:23:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e657ba578a91acee20011ee09dc356d06211a351bfc567cb226137dede28811e`  
		Last Modified: Tue, 14 May 2024 21:00:57 GMT  
		Size: 23.8 MB (23806957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f560114681ae90fdeb4b3aa9e73c5df58e01a45761ff30e7cfd88c377adec1`  
		Last Modified: Tue, 14 May 2024 21:00:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:61714c687e9fbef49ad166f3c6d6cf6dd8f8ddf7f91be2ab17edf0cf5d5d53a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3902458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a80e4ba22c4138ed60d6d40dc47ceadb8260207b2f28d417a0e31c4004ff24`

```dockerfile
```

-	Layers:
	-	`sha256:552967bd1c56e9b0019e4ee0310a99f4da5107f98e7332bbf3692f8c43030c3b`  
		Last Modified: Tue, 14 May 2024 21:00:57 GMT  
		Size: 3.9 MB (3886677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ad805380fa9f4c470a761163bd1a5b1ac261d3f0c75c9a3ac301867e75863f8`  
		Last Modified: Tue, 14 May 2024 21:00:57 GMT  
		Size: 15.8 KB (15781 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:f8b05478001e96dda4c59003d278cd34031f40bc0c4677942e49fbac778fa1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58586968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa3c0b40a2dc1d7267bfc643e7a2118e21d2572328a686c1d2633afa17bf9f3`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:47:34 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Tue, 14 May 2024 00:47:34 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df80bcdd419b0876c4573d5628d0ccf73929a559b28d56db21cdeccbf6319b53`  
		Last Modified: Mon, 10 Jun 2024 21:13:14 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b92c83b749dcacd3bd6ee52478cec61270bb62e654d6910003d6eae6fe8151`  
		Last Modified: Mon, 10 Jun 2024 21:13:15 GMT  
		Size: 26.2 MB (26162657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9accb8d74720a5ce0663e000254239769ce63fa3300d1ee4595ac5db3de0bb`  
		Last Modified: Mon, 10 Jun 2024 21:13:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:84f92bacb5dad4a4caf38166a6cfda5f91c9e315398d1d83a94e395e3eadabf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975c5b4974eca360bb9bfb68397b8878f4b8b2e60f40b10a0f1269fe3a6ea3f2`

```dockerfile
```

-	Layers:
	-	`sha256:af605d942ef14c1c1b13b63af0d7d2057a1615fc407ac48662fc63f12dd21f6d`  
		Last Modified: Mon, 10 Jun 2024 21:13:14 GMT  
		Size: 3.9 MB (3916623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9213fc44af94176d065e257d6e1aab160944814a13a80e8e17881fadc902b713`  
		Last Modified: Mon, 10 Jun 2024 21:13:14 GMT  
		Size: 15.8 KB (15799 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:a4e89e600ece2ef8d200c58861ba11b6fd3fdef4c1100f6dacf5959047b5de8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53259200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3700920e09ca6648f2a073fa1039b1919fd1147d1f343d4e25f4c53f5d54fd`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:ec3acf4bc32b149c2b67d1b2c5f3a6d1f16fbae266ac16c115e1fca276b970e7 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:38917083d8284ce1ec7533351600bab5d64f8295f3edc5dc651be130fb9a4bd4`  
		Last Modified: Tue, 14 May 2024 01:23:44 GMT  
		Size: 29.7 MB (29651870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864f2634f3fa0d01e4755e1380562b9015e1756bb6db04ec0de54e37d941060`  
		Last Modified: Tue, 14 May 2024 23:26:32 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941cdb36a0274cc4fef06757c296e4711934db49d3b514248d7089f71e37135f`  
		Last Modified: Wed, 15 May 2024 04:58:28 GMT  
		Size: 23.6 MB (23607065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01242d820050749456beacf0d7fe213ede1fd61746743f1fe461a79b3a22f1b7`  
		Last Modified: Wed, 15 May 2024 04:58:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:1a6b31a8ee05264793c9060cae84fe10f7e52955cedfa6057deabc20a852c95c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331483109a5e4a789beac2065cc8bc80ea683bae3a44783ad771bb52c19c5ac2`

```dockerfile
```

-	Layers:
	-	`sha256:2e74431a04e5c4cdc525cea7eb3a6fbb1f4c87fbba66bcf12377a4ab9699d4f9`  
		Last Modified: Wed, 15 May 2024 04:58:25 GMT  
		Size: 15.6 KB (15603 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:378ece282f01a741ea5cd3cc9d2aec21a262cd4bc69fac145cf5a186dc715a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60285774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5df34455712e34aeeac509137f8bc8059d0f61cb2507a23b5857bbe4ba53ef`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
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
	-	`sha256:f0fe8e9a3f64f183c39e647f780070c20fd155adb2c7a909d39846a8991e700e`  
		Last Modified: Tue, 14 May 2024 15:36:18 GMT  
		Size: 25.0 MB (24974351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffeb94aa99830465a7a34368845fb9480e91293895cf487606f63087ad2ce43`  
		Last Modified: Tue, 14 May 2024 15:36:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:456c7050597252d599f008be50251d77581a135464eb286f17da90c2480dd429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59097721689245d71814e0c9935e739bfda5c475f8623de082b2af6d47d909b6`

```dockerfile
```

-	Layers:
	-	`sha256:64cd0b5af9a5067a3fd04ec3e2f6c0b3f4b644fe848a62b8fafadb0e78e80608`  
		Last Modified: Tue, 14 May 2024 15:36:16 GMT  
		Size: 3.9 MB (3901118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f01430bb54c0094ad18c8f9b13039fdedc708ad18837e86f922eea1e16d937d`  
		Last Modified: Tue, 14 May 2024 15:36:16 GMT  
		Size: 15.8 KB (15806 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:f45378388976cedd2e628baa67f14537ec03e6ecb25b932f5565b133632a9d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53589987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9200b8b013e1a9ead4205609c4badd4a8fed310b42abe0bb052dc573c7ef41e0`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844db87c488fa935ee9d85d53f963b810712d17ade6ba07101f7ba199af23817`  
		Last Modified: Tue, 14 May 2024 18:45:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18100e4576f1a088802e71c9f98bcc531093734269c3dd4aa3f6bf33cba46f8`  
		Last Modified: Tue, 14 May 2024 22:54:50 GMT  
		Size: 23.9 MB (23916067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ab4c56b4441166a76988fd561faa9638b468d980268a31a78c921224bc1dbf`  
		Last Modified: Tue, 14 May 2024 22:54:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a783e8b2b3d30c159083050be8fc6a80cbb083fe3a1e783e3710e9e51e4b69d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee1e52ce1b45b72f8704e9b630bc77442b63d3f99b0fd1e8b1d8504548e0694`

```dockerfile
```

-	Layers:
	-	`sha256:ab37cafe4462a7a987c4ecb14da15d10794845bce6e36a40113e21ca1eb7021e`  
		Last Modified: Tue, 14 May 2024 22:54:50 GMT  
		Size: 3.9 MB (3901065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad7fe40d55c8aca47b8def0368f8b1751d7b41afc39dfe880cda6d8c14fb6c23`  
		Last Modified: Tue, 14 May 2024 22:54:49 GMT  
		Size: 15.8 KB (15772 bytes)  
		MIME: application/vnd.in-toto+json
