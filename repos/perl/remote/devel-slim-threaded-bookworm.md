## `perl:devel-slim-threaded-bookworm`

```console
$ docker pull perl@sha256:9c19a54269caf943b5d8deb5b1c450ef10cf6a8598a506b843bb9d4967cef4ee
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
$ docker pull perl@sha256:d6f5d86193f73b359d58ca3596af0984642795b8f56650cf45fe40012cdebb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58764870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdec87f0f1b30ed44891b888a67ae0b6089f883e7c5619b697fabfab34dd8384`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:55:57 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 02:00:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 02:00:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 02:00:54 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfea5a6b58ac7fce195a681f42c46b6fb2545b82eeebb6662cc4b88f44c09c74`  
		Last Modified: Wed, 22 Apr 2026 02:01:06 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfbbd34685e75bb819c56958e02fd2c93113bc10813f98e2b77dedd6149ef81`  
		Last Modified: Wed, 22 Apr 2026 02:01:07 GMT  
		Size: 30.5 MB (30528352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ca687dcaa4b5fb6a75f1aa0f394502bc45fbd5c6c279a052e03728af19c962`  
		Last Modified: Wed, 22 Apr 2026 02:01:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:002d4434179e136f9479985481c9f65725c2ec224ba35e086e97e4c2b10ad44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3957740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7240c822c1e430d19b0eb12d265825741030ab9c3dfa757663374e0f1b73fb53`

```dockerfile
```

-	Layers:
	-	`sha256:e6843b0e595905c6c4bc7313cb968a4ea34f6517013b058ac7d8d07f18bd8d43`  
		Last Modified: Wed, 22 Apr 2026 02:01:06 GMT  
		Size: 3.9 MB (3939394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a20128d045c822232ca1e1774eca70207ae84ad709f9bea255e66b40aa1281d`  
		Last Modified: Wed, 22 Apr 2026 02:01:06 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:b9c7ff285d7a88be2669dc9169fc9d86fbef3ff1c29f26219465d7d8db3b7b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53345478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864533cb626d2e188083984c58e5eb3c53f92043adb874c61be3880a0faa44a`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:29:05 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 02:35:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 02:35:25 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 02:35:25 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:10e5e7c244713d6618375e8360e3d0989303f5cbb40b7ea158ce628f92e32f96`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 25.8 MB (25765657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b716457d87e9c305299b77c303c8a511557249ce177a3dc0bf6d3e9bfaab116`  
		Last Modified: Wed, 22 Apr 2026 02:35:35 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c966b30de1c7b3b8e53b9268a91a7275e2f64dcac3bde0c9914f7d8c36eab5eb`  
		Last Modified: Wed, 22 Apr 2026 02:35:36 GMT  
		Size: 27.6 MB (27579557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64ec99d7b59973eb2b4444f2a57a64ee3bd40205ad6b48af3be1ac4dd4c634d`  
		Last Modified: Wed, 22 Apr 2026 02:35:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:3f3a281e9c0de65e83c1d88c2de3ff30e26ad8e792cf233dea78edeade31a172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e68c1ea0cc5a4b54fa5b8288c67611b1dcf7eefa529acd79d1bc43e23dbd2f`

```dockerfile
```

-	Layers:
	-	`sha256:c9815b4fd256207b45d52de270652a5f16e967303f056ea94ca03b6fc936b390`  
		Last Modified: Wed, 22 Apr 2026 02:35:35 GMT  
		Size: 3.9 MB (3910245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adf21cce908a49b9b7ace9d9ec69f42675feb7711a316501bf3d4165f267187e`  
		Last Modified: Wed, 22 Apr 2026 02:35:35 GMT  
		Size: 18.4 KB (18418 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:1e480632e74e770ab2241504fc27dedbff7abc1b86095f84d2e997e8db2b0063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50601447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41474ad9610c520b0fa6639708096f3bbc25d5c6badc201d4ac1adea4f008e7`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 03:04:09 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 03:10:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 03:10:13 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 03:10:13 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:d3311d55816cf34cc663f098f8e93bb8dca4772ce9f25ac1e909fa7b0628d17b`  
		Last Modified: Wed, 22 Apr 2026 00:16:41 GMT  
		Size: 23.9 MB (23941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09de623a4f608c8a948ffdc94f35ef2032766d26a05c7e81b173137870bbd3a8`  
		Last Modified: Wed, 22 Apr 2026 03:10:23 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f952d6211939390269016b301c2d3beb14276369b3753a209e1a00ce87fc01`  
		Last Modified: Wed, 22 Apr 2026 03:10:24 GMT  
		Size: 26.7 MB (26659756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3867fdcd8da5a863e526025cea00cc1dd41cbf0220fb6b70b0692808b7102f`  
		Last Modified: Wed, 22 Apr 2026 03:10:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d8f6328456a3508328d02cb614ed904907f8e142065e351ee28f6bb8daad2fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9182a0409c20c7a1a7a23f2c8215ca3be9c4e979c833a8be63b8974d3b8af346`

```dockerfile
```

-	Layers:
	-	`sha256:f3819f87c75a29fad9c903672a6a99d3e51e8e04da375b9d620801565689746f`  
		Last Modified: Wed, 22 Apr 2026 03:10:23 GMT  
		Size: 3.9 MB (3909470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09361149e076b791425de0837aa2de4c06245f102b3fd4f32878f44b8eba823a`  
		Last Modified: Wed, 22 Apr 2026 03:10:23 GMT  
		Size: 18.4 KB (18418 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:807c23d377867064ff8b11288ba6766e5ab60a15978d7aafc00fee06e5918a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57496185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c80651f73d1460f1f7082d8ba7a2bc7b2516d66984c9028a3b10b1101a8428`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:58:47 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 02:03:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 02:03:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 02:03:54 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883cfc74909e828bd67bf0f909ea9362ea3ae9568da8309475cfa189c3746638`  
		Last Modified: Wed, 22 Apr 2026 02:04:06 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d737cddea2bc1449eb3b7a449c195e960d274f34f64c8f0483036318b30ce81`  
		Last Modified: Wed, 22 Apr 2026 02:04:07 GMT  
		Size: 29.4 MB (29379807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ea6c4d7f8b0fa6583f54289605872f7cff307faf54ca0fdb06b7d843c60719`  
		Last Modified: Wed, 22 Apr 2026 02:04:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:3171d2fee890aaf4fbfe8ecc37bde43431ea10cef708f83e9cf171d08c609994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90f9d7a59464d5624023b03f5e552cc1eccffd37020d490311c65727784a612`

```dockerfile
```

-	Layers:
	-	`sha256:e0e883ba2d561fb7e6fdea3a5a170a83a621541e1da9b5fad379d23a0b9d3903`  
		Last Modified: Wed, 22 Apr 2026 02:04:06 GMT  
		Size: 3.9 MB (3910631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb62deb16f0055f2bf69aa0606ec006b23af519595376f0c7baf9701d09e4d79`  
		Last Modified: Wed, 22 Apr 2026 02:04:06 GMT  
		Size: 18.4 KB (18438 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:820575894f42ebe400b1caaa5dce194cd694c7ad30392d80973d10c751d8f60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58938076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66da2d2f62fda27a141a9c874741d2038266368d5ffa6a8160f80cccf7493ec5`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:50:32 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 01:56:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 01:56:09 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 01:56:09 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:ceab9188c99bb4807b7b5b31c76962e728b9040bd3676ebeeabf72b13d039523`  
		Last Modified: Wed, 22 Apr 2026 00:16:30 GMT  
		Size: 29.2 MB (29221696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0ba3c119e7a59f14567709db449fd26e4ec002f9ca2c9338327cb69177df24`  
		Last Modified: Wed, 22 Apr 2026 01:56:19 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd65ea3ebad548877c3369dab581442b547ff1e2f6a7f55fed0469ff11d8c515`  
		Last Modified: Wed, 22 Apr 2026 01:56:20 GMT  
		Size: 29.7 MB (29716114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4baeb4cebe3068f8934bd56aa690941c76ccb2bfd031596cdd0cfe92bea2429f`  
		Last Modified: Wed, 22 Apr 2026 01:56:18 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:afc04fe390792a2ec9d29b4c2dee109c3bf064b693532d92a8e0565a809539ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb6f26733e600e0077813c9cf235170ffe2049f81a44d522fc7e2f8d7143844`

```dockerfile
```

-	Layers:
	-	`sha256:3acb287d3fd7b9e225ced5b95e2b76c00fd1430a5940a4000cc293748b1fb162`  
		Last Modified: Wed, 22 Apr 2026 01:56:19 GMT  
		Size: 3.9 MB (3933336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f94c1ec6dbf3bd7771f25298899eb1181f647cfe034d0d7319474b746848f9`  
		Last Modified: Wed, 22 Apr 2026 01:56:19 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:2ed5a2db1678dd2c56a53243c68ce394f0d74e9a10b6cd2bee55547ecaff10a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57243394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a15c7628e4867213bfa50d438b144cc4e4fefceb4f3a4127ec3cdfaab558f7f`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 15:40:36 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 19:20:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 19:20:32 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 19:20:32 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:7377a524ccdc918cca6272a35a48618805ffa8fb443fe7f687971509cb1f8d53`  
		Last Modified: Tue, 07 Apr 2026 00:10:05 GMT  
		Size: 28.5 MB (28526285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61569bacde7390f6ac6013444e8d7cbdd110175943fd2a8363795805e8b5a91a`  
		Last Modified: Tue, 07 Apr 2026 16:06:41 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c486eff058cce3af3e36a9cacc5dd8553b994dcfd69aa8b95cc455b83651ff66`  
		Last Modified: Tue, 07 Apr 2026 19:21:17 GMT  
		Size: 28.7 MB (28716840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12483c941234a1367451929054d177c2b1a5bb4e1dca74ce4ea346b85e1b6d5b`  
		Last Modified: Tue, 07 Apr 2026 19:21:14 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:5edc0e2284a6c41b0ee9c32ee362c92a2847e39f2212cec4ff38e0a83bfbf001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ad2175105c5d85037f98d486df6ae98cc1b77d4cb556af8fa394138dcc2bf3`

```dockerfile
```

-	Layers:
	-	`sha256:8cdc0bc18a82ebee382a34e83f50268a52cc522c35ee5d9a902f13fb7e77a8fb`  
		Last Modified: Tue, 07 Apr 2026 19:21:14 GMT  
		Size: 18.2 KB (18188 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:11df3417d568905c023435324870a549250a9f86e15950ec8802cbc9c3109ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63464144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ff37d1506dfc6f59ad6dab602c5d0967298024a82077041e5ffb3a65a1799d`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:26:01 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 06:34:29 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 06:34:29 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 06:34:29 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340168cedbbaad69c0a1ed5b35ebf9c57e0e448ebbbfa035fd08f23ff167e4ad`  
		Last Modified: Tue, 07 Apr 2026 05:34:51 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2bf12d628098e71c74594f4689ac129e587918402e589a361ca2dec187fbf2`  
		Last Modified: Tue, 07 Apr 2026 06:34:50 GMT  
		Size: 31.4 MB (31385413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b45bca539f5a778733ac894ec2c38d5ac718ebfd9efef364ca1de7fc3e45e26`  
		Last Modified: Tue, 07 Apr 2026 06:34:49 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a097b7168f960cca894046d38bc7c2129e2f560331d226c1c41e072d2ef7ba72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3943706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10e41c75591b2a689fa9364d9c301beae4e4234192face2733738a29e308148`

```dockerfile
```

-	Layers:
	-	`sha256:79dd3c68cd66076627f5294e37909b63faa5603134bc6107583f3c65e8aca102`  
		Last Modified: Tue, 07 Apr 2026 06:34:50 GMT  
		Size: 3.9 MB (3925322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54d2b86784b4553f303595de8117c75fcbed9b19adaef023b27c6ad1ecb9bbf5`  
		Last Modified: Tue, 07 Apr 2026 06:34:49 GMT  
		Size: 18.4 KB (18384 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:773603d65590887dc687a6c9f52fb8a05aaaee2ae88a35edce350a3b5358f28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55993029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23bf644e5ca7d84c338265660be6f6e3b1eb9a71c86e35e5a1691cb93a637ad`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:23:54 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 03:53:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 03:53:37 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 03:53:37 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a939a92df72f194e8a308cab082b4e0f675cddd7b37884dfd9fd93903e6a41`  
		Last Modified: Tue, 07 Apr 2026 03:31:16 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555964fd3fb84ac688d2ac5c5068e2de9229775358af42b124d00ce2439e01af`  
		Last Modified: Tue, 07 Apr 2026 03:53:54 GMT  
		Size: 29.1 MB (29101127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8c21f1d2c7bda2544ef032fea002755db2a7d717468d5e6d58ae67971af740`  
		Last Modified: Tue, 07 Apr 2026 03:53:54 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:6636d5427998da52a1c36f32f70dc5871705b4c943f13f2634bd41eea1ecd9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3943013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c1821094858f44e0c6048d22dd5b8cca44c08f17392ae3efc459485e65bfa9`

```dockerfile
```

-	Layers:
	-	`sha256:ec82078bf937fc7061531d88b9210f98dddce582f2ed9b66e1b6b0c01bbfc652`  
		Last Modified: Tue, 07 Apr 2026 03:53:54 GMT  
		Size: 3.9 MB (3924667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf61ef06dd23302fb4888af7ccf39b15b1ecb75a2d6a8454eda3ced76483a7e3`  
		Last Modified: Tue, 07 Apr 2026 03:53:54 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json
