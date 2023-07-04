## `perl:devel-slim-threaded-buster`

```console
$ docker pull perl@sha256:25fc37e6ac89b79bb91c654067e2a1c00805bf87efbb0631bf3dc9062533c515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:devel-slim-threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:b4515f017846cf533566cfc846ffbb0d833fcf597b7d6b1c52298dc8f9e501aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54512784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cc412653b861a2c44259d9608fb7785bcf30f0c2f4fb7d0c9d1d09264c3597`
-	Default Command: `["perl5.37.11","-de0"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:47 GMT
ADD file:ca4076bfffab8d09636384070ca253570590554cff76a132afaae5cd89b363b5 in / 
# Tue, 04 Jul 2023 01:20:48 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 09:30:48 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 04 Jul 2023 09:30:48 GMT
WORKDIR /usr/src/perl
# Tue, 04 Jul 2023 12:15:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.37.11.tar.xz -o perl-5.37.11.tar.xz     && echo '3946b00266595ccc44df28275e2fbb7b86c1482934cbeab2780db304a75ffd58 *perl-5.37.11.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.37.11.tar.xz -C /usr/src/perl     && rm perl-5.37.11.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Tue, 04 Jul 2023 12:15:23 GMT
WORKDIR /
# Tue, 04 Jul 2023 12:15:23 GMT
CMD ["perl5.37.11" "-de0"]
```

-	Layers:
	-	`sha256:90ac1ecaf92c8ae0cb37d29d8cc01b5802612c12edb933c369ad4c586ea94c6c`  
		Last Modified: Tue, 04 Jul 2023 01:26:21 GMT  
		Size: 27.1 MB (27138502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4a5412d50699a19e450516de43abfd05d528f7ce2f2a5db3527cff5df98563`  
		Last Modified: Tue, 04 Jul 2023 12:18:20 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756fa96b653f9f43cc4793060441652bdc69dc3eb3ea2d75821cd432446ba406`  
		Last Modified: Tue, 04 Jul 2023 12:25:59 GMT  
		Size: 27.4 MB (27374116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-slim-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:c010dd29b007491352097174291a8a8f82cdedeeea062fcd5279cf7ae76759aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46663091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b87ad251d898e43f033956a524aa9da165f2eeacd7f8005c03dd73c3c9e307c`
-	Default Command: `["perl5.37.11","-de0"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:42 GMT
ADD file:d2008875df919cb9817e6af97438428c2632113c1ef2b67b96607e184a7af941 in / 
# Tue, 04 Jul 2023 00:58:42 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 16:01:47 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 04 Jul 2023 16:01:48 GMT
WORKDIR /usr/src/perl
# Tue, 04 Jul 2023 19:06:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.37.11.tar.xz -o perl-5.37.11.tar.xz     && echo '3946b00266595ccc44df28275e2fbb7b86c1482934cbeab2780db304a75ffd58 *perl-5.37.11.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.37.11.tar.xz -C /usr/src/perl     && rm perl-5.37.11.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Tue, 04 Jul 2023 19:06:12 GMT
WORKDIR /
# Tue, 04 Jul 2023 19:06:12 GMT
CMD ["perl5.37.11" "-de0"]
```

-	Layers:
	-	`sha256:966944a300a7cf6431aa9fc3454d07eb7764f6b99d43a67de45ba53c30d69010`  
		Last Modified: Tue, 04 Jul 2023 01:04:17 GMT  
		Size: 22.7 MB (22747297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca63d44964e8d548d7492213692335b30f9f027e45f1e2623277aea98a2bf8f`  
		Last Modified: Tue, 04 Jul 2023 19:08:46 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bb5b90f13615dfb3ca2e2b003579ad63ee84613bdb01fad85d6798d32dc86`  
		Last Modified: Tue, 04 Jul 2023 19:16:28 GMT  
		Size: 23.9 MB (23915628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-slim-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:b206d28a8ac926c89e3b19cb13dbd8aba1c99987a0085b363736b3fa555dad4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51901763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024a2aa2944cbba4c7fe9713dfc50c369e5f4f46e9753808f8f4f6ea0eb40cee`
-	Default Command: `["perl5.37.11","-de0"]`

```dockerfile
# Tue, 04 Jul 2023 01:58:08 GMT
ADD file:1368964550b1f674dd0365f72bb1d55cfebf5e3c651d49b5e168f9be97a6df76 in / 
# Tue, 04 Jul 2023 01:58:09 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 07:15:04 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 04 Jul 2023 07:15:04 GMT
WORKDIR /usr/src/perl
# Tue, 04 Jul 2023 09:30:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.37.11.tar.xz -o perl-5.37.11.tar.xz     && echo '3946b00266595ccc44df28275e2fbb7b86c1482934cbeab2780db304a75ffd58 *perl-5.37.11.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.37.11.tar.xz -C /usr/src/perl     && rm perl-5.37.11.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Tue, 04 Jul 2023 09:30:31 GMT
WORKDIR /
# Tue, 04 Jul 2023 09:30:31 GMT
CMD ["perl5.37.11" "-de0"]
```

-	Layers:
	-	`sha256:30bfbe1cefebb80f6f9d5d90c39fcdf9d6367bbc76fa68e33ea3b4391c0f9a77`  
		Last Modified: Tue, 04 Jul 2023 02:02:39 GMT  
		Size: 25.9 MB (25921455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d97ec7781afe6dd8ee65df9771e269a87f0c7c0919fc585243a2bddafa68b0`  
		Last Modified: Tue, 04 Jul 2023 09:32:51 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4e2f2e32ad81a8319568cb40c56577eb72ec25b2c7377afd9f4fc362a05d8b`  
		Last Modified: Tue, 04 Jul 2023 09:39:48 GMT  
		Size: 26.0 MB (25980142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-slim-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:6fbae23f25176adf04640361662dde3646579d4b11529c998b621c658ea06217
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59343576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8dc330dd4300da64234460ac6203a1fe5b3fdfe8d156599ea48c9075109eff`
-	Default Command: `["perl5.37.11","-de0"]`

```dockerfile
# Tue, 04 Jul 2023 01:39:22 GMT
ADD file:0be890be1c2ff0966cf1b714bd814e6859e1a2cb4a491ebd6c28d551eeedd66b in / 
# Tue, 04 Jul 2023 01:39:22 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 09:39:33 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 04 Jul 2023 09:39:33 GMT
WORKDIR /usr/src/perl
# Tue, 04 Jul 2023 14:17:27 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.37.11.tar.xz -o perl-5.37.11.tar.xz     && echo '3946b00266595ccc44df28275e2fbb7b86c1482934cbeab2780db304a75ffd58 *perl-5.37.11.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.37.11.tar.xz -C /usr/src/perl     && rm perl-5.37.11.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Tue, 04 Jul 2023 14:17:27 GMT
WORKDIR /
# Tue, 04 Jul 2023 14:17:27 GMT
CMD ["perl5.37.11" "-de0"]
```

-	Layers:
	-	`sha256:b4637b85bb10ca071ae2bfe4ea2e6dd6ca216cecae3d9db6787e67046e0c1f70`  
		Last Modified: Tue, 04 Jul 2023 01:44:56 GMT  
		Size: 27.8 MB (27797000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee08f14a1fd18309aa483b5f1991ca7749a83d61a1bec2fa4c8983c35c4117a`  
		Last Modified: Tue, 04 Jul 2023 14:20:00 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9145de38a7597b9d1a0e267599867cb72cca43a8def51638c4c7dbf2501b31dc`  
		Last Modified: Tue, 04 Jul 2023 14:28:39 GMT  
		Size: 31.5 MB (31546409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
