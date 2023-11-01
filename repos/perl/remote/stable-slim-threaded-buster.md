## `perl:stable-slim-threaded-buster`

```console
$ docker pull perl@sha256:53bcb88e0478c84e7f08ec87d148382c54e9befc8e0746d70479d0e64f09f863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:stable-slim-threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:82210e7f7fdb2764530af5400517959128cf207eb365e32ebf9728dd19ed7949
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54573307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871a68939593ccf4f451afa1445e82fcb318cf2a12508d3287442148c93fe8c6`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:35 GMT
ADD file:04482e1456288a566d216ed1cea383eabd946f66656da78e1e151056edf936d1 in / 
# Wed, 11 Oct 2023 18:35:35 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:43:45 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 12 Oct 2023 00:43:45 GMT
WORKDIR /usr/src/perl
# Thu, 12 Oct 2023 01:09:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Thu, 12 Oct 2023 01:09:09 GMT
WORKDIR /usr/src/app
# Thu, 12 Oct 2023 01:09:09 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:b70638ed4228556f5f57f76a636b1668fe301e86662437141774e61963da1b4f`  
		Last Modified: Wed, 11 Oct 2023 18:41:01 GMT  
		Size: 27.2 MB (27187490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c738a5458b6848c66a6e1537beabad5f60e4519e2302e0d42e6f0bc5e3505b5e`  
		Last Modified: Thu, 12 Oct 2023 02:40:49 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7915fe0b58fa018607c8e4a415bd59fa84af0dc455b5224a65b593675920b8d6`  
		Last Modified: Thu, 12 Oct 2023 02:42:12 GMT  
		Size: 27.4 MB (27385485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1395f82548e8ce4619f9ba9c80b99d83f4ec7df7417f3838ef06d5cab536812d`  
		Last Modified: Thu, 12 Oct 2023 02:42:08 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:stable-slim-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:f141c4db52f589daeca5a9924ea2083521c91530249c081f3417bb3341ce8b2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46719089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a173a9d4f046cc5f3e98834f548e2cf95d78706f88d3b43c72e382b170de6e`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Wed, 01 Nov 2023 00:58:29 GMT
ADD file:dd923e222804a3bd200ecd72437d80c805c7eb6009aaa6b274da0574ccde56e0 in / 
# Wed, 01 Nov 2023 00:58:29 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 03:49:46 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 01 Nov 2023 03:49:46 GMT
WORKDIR /usr/src/perl
# Wed, 01 Nov 2023 04:32:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Wed, 01 Nov 2023 04:32:22 GMT
WORKDIR /usr/src/app
# Wed, 01 Nov 2023 04:32:22 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:43c30e0275ed5286753ad05a34be76f873205cce5130a05b3e968c87c888a5bf`  
		Last Modified: Wed, 01 Nov 2023 01:03:42 GMT  
		Size: 22.8 MB (22795940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b5ef21cc3a06a4e862f7348727cfceaee9a7faa45ae11f71954f46e4239946`  
		Last Modified: Wed, 01 Nov 2023 07:25:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3bd4f28901f5c9e215e20a3159882c7bfed0f20dd5adff21fbfa34ee31b677`  
		Last Modified: Wed, 01 Nov 2023 07:28:23 GMT  
		Size: 23.9 MB (23922815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda343de4f545abd0a7b25acb89271649c7f3aa0a8c9a463f71ffe770601cda3`  
		Last Modified: Wed, 01 Nov 2023 07:28:15 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:stable-slim-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:420d374f54f7d41a88c6523ec13a5382b46a156bac6f8bc188a4630daa8d69d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51960613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474bcb037c11caf8ceb801277c71484ee92809220d3950863f72610fadad0082`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:09 GMT
ADD file:ad1947b1fc97bcc228c004c15afeb2d9006d47167db69cf7b05c3e634c648166 in / 
# Wed, 01 Nov 2023 00:40:10 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 05:05:27 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 01 Nov 2023 05:05:27 GMT
WORKDIR /usr/src/perl
# Wed, 01 Nov 2023 05:39:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Wed, 01 Nov 2023 05:39:19 GMT
WORKDIR /usr/src/app
# Wed, 01 Nov 2023 05:39:19 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:094e0a7927f79c559fdab346774d7de6e5fc38e2d998e82dd663850ebbff4648`  
		Last Modified: Wed, 01 Nov 2023 00:44:25 GMT  
		Size: 26.0 MB (25967703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd48feab1145685f8b1a9b73d524444685a4266701e08ef6eb365d33619f041`  
		Last Modified: Wed, 01 Nov 2023 07:59:20 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece6288239743e91106675382cfcd819548aee82803abae921c4a440483ac2d3`  
		Last Modified: Wed, 01 Nov 2023 08:01:29 GMT  
		Size: 26.0 MB (25992576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7d3edea3b8df240ef6a3d14aebdce6f270612a5067a478a91ae3701683adcd`  
		Last Modified: Wed, 01 Nov 2023 08:01:25 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:stable-slim-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:df80e53ff820153586d0af1117a7cf9857bc036ae67c764fd33291e6b8403ff2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59392745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec4f76117a1b5a9b31e164519a2c807c97110b545f79680b1f790c0f49196d8`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Wed, 11 Oct 2023 17:41:25 GMT
ADD file:854b4f9d83a5c35cd381aacfe3bcf395a5752cc3b42cbd0fbb826031e02177f9 in / 
# Wed, 11 Oct 2023 17:41:26 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:54:13 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 11 Oct 2023 22:54:13 GMT
WORKDIR /usr/src/perl
# Thu, 12 Oct 2023 00:08:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Thu, 12 Oct 2023 00:08:32 GMT
WORKDIR /usr/src/app
# Thu, 12 Oct 2023 00:08:32 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:dd9239100b85afbacf77eac49110cab92785ed349763f8d2365623be42aad25a`  
		Last Modified: Wed, 11 Oct 2023 17:47:12 GMT  
		Size: 27.8 MB (27846890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583e28d19f6f9d09ca7d90e5a5e2d291c9d3d5f40ebbceea581ca4566a8c96ef`  
		Last Modified: Thu, 12 Oct 2023 05:09:56 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559957afaf973ba6e31756ad6ff459570e00bdacbd25bdae236b5968501f9a6b`  
		Last Modified: Thu, 12 Oct 2023 05:12:32 GMT  
		Size: 31.5 MB (31545523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc309270416dcf2e0be2ba3912a0371f903a6cbf2a6e592fba3330e87af5aa35`  
		Last Modified: Thu, 12 Oct 2023 05:12:24 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
