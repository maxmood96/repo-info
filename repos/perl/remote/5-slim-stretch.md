## `perl:5-slim-stretch`

```console
$ docker pull perl@sha256:c45f31ba57c1a4785f671935e3c175fef0302943958ae6e96a535742d3e1d50a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:5-slim-stretch` - linux; amd64

```console
$ docker pull perl@sha256:9a75bd0391dc86e25bb8db7124c03e1d80c53e2823ec85814ecf2e6b94cd36d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37119785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c58133e5f4e89245e174a3ed8830c4d703d97f39e8a823889b1058f99603d4`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 00:43:35 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Sat, 27 Mar 2021 00:43:35 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Sat, 27 Mar 2021 00:43:36 GMT
WORKDIR /usr/src/perl
# Sat, 27 Mar 2021 00:54:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Sat, 27 Mar 2021 00:54:00 GMT
WORKDIR /
# Sat, 27 Mar 2021 00:54:00 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2172cc2587258b47e43d0131c56a65489dbcd1664cd02b0d8cb1f2219940a9a9`  
		Last Modified: Sat, 27 Mar 2021 02:25:06 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862da7cfba0c5f224b8e961a561757eb9ea79779f6483fe2082c06a72d3ef027`  
		Last Modified: Sat, 27 Mar 2021 02:25:10 GMT  
		Size: 14.6 MB (14591181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-stretch` - linux; arm variant v7

```console
$ docker pull perl@sha256:4868c4865313dbf5667f5626f96127157c64e5e445ea26bced84b26aaf8982be
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33047516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf1ee3b29f3dc771c1168ac8cf114edd7580cabfa43ec7775652c4d0e700381`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Fri, 12 Mar 2021 02:05:43 GMT
ADD file:37f1c27246cb6d0d42be6f807f54c620cc083043d7395656a56178df89e5d6d9 in / 
# Fri, 12 Mar 2021 02:05:45 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 05:30:35 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 12 Mar 2021 05:30:35 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 12 Mar 2021 05:30:36 GMT
WORKDIR /usr/src/perl
# Fri, 12 Mar 2021 05:41:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 12 Mar 2021 05:41:07 GMT
WORKDIR /
# Fri, 12 Mar 2021 05:41:07 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:61211de2ba721a5e516c346a68bf2ae409d80525a872c3ad47ccefce648dc07c`  
		Last Modified: Fri, 12 Mar 2021 02:14:31 GMT  
		Size: 19.3 MB (19316567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111b755ad5c9dabb6951b2ae70635499104b8df1dc50f274cd4b9cec21e6e7d`  
		Last Modified: Fri, 12 Mar 2021 08:52:22 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0ed4ec41ca14a3fc018cd3e96ae47b31a0c2cfeec641a3e7a9a335ec31257e`  
		Last Modified: Fri, 12 Mar 2021 08:52:29 GMT  
		Size: 13.7 MB (13730747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-stretch` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:c214bd3473fc9e5bc967b88cea3fa0bdc92c90b16699510370bd822a88c7369b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34793821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c39812a8780612925632f1818dafcba5069722ee17dda3429ca74669404858`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Fri, 26 Mar 2021 15:44:41 GMT
ADD file:d54d0988e0451a81b9cd10a0eb2d8dd60d3b53434cf64e32131fb89d6569b469 in / 
# Fri, 26 Mar 2021 15:44:43 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 22:33:45 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 26 Mar 2021 22:33:46 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 26 Mar 2021 22:33:47 GMT
WORKDIR /usr/src/perl
# Fri, 26 Mar 2021 22:44:14 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 26 Mar 2021 22:44:16 GMT
WORKDIR /
# Fri, 26 Mar 2021 22:44:17 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:a1d6052e2be30a420519e61a06519837b570da894327e9db568747653c30343f`  
		Last Modified: Fri, 26 Mar 2021 15:51:19 GMT  
		Size: 20.4 MB (20389256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a8ae7cd7d717f6680ba0a1f28c76f244e5e596b3b4bcdd9362355d033886a6`  
		Last Modified: Sat, 27 Mar 2021 00:37:04 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09461ad6c2e7421ed20d2a7d08fe14816398319518bbded4e58494ae126ff40e`  
		Last Modified: Sat, 27 Mar 2021 00:37:13 GMT  
		Size: 14.4 MB (14404362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-stretch` - linux; 386

```console
$ docker pull perl@sha256:f8f2551937730459f999a2e1e255bb0bd74c10a39af098d1cb873b58931c1ebc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37244318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb647d0ce3f00d05a7e710592e948e2f19e8f61c00d9720cde0b8657eb1f1c7`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Fri, 26 Mar 2021 13:56:15 GMT
ADD file:91732be8769ce7a48c8edbcacde510467db8bf638bbaa006e2c16b934db4b194 in / 
# Fri, 26 Mar 2021 13:56:16 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 16:57:10 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 26 Mar 2021 16:57:11 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 26 Mar 2021 16:57:11 GMT
WORKDIR /usr/src/perl
# Fri, 26 Mar 2021 17:05:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 26 Mar 2021 17:05:46 GMT
WORKDIR /
# Fri, 26 Mar 2021 17:05:46 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:6a3bf74280798a5f5e64bcdb089e5b7574c9548f225981dcae24575c66cba2af`  
		Last Modified: Fri, 26 Mar 2021 14:07:05 GMT  
		Size: 23.2 MB (23156367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08edf1c34250cfa07baf0699e605e741163e7e98528edd88765bc237f9e65fb5`  
		Last Modified: Fri, 26 Mar 2021 18:39:00 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721d92324a42f5d2ca11830ed5b1c9912b917fa3e5f335ee140b32a4fe5584a5`  
		Last Modified: Fri, 26 Mar 2021 18:39:05 GMT  
		Size: 14.1 MB (14087750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
