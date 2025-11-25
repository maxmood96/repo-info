## `perl:devel-slim-threaded-trixie`

```console
$ docker pull perl@sha256:d054ce794754888aeada6727fa3f88211f21cf2beb1bbde2d209ccdde04c3237
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `perl:devel-slim-threaded-trixie` - linux; amd64

```console
$ docker pull perl@sha256:4a121667a56ea25c8b4153f4eee38bbf293bd4ac00acefe8541919d102b25ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61925014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf468a1e5bf4c5d060e70bbac27ac947886ee91fed0841fd1f37198e21a2a1a0`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 25 Nov 2025 16:38:53 GMT
WORKDIR /usr/src/perl
# Tue, 25 Nov 2025 16:43:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 25 Nov 2025 16:43:47 GMT
WORKDIR /usr/src/app
# Tue, 25 Nov 2025 16:43:47 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe3514df2e3b5055ca5e4d43a0725e6efc81f04c2e6245baa4984fe57c0ecca`  
		Last Modified: Tue, 25 Nov 2025 16:44:04 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e019b356390d861c0bb705c8fdd0f8817012c8f5bdddf1cfa46957313cb1460`  
		Last Modified: Tue, 25 Nov 2025 16:44:12 GMT  
		Size: 32.1 MB (32148262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d24b209a0a779aef9e9934b8ac67ae784dcf288f290bc09fbd5911ad9c69a1f`  
		Last Modified: Tue, 25 Nov 2025 16:44:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:d65a3b550ec315207901c5bc4cec3e16c23218582f6e8c77b4d7142e99a65b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb6c3ac22591f0f7fea06730a8355b25e6b374c80c4087e84fb33fca911e827`

```dockerfile
```

-	Layers:
	-	`sha256:1909c91e4bed7b74dfd653fbfab7109693b578d6d2d3b2b5260314ae6acd1a5f`  
		Last Modified: Tue, 25 Nov 2025 17:41:30 GMT  
		Size: 4.0 MB (4009386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99eed458e25bc79d8df8c93a27a783a4b45b04af05f522d38133e0f2f1767fe7`  
		Last Modified: Tue, 25 Nov 2025 17:41:31 GMT  
		Size: 19.3 KB (19283 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-trixie` - linux; arm variant v5

```console
$ docker pull perl@sha256:4fe2a8d01012df4b835d155403e9a8f7fba96e253fa06b22d93c52985dfa4fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57322688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6997f54f8d25af0c4e81ffde979e9965313f0ff49a55a3eddd5e0d13325c50`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 25 Nov 2025 16:44:06 GMT
WORKDIR /usr/src/perl
# Tue, 25 Nov 2025 16:49:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 25 Nov 2025 16:49:59 GMT
WORKDIR /usr/src/app
# Tue, 25 Nov 2025 16:49:59 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9629c070cb5986a70fde748f9ea8146deda81fde2fa4831de88a561d50be3394`  
		Last Modified: Tue, 25 Nov 2025 16:50:17 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6a16e853eea380312adb590a9949ee42f00b339dec4ef3ca73883ed19bca92`  
		Last Modified: Tue, 25 Nov 2025 16:50:19 GMT  
		Size: 29.4 MB (29378273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7f3fe00a498e4491bd69818900619ff5ea1ab2f4f23d93c18c000fa717a9c2`  
		Last Modified: Tue, 25 Nov 2025 16:50:18 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:4616217ccaee142d9098fd0ddc104a008edc06c89efb8e673403c3d5411d70c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4021810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc74d422900590a65c39e508306e5e12785c4ef40a005a7dde6a4dd28c2ad96`

```dockerfile
```

-	Layers:
	-	`sha256:27ae833e35d95d4903fd9ceeed1a2e10f1d58256a1c3aec35d2153ba2c867c3f`  
		Last Modified: Tue, 25 Nov 2025 17:41:36 GMT  
		Size: 4.0 MB (4002431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c070ec805554def0e08e15d78b1a14c85071b18b2aad856ee9483ed9657dd62a`  
		Last Modified: Tue, 25 Nov 2025 17:41:37 GMT  
		Size: 19.4 KB (19379 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-trixie` - linux; arm variant v7

```console
$ docker pull perl@sha256:fcd1ef8d8b53d93f595b88ac96b5513a1c5171bc95d6b862cfd242187eed1a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54656683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209dbaafcf8736b6cc9994e14b08da8caafe78257050da9aedca002e8c2b98a3`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 25 Nov 2025 16:43:37 GMT
WORKDIR /usr/src/perl
# Tue, 25 Nov 2025 16:49:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 25 Nov 2025 16:49:24 GMT
WORKDIR /usr/src/app
# Tue, 25 Nov 2025 16:49:24 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4ce769500ad67b50c2fb6ad559c89d4237e3597f532a5eae12f958070e64d5`  
		Last Modified: Tue, 25 Nov 2025 16:49:40 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312a99ac07a4dea2d40779dfdd6514b8350f5705b47f74658726f35f9f94f8b5`  
		Last Modified: Tue, 25 Nov 2025 16:49:44 GMT  
		Size: 28.4 MB (28446456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5ab621f3b782d31175566718807fd445a9188c7e5ab114cd211752f56afaa6`  
		Last Modified: Tue, 25 Nov 2025 16:49:40 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:c42ccadca0145891ae35790d851ccdbcfcf16dfeb513a415f6c125851e959ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4021001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7042e08b152abc02326cae9de6560ff2ef4ac9314217898ad69b2239681f0246`

```dockerfile
```

-	Layers:
	-	`sha256:34bea123ce9f1c9b37e5fd5ea7c266cb8e9659661d7b2a2a0d325ece6328f62b`  
		Last Modified: Tue, 25 Nov 2025 17:41:42 GMT  
		Size: 4.0 MB (4001622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf87ea151e14502dd3dd83d49199174c6974a6817df0d4437d61472c42c9ca2c`  
		Last Modified: Tue, 25 Nov 2025 17:41:43 GMT  
		Size: 19.4 KB (19379 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-trixie` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:ee684f16af0ba4aedf5df87b4e0db8b1220a07cc00159e528fae05bf1bc9a262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61942912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4882fd24b21f59bcd4cb8216e8a3509ce0abc60320962340d080c9d430ad7f94`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 25 Nov 2025 16:36:50 GMT
WORKDIR /usr/src/perl
# Tue, 25 Nov 2025 16:41:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 25 Nov 2025 16:41:50 GMT
WORKDIR /usr/src/app
# Tue, 25 Nov 2025 16:41:50 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c771aa487174f8e34d05dec932f915a0ad358d8620beab0480094ecf600b071`  
		Last Modified: Tue, 25 Nov 2025 16:42:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e671622a17867d351bcc84183812e3ccc3441cc06fe9b3554cf1785062f66c7`  
		Last Modified: Tue, 25 Nov 2025 16:42:28 GMT  
		Size: 31.8 MB (31804034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f886f4e1e1197442658988e34cc1a0217684252c033c15f9890a7a37987753`  
		Last Modified: Tue, 25 Nov 2025 16:42:22 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:929be04c83fb82cce1336bb747397cc68cd103edf7a04b2191139103dd6703be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148cea7bfdb16149d8d94f2420dcdf14df13a2391f6782d8ec7b8828e9e4a0aa`

```dockerfile
```

-	Layers:
	-	`sha256:88fb7d549eea8f55e4993e5b5b217e6d5fea8e76f428b35e850473d42993dfec`  
		Last Modified: Tue, 25 Nov 2025 17:41:47 GMT  
		Size: 4.0 MB (4004481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b31f810bac8f3ae5950c61ec566be4a1afddd54b3cdac95883691187b8395dc0`  
		Last Modified: Tue, 25 Nov 2025 17:41:48 GMT  
		Size: 19.4 KB (19411 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-trixie` - linux; ppc64le

```console
$ docker pull perl@sha256:1012805ec3c9dd8966ae17b94541400ae11d4cd4d3be87ff2c16e86517e3ffdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66516675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4510bee9bc9a5c59e7b3ca01eaa0eb9d4185b7f7306f40bcbcf8872ba25c21ee`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 25 Nov 2025 16:43:27 GMT
WORKDIR /usr/src/perl
# Tue, 25 Nov 2025 17:06:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 25 Nov 2025 17:06:38 GMT
WORKDIR /usr/src/app
# Tue, 25 Nov 2025 17:06:38 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37cfad7a118094b92f5683876be1bc6c70055cdad14fe6c09e34ba330106768`  
		Last Modified: Tue, 25 Nov 2025 16:51:36 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323a2a42a73a94b4c1e64e4341552a7455310f181d9ebba1e0014d4c9adc276b`  
		Last Modified: Tue, 25 Nov 2025 17:07:39 GMT  
		Size: 32.9 MB (32919550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe459729f01d84817b7b9041e1307547edd286c13869b3cc12e92a740a4a3fc`  
		Last Modified: Tue, 25 Nov 2025 17:07:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:c8d868483699718a18e442d486b4176c734ce14f401a403ec616e77d90d2d330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52693da4ccc28fa0b496ec61967b08db6a298994b5fc7bcb967e427b6fc56ec8`

```dockerfile
```

-	Layers:
	-	`sha256:3e30b8da8671b185fffca856ab77d02ba7f75978e2ecfa8e08e2bd8bc88011d6`  
		Last Modified: Tue, 25 Nov 2025 17:41:52 GMT  
		Size: 4.0 MB (4005398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d11eb44e1f1dcf86f1299408f99bfede0f7221a242784258ffcb496ccdba3889`  
		Last Modified: Tue, 25 Nov 2025 17:41:53 GMT  
		Size: 19.3 KB (19339 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-trixie` - linux; riscv64

```console
$ docker pull perl@sha256:dbd29e0bb250d726f64a4b2c83424ffe7795d634b652883c5116f172c0397bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68219174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3e3bef9277f08784079b1179224371ba3974279eecb31957ad9c2c83d3bcef`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:46:07 GMT
WORKDIR /usr/src/perl
# Fri, 21 Nov 2025 14:02:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.4.tar.gz -o perl-5.43.4.tar.gz     && echo '75676cc02c1d4d6f4577f7fd953e07ab5d06f71cf4201753ab6e2b0ddb5a4931 *perl-5.43.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.4.tar.gz -C /usr/src/perl     && rm perl-5.43.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 21 Nov 2025 14:02:51 GMT
WORKDIR /usr/src/app
# Fri, 21 Nov 2025 14:02:51 GMT
CMD ["perl5.43.4" "-de0"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6928c7e45a6fa759c436ba0c58b6a512d4cad42edd79bb3f56b5ca1813ced5d4`  
		Last Modified: Wed, 19 Nov 2025 20:56:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe16164b6306a8072c8b092e54421d2ffc8276139894a47a7ba30b08e19ed42d`  
		Last Modified: Fri, 21 Nov 2025 14:05:33 GMT  
		Size: 39.9 MB (39945780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6522db90613c3fb66877ada86946dc735e9998e16ca16b9eef56fd05f3d29c`  
		Last Modified: Fri, 21 Nov 2025 14:05:27 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:e4fba90980f9cebe3db34b1f95d2d08c0c701c1ca5426ac787dde0274ba0a552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30d7067ebca3da9ec5cd8bd376c1089580a728279311935573debd9e4e33d40`

```dockerfile
```

-	Layers:
	-	`sha256:8114d00c6d69c3556c5624f4133803d8ae72a849892df23a86ac3c51d1d3601e`  
		Last Modified: Fri, 21 Nov 2025 14:39:47 GMT  
		Size: 4.0 MB (3996664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e193d0f13f7d3b7195c128f2a4e397a9d3863c05a59b2d5d7721564cbf6621`  
		Last Modified: Fri, 21 Nov 2025 14:39:48 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-trixie` - linux; s390x

```console
$ docker pull perl@sha256:bbffe4137e26f7383b467e99504aceb5894654f111f82c8e60df2ea861466815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61334171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d06eb9e121e8ddb7ea47e40f40a0ddca2ed346e5fe502c9be72620522725ede`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:14:31 GMT
WORKDIR /usr/src/perl
# Tue, 18 Nov 2025 07:15:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.4.tar.gz -o perl-5.43.4.tar.gz     && echo '75676cc02c1d4d6f4577f7fd953e07ab5d06f71cf4201753ab6e2b0ddb5a4931 *perl-5.43.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.4.tar.gz -C /usr/src/perl     && rm perl-5.43.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 18 Nov 2025 07:15:20 GMT
WORKDIR /usr/src/app
# Tue, 18 Nov 2025 07:15:20 GMT
CMD ["perl5.43.4" "-de0"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3606695f08f26553c27b321edc2320d379d4a4e37b4868fdd057c106d3823754`  
		Last Modified: Tue, 18 Nov 2025 04:20:52 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1069b0b7e7e937a98afb00fdd48482a3408c66bda54cbec8003eac083ffe6d13`  
		Last Modified: Tue, 18 Nov 2025 07:15:48 GMT  
		Size: 31.5 MB (31499532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71736d6b30924ff0d1761789e5387c7c577150324743b00b096fadd7d6da8e0`  
		Last Modified: Tue, 18 Nov 2025 07:15:46 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:90dc58707497dca65165c82deee6026d2192155fff3125332d62be3c102b0dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4021002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea34d1591ef6cef01e38f93746e688b930a549b2ff6bcc802bdc58a33c6f61d`

```dockerfile
```

-	Layers:
	-	`sha256:1d1d4cfafbf3e4ef9befdb9f9ad2bd42b3b24d987b7f024318b91263a66a97a0`  
		Last Modified: Tue, 18 Nov 2025 08:49:08 GMT  
		Size: 4.0 MB (4001714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d662e40a2be165321821e50486e155118ff8922a7c68c6698a3d01284df530ee`  
		Last Modified: Tue, 18 Nov 2025 08:49:09 GMT  
		Size: 19.3 KB (19288 bytes)  
		MIME: application/vnd.in-toto+json
