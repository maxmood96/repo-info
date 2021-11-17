## `perl:slim-threaded`

```console
$ docker pull perl@sha256:901fb89e7a432fb16f9621355fda13791b0641064195cec3d773e7dc35b94c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `perl:slim-threaded` - linux; amd64

```console
$ docker pull perl@sha256:ca43058bf37dbf0ef9e6a7446e3456622ae0b9a891c61d85d8a824fb77e2b1db
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46272244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efefa74e039218a5b99f5802021ddb11877ca1c018eb200a8a3b70457f6ce34`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:42 GMT
ADD file:16dc2c6d1932194edec28d730b004fd6deca3d0f0e1a07bc5b8b6e8a1662f7af in / 
# Tue, 12 Oct 2021 01:20:42 GMT
CMD ["bash"]
# Sat, 13 Nov 2021 12:19:48 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Sat, 13 Nov 2021 12:19:48 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Sat, 13 Nov 2021 12:19:48 GMT
WORKDIR /usr/src/perl
# Sat, 13 Nov 2021 12:45:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Sat, 13 Nov 2021 12:45:59 GMT
WORKDIR /
# Sat, 13 Nov 2021 12:45:59 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:7d63c13d9b9b6ec5f05a2b07daadacaa9c610d01102a662ae9b1d082105f1ffa`  
		Last Modified: Tue, 12 Oct 2021 01:26:05 GMT  
		Size: 31.4 MB (31357311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c7f22d5b4bc3005e448f197d048661f5ddb2df2470503fd3157d1cf8ec09c1`  
		Last Modified: Sat, 13 Nov 2021 13:52:28 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8414a01b7a819dd60401a7613ec97acdac5882b0a1a182b3ba419e53769a5d`  
		Last Modified: Sat, 13 Nov 2021 13:53:31 GMT  
		Size: 14.9 MB (14914730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:090562bae084248e6cdea7d99cf4dcc4ddbfd313c9cf4b43d66dc1305b73785c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43089004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13e95ae40122a56c6a8e2d1a6b13c3d36fa7d319350aba2d9d04b3e6691a456`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Wed, 17 Nov 2021 02:50:37 GMT
ADD file:738a04a17bdb9077594ad9a847333abe28216a7f04d3058718a5e21c236c24bb in / 
# Wed, 17 Nov 2021 02:50:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 04:17:36 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 17 Nov 2021 04:17:37 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 17 Nov 2021 04:17:37 GMT
WORKDIR /usr/src/perl
# Wed, 17 Nov 2021 04:55:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 17 Nov 2021 04:55:35 GMT
WORKDIR /
# Wed, 17 Nov 2021 04:55:36 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:a960a56baa1baffbe2aa1e0c1fb02f9ee4816337d02fec259b312c409d77fafc`  
		Last Modified: Wed, 17 Nov 2021 03:06:09 GMT  
		Size: 28.9 MB (28911006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f10e5b46bbdb14f43b1547dd1c226f55ae00622486eab6ac1b84dbb528ad21b`  
		Last Modified: Wed, 17 Nov 2021 06:56:30 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6715068f8ef892cc708a54d11c8f7c5594d7d4c71b3affcb5d043f60c1b0e69`  
		Last Modified: Wed, 17 Nov 2021 06:58:17 GMT  
		Size: 14.2 MB (14177794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:e479bf8c25710cfd1958741bae8e1ad7d5266b3d31512e68069dfa1806f55062
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40542722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f181ac2da417cd154eead2244d047234a090b7bd0f1027645f6f713d916d5d01`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Tue, 12 Oct 2021 01:28:36 GMT
ADD file:89eac94007ac04f9168737686fa0a6c737f2c28fc9e5918d4d512924fe1973be in / 
# Tue, 12 Oct 2021 01:28:37 GMT
CMD ["bash"]
# Sat, 13 Nov 2021 13:16:07 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Sat, 13 Nov 2021 13:16:07 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Sat, 13 Nov 2021 13:16:08 GMT
WORKDIR /usr/src/perl
# Sat, 13 Nov 2021 13:49:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Sat, 13 Nov 2021 13:49:53 GMT
WORKDIR /
# Sat, 13 Nov 2021 13:49:54 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:4e5300249f84466df4dc73ea0ce09938ca00c1718bb12619c4f26bd936162331`  
		Last Modified: Tue, 12 Oct 2021 01:44:28 GMT  
		Size: 26.6 MB (26561058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e79c02b4d6d870290e891b1107f3b5d00c3294887365e4955e4e9da733d709`  
		Last Modified: Sat, 13 Nov 2021 15:28:28 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51e910516e501a6ddf268eb47405b02abb29a35c7747389a49c39588daa989a`  
		Last Modified: Sat, 13 Nov 2021 15:30:29 GMT  
		Size: 14.0 MB (13981461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:eb33377a8d631240994f96231d81731922045ffc3fdb8bf77841b4d442a892cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44900790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2e41bb1789809c9c8eac35187f17e1c366fea42ed9045c7270e0527c6fa7df`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:15 GMT
ADD file:4203242b2b09a65239092c4780b59181da7b861b3c0be40810b3588aa200f72c in / 
# Wed, 17 Nov 2021 02:40:16 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 05:10:47 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 17 Nov 2021 05:10:49 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 17 Nov 2021 05:10:49 GMT
WORKDIR /usr/src/perl
# Wed, 17 Nov 2021 05:25:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 17 Nov 2021 05:25:48 GMT
WORKDIR /
# Wed, 17 Nov 2021 05:25:49 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:eb9a2845ed124d072b117aba4f0508e00c1ecd0d147dc324d14b00d24092046c`  
		Last Modified: Wed, 17 Nov 2021 02:47:17 GMT  
		Size: 30.1 MB (30056521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01219708c0968331386e45c214a2b97d25eefca249e026278020bd7f4d9fcc5`  
		Last Modified: Wed, 17 Nov 2021 06:14:07 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40f4ff533c55e35d52dbbce564a2daea4b839fae7a475e218c24621da7f5a6c`  
		Last Modified: Wed, 17 Nov 2021 06:15:10 GMT  
		Size: 14.8 MB (14844089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-threaded` - linux; 386

```console
$ docker pull perl@sha256:117f2416becdeec09054b1a4ab15d5c68b70b4f93afcde0151a7995945f6704c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46815201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922757e9d98ad00b4c1784c640ae2eec20ec26c35c29ea3c2d04d93f0456ebb4`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Wed, 17 Nov 2021 02:39:53 GMT
ADD file:ff018048717c0f5aa1730480d0bfea1c2bf94d6e2dae2d7cef46d05ffb0d93e1 in / 
# Wed, 17 Nov 2021 02:39:53 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 06:32:00 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 17 Nov 2021 06:32:01 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 17 Nov 2021 06:32:01 GMT
WORKDIR /usr/src/perl
# Wed, 17 Nov 2021 07:16:29 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 17 Nov 2021 07:16:30 GMT
WORKDIR /
# Wed, 17 Nov 2021 07:16:30 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:0bae0e1d4cb1d56ffeb9d05de7a097d3157267eef07b6d8131344d99bd97c431`  
		Last Modified: Wed, 17 Nov 2021 02:47:49 GMT  
		Size: 32.4 MB (32380683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb715e02750e3ab8a4d14193d1ea579b80018dcf478d50eb7b18dae5bad3897`  
		Last Modified: Wed, 17 Nov 2021 09:10:27 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81664c503fb64ee0d98b4a73b879eff884860f421d55a015aeaa330e93d049a1`  
		Last Modified: Wed, 17 Nov 2021 09:11:38 GMT  
		Size: 14.4 MB (14434314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-threaded` - linux; mips64le

```console
$ docker pull perl@sha256:f1609ccd623613755727346c8ff4ad8844025b53480238bb52a4fe5fcf9c3db6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43807718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d19b0c3a08ee4955a33060556ecd931ceeeda1247bb11d4fa876b6f356361fe`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Tue, 12 Oct 2021 01:11:15 GMT
ADD file:f90ca8957172106f42a9096c9a21082d51f3201aa78e6f64621a73117e2b7b6a in / 
# Tue, 12 Oct 2021 01:11:16 GMT
CMD ["bash"]
# Fri, 12 Nov 2021 20:48:33 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 12 Nov 2021 20:48:33 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 12 Nov 2021 20:48:34 GMT
WORKDIR /usr/src/perl
# Fri, 12 Nov 2021 22:29:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 12 Nov 2021 22:29:32 GMT
WORKDIR /
# Fri, 12 Nov 2021 22:29:32 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:59ddca50ce05605e6234c1e7213c39cdedabc48ef11637e12156b7bd69afe161`  
		Last Modified: Tue, 12 Oct 2021 01:20:03 GMT  
		Size: 29.6 MB (29618732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28fe078d247dad664c103dc32037e5122f49446fa1864007a3364fb68178387`  
		Last Modified: Sat, 13 Nov 2021 04:02:22 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ec5f8b23ece5503341133178136fc8c18b8c08d1798437504e957c580967a0`  
		Last Modified: Sat, 13 Nov 2021 04:04:46 GMT  
		Size: 14.2 MB (14188809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:98e4276e127df604497abbc4d523e77337ae9ad2f1d87f1d116f3b9dda25e557
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50231324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38d6f024982be813b223fe925e99e3c3e309b5459f1bf88d55d82202e69d801`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Tue, 12 Oct 2021 01:25:45 GMT
ADD file:d8794fadf16c9948c3574ba28740d08393eca57766340333ad91f9c2a33eb719 in / 
# Tue, 12 Oct 2021 01:25:53 GMT
CMD ["bash"]
# Fri, 12 Nov 2021 23:16:51 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 12 Nov 2021 23:16:53 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 12 Nov 2021 23:16:55 GMT
WORKDIR /usr/src/perl
# Fri, 12 Nov 2021 23:43:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 12 Nov 2021 23:44:08 GMT
WORKDIR /
# Fri, 12 Nov 2021 23:44:13 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:6c28c1405c677dd809094d06190225b38cee3d24f18da38d287ef5bcc67884d6`  
		Last Modified: Tue, 12 Oct 2021 01:37:00 GMT  
		Size: 35.3 MB (35258729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b1371965ee604f32c7ad3a1fd03776c4c61a5060e0c4d3a2086de51645e838`  
		Last Modified: Sat, 13 Nov 2021 00:59:52 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ace03aa82140da61b13d490201a9dc6058d13e173c580f613a392301dae9ae`  
		Last Modified: Sat, 13 Nov 2021 01:01:06 GMT  
		Size: 15.0 MB (14972390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-threaded` - linux; s390x

```console
$ docker pull perl@sha256:27a3437afa1367c6b1c756ea5a4b0cac42668dd610f69a24284ab3adee857082
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44915475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba13378d4576931ac9d435a4f2a3e272ec679ab644fc3f6a37c2b24a620bd221`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:27 GMT
ADD file:42f73dac307a6a5232e3100f3d3b36e8125f73a4ca504b106e60e2b66d242b2f in / 
# Wed, 17 Nov 2021 02:42:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 10:02:29 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 17 Nov 2021 10:02:29 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 17 Nov 2021 10:02:29 GMT
WORKDIR /usr/src/perl
# Wed, 17 Nov 2021 10:30:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 17 Nov 2021 10:30:49 GMT
WORKDIR /
# Wed, 17 Nov 2021 10:30:49 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:8d71e885edf612b507bbdcc48a970548d436b8709eeedfc2c98f6843a214b5e2`  
		Last Modified: Wed, 17 Nov 2021 02:48:25 GMT  
		Size: 29.7 MB (29650960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21df39bcbc372f2d6a01cedf58da2406111968fb5b069f09eef47155d0e8bde`  
		Last Modified: Wed, 17 Nov 2021 11:59:50 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b7368230b07e74b78c80e2a59ec9b644580767f35a7a06da5fd0d39b135b73`  
		Last Modified: Wed, 17 Nov 2021 12:00:58 GMT  
		Size: 15.3 MB (15264313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
