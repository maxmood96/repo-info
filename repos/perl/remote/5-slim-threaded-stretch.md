## `perl:5-slim-threaded-stretch`

```console
$ docker pull perl@sha256:5e4432a7e86a87274a5e7fe7beef3bfb8fb5f67639974953c8d4d7912e0f55e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:5-slim-threaded-stretch` - linux; amd64

```console
$ docker pull perl@sha256:5ded00283aa4d623f663f6237b3a9468b55ce50ab54413f5670b3fb2157b2826
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37175239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a1f6c6ad0a83130788875b0b1a5a3ba36093a62000b77e9c22f948e54d3b54`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 10:27:27 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 03 Sep 2021 10:27:28 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 03 Sep 2021 10:27:28 GMT
WORKDIR /usr/src/perl
# Fri, 03 Sep 2021 11:15:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 03 Sep 2021 11:15:51 GMT
WORKDIR /
# Fri, 03 Sep 2021 11:15:51 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114effe01cdd1e99382416cc7b1989d8cc827b3c32523c8542c499862a94e5c9`  
		Last Modified: Fri, 03 Sep 2021 12:50:13 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d475316a96a135105460a9b3efb826d2ca2ff5ae59008561372226a6f477ca09`  
		Last Modified: Fri, 03 Sep 2021 12:51:32 GMT  
		Size: 14.6 MB (14647612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-threaded-stretch` - linux; arm variant v7

```console
$ docker pull perl@sha256:7f0470c68188d82d85c50c58cf1a5224078dcd95781ed8cf4c52ac9b7e87420e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33077194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087ca7aa176f834af9d4fb4f4f47e46afa96590b5af8f1901454eaa99da347f6`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 10:30:49 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 03 Sep 2021 10:30:49 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 03 Sep 2021 10:30:50 GMT
WORKDIR /usr/src/perl
# Fri, 03 Sep 2021 11:27:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 03 Sep 2021 11:27:46 GMT
WORKDIR /
# Fri, 03 Sep 2021 11:27:47 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6820ef61f46bf8b6d3a37755deec9fcdb378f73b4e1c3eb475781d6d563f850`  
		Last Modified: Fri, 03 Sep 2021 13:11:07 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c694dd8d9403f8943185c267dd42e94915029b64d15e30a1f5f1741c8a97cb7a`  
		Last Modified: Fri, 03 Sep 2021 13:13:32 GMT  
		Size: 13.8 MB (13760893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-threaded-stretch` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:a58094a7570ea3d4ac883067022833bc4c3ffd377b151cec8f594e3e9af2a373
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34824081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cda25bffb2bacd3f3757b454422c58076e6362ca505effbacaa6eff750b57b`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:48 GMT
ADD file:f45934b05bd47c443a0ac02ba0771c25002763d29eb9f8ae723980605ff6f091 in / 
# Fri, 03 Sep 2021 00:42:48 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:11:38 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 03 Sep 2021 03:11:38 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 03 Sep 2021 03:11:39 GMT
WORKDIR /usr/src/perl
# Fri, 03 Sep 2021 03:31:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 03 Sep 2021 03:31:47 GMT
WORKDIR /
# Fri, 03 Sep 2021 03:31:47 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:bafcab9e99462b57e2818f0017c17049cc46e69473e9d80342344f7116f32e83`  
		Last Modified: Fri, 03 Sep 2021 00:53:26 GMT  
		Size: 20.4 MB (20389506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797e9a406a3185a8310015dabdc2fdb957a199c8c505d9587d321706c2ba64a2`  
		Last Modified: Fri, 03 Sep 2021 04:02:15 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31ac19a9040c135dda0fc01ee112f3bee3dc56d73a078173d14499627966141`  
		Last Modified: Fri, 03 Sep 2021 04:03:09 GMT  
		Size: 14.4 MB (14434373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-threaded-stretch` - linux; 386

```console
$ docker pull perl@sha256:8c44eb2940615424072056666b8ef46d0c3cae77ea9dbcc459b6458d9457db2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37345484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641578949aef820270fce72c724583a699fbee845cd89925376d40c9cf0b2ac2`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:46 GMT
ADD file:6c8a44184bf1d38b16f52d58ecb80d627ab86fce72a78b094170535fe1f76ad0 in / 
# Fri, 03 Sep 2021 00:42:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 13:28:33 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 03 Sep 2021 13:28:33 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 03 Sep 2021 13:28:34 GMT
WORKDIR /usr/src/perl
# Fri, 03 Sep 2021 14:23:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 03 Sep 2021 14:23:26 GMT
WORKDIR /
# Fri, 03 Sep 2021 14:23:26 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:0b43614231856f083f6dc06bd012a7ac7ff26410a945ea25d4c887e8218a878c`  
		Last Modified: Fri, 03 Sep 2021 00:53:23 GMT  
		Size: 23.2 MB (23156443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1830d404b40d8957f37647f37cc3d69ca81f55d895279bdaa8786f66b6addd7`  
		Last Modified: Fri, 03 Sep 2021 15:54:01 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a5a44d021037bf6d36ff5159fa7ccdb1e3487f72efa99d039236299b69ed2a`  
		Last Modified: Fri, 03 Sep 2021 15:55:44 GMT  
		Size: 14.2 MB (14188842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
