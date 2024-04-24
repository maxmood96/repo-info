## `perl:devel-slim-threaded`

```console
$ docker pull perl@sha256:d86ae50e8b1f43afa916e8a1f0bb1f80a6d5e47c7031c7494fac750c7c7fb05a
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
$ docker pull perl@sha256:9c900d0286e45ec255e6ec827b51f756315ba2f436fa2283aff7620371b693da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57771325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e22bde648332c7b4aa37cb55cc390d1b0228bb5a747f0f0cfe343434abb17f`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ec6dca4b6d16a5cd5e769596ce7bceeb4b9925181340a5d1fac5835513f2c7`  
		Last Modified: Wed, 24 Apr 2024 05:04:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe457171a6462f2f184d7b72425cbee8351b78dd7939ed3ea52ee901ad94801`  
		Last Modified: Wed, 24 Apr 2024 05:04:32 GMT  
		Size: 28.6 MB (28620578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ebff7c5cb848c8d84b6d99c6e968f36df1ec83ff5200504f21b2a4e1646abd`  
		Last Modified: Wed, 24 Apr 2024 05:04:31 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:68b103156914a8b98f0a64e2cd0e943fbf2b3df4ad4dd35f5218bd29bcd6369b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15671fad5037d1b5df33309535366e517e60edff456e411f15a446df0e9bd596`

```dockerfile
```

-	Layers:
	-	`sha256:80fe757e3fe9e3e40016004cd4d4058e28604d10098596350922bb85576c0ab9`  
		Last Modified: Wed, 24 Apr 2024 05:04:31 GMT  
		Size: 3.7 MB (3719354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c65bc37d230459b30fdbe62d4378492516b7579e69a926d25c26ea78e90ccf`  
		Last Modified: Wed, 24 Apr 2024 05:04:31 GMT  
		Size: 16.9 KB (16886 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:bf460d332613f896c0df46ddeb1f32bac2041771cae63a517582f6bda52da00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52606779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548b76883035a189e8713ff6dc17ffbbf964fbf87945d69a0ffaaf52fd1fd76f`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa002d450c5ab1d539a38a7c86c6c2e5adbc71da7588db05ce9cf451447a4fd`  
		Last Modified: Wed, 24 Apr 2024 17:54:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d826df8b28409987b3e7ba456be7f4db8f276fd7e33af595cceff8f370fd15c8`  
		Last Modified: Wed, 24 Apr 2024 20:48:16 GMT  
		Size: 25.7 MB (25696483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea19fa92d881eee1efd6a5b7115386c8f31027c960edec5860745e5087ba351f`  
		Last Modified: Wed, 24 Apr 2024 20:48:15 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:2a1d17117e93d3132c05195896836327d565565b159913b717caee877e6b56ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3706422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9600a4b7cb12aca2c6480b1efdcfb7160b5e01eaff5e695bd10e5026e8c23213`

```dockerfile
```

-	Layers:
	-	`sha256:8c3d90e15cd577a2bf3feee6931e1d2077633cc1f5d9562c0526a2d2ee6d701e`  
		Last Modified: Wed, 24 Apr 2024 20:48:16 GMT  
		Size: 3.7 MB (3689617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1123a8540fcf7db8c5e4f25e3ab134e5673524ab52a28cc8188c7fe48bfe89`  
		Last Modified: Wed, 24 Apr 2024 20:48:15 GMT  
		Size: 16.8 KB (16805 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:6cbe532d34c7533d8255fd47115455f12086055211d97a1068184418a84caa22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49652870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7589ff8dc8eea7211850672d3d3a1b6cce834c4bccbd7e3897a52ddf1096f93c`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b51872060208912f28244a31d373751f410c53d744c327127ec76ca92009e89`  
		Last Modified: Wed, 24 Apr 2024 16:58:21 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342d31a1b535ed3835da1eafa022f5c5fbbf1e5fc4a3b25540935f10aa1fb3ca`  
		Last Modified: Wed, 24 Apr 2024 20:21:35 GMT  
		Size: 24.9 MB (24912162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4b97c97beec57d0f24ede1826a2e784014c41d8982adcc21bcacbc3b0d602c`  
		Last Modified: Wed, 24 Apr 2024 20:21:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:da9f86a0ce53d6f69b96d6ee5fd271ec1fe31a85b187f4486407d85b8c90364f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3706180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c8f430f93703f9a129f600fb457b7e1ccdf96a1855708049fcec10d4ae45d2`

```dockerfile
```

-	Layers:
	-	`sha256:98652ab09094c134222c5ee866cfed6c540ecd14bfee43516b20a6ae31a60026`  
		Last Modified: Wed, 24 Apr 2024 20:21:34 GMT  
		Size: 3.7 MB (3689375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04a1115b88760f327f30086130c94ecf2ccdedc0f13f6ebaad53aa74b39b1b3`  
		Last Modified: Wed, 24 Apr 2024 20:21:34 GMT  
		Size: 16.8 KB (16805 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:936fe3b02428e080b089d5dba92ea5fa5517404d32d8d6064b5063d3f27542e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56751425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6015246e66e66628fcdd9c425620ae9f776d7ff0c680ad9780d03be3cbc3d8`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe961d440955688f8659df672f0d7478ea5e34abc65767f0d6c2df2b2d4c6522`  
		Last Modified: Wed, 10 Apr 2024 17:05:31 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fe2247a00c6b6a050f8bb957b42352ce67cc6a0c57c1c291f7a114b8d28d18`  
		Last Modified: Wed, 10 Apr 2024 20:20:08 GMT  
		Size: 27.6 MB (27589001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa56f3992edb3b67b1e7f8a0e1a993c7f989c349702c35bcb48dbf199e444c3`  
		Last Modified: Wed, 10 Apr 2024 20:20:07 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:a1efe5503b12931d03334416a9d1413d393d3c890d01ea07ab8675b00cf31298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3707127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c2aaa9cbc0fa7e4afa0d621b74219cedbfc0ea0195dfebaa31f9fe25bf6653`

```dockerfile
```

-	Layers:
	-	`sha256:e0c4d1540933a6703642cf793076258f430f9a083ec0b4b6071f50a8e1c3dca9`  
		Last Modified: Wed, 10 Apr 2024 20:20:07 GMT  
		Size: 3.7 MB (3690398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7928ea1ec1228aa4d6478576b49ad0fe6a2dfa4d0dedde5c3b0825bbed84acaa`  
		Last Modified: Wed, 10 Apr 2024 20:20:07 GMT  
		Size: 16.7 KB (16729 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; 386

```console
$ docker pull perl@sha256:7b5240b5915afb5262e6ec425d2721451c01d24c8ca74f49b61bc2407241229f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57820519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d73a731d38bdea4d7dfa91021b2dc8a1e943eb9fd8702aa81a8c35b28ba4fa9`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf593f8ee719f8a663c76224c357474a53dae630abe973e97f9076b64224d35`  
		Last Modified: Wed, 24 Apr 2024 05:05:41 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f919e2eaaca4caafe5f59465e7000f8014863bbb6b2dc8c51754a922647fb96f`  
		Last Modified: Wed, 24 Apr 2024 05:05:42 GMT  
		Size: 27.7 MB (27657069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a01f31b37ba8e07578f0e01fa85625c538ad1698f1ceb89c24bff5851be38c0`  
		Last Modified: Wed, 24 Apr 2024 05:05:41 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:58614a194530bcbcd29b314588a2980f6d6f5c36599edab99b826e4a3dc75cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d0ca58be42650d9bad0935c892901dcaab3e8cbaeb320d56ba1edb5431fe46`

```dockerfile
```

-	Layers:
	-	`sha256:21ddf4de96c08d0fb007e2a544c3a14a7bc3df3669671e13ee51edfe16662767`  
		Last Modified: Wed, 24 Apr 2024 05:05:42 GMT  
		Size: 3.7 MB (3713247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:325339a1431ae2c32c41e7db087de34ba925121801feca5fb993a8074c310064`  
		Last Modified: Wed, 24 Apr 2024 05:05:42 GMT  
		Size: 16.8 KB (16847 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; mips64le

```console
$ docker pull perl@sha256:f4eb4263c7282ff880f576422d505b70278e6c36e505fc08a14303a7b0bc6024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56095434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fc94e6b8b6cf3da6dc783f9d5ab1f5fb5cf78254927a52ba852b15172e2a60`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:c07831a1f2abb22986c788bb198b484a259e7e68ee8b03da0daeb4b41d8d83ce in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:a99180cf1634aa211024be7ce3258cac9c0823e82f09b97870da9d9b21ea68ca`  
		Last Modified: Wed, 10 Apr 2024 01:21:58 GMT  
		Size: 29.1 MB (29124665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecf89cb254e2f5656809db8155c1d50808738b00ff076d579f23844524ec120`  
		Last Modified: Thu, 11 Apr 2024 02:53:22 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8d7eab6e319ac3be6c9e44a313d908fbe7da98179afbc93e13ead17e828b69`  
		Last Modified: Thu, 11 Apr 2024 08:21:27 GMT  
		Size: 27.0 MB (26970500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdfbde3203c764cc2ec61922262cc01934941995744c9c1cd2f4a0414d9ce83`  
		Last Modified: Thu, 11 Apr 2024 08:21:24 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:dcc2238316cb306bfdd8a12000d8d236ac0e1bfd0eaa13278361764e2d5138da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 KB (16575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb08dbbeab3b0db6f4ba485d8d0d231f9eeff23960db4767c5257d5931a53bb`

```dockerfile
```

-	Layers:
	-	`sha256:6ad24783b87def82ae4bdf968b8b880d72a8c41fe67d7c47cb501d7a9ddc61b1`  
		Last Modified: Thu, 11 Apr 2024 08:21:24 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:6f44d6ae8ac1cdeaf190c8a528f08b1a16939f29eefa2b4a3c3dabaaf70ee81a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62528070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5088ac1925ed3cd8c742556b9feb74dacfd6aae5dba066aa25ada15b04fecbc`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ac7e27cfc922464a219c5f40ab2b8831291168f409f5a6cdd769573c9e5dbf`  
		Last Modified: Wed, 10 Apr 2024 19:39:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798c85e9c9c7acefb4a480e3ec8b2e022909731e56b6057e11ff2f6d02d746f4`  
		Last Modified: Wed, 10 Apr 2024 21:17:12 GMT  
		Size: 29.4 MB (29402966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2367086a7265430a9578976b2221745106f143683ac18939de57a6fcfcc04a87`  
		Last Modified: Wed, 10 Apr 2024 21:17:11 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:80fd122c761d0b4de9d17dea88441debd706d2ba6573f22909dc57f709d5f160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfef0a20287404f2c372864cbabdd2a2f578cf7a29813adbf9c88846c3785b70`

```dockerfile
```

-	Layers:
	-	`sha256:9e4beddcfeaec90f9dcb8f5757c231d6f79010a6dd186ded1f79e6629a64e59b`  
		Last Modified: Wed, 10 Apr 2024 21:17:11 GMT  
		Size: 3.7 MB (3704943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7ff71c5c58723b21885bb3671d65de449757f5de13b3a51fde43e8317cf72e`  
		Last Modified: Wed, 10 Apr 2024 21:17:11 GMT  
		Size: 16.8 KB (16765 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; s390x

```console
$ docker pull perl@sha256:a0eced82c95648c9af2cff328b3c4aa5ebe8481e48f177c00575f100fd79aa31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54836873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adcc9e252dc634ff3915e2b52f3cdaff39dfba74edccd9723e260219df685bbe`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:0e66ba8384d53d3671a6a148f8bad9decf482a97ef81d0740132e74b8e30c670 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:06d33788df65214dbd82280e1b49e32ce4580d4f3df100d32090f4eae8ccd99c`  
		Last Modified: Wed, 10 Apr 2024 01:48:29 GMT  
		Size: 27.5 MB (27494178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94da905217dc55d867ea4d85c8c1ab64ebf87d8be81345ca85d4ef400c96c069`  
		Last Modified: Sat, 13 Apr 2024 05:28:38 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17fc950c746836889b3bffa51b1de84791bd4b24e2f5366629379de997fc7d2`  
		Last Modified: Sat, 13 Apr 2024 12:33:07 GMT  
		Size: 27.3 MB (27342428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bec634280ab3d87b71735e95e65ab5fd175b847329fb40fd3c247c838a8cea5`  
		Last Modified: Sat, 13 Apr 2024 12:33:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:a422da4d427ee66587043e3642deafc14dc77bd112381d688e6fd3d623f4708c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7410f28360e60014e86f865f706c840bd76557ceec0634407fff017beaad07de`

```dockerfile
```

-	Layers:
	-	`sha256:de4d4c0bc2c7bdd4d3a01d53b546ec0bbecfefeaa8507e6498b37d0362b99f10`  
		Last Modified: Sat, 13 Apr 2024 12:33:07 GMT  
		Size: 3.7 MB (3707510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b394c4ee54129a8133892cb41769cceec2e69214bd9296eacfffd0910214a63`  
		Last Modified: Sat, 13 Apr 2024 12:33:07 GMT  
		Size: 16.7 KB (16715 bytes)  
		MIME: application/vnd.in-toto+json
