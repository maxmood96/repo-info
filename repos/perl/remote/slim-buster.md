## `perl:slim-buster`

```console
$ docker pull perl@sha256:d12b79b8db555806e453c4b8440bfb331d8f140a1d1592c9b02c97a3582c2ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `perl:slim-buster` - linux; amd64

```console
$ docker pull perl@sha256:ea2e18c31a246454faf8c54f6fb355a092a349b5cb3622c8011b37ab135de03e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41440671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d84950f361f1f70cc4940a66f060076977b841e090d1995cabf9aecb2dd7ce2`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 09:06:34 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 31 Mar 2020 09:06:34 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Tue, 31 Mar 2020 09:06:34 GMT
WORKDIR /usr/src/perl
# Tue, 31 Mar 2020 09:19:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 31 Mar 2020 09:19:10 GMT
WORKDIR /
# Tue, 31 Mar 2020 09:19:10 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bb6449b98354da111bb05110addf19650a35a9b3b4e85cc10470fa8adab65b`  
		Last Modified: Tue, 31 Mar 2020 13:16:48 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d17471bbb64548de7a37b1f7606b9d9de50c0a0a43d4fe2a1d8446fab92397e`  
		Last Modified: Tue, 31 Mar 2020 13:16:53 GMT  
		Size: 14.3 MB (14348394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:96af2c7c341e89f51bd5af72d16cb5c4ab08b03d9b80ec50ae031b994b4ca4a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36190622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15e6787e278f622c55d08677975f7ef4e8d4d765e133c3f1f8c118520d1257e`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Thu, 16 Apr 2020 00:59:45 GMT
ADD file:e346a36a456d66d8019344b5f7d60df8b5b24aea1461c19838982135ad1f4d7d in / 
# Thu, 16 Apr 2020 00:59:47 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 05:46:26 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 16 Apr 2020 05:46:27 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Thu, 16 Apr 2020 05:46:28 GMT
WORKDIR /usr/src/perl
# Thu, 16 Apr 2020 05:56:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Thu, 16 Apr 2020 05:56:43 GMT
WORKDIR /
# Thu, 16 Apr 2020 05:56:44 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:838dc71644c10eab485c4bdfa3879e0fb9e72426de1239cfac1d4c05c23db7be`  
		Last Modified: Thu, 16 Apr 2020 01:08:59 GMT  
		Size: 22.7 MB (22705228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d776e425bf2c7042cfd8a0efc1b1d83c51714548dd88626226438cf6e57344`  
		Last Modified: Thu, 16 Apr 2020 09:46:40 GMT  
		Size: 440.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444735ed6664a5e3f69775fa298710d0e89de7b3e479f1b53fb2593f8596cfcd`  
		Last Modified: Thu, 16 Apr 2020 09:46:45 GMT  
		Size: 13.5 MB (13484954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:e44bd2d998201e957149a368309442da6d95296122b196e17c47e656f5503e34
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40162077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d545d9c4c427287bac557ed56273155259136adae9318f765372d92f0c4de935`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Thu, 16 Apr 2020 02:41:52 GMT
ADD file:1aab17002a9095c31dd6928277a045cb26846ac58c3d2d63316332c99a5f90bd in / 
# Thu, 16 Apr 2020 02:41:57 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 07:58:19 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 16 Apr 2020 07:58:20 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Thu, 16 Apr 2020 07:58:21 GMT
WORKDIR /usr/src/perl
# Thu, 16 Apr 2020 08:08:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Thu, 16 Apr 2020 08:09:00 GMT
WORKDIR /
# Thu, 16 Apr 2020 08:09:01 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:3d48095d71a365b5910cea98e5566c152a3f9aa11657560568259bf93ff2f4cb`  
		Last Modified: Thu, 16 Apr 2020 02:48:58 GMT  
		Size: 25.9 MB (25857715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7935b9b8ba70760c44f33a77aa418070b030518eca446840165e10ce778c699`  
		Last Modified: Thu, 16 Apr 2020 11:56:09 GMT  
		Size: 441.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa8e111ffe3448eff175943408e19f969910a36d2d3961e9748bb5d71e3db69`  
		Last Modified: Thu, 16 Apr 2020 11:56:15 GMT  
		Size: 14.3 MB (14303921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-buster` - linux; 386

```console
$ docker pull perl@sha256:1f3a7ae4500f34835c1483769352700c09799e360e005f8b2cf7a6085aa60eb0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41605686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c254052c1649a4f71d4c8e386999660f2ffc13c8225638365e2a6d18468882`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Thu, 16 Apr 2020 01:39:55 GMT
ADD file:ab0bbfba6c4b56420ffffc6cdddcc4592fff018f0cd07578c7dc0a5faa49df2f in / 
# Thu, 16 Apr 2020 01:39:56 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 07:10:42 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 16 Apr 2020 07:10:43 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Thu, 16 Apr 2020 07:10:43 GMT
WORKDIR /usr/src/perl
# Thu, 16 Apr 2020 07:25:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Thu, 16 Apr 2020 07:25:41 GMT
WORKDIR /
# Thu, 16 Apr 2020 07:25:42 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:75bc60a98e6523be3fadd9128c1a630cb5cbd2d2d813ee5e99dc146a3de22254`  
		Last Modified: Thu, 16 Apr 2020 01:46:20 GMT  
		Size: 27.8 MB (27753976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8749655ca37aea5566b65dc8539fb75eb95620c3972d245fdc54582fa5dffaab`  
		Last Modified: Thu, 16 Apr 2020 11:36:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea065b7a32dc659feb693410e7608b54f8dc947a927c1c1961cf9743705ff37`  
		Last Modified: Thu, 16 Apr 2020 11:36:51 GMT  
		Size: 13.9 MB (13851295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-buster` - linux; ppc64le

```console
$ docker pull perl@sha256:ed19df5fe9aefb48b0172edf1e5d469a379bd93de8a6e6213a26a4fedfc31dbf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44954552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0509e86c4757d6a42d0aa8657af32a5b83f3822fd2d925e7e2633da3a95ea7b`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Thu, 16 Apr 2020 01:38:30 GMT
ADD file:9beea54416432abbd09d26b965c3c8e5bea8e233113f9bc308294c0008ee886f in / 
# Thu, 16 Apr 2020 01:38:39 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:09:19 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 16 Apr 2020 03:09:25 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Thu, 16 Apr 2020 03:09:30 GMT
WORKDIR /usr/src/perl
# Thu, 16 Apr 2020 03:22:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Thu, 16 Apr 2020 03:22:17 GMT
WORKDIR /
# Thu, 16 Apr 2020 03:22:20 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:f268991f8af64097bbfefa3f01dd3fdb7f715051a3681f352504a3ecaa9d3596`  
		Last Modified: Thu, 16 Apr 2020 01:54:39 GMT  
		Size: 30.5 MB (30524651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51bb810574f841f73acdcbcbcdedac7995174112858c52e8eb5a1414d58b9d3`  
		Last Modified: Thu, 16 Apr 2020 05:12:33 GMT  
		Size: 441.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d578b0b0c4a20bf1dd480412a06d6020c9eeba8816eaa90aa3625a55ae57255`  
		Last Modified: Thu, 16 Apr 2020 05:12:39 GMT  
		Size: 14.4 MB (14429460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-buster` - linux; s390x

```console
$ docker pull perl@sha256:89419f9fb598ca3f067178575e297df3e7228bf8d4077a863a5f37fae13a8fed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40404919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f55ddb2d8dd4fcd6e3842ca18d225b052a2fd640223e92b1024a259385b013c`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Thu, 16 Apr 2020 00:42:19 GMT
ADD file:f328b5d6dce2eaf00360542c1e3280958b818268b9150b12ffd1fddf030daf2f in / 
# Thu, 16 Apr 2020 00:42:20 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:40:20 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 16 Apr 2020 03:40:20 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Thu, 16 Apr 2020 03:40:20 GMT
WORKDIR /usr/src/perl
# Thu, 16 Apr 2020 03:44:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Thu, 16 Apr 2020 03:44:40 GMT
WORKDIR /
# Thu, 16 Apr 2020 03:44:40 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:043f95f5412a986fb082b0193860bb9c0388c2fbcb5e8bf5bcbbeefb0e45c9c5`  
		Last Modified: Thu, 16 Apr 2020 00:46:19 GMT  
		Size: 25.7 MB (25712234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294a6d99a6b169adb049c3fa802cd4d59583589b40a174e85a557d264122443f`  
		Last Modified: Thu, 16 Apr 2020 05:23:25 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d11099095c32ff084194888ab945b8add2ec171cf36d8603c386b96731cbae`  
		Last Modified: Thu, 16 Apr 2020 05:23:28 GMT  
		Size: 14.7 MB (14692249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
