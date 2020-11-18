## `perl:5-slim-stretch`

```console
$ docker pull perl@sha256:b7bc9697bbf40103d29fa6e02c4b6f2bb0a5ae0b728789745cac83ec7c95c77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `perl:5-slim-stretch` - linux; amd64

```console
$ docker pull perl@sha256:194bb69ac84b0dc6a96478044ecdcd58c909e574b2bece055d9acb594a5ad9f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37118905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a90c4310fa8a85f341fe446cdc3544e0bf6b99bb39d3e414c9fd7cb812d790d`
-	Default Command: `["perl5.32.0","-de0"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:29 GMT
ADD file:02294bc9e72a3f3314955f0b5e0e728cd75321e88a1fae9bfbac77c76bfaf05d in / 
# Tue, 17 Nov 2020 20:24:29 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 01:33:30 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 18 Nov 2020 01:33:31 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 18 Nov 2020 01:33:31 GMT
WORKDIR /usr/src/perl
# Wed, 18 Nov 2020 01:43:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.0.tar.xz -o perl-5.32.0.tar.xz     && echo '6f436b447cf56d22464f980fac1916e707a040e96d52172984c5d184c09b859b *perl-5.32.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.0.tar.xz -C /usr/src/perl     && rm perl-5.32.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 18 Nov 2020 01:43:38 GMT
WORKDIR /
# Wed, 18 Nov 2020 01:43:39 GMT
CMD ["perl5.32.0" "-de0"]
```

-	Layers:
	-	`sha256:4297e02295585beb3f148a5740b644ce87e059455f8d98a5adb7bf95105e011c`  
		Last Modified: Tue, 17 Nov 2020 20:30:42 GMT  
		Size: 22.5 MB (22527663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53fab9999a3a6392c744462dd51d02baba9a354e99a60ef0c9eead37a01a203`  
		Last Modified: Wed, 18 Nov 2020 05:53:31 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28ed577b7c5cd72585f3dd5c0d95e939441bc6109b00923c1f4f86bcc854cab`  
		Last Modified: Wed, 18 Nov 2020 05:53:34 GMT  
		Size: 14.6 MB (14591066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-stretch` - linux; arm variant v7

```console
$ docker pull perl@sha256:74d989383f3ed9d863929c230531063557d80c2041ce8d34c31af40a235c8c1d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33052508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb384ac2a9379b12d6df0be51caece59f6bffbb16737007d862b65e03367598`
-	Default Command: `["perl5.32.0","-de0"]`

```dockerfile
# Tue, 17 Nov 2020 20:27:23 GMT
ADD file:de081793a94d15fb89877812e1c838c9e3836070e36a6fb7f01b858a884b6680 in / 
# Tue, 17 Nov 2020 20:27:24 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:59:48 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 18 Nov 2020 08:59:50 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 18 Nov 2020 08:59:51 GMT
WORKDIR /usr/src/perl
# Wed, 18 Nov 2020 09:11:49 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.0.tar.xz -o perl-5.32.0.tar.xz     && echo '6f436b447cf56d22464f980fac1916e707a040e96d52172984c5d184c09b859b *perl-5.32.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.0.tar.xz -C /usr/src/perl     && rm perl-5.32.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 18 Nov 2020 09:11:52 GMT
WORKDIR /
# Wed, 18 Nov 2020 09:11:52 GMT
CMD ["perl5.32.0" "-de0"]
```

-	Layers:
	-	`sha256:a97dc136886474245bdc5c70c58e70e18fc55d193dae8225f0543e0b500b484a`  
		Last Modified: Tue, 17 Nov 2020 20:35:46 GMT  
		Size: 19.3 MB (19313228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab63dd8e169a82553bd088a9722b164b0c3b2e64ba87974cb69591a47ebf93ea`  
		Last Modified: Wed, 18 Nov 2020 12:38:12 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bac06df9c52c96a34411f972bddf5ad793e1a17f8f8c8db9f1f5b909939a437`  
		Last Modified: Wed, 18 Nov 2020 12:38:18 GMT  
		Size: 13.7 MB (13739079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-stretch` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:96f7baa0fa3124870f64ccef1df09312566cbbcb5d5c7748e6839dc13ca4b2b6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34787891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f32b6e14319986e06fbdf4f2b15c10517e37349b935a14a67878f87ad495a0`
-	Default Command: `["perl5.32.0","-de0"]`

```dockerfile
# Tue, 17 Nov 2020 20:28:08 GMT
ADD file:b5b22f625d299254bffe6243b53eb5867cecdaab5c226e41411fa55763587755 in / 
# Tue, 17 Nov 2020 20:28:10 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 12:28:32 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 18 Nov 2020 12:28:42 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 18 Nov 2020 12:29:01 GMT
WORKDIR /usr/src/perl
# Wed, 18 Nov 2020 12:45:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.0.tar.xz -o perl-5.32.0.tar.xz     && echo '6f436b447cf56d22464f980fac1916e707a040e96d52172984c5d184c09b859b *perl-5.32.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.0.tar.xz -C /usr/src/perl     && rm perl-5.32.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 18 Nov 2020 12:45:39 GMT
WORKDIR /
# Wed, 18 Nov 2020 12:45:40 GMT
CMD ["perl5.32.0" "-de0"]
```

-	Layers:
	-	`sha256:f37c1cd284d6b059670ae5ae080ea2b30b095b4328a6580f4f0d90ef0da06b9a`  
		Last Modified: Tue, 17 Nov 2020 20:34:38 GMT  
		Size: 20.4 MB (20387780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad75425c232a238a447f95c86094b052cf1777980219de6b45e9ebeec3a04b7b`  
		Last Modified: Wed, 18 Nov 2020 16:13:12 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca57b09f88ad6554f24ee7498e281dd0107bea88b91821fff2e9ca54551c240`  
		Last Modified: Wed, 18 Nov 2020 16:13:17 GMT  
		Size: 14.4 MB (14399908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-stretch` - linux; 386

```console
$ docker pull perl@sha256:dd4a5add110e5cb4d11a6a1a7734d9276190a925930e350894d75ae9b217edc4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37238168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb11ef5b7a45d568dc9b2049ec9917e4ce630912fc02f5d350fa0b2d161ac3bd`
-	Default Command: `["perl5.32.0","-de0"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:25 GMT
ADD file:6d0d227a50cb77b9603ef598794fe0f583312a776daf61e7cd7e5493260354c9 in / 
# Tue, 17 Nov 2020 20:23:25 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:51:32 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 18 Nov 2020 07:51:33 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 18 Nov 2020 07:51:33 GMT
WORKDIR /usr/src/perl
# Wed, 18 Nov 2020 08:03:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.0.tar.xz -o perl-5.32.0.tar.xz     && echo '6f436b447cf56d22464f980fac1916e707a040e96d52172984c5d184c09b859b *perl-5.32.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.0.tar.xz -C /usr/src/perl     && rm perl-5.32.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 18 Nov 2020 08:03:21 GMT
WORKDIR /
# Wed, 18 Nov 2020 08:03:21 GMT
CMD ["perl5.32.0" "-de0"]
```

-	Layers:
	-	`sha256:657537e4548aa71eaa79344d36c62360306a66e11486f3d90ce21ecef49a62cb`  
		Last Modified: Tue, 17 Nov 2020 20:30:22 GMT  
		Size: 23.2 MB (23154739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64b77b89bcb46f661c77301eaa530b6e783fe07d3bb2413ed1f41906305c316`  
		Last Modified: Wed, 18 Nov 2020 12:33:02 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694ac0c6290fa4c0e5cadc8c5adfe18c29853a8bf9fdd0ac7342df2b7f85f4b0`  
		Last Modified: Wed, 18 Nov 2020 12:33:07 GMT  
		Size: 14.1 MB (14083252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-stretch` - linux; ppc64le

```console
$ docker pull perl@sha256:ef09d2eb473c046e6c9f8098b3a7fef9875dfbba0740aa4ed68e13433e884eb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37221053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6939da09b4685b49a0814e877fbcf985bc2a23ba434c4e52ba6c01c6c5c0f2`
-	Default Command: `["perl5.32.0","-de0"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 14:27:23 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Mon, 22 Jun 2020 15:40:21 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Mon, 22 Jun 2020 15:40:24 GMT
WORKDIR /usr/src/perl
# Mon, 22 Jun 2020 15:49:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.0.tar.xz -o perl-5.32.0.tar.xz     && echo '6f436b447cf56d22464f980fac1916e707a040e96d52172984c5d184c09b859b *perl-5.32.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.0.tar.xz -C /usr/src/perl     && rm perl-5.32.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Mon, 22 Jun 2020 15:49:49 GMT
WORKDIR /
# Mon, 22 Jun 2020 15:49:52 GMT
CMD ["perl5.32.0" "-de0"]
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0789a92ac122eecdf7b0bd168e70ec21062493b4fa3617f62eb7fd387e9d6780`  
		Last Modified: Mon, 22 Jun 2020 16:28:33 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b51e098d1488dc904c2ad47c4125a22de29c445c6aaad9ad48c920949933f27`  
		Last Modified: Mon, 22 Jun 2020 16:28:38 GMT  
		Size: 14.4 MB (14429582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-stretch` - linux; s390x

```console
$ docker pull perl@sha256:7146bba14d71cdce8bd1c0461d2c192371c8bab9d849016c1aa3c3ed830cdff4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37421460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2901811c2c8c82b4620055bacd2a71b4b7ceeba35e57cc4a5d216e4ef95038`
-	Default Command: `["perl5.32.0","-de0"]`

```dockerfile
# Tue, 09 Jun 2020 01:44:20 GMT
ADD file:b3e01a52177029e9c3ba14a708f5dd33a38777f05d0e43656aca742b2991b13c in / 
# Tue, 09 Jun 2020 01:44:22 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:04:12 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Mon, 22 Jun 2020 16:00:38 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Mon, 22 Jun 2020 16:00:39 GMT
WORKDIR /usr/src/perl
# Mon, 22 Jun 2020 16:07:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.0.tar.xz -o perl-5.32.0.tar.xz     && echo '6f436b447cf56d22464f980fac1916e707a040e96d52172984c5d184c09b859b *perl-5.32.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.0.tar.xz -C /usr/src/perl     && rm perl-5.32.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Mon, 22 Jun 2020 16:07:18 GMT
WORKDIR /
# Mon, 22 Jun 2020 16:07:19 GMT
CMD ["perl5.32.0" "-de0"]
```

-	Layers:
	-	`sha256:428ea12d5f095d89f941ce335d5f799da515abfd0c161e7ee85e12cd3d97fd4e`  
		Last Modified: Tue, 09 Jun 2020 01:48:04 GMT  
		Size: 22.4 MB (22371004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bda422b0ebe5506ce35e51f433e6f95412877201e00691a90070ae6509418a6`  
		Last Modified: Mon, 22 Jun 2020 16:32:54 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d20fd97473b0068f2b823519fb8126c13e9f5b7477ff0785d497bb4d1e37bb`  
		Last Modified: Mon, 22 Jun 2020 16:32:56 GMT  
		Size: 15.1 MB (15050254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
