## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:cef5cb8dcbe4f7d847052694bc9d2646f675fd71eee4bba0d587073e2f818ec8
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
$ docker pull perl@sha256:977347db47b4d322ae17c80b7b8336b5e73088130004e0409b3d5ebdfcf31357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53894809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda725596b3de31ef6c721f259c5d2afac07d6effa1ca16e978185717d0115ed`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
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
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c67b87c90ce6a0c26a97b0fe933ebea19679123eef2a6d6ce066a52f0aed09b`  
		Last Modified: Tue, 30 Apr 2024 05:39:08 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b593b5103c7d935c293aecb4d8951fbdae29a9083c350f8103b89ef983d7e`  
		Last Modified: Tue, 30 Apr 2024 06:23:34 GMT  
		Size: 23.8 MB (23807209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adab69846b50fbe147c79f90ca47f174cd777a43cdc79abf74872d9ad1e91a9`  
		Last Modified: Tue, 30 Apr 2024 06:23:33 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:29b7c5d6850735ae94d1a88c43f4ae066bc9b2b29f3009cc6a6b9c3c79c52ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3902449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710e9808f07121b197ef4dbb47b86378a2c69915c8335fe55c4b771088d178e9`

```dockerfile
```

-	Layers:
	-	`sha256:df5dca0c945a06f6479af4dbec11b3d6ee25c62abc88c0aada9eee630a89d859`  
		Last Modified: Tue, 30 Apr 2024 06:23:34 GMT  
		Size: 3.9 MB (3886667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e2580d5d38a462d61c307348df9d5a338856ffac8dafe9b289d24f2bac95f6`  
		Last Modified: Tue, 30 Apr 2024 06:23:33 GMT  
		Size: 15.8 KB (15782 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:9c214fce9f48f05a8964f869b2204898cf29eda34bcfa4ccca9cf09f5be5c0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58586054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09b44b18bb4a7c8f94f61df1ffd6615fe4bd08b27694e9b0a38e63d41f9cfdd`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
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
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eae910a541e2624007da3cbf0e257bdb9094fefc7c4900e71ce9d065edf642`  
		Last Modified: Tue, 14 May 2024 02:02:40 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541bc2c95d6cafe12b0e2e714f9bae8988e6281de106c06f55226621d596c0ee`  
		Last Modified: Tue, 14 May 2024 02:02:41 GMT  
		Size: 26.2 MB (26161747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5520bfb224731cb0e4c2a04470f6ea8dea6f4b5957109c8f7bb4c1bc8e0b`  
		Last Modified: Tue, 14 May 2024 02:02:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:2fbbb97a437cacd75b1d3696147d5486f19b4fc804a40e3714a138d7e76ca8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa8b933e8452bd16c0a7b986c6dfbfd5d60687c5e728fcecb0d9cd19e4431c3`

```dockerfile
```

-	Layers:
	-	`sha256:dd141f61d3c09f28496cea0cf5407b9d9747164d0930106e18118790fa7d0a7a`  
		Last Modified: Tue, 14 May 2024 02:02:40 GMT  
		Size: 3.9 MB (3916624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19703a1d67a78d821f0f88bcd24354451d7ddf4482b85d64158dfc74e88d8f2c`  
		Last Modified: Tue, 14 May 2024 02:02:40 GMT  
		Size: 15.9 KB (15917 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:abbedd7925cddf216654e2de388e30d35448018b82eb2de96d08de945a1e04eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53259439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde23e909243a65755d2c27cbaf94d2379f93e4d0147430c25a8741629f8a21d`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Wed, 24 Apr 2024 03:15:35 GMT
ADD file:87680940dfe26d5f4583964a639405d4e00c6a3f72863f7b7e18eca764a73c67 in / 
# Wed, 24 Apr 2024 03:15:40 GMT
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
	-	`sha256:2d257022fa7c7f0c7879f59891b7e4277d67c9114b820f229207724d5e65d6cf`  
		Last Modified: Wed, 24 Apr 2024 03:26:43 GMT  
		Size: 29.7 MB (29652163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e753bac24951579a6d53a1c8bf76d94e8986b8860142314ec586debea5ff97af`  
		Last Modified: Mon, 29 Apr 2024 21:32:18 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546cd7b5d99500dedc461556d2638f2bd7d6a41470785718d5ac836ee14b4389`  
		Last Modified: Mon, 29 Apr 2024 23:37:21 GMT  
		Size: 23.6 MB (23607012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c116769e1d67cc3363794051fcced401a5884cbb74db1f135d8e61e28c2a3ce3`  
		Last Modified: Mon, 29 Apr 2024 23:37:19 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:8401de2f8b91393723d6cdcf43eff29f9a0d7b32507f31fe1790625970997609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54a8e7c9cdf8f4e3591914d2afdfb26c13fb000f40a31e4ae7d2b62fdc29c24`

```dockerfile
```

-	Layers:
	-	`sha256:c6c351e7998f912d5d8b6a5f92c8ece6a383b0fc64ea413070aa14e7610d5c2f`  
		Last Modified: Mon, 29 Apr 2024 23:37:19 GMT  
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
$ docker pull perl@sha256:5bbb33e1a9047efee13a249bf3c23c6a6ea2d67cd060fd880d3b554ec34b780d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53590681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a1a12e2833d6796d3f4041a3b39ac5ae632153093b08d97c8c508b9ad96a06`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Wed, 24 Apr 2024 03:44:03 GMT
ADD file:acaea4e054f1ab7ae5cbc8f02c73b546c367aebfcc48c7fb4f0dd9f3628bc25e in / 
# Wed, 24 Apr 2024 03:44:09 GMT
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
	-	`sha256:6f588995519e0e04ef4c150b91ad96c3c85667869db0ad72e5a78d4fab796e70`  
		Last Modified: Wed, 24 Apr 2024 03:49:47 GMT  
		Size: 29.7 MB (29673934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9a80240e29f2e5d48455f7f7ec669e99c757751c116b1b2b87ff5933d6b0e1`  
		Last Modified: Thu, 25 Apr 2024 03:25:05 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f72b39dfd9ed225030ef0e54be00d83ac9804d26f82619d5dc7fed58c2b89d7`  
		Last Modified: Mon, 29 Apr 2024 19:30:17 GMT  
		Size: 23.9 MB (23916483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1981b1b07d7c9f0a07d0408b7d7d91ebdba48367d6e50b37bc7b3d285488863`  
		Last Modified: Mon, 29 Apr 2024 19:30:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:033ef7859f0ce2700929bf0a785bd686e5987c2f7dc28bd7975e5a8d92890d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff47dfcafb59d33d35df4694d98cf0e7b3546a4262557c739b9aa11e5049ccb`

```dockerfile
```

-	Layers:
	-	`sha256:5adf3552eb021b210eddabf696f8f308d32c5b9471499a543f963853f2cdff71`  
		Last Modified: Mon, 29 Apr 2024 19:30:16 GMT  
		Size: 3.9 MB (3901055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e48920b694c6b7981d91962c0966fa9ad78911b4ac8630de79e2dca715620f09`  
		Last Modified: Mon, 29 Apr 2024 19:30:16 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json
