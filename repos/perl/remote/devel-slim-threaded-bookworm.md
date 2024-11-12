## `perl:devel-slim-threaded-bookworm`

```console
$ docker pull perl@sha256:1b222baa46a66fdba4fb0d4456f1ec263e62938e847168e3a62a18542144f5ee
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
$ docker pull perl@sha256:30c470280028c9e4f1fbc8adc044e2556bd8edd8dc5a96ce32a4c80c43e637dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59375582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5fbd4eeff56036c0c3bfc3ebb036614b769943980d18d16819760f9dda3c8eb`
-	Default Command: `["perl5.41.5","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.41.5.tar.gz -o perl-5.41.5.tar.gz     && echo '844d47856b8347fba553c90fa10e76de7ae579f81ed5312acf5f638d72079df4 *perl-5.41.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.5.tar.gz -C /usr/src/perl     && rm perl-5.41.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.41.5" "-de0"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670d9b9006a073f3477c21ce6708b97cd6bf74ca6be3d8086fcaaa37b55c664e`  
		Last Modified: Tue, 12 Nov 2024 02:49:50 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d164e25b19655c70bc20b350874bb3e590a9fe8b96606207b12d52104b5fdb3`  
		Last Modified: Tue, 12 Nov 2024 02:49:51 GMT  
		Size: 30.2 MB (30247322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251778b795411dbd824aef7d543d9951faac94021c4f6d3a7b8369ad9ed7100a`  
		Last Modified: Tue, 12 Nov 2024 02:49:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:3704f8f959ecc1d6d10c3dce0f686846edde11748edf1e03493f2bdb7defde20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bba2509ecd34fa0d0c3cec99a84b31e24a81a704c7d314fe0afdb0d0868593`

```dockerfile
```

-	Layers:
	-	`sha256:7c1cf7ae679969a5a97c90ed7579874b7fcc88bbd1f8f52ba2c0a66bed7d2691`  
		Last Modified: Tue, 12 Nov 2024 02:49:50 GMT  
		Size: 3.8 MB (3814081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9e2bc248a1ba876e43813f283abed273c2deb2c255989d8e821a24aeb5493d0`  
		Last Modified: Tue, 12 Nov 2024 02:49:50 GMT  
		Size: 19.3 KB (19327 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:f348cf744992b6d6bb2259805952cc19543227bc154e74976253e5c2157d78f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54156782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec71d8a7994aa04deec1820e8b576399f41dbe3b0f057100ee7a98012612b25`
-	Default Command: `["perl5.41.5","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.41.5.tar.gz -o perl-5.41.5.tar.gz     && echo '844d47856b8347fba553c90fa10e76de7ae579f81ed5312acf5f638d72079df4 *perl-5.41.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.5.tar.gz -C /usr/src/perl     && rm perl-5.41.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.41.5" "-de0"]
```

-	Layers:
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04209475e978f93a62a76f714523f214b85f644ce8192912158891b495d96f3`  
		Last Modified: Tue, 12 Nov 2024 06:57:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15b1f4842d596c36b3c4745b43348388d23d747d52452c5f85f08b82324f564`  
		Last Modified: Tue, 12 Nov 2024 08:15:35 GMT  
		Size: 27.3 MB (27266457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435374e23f3cf4f5494849ac32fa176340980de6364637ff9f406dc5d25f9608`  
		Last Modified: Tue, 12 Nov 2024 08:15:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:5297f88fd4ef1a630a8e4e58c26027d8cdd42a3276d304ff6583ada163bdacf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d90c3d1d06c5d7f860e42241ea53b7608f60508063ce2fcb952f8fc6a6783a`

```dockerfile
```

-	Layers:
	-	`sha256:4f839e6d71f87779bc004715c05464a4fd746f1f2ed11406893904e2c23ae0c3`  
		Last Modified: Tue, 12 Nov 2024 08:15:34 GMT  
		Size: 3.8 MB (3784605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df72b3a4f705d183acd37d9cb658288237209f6da3d39430073fc27963acc02`  
		Last Modified: Tue, 12 Nov 2024 08:15:34 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:9916509973f7e38561d5aa60c034a34f890ff3a7193e981d63dd574d71d973b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51061010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f04c381de3415b6134bfc7cb324663626e55fee687bacb4ba7d7072780e58d1`
-	Default Command: `["perl5.41.5","-de0"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.41.5.tar.gz -o perl-5.41.5.tar.gz     && echo '844d47856b8347fba553c90fa10e76de7ae579f81ed5312acf5f638d72079df4 *perl-5.41.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.5.tar.gz -C /usr/src/perl     && rm perl-5.41.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.41.5" "-de0"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb9475168dc9ca57175b1b4be56751886989d3eb029c21f9fb85f4ed1751650`  
		Last Modified: Thu, 17 Oct 2024 15:06:29 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ceb3e8c38859cd3b27bfd7fec77633d7e8161cc53f80dfc6ea1b5d5fbaa1ff`  
		Last Modified: Mon, 21 Oct 2024 18:46:48 GMT  
		Size: 26.3 MB (26342547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130c238c6e8116ad95ac584c1cfb6ac6a96f857b080f2f390cd2d52cf8d85ec9`  
		Last Modified: Mon, 21 Oct 2024 18:46:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:f93cf9421f63cb9d8841ad7de495a54166b83acb88312ad96f67c93283ae1e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25306f6ab4cee2336be73805f46fe4a87bc815c43679a3d27fac9f9ba4b4c39a`

```dockerfile
```

-	Layers:
	-	`sha256:6be63172ed791cb2380006efd7a08ee4b45f5c694ae15eca57aecbdecb1d69b9`  
		Last Modified: Mon, 21 Oct 2024 18:46:47 GMT  
		Size: 3.8 MB (3784138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8992c04905771fa192c8d2dcfd4555109c735ca947216e68c4457b37d8edc60f`  
		Last Modified: Mon, 21 Oct 2024 18:46:46 GMT  
		Size: 19.2 KB (19241 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:a63b087259a01f35d86c39711122e1bfe498bed2114db2b8bd74654f9cf1d8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58186386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183ea9ca6979c013dd0fdc6e128d3dc74391ff98908222c8db08d952be715259`
-	Default Command: `["perl5.41.5","-de0"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.41.5.tar.gz -o perl-5.41.5.tar.gz     && echo '844d47856b8347fba553c90fa10e76de7ae579f81ed5312acf5f638d72079df4 *perl-5.41.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.5.tar.gz -C /usr/src/perl     && rm perl-5.41.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.41.5" "-de0"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e0438a6dc8ce9271e707806179b7fc30232d02cfdc0006118b01bfcc8088cf`  
		Last Modified: Thu, 17 Oct 2024 14:10:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cda14f5c8042783e649f4a322a5c65a1cdc802ccdefd799eebfa421efa555f`  
		Last Modified: Mon, 21 Oct 2024 18:37:38 GMT  
		Size: 29.0 MB (29029779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e618e330b5e0ab74767943850891c27329f9bb3b6906a51624802fcd6d3f187`  
		Last Modified: Mon, 21 Oct 2024 18:37:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:534ff66b25a77f4addc026a6b4554b4c89f09bea10dfc8e57994e8b539884327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7c54318a474a250f8005c3b6813ac6aaa865ec7317485b87e9d4d67d57a7ff`

```dockerfile
```

-	Layers:
	-	`sha256:fd00071973ccff414288f8562254869fcbc1bb8bbf5ad41f68a319ccfc6aa674`  
		Last Modified: Mon, 21 Oct 2024 18:37:38 GMT  
		Size: 3.8 MB (3785316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc49852a05b179c9cc870ecae43139620d80116d14d17093c35bfcc2d8d7dd4`  
		Last Modified: Mon, 21 Oct 2024 18:37:38 GMT  
		Size: 19.3 KB (19277 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:8d38b3225c479de0269def8363b27f7f9164ff0908f0f3b8798f1424c751f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59535236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0258ca1d821b92063289e722aea6e7a0078ef02f94c06d763bd7c15e35012e81`
-	Default Command: `["perl5.41.5","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.41.5.tar.gz -o perl-5.41.5.tar.gz     && echo '844d47856b8347fba553c90fa10e76de7ae579f81ed5312acf5f638d72079df4 *perl-5.41.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.5.tar.gz -C /usr/src/perl     && rm perl-5.41.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.41.5" "-de0"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e301206c10d3a0f6b1888356862c89648f736e41d96ca4f94891dcce9cae542`  
		Last Modified: Tue, 12 Nov 2024 02:25:11 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bfe392d2ae70636bb5d11837f1e536e698e59ff0118fed6ede7822837f456e`  
		Last Modified: Tue, 12 Nov 2024 02:25:14 GMT  
		Size: 29.4 MB (29389520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e509d5950a5d54f24c25d81231f74fa0818fbe188a482d56b74df8b0ede5aaac`  
		Last Modified: Tue, 12 Nov 2024 02:25:11 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:664473d3eeecbe9d464e8dbc7ac3b8f0f8d75a98e901e66c12e7182377196916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3827226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9534a7c3525f95e3d6f276fba9d1f189b93c988acccbf45d0a6e60de47ef6c00`

```dockerfile
```

-	Layers:
	-	`sha256:af702545524476ec80c87f061edc60c08f80eaf9607482031e1f9f052171f0a4`  
		Last Modified: Tue, 12 Nov 2024 02:25:12 GMT  
		Size: 3.8 MB (3807941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a72a3fefdf27c7bb8548ffec6bb017cb8d738379aacf2a39d50d4f4d85bc39f0`  
		Last Modified: Tue, 12 Nov 2024 02:25:11 GMT  
		Size: 19.3 KB (19285 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:c9c06b1cad86347a63a7c79d0751a1d4e873c07d001e83d693af676af1ad711e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57516318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8e69e8cc29972d74748fefaecfb507957e202eb3389fb4345b4e4eeecb08e8`
-	Default Command: `["perl5.41.5","-de0"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:35 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Thu, 17 Oct 2024 01:09:40 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.41.5.tar.gz -o perl-5.41.5.tar.gz     && echo '844d47856b8347fba553c90fa10e76de7ae579f81ed5312acf5f638d72079df4 *perl-5.41.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.5.tar.gz -C /usr/src/perl     && rm perl-5.41.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.41.5" "-de0"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bc152ccb63abe4a025a92e16e303ad6eb5e2e6cd356d2ee0539ed4d80f7933`  
		Last Modified: Thu, 17 Oct 2024 19:27:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6240096df93bbc6a6782d281fb94003da7e881543939939b9f462dee74f4669d`  
		Last Modified: Mon, 21 Oct 2024 21:37:59 GMT  
		Size: 28.4 MB (28391273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa0dc9a4fc3921aa76df780275111553503555e9282ad7ce34f4af9a3229c3c`  
		Last Modified: Mon, 21 Oct 2024 21:37:55 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:b572d1a9f2ba956297c416f9241813a8b466431cd8332bf05bc7a09c1640ecb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4396f5435a724c2ccc2e5dc80257b19fa0d04d17bcb7cb40379ae28f6c950b49`

```dockerfile
```

-	Layers:
	-	`sha256:e516460155a69fec1d474319c076fd59c37ab7cc1b855207209e8b16f1a7c880`  
		Last Modified: Mon, 21 Oct 2024 21:37:56 GMT  
		Size: 19.0 KB (19014 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:f44068db7d742b96b8f54c52af72c71a022514b6a667970a7e316e7bbba1e17d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64176980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6bd44dd5ed032156a172ccc50a366e0ed935075362614569ea325d8a70bf52`
-	Default Command: `["perl5.41.5","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.41.5.tar.gz -o perl-5.41.5.tar.gz     && echo '844d47856b8347fba553c90fa10e76de7ae579f81ed5312acf5f638d72079df4 *perl-5.41.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.5.tar.gz -C /usr/src/perl     && rm perl-5.41.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.41.5" "-de0"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038dec34a00d814cd80151c62bdf80c416dedb23d4e1a4281867789fac6e604f`  
		Last Modified: Tue, 12 Nov 2024 10:20:12 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d66394d1ea75c3f3c2b6edcba83965bcc7e5979cca24dd17de5731f6b392e2`  
		Last Modified: Tue, 12 Nov 2024 11:11:48 GMT  
		Size: 31.1 MB (31051360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f71936de641f89a780822d5dda83a6a6bd7065f6f853001b2e71af74973f7dc`  
		Last Modified: Tue, 12 Nov 2024 11:11:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:38ec2db208ec42316026780ba17aa91ea9b512f1433cd8b0de4c7ee487a49099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3819245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d620487ad6b053820c1970506efb5bf446c46f0b82f81204f7867416d9e834ed`

```dockerfile
```

-	Layers:
	-	`sha256:f26b7773bc096a9811b1e0091e744d92dbaaafb983578a6905a6067b134286f6`  
		Last Modified: Tue, 12 Nov 2024 11:11:48 GMT  
		Size: 3.8 MB (3799862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac1698b396be642ed6ec816d9c8fce8adcf3794b6816dcb7efd7785b0e3cb34`  
		Last Modified: Tue, 12 Nov 2024 11:11:47 GMT  
		Size: 19.4 KB (19383 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:6007de0af5f38558f3313e663c8fcee598ed1ec888e0291b11f6d893928aae09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56252969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac45bcbfc7890889df68413a99f184ab5e2663372beb732eaf14e3ea22489ba`
-	Default Command: `["perl5.41.5","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.41.5.tar.gz -o perl-5.41.5.tar.gz     && echo '844d47856b8347fba553c90fa10e76de7ae579f81ed5312acf5f638d72079df4 *perl-5.41.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.5.tar.gz -C /usr/src/perl     && rm perl-5.41.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.41.5" "-de0"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a6c7dd8a651e2ba69544a46bb623124f069c40425a7a7994d936c7f9ddc447`  
		Last Modified: Tue, 12 Nov 2024 17:42:02 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617bb6930ccd4d93a4d50359cda9be455b5c8a1c724d63803bff6207234d5531`  
		Last Modified: Tue, 12 Nov 2024 18:55:39 GMT  
		Size: 28.8 MB (28761076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d77d7dfbf3e7dcc837f3bfdf3c825f8263009608db720c7d548709d6f093051`  
		Last Modified: Tue, 12 Nov 2024 18:55:38 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:e0c675198927c2335379064a8d1bcd8c812c6b155e3ac55c43908d9abe302856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3821560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a534f0bc3eaa936c91ba797d62bcf5a4ddaf17f05c54f26f3fdb86e8e2331ada`

```dockerfile
```

-	Layers:
	-	`sha256:c389e770baad999e6f0dda3225e22691a980806793e7d0a513bdfda0e8afe308`  
		Last Modified: Tue, 12 Nov 2024 18:55:38 GMT  
		Size: 3.8 MB (3802233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5111bb29e908721590eeef88aa3757b8b5f5d2a65c27ee804a74f32a56affe86`  
		Last Modified: Tue, 12 Nov 2024 18:55:38 GMT  
		Size: 19.3 KB (19327 bytes)  
		MIME: application/vnd.in-toto+json
