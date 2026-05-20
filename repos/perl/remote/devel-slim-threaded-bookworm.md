## `perl:devel-slim-threaded-bookworm`

```console
$ docker pull perl@sha256:cade13e3535ff1725af293ddb5c3e9fe3610a191e9e278ddafcecf31fb268e12
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

### `perl:devel-slim-threaded-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:d66c84a38cd4cc2628a3252a03c9cd492810cdb83854f4de0de043aff61df840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58768916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e1374e7692471c749f9ead4dfd9f7f09fd2d82e136d6628c9b8757602341b4`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:28:39 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:43:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:43:04 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:43:04 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a85acbd4d816eac5e3de1b33abfc7db152f17443f4a6e41311b61db3748b4`  
		Last Modified: Tue, 19 May 2026 23:33:04 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79efd3c5a1ba607b7ff62a5453c50a4d2e81486bc76ca69f3a9167a47e5ef5cf`  
		Last Modified: Tue, 19 May 2026 23:43:16 GMT  
		Size: 30.5 MB (30535105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20de530097e23e5b06f7bc608730b0e86f0c37f0bdf2dcc7e20331ede15c1f1c`  
		Last Modified: Tue, 19 May 2026 23:43:15 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:7e230ab86c9965051558e7da7afe5db7e3703f2e1676d191bd3afc5258449c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3957758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402da4e3869a7c7f681973ee027dfac0c21c690a3f45a8c66bc8219dc65011fe`

```dockerfile
```

-	Layers:
	-	`sha256:a4c872a63ab53d49aef482c0786dcdb9fc836e3815d91572487e301eeeca7ba6`  
		Last Modified: Tue, 19 May 2026 23:43:15 GMT  
		Size: 3.9 MB (3939412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf97cb8c7b45af935768de7e98e1338cf000b96ecac554644f28a95c7df4558`  
		Last Modified: Tue, 19 May 2026 23:43:15 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:b44ff7149f41cbe98a7453f2f84eec345c13d74d10e6e607e3a4a5d4caeb309c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53345844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebef8a638c96923c1a4d36ffb30d111fa6c38187a6280aa2dfacf94af6f02798`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:58:20 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 21:11:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 21:11:02 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 21:11:02 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:0496e5b1fd9475851f8b3578080061a05ea61be300ea5a278a4a08a883855adc`  
		Last Modified: Fri, 08 May 2026 18:33:05 GMT  
		Size: 25.8 MB (25765670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdf3550ab5cc551d02e7cf4ada59b6bc9f91d6b4c9c1d20006a9226a0015758`  
		Last Modified: Fri, 08 May 2026 21:04:42 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4d729bd1b167a29a90f891156c8ec801e653b07d43f8483750664ead9f0a4d`  
		Last Modified: Fri, 08 May 2026 21:11:13 GMT  
		Size: 27.6 MB (27579905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b5ec1c5d9f8d64ac1110ab45ba77b336020912688e3c3a3cdf954fb142fc8`  
		Last Modified: Fri, 08 May 2026 21:11:12 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:b88a85b9346e509b90357091ebbc51e6dfc2fb6359bcdf571adb5f77f94153fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037860ec92aa6b695c761882abc4f8dd29c237fe86e5add2a448e4c8e8226a16`

```dockerfile
```

-	Layers:
	-	`sha256:e00714928a5b698a8790fc917d58198b2688d2110ece30b2a950864a5b59e7d7`  
		Last Modified: Fri, 08 May 2026 21:11:12 GMT  
		Size: 3.9 MB (3910245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cfefdc261035bc52c96cb8499042fcf21fd70cd6026aecb7f65130fd37380e8`  
		Last Modified: Fri, 08 May 2026 21:11:12 GMT  
		Size: 18.4 KB (18417 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:30f18653b1d6ad92e40095f55cceb1c6aa2fd75f8b01085e6d572c18f3c11c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da89c540c5cf06f9f6e6c9f1949c639075e7873141a05cbd7f80cb7949210557`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:46:02 GMT
WORKDIR /usr/src/perl
# Wed, 20 May 2026 00:51:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 20 May 2026 00:51:56 GMT
WORKDIR /usr/src/app
# Wed, 20 May 2026 00:51:56 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e10eb12d5cb9f69616f61d5e1dd551f3634fa3468d36660418b3f347d1a8ba7`  
		Last Modified: Wed, 20 May 2026 00:52:06 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820ca9dedc830eb7f222bda74e1a849196fd7a30eafe5de77c82d3ec7aa3549e`  
		Last Modified: Wed, 20 May 2026 00:52:07 GMT  
		Size: 26.7 MB (26664419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3300dd6da0e74b8dac9ee6666cb3ada02f22c5324ce05c143689b34eb5dcae8`  
		Last Modified: Wed, 20 May 2026 00:52:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:7945a2e21465811c2f6a6f90779a1f214101032f3fe0ae0f575bca6cbc2a22af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc1cd2af3771e848bb7a1bd1e17c93ab7dbf4b1f4e5746d6782758c741b0972`

```dockerfile
```

-	Layers:
	-	`sha256:fa5ef57c271c25307ec79ea598232ef7b82c90087c8f98fda3f0a2f4f0ef79b6`  
		Last Modified: Wed, 20 May 2026 00:52:06 GMT  
		Size: 3.9 MB (3909488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e220dc173a5994c451c57525f9593a062e6b129bd6a1f21c1a5a0ac6c5b03578`  
		Last Modified: Wed, 20 May 2026 00:52:06 GMT  
		Size: 18.4 KB (18418 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:7ad0a89bd90349908de522b878542cc05018c480a201a52dbe81322eadfa4c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57497999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbc47b8a1530adbd1ae283ebebbc659b1ad7c7d1c695761a1537903784eddf1`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:42:26 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:47:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:47:39 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:47:39 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06993abf41106c5cf38ad68bc95822616c2c5f3935238531bbe4d61e323970f`  
		Last Modified: Tue, 19 May 2026 23:47:49 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779932cde1292b1b1907a909c3b8634cca4268ca19839988134f6085e4a9870`  
		Last Modified: Tue, 19 May 2026 23:47:50 GMT  
		Size: 29.4 MB (29382688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e62603dbb2537fe55ef1eb78ad5ffe133620df61c70814b7a88bf12e246024`  
		Last Modified: Tue, 19 May 2026 23:47:49 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:8a57b2ffefdf3e85bf8de1312cc965315aeb079a316542022559020a91b169b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e77f4e11f29838c0085855edaee33b1aa7f253a67a3985d7ce85e8574f219d1`

```dockerfile
```

-	Layers:
	-	`sha256:6b0dd235b4137d0ab80ebd789a915bfe6a71225898f6e041a35ee3e1e2d8ddba`  
		Last Modified: Tue, 19 May 2026 23:47:49 GMT  
		Size: 3.9 MB (3910649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:800a27f3487921e265ae1c41fabe9605090990fbd8b30f14d84c8e98e8942ab3`  
		Last Modified: Tue, 19 May 2026 23:47:49 GMT  
		Size: 18.4 KB (18438 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:99fe3ca365e41b0b6b96250f39a87f6e3b3cdb835335560e73ef0dec9d3e1742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58936782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81e1bb5525deb99b32d82551384c4cc002616d3fded3f6318e08718f1e09f66`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:33:01 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:38:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:38:40 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:38:40 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bd0b8ce3f8de2b2744826396bc60f745e52eda1dd9c2c0e1aebff4dc3c20d7`  
		Last Modified: Tue, 19 May 2026 23:38:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aba494000114edcb3ae71508d6f1ea6c68d0d23f8ddce91086baa9c59c0dd75`  
		Last Modified: Tue, 19 May 2026 23:38:51 GMT  
		Size: 29.7 MB (29717914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa4e86abcbf9bbaae7cc23c3e90a5828a34a3cafc0e08779fdb21a75ab54c8d`  
		Last Modified: Tue, 19 May 2026 23:38:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d3fcc3fee335a676de0465bf65149153b8864e3a3d6b1410af6f7c77580a8edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062440d2c6297d254fce451cbdee79278b6ca11297033cef126fba6f2e297080`

```dockerfile
```

-	Layers:
	-	`sha256:3f0c7b6910608ec633f4df211f8faac01b668410f87945cc967d68c576e8eb76`  
		Last Modified: Tue, 19 May 2026 23:38:51 GMT  
		Size: 3.9 MB (3933354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07bc08af3b71650d73a47ce430171f8de219fbaff2fb0395bfd3b4c3f752b7fd`  
		Last Modified: Tue, 19 May 2026 23:38:51 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:23db1c2cc87e00a8ea76c63639ee46420c8a396ddcf4608aeba4b129c373759b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57224522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc87dc268a6a7de434741e33e2afa48e3421cbca0cfc6cd7f1da1a74d0805db`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 07:08:16 GMT
WORKDIR /usr/src/perl
# Sat, 09 May 2026 10:45:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 09 May 2026 10:45:26 GMT
WORKDIR /usr/src/app
# Sat, 09 May 2026 10:45:26 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:8e1a6f4f5a9e9628f902e3c8df639d1691d7f1000dc904f820155d1b9b2fa2ff`  
		Last Modified: Fri, 08 May 2026 18:20:04 GMT  
		Size: 28.5 MB (28526280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d14ddd3bed515cfc752781c3991360ceb5cf7a65ec98dc867fe1a1ae48e6ab`  
		Last Modified: Sat, 09 May 2026 07:34:02 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e372041a9f4e48122e68b7b4231e6160281e4510222c69e3f9bb784ffb4ecf71`  
		Last Modified: Sat, 09 May 2026 10:46:12 GMT  
		Size: 28.7 MB (28697974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df8a2dd3ebc1a591b4bb34037974ee82bba3d9dbd80c206bdbcc718b27d614a`  
		Last Modified: Sat, 09 May 2026 10:46:09 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:69a81e4a785ae9e04820e1dc93ceea979e38451da3cdea0478245e023c3c74ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6b8159fd87fba0701ae54bef562688cd942e4007431ceaf6f063034d6cfc9f`

```dockerfile
```

-	Layers:
	-	`sha256:f5a9382c27752ca2c16fe5985a46834b1e7b9fe0c06e2c25fc7795f5fb469f35`  
		Last Modified: Sat, 09 May 2026 10:46:09 GMT  
		Size: 18.2 KB (18188 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:8bad78835f1e68e0cb9a7ae5280b80549cb17021729be64c88d612619e4c18e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63453393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1e2af0a738a91ebfe0ade164f0ec6d800e287efc09b829172d8ae37a7251d2`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:50:43 GMT
WORKDIR /usr/src/perl
# Sat, 09 May 2026 00:01:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 09 May 2026 00:01:50 GMT
WORKDIR /usr/src/app
# Sat, 09 May 2026 00:01:50 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6e6f1c77c9955dfc698489a3c4d78858bb1799b5a5f328728717274537eb4f`  
		Last Modified: Fri, 08 May 2026 23:00:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c3e1e201ee2d625713263ec833f9a879ab39db3d261231b35e4270c60abfc7`  
		Last Modified: Sat, 09 May 2026 00:02:11 GMT  
		Size: 31.4 MB (31374672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc5f3ff19254d3dbb37caa3119c0835dd14e89d13df433b7009c6a60f24f037`  
		Last Modified: Sat, 09 May 2026 00:02:10 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:96df57c9a210f5424ecd8cddb925ff6fec30b7ba12bd00bba399db43c0f0d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3943706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66942fb88b76ebec365387d248f8fc1e5cea6a6b31bdab6549f9d023de283b93`

```dockerfile
```

-	Layers:
	-	`sha256:e978b7466ced4567158f7634251329bd052b76a4b3d210b8e2dea3b2b274a986`  
		Last Modified: Sat, 09 May 2026 00:02:10 GMT  
		Size: 3.9 MB (3925322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed15e0d5ccd9831a0e8b72b1ade7c196500eca61b1d040d15538f7bb41fab19`  
		Last Modified: Sat, 09 May 2026 00:02:10 GMT  
		Size: 18.4 KB (18384 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:69d4ccc7bc5e272d0316b014f6e26d823250fa5b6ac29175bc721d9769b1bff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55982100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1829c1dc4f510f82f4bd4b02b84cb9af557b3d9c843af2615a9e6c21c830a7b4`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:28:17 GMT
WORKDIR /usr/src/perl
# Wed, 20 May 2026 00:58:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 20 May 2026 00:58:56 GMT
WORKDIR /usr/src/app
# Wed, 20 May 2026 00:58:56 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcac51e608144bb4cad5af5e0229a894daa7828e4b10b3a7b4ef14d086994a7`  
		Last Modified: Wed, 20 May 2026 00:35:47 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94913d1b04768610e2366c4103fae978fd90755b7ed5ead342fdc436c4bda109`  
		Last Modified: Wed, 20 May 2026 00:59:14 GMT  
		Size: 29.1 MB (29093236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87adf06a9c9f5f43edc5b22d86ede48efc073bfdd002b269715f71b70528bad`  
		Last Modified: Wed, 20 May 2026 00:59:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:0272cc77272b8373302906552858d9325a80b1f2b0280ea673096e8838f19bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3943031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7524b9e1574da3eb889632a7c7ea4d5f60cfd614959714b86a89a0dfbb45e413`

```dockerfile
```

-	Layers:
	-	`sha256:f2518fb46822c1b4f807d7f878f20fb28d42a3e1ebd6d69e0fa537984e471b0b`  
		Last Modified: Wed, 20 May 2026 00:59:14 GMT  
		Size: 3.9 MB (3924685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7475406f569be64919cd02b26417bf8d7f67732e7ef8bd0f13a5451849af4ff9`  
		Last Modified: Wed, 20 May 2026 00:59:14 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json
