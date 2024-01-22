## `perl:devel-slim`

```console
$ docker pull perl@sha256:f37a5b7e671c163fd12db4fee3e92e507b35207d68cf2d1611c83a8bae1fab84
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

### `perl:devel-slim` - linux; amd64

```console
$ docker pull perl@sha256:7f2d3716ec117099d7f27025c63e7b2bb2115c3fd0079d3f29750b055e8175aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57823186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b863dadbe08c6d0595587676ae966fd502123a3c66c44e50a0c4dd27933c9c63`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0233d65ef9a46f5e723771c4449313eec8680ea1304d388676bffc3baafb61`  
		Last Modified: Mon, 22 Jan 2024 19:03:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7ee301de2310533e88d8d7b1a2d3afd10627320cfa9b7aba50a8ce638f60f8`  
		Last Modified: Mon, 22 Jan 2024 19:03:53 GMT  
		Size: 28.7 MB (28696998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9292426974f59280a906be5ac57f9491c6a60615b938ff4c7fe5c8500680e528`  
		Last Modified: Mon, 22 Jan 2024 19:03:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:b4d524ac5425d5defde9f530ab23e0d94fe42a2292296fcc97234bf3fc4ed880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3248328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcade7534bec55a3a4e4362e371401ae3cf2bfc4e2258a72ce98abfe6420a10`

```dockerfile
```

-	Layers:
	-	`sha256:c866e12f7eab3cc89d20cbaea9cbbe119dc2aa2abfe5b72257f1fface8b20782`  
		Last Modified: Mon, 22 Jan 2024 19:03:53 GMT  
		Size: 3.2 MB (3231602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82bb1748f64b151105fa68b5aea7af03fa91d5d61097d0329920335cce05717f`  
		Last Modified: Mon, 22 Jan 2024 19:03:53 GMT  
		Size: 16.7 KB (16726 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:e0002e648335a80ece666a5c7f0926cf5d59f887178cdd0bc84d85b39e374beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52699171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47cd5dfe60da47f0313c708062f48392b1831c74cf233762957ef6c910e2d1ce`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Thu, 11 Jan 2024 01:48:56 GMT
ADD file:2e234aad355a61f304982c134eb72c46730200cc475a400c78836ba8761cd52e in / 
# Thu, 11 Jan 2024 01:48:57 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:7b3d38e58d48b1d7eb80e8663c89d5f32b423059b0dbee65b1dc132a6d707cff`  
		Last Modified: Thu, 11 Jan 2024 01:54:05 GMT  
		Size: 26.9 MB (26885480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16f7392b771be05db763c31a4c469f6fbb2e94cdf553bb43b7162cc082d70c2`  
		Last Modified: Fri, 12 Jan 2024 16:40:19 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2f7e23cd03092801a288efa54a5351dc0f19230d9acc1b2f91e583eaea5ce`  
		Last Modified: Mon, 22 Jan 2024 19:44:58 GMT  
		Size: 25.8 MB (25813424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0f779dd7a621bad645e5ae2087a588abce39513b990b4d5e0282f710ec0ea5`  
		Last Modified: Mon, 22 Jan 2024 19:44:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:1d4823f2cabf979b8e518f2596587f42da7e184667c7566c236356a72c5e5878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b04545235a4366e5132cf8399c858df9b7d04d35d676005338760a856ea515`

```dockerfile
```

-	Layers:
	-	`sha256:41153756c187b7d99c5694bb64b446e78fdc63b01010440073d4348916c43e2c`  
		Last Modified: Mon, 22 Jan 2024 19:44:58 GMT  
		Size: 3.2 MB (3206317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b80a257f587f83e6358c2dcca6b4e1050d78d89dc6ae0d2bee3f020e7856d2fd`  
		Last Modified: Mon, 22 Jan 2024 19:44:57 GMT  
		Size: 16.6 KB (16645 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:9283559711e73b3b4d13e796c5351b3fc9d636c807ca43a431b4240afb68f7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49734470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fe05d61b81f363c0a7f428081a810ccb03964f5cb6c83bfb06da63ed2a7c16`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5f2d303289ff6605957a6c86c67a1dd0cf7c3fb8455b2507d220775adfd096`  
		Last Modified: Fri, 12 Jan 2024 20:40:01 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe54e19ebb4048fa5d13fbfcfdbec635ada592f7650831653ef069b4e95f58a`  
		Last Modified: Sat, 13 Jan 2024 08:52:06 GMT  
		Size: 25.0 MB (25016077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909033011bbce360918910874e92e87422108eb8d2da635e94db9379a5e36449`  
		Last Modified: Sat, 13 Jan 2024 08:52:04 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:18cb1cc6ce525b2078204f22cb77cd2432e7c77c2440f9619f4634e16c2e4548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b2cabcd4b1b819b85331a78ce7c0abb8ccce543842280ac04402692dbcc95e`

```dockerfile
```

-	Layers:
	-	`sha256:1ebbaaeb09c7e54693b14f458383f20317c5219e5b222a12006842c9cbacfc71`  
		Last Modified: Sat, 13 Jan 2024 08:52:05 GMT  
		Size: 3.2 MB (3206181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3856a11614a323b33c85a49ea39ad5897b3ff8940749f77c1dc66c567d6e652d`  
		Last Modified: Sat, 13 Jan 2024 08:52:04 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:36a8fc55fb78ea3aaf97fe807e55361ceb5213ed55b5833d3e3770d3c8f2ed5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56644897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8accd66c4f3f9a1a24521f9212d9d8810d4c54e58bfb1ed08c02992c134f681`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ea23939bd3b30b5813dec02bedfb73a5045ccc956bbe0e941e42c2e6e40f73`  
		Last Modified: Fri, 12 Jan 2024 09:59:33 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7275ea1b57313c34ce68ce62d6ccb66a33fcaf9e14c279da7f5cc0ade4540d1d`  
		Last Modified: Mon, 22 Jan 2024 19:41:35 GMT  
		Size: 27.5 MB (27487295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda0d4bb2281dfc7d93276ff0d2295651ba053eac8ab061872308b9f8c23fe31`  
		Last Modified: Mon, 22 Jan 2024 19:41:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:0d42e0069a071892e0eb24c277b85a6000da9dff559df475b453ac482d143be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3223362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c003a12a86395109e9d689cca381643bdacf1a23183be5769e30033a7aaa0d`

```dockerfile
```

-	Layers:
	-	`sha256:df4c66e4626cbee0f533b60625eb74e462353d7499c2f436f4de56f722e9fceb`  
		Last Modified: Mon, 22 Jan 2024 19:41:34 GMT  
		Size: 3.2 MB (3206788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d208f2779382f7f8e5441ffbc68cd0a6cda95f1e6d2ffbc0732422859a43f6`  
		Last Modified: Mon, 22 Jan 2024 19:41:34 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; 386

```console
$ docker pull perl@sha256:37ddaf4a490c62f7e60030643995396d8845b8cd08ab590c1597d7dffa83a88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57841652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d9c142282bf13c7ad26076730812134097a76a0dce7a16333a26e10a50ee67`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:39 GMT
ADD file:48689786b7812032adc0d36643501f16ddee15750a8f0f8b614dba58e5037b2b in / 
# Thu, 11 Jan 2024 02:38:40 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:de2bfe459016bec412fddc313b793adc6d47c8a4540608a6f3e217998027f073`  
		Last Modified: Thu, 11 Jan 2024 02:43:20 GMT  
		Size: 30.1 MB (30143875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3178d50e54df6a537dc0b66f24a6d9bcaf8954e54990c8c70e2f9073bac0e51f`  
		Last Modified: Mon, 22 Jan 2024 19:04:54 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2d14184302192cb2ffd5ad85a73aa8e21942354cc4b95a43328b1abb1bacb`  
		Last Modified: Mon, 22 Jan 2024 19:04:56 GMT  
		Size: 27.7 MB (27697510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed83cb5cd25f0da978cf3ed3ee5a4d6814253750a71cd7a6f82434b126cf279`  
		Last Modified: Mon, 22 Jan 2024 19:04:54 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:7a8967738cf1a8e7a34c07da213f2d2c5ebb8987705bbbe13a6806877b969975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3242607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c80571e3336208151822e12606503c37295fa533daf434bf638126d3a993ffd`

```dockerfile
```

-	Layers:
	-	`sha256:cee21b95397f653d8ae6519ea76e46388ac3f440f1c7b8a0d21ac2677d13eb61`  
		Last Modified: Mon, 22 Jan 2024 19:04:54 GMT  
		Size: 3.2 MB (3225919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc30fa711c9fb217cbb1727e34bd5efbb836c0bc34cbce32a6f8cd867cb438ff`  
		Last Modified: Mon, 22 Jan 2024 19:04:54 GMT  
		Size: 16.7 KB (16688 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; mips64le

```console
$ docker pull perl@sha256:6490b6c2bd103f25dc198c2e898750e1c44f966fccc9816b79db97cab14a55fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55973624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f62a6931879d5e1d608786938f726894cbc5feb294b597b87bbfd662baa3633`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:61bc6da4a8a8247e6b88cf149051dbb04a6a5e6e1ffc5da16a85d1b4f24be297 in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:4f1541106f1f6cee2d65a870d8d3fbbaef35e04dbcb8abaa9623a9f7137a6ae5`  
		Last Modified: Thu, 11 Jan 2024 02:22:46 GMT  
		Size: 29.1 MB (29121397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dcd18743c2f4e0070ca9d8d5b7b8ac5f7f8d405be3530d395ba2aaf9a787a8`  
		Last Modified: Fri, 12 Jan 2024 05:57:01 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc10227cedfb11ca81d0c856e262f3525dbcd8b46c08ccc71dfe64a0c3682da`  
		Last Modified: Fri, 12 Jan 2024 15:08:58 GMT  
		Size: 26.9 MB (26851958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98ba15b15a07cd84deb1b26806259772e6a2e2f2bf7d69d885e0ca0a723fc87`  
		Last Modified: Fri, 12 Jan 2024 15:08:55 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:4618390b783dbd3821b4cfad66a09cd2b0af16d9d650dfd178e7197fe921074d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 KB (16414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d76e0147d10be84b14df6e61a24c42770baf0897f44b93615001c00367e4b5`

```dockerfile
```

-	Layers:
	-	`sha256:01646688fd5e432822fb447e1b6c0cb9aef774bb6e364d8f89de7755d39fa241`  
		Last Modified: Fri, 12 Jan 2024 15:08:55 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; ppc64le

```console
$ docker pull perl@sha256:e974bb434d6fa355521ae161e772777a8553d40808be8f89305d017855b3327a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62375419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60cd9632806035a9c1715feef2136de7fd514bbd9bc483e026b797a243bb4ce`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:27 GMT
ADD file:fcbdad385ae78401c4f5aebfeed9ba8edc6adcc9870a328a756cef32458e50ca in / 
# Thu, 11 Jan 2024 02:34:31 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:5d34c3dd8c95d308ec07fd694f24411653403413305af18811f2d53cc052f152`  
		Last Modified: Thu, 11 Jan 2024 02:39:25 GMT  
		Size: 33.1 MB (33120536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f672263b4dcb09c8e02ace9429c79c1dcaad80ea87d90b00d95240adaa85f29c`  
		Last Modified: Fri, 12 Jan 2024 10:12:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f462ef92787e5275a07382c32f5cd1ef96dfbd8cb895d381d1eb6d0c01697d9e`  
		Last Modified: Mon, 22 Jan 2024 19:37:23 GMT  
		Size: 29.3 MB (29254615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e18dc3783a15d8bc2aea015bd55fd346795d77f38b3eb0bc335d2120741d646`  
		Last Modified: Mon, 22 Jan 2024 19:37:22 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:61f743432219589903bfe49a3de302939ddcd1dbb26caddf2a485c4ad26293e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3236777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1963dfc908442363b75de95b0073ffcd0e434ad06cf408c6516668d0e9d6e540`

```dockerfile
```

-	Layers:
	-	`sha256:6d666e3b0716327b5702fa6db432b1c4254b6022a0847275cd848ba5b7d281c6`  
		Last Modified: Mon, 22 Jan 2024 19:37:22 GMT  
		Size: 3.2 MB (3220167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d45ba4ede3456704a5c5310eafb9b577cca60d81cbc80ddce86690580036f5e`  
		Last Modified: Mon, 22 Jan 2024 19:37:22 GMT  
		Size: 16.6 KB (16610 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; s390x

```console
$ docker pull perl@sha256:3824a8bfe5499f25998b8e2163b2b0fe482fd5ea74b03317d0b6caea9c418ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54719691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb920e3b883f220a30127bd7c4c1c1259de19511e19af1d2e1108e08eab11fa9`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0a331710561d1b0c32cf5ae4729c6bdc67cee4991756dcad73317924da1d9e`  
		Last Modified: Fri, 12 Jan 2024 10:51:21 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c05b119a269da466ca86f347e0864ebcb1fdb705841d8a079f0bb1abe23bca`  
		Last Modified: Fri, 12 Jan 2024 13:40:45 GMT  
		Size: 27.2 MB (27227573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e491f4ad14d87b5f74b239267fb01730355ba94369fee10d4738661e1cbdad`  
		Last Modified: Fri, 12 Jan 2024 13:40:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:23a2a46465cac4a26dbf6db7da28be766f6118697e4a32240f38add4c2373ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3237697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8c4ae035496abfa98ac20ea2e6c0ababbb8ee08e711708098dd5b2302702c0`

```dockerfile
```

-	Layers:
	-	`sha256:ca8cd38164403223ca41c1973b64bd24bfa59baae0b56b270ce9b0707e85d20a`  
		Last Modified: Fri, 12 Jan 2024 13:40:44 GMT  
		Size: 3.2 MB (3221144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57c61e54b8b03d068eb75863755c316c391566f3255680f8384123f54c545e1`  
		Last Modified: Fri, 12 Jan 2024 13:40:44 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json
