## `perl:5-slim-stretch`

```console
$ docker pull perl@sha256:afbf99a02ba0eab67562e6feadfed3e0b01abaf177c2b40a82f47391b5cb4b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:5-slim-stretch` - linux; amd64

```console
$ docker pull perl@sha256:5c38ca1b5fcea6426aa912208eeeb2795f6de9d6cd91c5df2c233335453e7438
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37119692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ec2b4534765ad9b7aa9252bff938455474518f5a787c814ab112ac0860e6c`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:30 GMT
ADD file:c7a3b8a1e87bedfb6605855ad703321050112d02c9925ece42f4111d7a42cdd0 in / 
# Tue, 28 Sep 2021 01:25:30 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 11:10:00 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 28 Sep 2021 11:10:00 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Tue, 28 Sep 2021 11:10:01 GMT
WORKDIR /usr/src/perl
# Tue, 28 Sep 2021 11:20:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 28 Sep 2021 11:20:30 GMT
WORKDIR /
# Tue, 28 Sep 2021 11:20:31 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:36d925ed8e305498a951c3b56d100d153ae3babf046b88e2d00899105fe81c31`  
		Last Modified: Tue, 28 Sep 2021 01:32:51 GMT  
		Size: 22.5 MB (22527699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262fe9a6122bcb2cd3d47fa19864a97d91c4b136623ec82d707ec004c08caeab`  
		Last Modified: Tue, 28 Sep 2021 13:34:00 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e4f6637fab81dd464ed8d17ed70c63c3857d84034a4df4be4789eac726a935`  
		Last Modified: Tue, 28 Sep 2021 13:34:03 GMT  
		Size: 14.6 MB (14591790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-stretch` - linux; arm variant v7

```console
$ docker pull perl@sha256:39795b6d9f368237992d084d3057b952745bfcfcae394c4b689de2d1f753d4ed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33047528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa97ac8a2ae5ab0790fb9493a54917597fbbba7e1c31c73bb9641930df740900`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Thu, 30 Sep 2021 18:09:32 GMT
ADD file:a037f8ced10b72f1e0d62328b77376ea1efe206b6116e858b7a641d26fd5b1b0 in / 
# Thu, 30 Sep 2021 18:09:33 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 12:31:03 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 01 Oct 2021 12:31:03 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 01 Oct 2021 12:31:04 GMT
WORKDIR /usr/src/perl
# Fri, 01 Oct 2021 12:42:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 01 Oct 2021 12:42:57 GMT
WORKDIR /
# Fri, 01 Oct 2021 12:42:58 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:fce8291cdcf067da304d19441e493cb62fd5be1dcc768569fdeb1e0db374c983`  
		Last Modified: Thu, 30 Sep 2021 18:26:53 GMT  
		Size: 19.3 MB (19316455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d57e3fc1648a463d86a2d335584b0bb6a6827b20a585bcae9a7f55284c64615`  
		Last Modified: Fri, 01 Oct 2021 15:11:49 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c8ef34c6241e32adf178763f66e5fec58bcef98ee59cd8dc7957e33c01e80`  
		Last Modified: Fri, 01 Oct 2021 15:12:02 GMT  
		Size: 13.7 MB (13730871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-stretch` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:f02871d8790193e60bd4e65b23a9714bc447637232236ebeb69e95425652dd59
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34793641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c6282611506938d7d079bb15ed4d4ebbd26ec4544807525d2ef4ada1ad0db9`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Tue, 28 Sep 2021 01:43:26 GMT
ADD file:be175324382a4d494cf1f644f77b27f17829f187478f9eed602be03b358ffbdc in / 
# Tue, 28 Sep 2021 01:43:27 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:06:29 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 28 Sep 2021 07:06:29 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Tue, 28 Sep 2021 07:06:30 GMT
WORKDIR /usr/src/perl
# Tue, 28 Sep 2021 07:12:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 28 Sep 2021 07:12:30 GMT
WORKDIR /
# Tue, 28 Sep 2021 07:12:30 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:754614322eeee5db75df451bbdaf75a2049b3ffb0bbcc404a80770f454125583`  
		Last Modified: Tue, 28 Sep 2021 01:52:52 GMT  
		Size: 20.4 MB (20389432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3076053f00f6e7fd6d273bb606348478d7279d2aab04cad3c3d22c97a08bab2f`  
		Last Modified: Tue, 28 Sep 2021 08:35:51 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5c7f6a9cbb660d9a99beb0c95347a754849dd98bc50e09f24dadf8b337757b`  
		Last Modified: Tue, 28 Sep 2021 08:35:55 GMT  
		Size: 14.4 MB (14404007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-stretch` - linux; 386

```console
$ docker pull perl@sha256:73bdb01207de1bf0bf383ce00f8bc748e0cfaf6f624122923621d932812e7dc8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37244942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c50f64fc8151b09dbcf802128ebbffea7672150173833202c6acf272c95b7f`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Tue, 28 Sep 2021 01:43:39 GMT
ADD file:701bf587ade8c18fa108e900dd6f545e5c1aeb5fdbdd4fdd3a9b54bf2e38f478 in / 
# Tue, 28 Sep 2021 01:43:39 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:46:59 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 28 Sep 2021 09:47:00 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Tue, 28 Sep 2021 09:47:00 GMT
WORKDIR /usr/src/perl
# Tue, 28 Sep 2021 09:57:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 28 Sep 2021 09:57:19 GMT
WORKDIR /
# Tue, 28 Sep 2021 09:57:19 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:0952a5e9bdc54f828420f1481d98478c53df6eab6bf7b299f150d6b5481457d4`  
		Last Modified: Tue, 28 Sep 2021 01:54:01 GMT  
		Size: 23.2 MB (23156768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f14b345adedbff8904744724ed084252586234200c7071604866c2f07186b`  
		Last Modified: Tue, 28 Sep 2021 12:36:50 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f2e6651c152d7a40e47d501a88e65c8242137870ff4a774c9aba46673ca592`  
		Last Modified: Tue, 28 Sep 2021 12:36:55 GMT  
		Size: 14.1 MB (14087970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
