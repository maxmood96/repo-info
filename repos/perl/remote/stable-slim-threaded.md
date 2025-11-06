## `perl:stable-slim-threaded`

```console
$ docker pull perl@sha256:511e8888e5704255849367f2d1f613c09007d89fe0b5f23323a88e90ac78307c
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

### `perl:stable-slim-threaded` - linux; amd64

```console
$ docker pull perl@sha256:289cff06226fda55010e855345cf19c8e45ec7131d8576f0f0ceb0c0c476e3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61786084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f7492d2895f01ac78f624c342026e1e9386cf4eb3da6c2ba58ab0222217657`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:18:10 GMT
WORKDIR /usr/src/perl
# Tue, 04 Nov 2025 04:22:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 04 Nov 2025 04:22:40 GMT
WORKDIR /usr/src/app
# Tue, 04 Nov 2025 04:22:40 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddb8a3f0f82134466fd7f8901f0d8c9ee39934dab730346bb48305be2ec691c`  
		Last Modified: Tue, 04 Nov 2025 04:22:54 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14e99aa6928ac2fd80ca47399055c69a8984029893b1f0d72b1fc1fa25652d9`  
		Last Modified: Tue, 04 Nov 2025 04:22:57 GMT  
		Size: 32.0 MB (32007718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652438619a43f232388276542e57b7716f72f0f1a2d2d2a811925534caa4e4a9`  
		Last Modified: Tue, 04 Nov 2025 04:22:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:202681c90e969fc1c0469efacd44e514225f8346ed671fc4cea534c3228acdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958bb4e70a1245ea93caf38c8da855f57455186aeace1d0a106a610c4b39c7c9`

```dockerfile
```

-	Layers:
	-	`sha256:988e668eca5dccc03d8c7e676bc9d463e243f56ca746edfe9a450eb600f39b14`  
		Last Modified: Tue, 04 Nov 2025 11:38:46 GMT  
		Size: 4.0 MB (4010630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f4cf57083a375ca55372dfe43acfa4b68cc411174c9b7a155c60140ecd98aa3`  
		Last Modified: Tue, 04 Nov 2025 11:38:47 GMT  
		Size: 20.5 KB (20483 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:73280d013186ded2e52943f5a9fe864ddf919eadcb1b654ef3e4743a7cd1708c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57170228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0df43d4388518701f37e287b6e67cff6a1297d5e4f632b1275c4f61f3f60dd`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:37 GMT
WORKDIR /usr/src/perl
# Tue, 04 Nov 2025 01:36:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 04 Nov 2025 01:36:41 GMT
WORKDIR /usr/src/app
# Tue, 04 Nov 2025 01:36:41 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdb4a1768cd8d4e4df0d753981463d9b4956d590a94889421e39a0c91296341`  
		Last Modified: Tue, 04 Nov 2025 01:36:58 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158fb9449aeaa2b3645a48a73e330def8e03d041c2946fa2619d47f63794e2fd`  
		Last Modified: Tue, 04 Nov 2025 01:37:00 GMT  
		Size: 29.2 MB (29223528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f80f7ce57e14b84634f6652c6a3e2299a89bae33c06ba953f042f7b4be183f9`  
		Last Modified: Tue, 04 Nov 2025 01:36:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:80cc8c0980d3cb29315ee9caf650e05e7955f14926c61548e66142ea5d567ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9796e29cc2cabbbfd3aba859e220f79d29d64af8f472088c169477eb7baa5873`

```dockerfile
```

-	Layers:
	-	`sha256:449ef7895ef0c64ef06c12dc20c974cad6350bd43769cccd3dd20fcd8e25dcc5`  
		Last Modified: Tue, 04 Nov 2025 08:37:59 GMT  
		Size: 4.0 MB (4003707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de590bf4f9b28c42e6141251669d6a21442e73a6324c682ed9cdd0f929d23453`  
		Last Modified: Tue, 04 Nov 2025 08:37:59 GMT  
		Size: 20.6 KB (20611 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:502bb47708d56cf955e57cb9918f4305b79e1ed93211b856a7cfcf513e674a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54515580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75a8efc70a32b4351c2e3cc63378c7ca3d7c8b70150babbb6f9b1e50c27d730`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:27:12 GMT
WORKDIR /usr/src/perl
# Tue, 04 Nov 2025 02:33:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 04 Nov 2025 02:33:03 GMT
WORKDIR /usr/src/app
# Tue, 04 Nov 2025 02:33:03 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cf55b416e648d343e9e532ab1a846951db9470aabb98d96d07ade9514a0b78`  
		Last Modified: Tue, 04 Nov 2025 02:33:18 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6528d2ba0fac377999b084b0467ebe09f42722019551cc0d76ceac335d08d31`  
		Last Modified: Tue, 04 Nov 2025 02:33:22 GMT  
		Size: 28.3 MB (28302276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11194ba7e976ebd7807209cbd58d2928afa4533e2d27ca4abedba2d0813a06a3`  
		Last Modified: Tue, 04 Nov 2025 02:33:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:07434601c5351d4cb174d0b459de5a43a0733b6b2e870b044bafc07eda56e3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fecc53cf9fb732aacbd6bd35f15dd6363e1bda2d9e5a331d0040404ce07280`

```dockerfile
```

-	Layers:
	-	`sha256:517f6f074e2bb78fbc70a8b45183c891547f73a268f1b5d60a80497a6ae7d2e6`  
		Last Modified: Tue, 04 Nov 2025 11:38:54 GMT  
		Size: 4.0 MB (4002898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a293d669eeb355e4fd40278696208b4aabe02346a6f0d5c735cf4910f38eb613`  
		Last Modified: Tue, 04 Nov 2025 11:38:55 GMT  
		Size: 20.6 KB (20611 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:59bcc2d7e4a5f4c3fe4bbbbfcfedeb93c10db5e02208553474e2bfdd059a229d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61803016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f757f35442d02e2fffc8b020b9f941721c3a2c4c0de6b9ecc0b4f6ecfe2f25`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:33:39 GMT
WORKDIR /usr/src/perl
# Tue, 04 Nov 2025 01:38:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 04 Nov 2025 01:38:47 GMT
WORKDIR /usr/src/app
# Tue, 04 Nov 2025 01:38:47 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dfeaeed85b733780a5a1b91f9d12d77d1c8cb4fc64496cf0fe2a704635697e`  
		Last Modified: Tue, 04 Nov 2025 01:39:05 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c005538d1ebbe9d949bbd2945a466d3facc3acc8aa9ef8b783c22c60640bbc73`  
		Last Modified: Tue, 04 Nov 2025 01:39:08 GMT  
		Size: 31.7 MB (31660454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f064ada0f147b9bb4b61e26323bb2bee74ecb24f418ec4b5e056d2cdbc762a6`  
		Last Modified: Tue, 04 Nov 2025 01:39:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:1cf72503202e4bfd66d5c88c8ee33ff9d5ad26751f465ac2524d0a212db3fb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022557a3a62e0383483a000a0092cdefccb70b2a20a457c4571afcf591c3c9dc`

```dockerfile
```

-	Layers:
	-	`sha256:b38201c7f6514038cf2fbeb25cf00645671e9b4314ab49eeb1261239df0c35f0`  
		Last Modified: Tue, 04 Nov 2025 11:38:59 GMT  
		Size: 4.0 MB (4005773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb17c43790b5b6f493dd02e509d43c55db514771446d70e5a021636fdecbb97`  
		Last Modified: Tue, 04 Nov 2025 11:39:00 GMT  
		Size: 20.7 KB (20659 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:a2754b362b7a6bdc18367fc8dbb404c20f73ca3c48e6fbcd081acd3e5f1a80f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66370574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cbae4efd32bdbed19bd1dc69678156a0e9f0ad8a6bf3b310c9585efd6900af`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:50:08 GMT
WORKDIR /usr/src/perl
# Tue, 04 Nov 2025 07:15:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 04 Nov 2025 07:15:26 GMT
WORKDIR /usr/src/app
# Tue, 04 Nov 2025 07:15:26 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46a9497fde7a377af3120a2874dc0acf0eac719325537c05c5b8e98b598ea51`  
		Last Modified: Tue, 04 Nov 2025 06:58:28 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11b2e83bea8e661a1fbd58e109cd9cb287470ad5fac62256dfc79d5c4f08205`  
		Last Modified: Tue, 04 Nov 2025 07:16:21 GMT  
		Size: 32.8 MB (32771664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0ac23d75d1f12ff1e75f0f52cd2974e0b96b0f1bd533b1a41b4915fe39b1b2`  
		Last Modified: Tue, 04 Nov 2025 07:16:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:948024e85cc586ccbba451f5ed27fa6c106c323d115eebbe02022424b69c784b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4027228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0afadd5d233c17c51446a5aacd1af5cce7c2f2f16e4950161d677a6ade6103f`

```dockerfile
```

-	Layers:
	-	`sha256:28e59eac6ad2fad00b0daab4e89611fa6334cf0e9772299ac86f958f651a195b`  
		Last Modified: Tue, 04 Nov 2025 11:39:05 GMT  
		Size: 4.0 MB (4006666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91234e71fe0f138e9d34139e3bb7b1021ce1bfd662d42c2f02e4313bf069761e`  
		Last Modified: Tue, 04 Nov 2025 11:39:06 GMT  
		Size: 20.6 KB (20562 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded` - linux; riscv64

```console
$ docker pull perl@sha256:1b5c98e71f1223fab2cd3114122fece36c32d11e577ebc4dd71535aecf983048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68084252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ced9f06deb7ceb56f3c9e4742e17160992ab91e1a898fee7bc464cd4071fd1`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 12:15:42 GMT
WORKDIR /usr/src/perl
# Wed, 05 Nov 2025 14:37:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 05 Nov 2025 14:37:33 GMT
WORKDIR /usr/src/app
# Wed, 05 Nov 2025 14:37:33 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84faa22d9b11ce3c069263d2a25f95caf79d357665c9586a3d3f0ff2e443f661`  
		Last Modified: Wed, 05 Nov 2025 13:25:29 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc5c09399a3b4d9cbb857dfc3af585c7cd95b2b1d13960a61d72ec120712a3`  
		Last Modified: Thu, 06 Nov 2025 11:19:19 GMT  
		Size: 39.8 MB (39808200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba5056b7dea962c995c01b1ebc06f83bf055c00c308e8a79e21dfbde4b67994`  
		Last Modified: Wed, 05 Nov 2025 15:15:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:79123fabac75be9e12f451e98dfa103ef1cb1167dd0de2faa95fd8fabde8cd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4018495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d868a46677b0de89f8fc4aee5185ddccca787e90d91cb742ca4926f31e9c964`

```dockerfile
```

-	Layers:
	-	`sha256:fdeaa321fc783950d43085cc4ae56ebe8193930f20f62d36e71ea0cf0edfd421`  
		Last Modified: Wed, 05 Nov 2025 17:37:43 GMT  
		Size: 4.0 MB (3997932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef368198c54a613393ce1ff59fd9674e3236d6b0982059ad2168f80255da2c1`  
		Last Modified: Wed, 05 Nov 2025 17:37:44 GMT  
		Size: 20.6 KB (20563 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded` - linux; s390x

```console
$ docker pull perl@sha256:c638de3fdd41feb5e77417bca6e2d6f412b9cb75087ec495619df0f9ddb8e486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61183058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64075c0bca47a56895ff0d1717a1a6deac356174a078eb2fee471205d6b354b`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 10:37:40 GMT
WORKDIR /usr/src/perl
# Tue, 04 Nov 2025 10:51:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 04 Nov 2025 10:51:28 GMT
WORKDIR /usr/src/app
# Tue, 04 Nov 2025 10:51:28 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fe8f64f72a971c6ef3b29f23d98bd706faec8c66727f7756a94837942aa4be`  
		Last Modified: Tue, 04 Nov 2025 10:44:17 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480bdb45b3debbe40d674eb480a8aef1f74b5017c20b9d4f616179a087ba454d`  
		Last Modified: Tue, 04 Nov 2025 10:51:57 GMT  
		Size: 31.3 MB (31345401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c062bb693248efcff4e048618b7f3f6e0a6929ed5245aecd4c4abb024b397d8`  
		Last Modified: Tue, 04 Nov 2025 10:51:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:8105fa9356ceff0434b32d94e926bb75683486d21be5ee3298921287b9e58721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1515df6698bdcac561b1b3573494337b19876448ab87d5d81082c91bbd3c53`

```dockerfile
```

-	Layers:
	-	`sha256:3ae5a1cdd61122345f944dc62b1a9b067b9ecf833ba0da54cdea48f9d8090a0f`  
		Last Modified: Tue, 04 Nov 2025 11:39:14 GMT  
		Size: 4.0 MB (4002958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cefb84055d192dc9df37a27005a787f73b11586686c92fc96a7e25177136934`  
		Last Modified: Tue, 04 Nov 2025 11:39:14 GMT  
		Size: 20.5 KB (20482 bytes)  
		MIME: application/vnd.in-toto+json
