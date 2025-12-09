## `perl:devel-slim-threaded-bookworm`

```console
$ docker pull perl@sha256:2a00ea8629280e8c961c5895f54d4ee9b11ee49fc4bd30d0dedbbe2f42f145b3
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
$ docker pull perl@sha256:cf639a549986bd3093fc7402e51dc1ddc9ead0d9fe001ec5e206bfb300313c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58633771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbaa8b9460313f191755a42b6e6ddecb0b43eeaf9265b6ce059630e2618309ed`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:28:26 GMT
WORKDIR /usr/src/perl
# Mon, 08 Dec 2025 23:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 08 Dec 2025 23:33:39 GMT
WORKDIR /usr/src/app
# Mon, 08 Dec 2025 23:33:39 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6e79443292503a2f594b743569afec89928c4743b34026d10e20b2a8aa552`  
		Last Modified: Mon, 08 Dec 2025 23:33:27 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7964b7692523f16a981d5dbcbc09b2b98c2dea980253c2311a3b481f2f1039c2`  
		Last Modified: Mon, 08 Dec 2025 23:33:59 GMT  
		Size: 30.4 MB (30405086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796bba174fe3f3f2aac574c680398f8948c53538e8f906ddf8823049b2ce5f5d`  
		Last Modified: Mon, 08 Dec 2025 23:33:57 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d5d652aeb321cd65946db24bf393de1cd9a0e76e6346207926ac1efbdf6f7e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3957729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6689fdf8f01ad163b4a9d00f808b8e1e3a5fa7766c4c64c416929914aa4f00`

```dockerfile
```

-	Layers:
	-	`sha256:a06daab84fa2746d08f68614cd96ae179d6af6b35c58251fe1ca3624b28a3b62`  
		Last Modified: Tue, 09 Dec 2025 02:49:23 GMT  
		Size: 3.9 MB (3939384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0143ec26ace666b5520df172ff995de51b7b69f3db55096a483e294980651b58`  
		Last Modified: Tue, 09 Dec 2025 02:49:24 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:25325281fb70fc432368a064eb09fbf7672eeadd8313e7670154031c274ef3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53215622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57e6eaf6283cbaa90c68ea939d211b18dcde3102b3c78f1e3f4d072ceec1c1a`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:10:58 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 00:17:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 00:17:03 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 00:17:03 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:20ca79728ab9e4eb574872cf271bd965c51cf4e8ac84660ef17b281a3aeb750e`  
		Last Modified: Mon, 08 Dec 2025 22:16:26 GMT  
		Size: 25.8 MB (25757588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09508b52a933fc1f698955debe70d8d9f7da96a23c7910df5789fa2ea39876ad`  
		Last Modified: Tue, 09 Dec 2025 00:17:19 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b43668f6dd1ecab7ee9bf1ee795033f402d365e1c26e689a04b77aa230a657d`  
		Last Modified: Tue, 09 Dec 2025 00:17:21 GMT  
		Size: 27.5 MB (27457767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d912e99e8e9cebc4cef6fb4b6b1e972591dc8fbe49fe5a14e9c6f3d5bb617d7c`  
		Last Modified: Tue, 09 Dec 2025 00:17:19 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:6468c1c3844466ee99b8bc041f97c28899e78e1308d91449d941842710ce76d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb18cc0ae71e84280125736d2b8ed21eeb609fac0e3f51217afb4bb9a222dbca`

```dockerfile
```

-	Layers:
	-	`sha256:3efc650b89d104a4c1d6eeb82f2c2019a0e616fd6825b29ed6ab79bc62eac496`  
		Last Modified: Tue, 09 Dec 2025 02:49:33 GMT  
		Size: 3.9 MB (3910235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:707cc60c85d23b4afbf53ea489134859256a173ebd1fd70803a2e6f22b1b90dc`  
		Last Modified: Tue, 09 Dec 2025 02:49:34 GMT  
		Size: 18.4 KB (18417 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:5f1fb01e20e3223ff390cdc6cafcf9407c1e700c4e4651d9715026e76937a3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50477202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9250a0162757608d139910936a6d2d4aa1971e8a97d87875fb8921179193aca`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:37:38 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 00:55:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 00:55:35 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 00:55:35 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b70368822accd52ad083847121c8f8c4d60d6c6f16d3ac27f1663e9442ec64`  
		Last Modified: Tue, 09 Dec 2025 00:43:48 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b677329d2eee457b93a12865879144479baec33d6c8f875417e65979e161d21`  
		Last Modified: Tue, 09 Dec 2025 00:55:54 GMT  
		Size: 26.5 MB (26542916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b80c9e79f7dd846bdc62e4a8d99238d3b62f5ca1c9c00ab6ceff8138147636b`  
		Last Modified: Tue, 09 Dec 2025 00:55:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:93626272c23abdb24bbfbe44255c5f5c3f6a44fe6b18444332f9c9784c573c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1046a656f0f3848525657be82b59a942348396f12ff9deb7651f0785d336351`

```dockerfile
```

-	Layers:
	-	`sha256:4cfaa25dccfc6715a85e18d30f75b8c2210b64ce5860db1028df81979fa8a943`  
		Last Modified: Tue, 09 Dec 2025 02:49:41 GMT  
		Size: 3.9 MB (3909460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03ff7f2a8f52b1a6730fa777530be1dd3ddda9672d1db9516a39bd499b61d950`  
		Last Modified: Tue, 09 Dec 2025 02:49:42 GMT  
		Size: 18.4 KB (18417 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:70b729662dd806fcce643dc90fa9c730f063828efd4939d094aa1e2b3793ce74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57355997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae2ce92ed32140a3324a93c34ea1a06e516ed3b985d064304318fc3b49855ee`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:33:22 GMT
WORKDIR /usr/src/perl
# Mon, 08 Dec 2025 23:38:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 08 Dec 2025 23:38:22 GMT
WORKDIR /usr/src/app
# Mon, 08 Dec 2025 23:38:22 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec9b4e794b5509e3cfe34c7275a1207cd75db3bdac83b28b1ffd52d6522f6b3`  
		Last Modified: Mon, 08 Dec 2025 23:38:40 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee9c7ba7ff61a8c514e55200731de6985e09af29ec9a9d0bd04a61065756be7`  
		Last Modified: Mon, 08 Dec 2025 23:38:43 GMT  
		Size: 29.3 MB (29253503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504a39c31c1f34438651b7498d250ab579fa23fc71dafb41596349df6093e0f5`  
		Last Modified: Mon, 08 Dec 2025 23:38:40 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a546fa705c2c9b11719c29556a24d6b1b1d6fb7f5d66b8bf6f0ad06d228bdf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae227c99ad12f54ad97f1538a1d3c2c1873ee9ea35f1dbefafe2b00c49d2b50`

```dockerfile
```

-	Layers:
	-	`sha256:6f9ec156ed3dafb586999e5c479ca7a331715c7059e27d2e614c37285adcd5db`  
		Last Modified: Tue, 09 Dec 2025 02:50:49 GMT  
		Size: 3.9 MB (3910621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce5380668b019aaed2f99eebf6d771510b6c01ab8a14a2a17a6960d79138580d`  
		Last Modified: Tue, 09 Dec 2025 02:50:50 GMT  
		Size: 18.4 KB (18436 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:b3e0c0595716d52112245e45525594f8a4c46a04015a5d199ea46fee9d088ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58793293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a349ee886c0cb8ab4087786fb18f89202e917e35bf37d2d897e6e1ef65074d`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:16:17 GMT
WORKDIR /usr/src/perl
# Mon, 08 Dec 2025 23:27:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 08 Dec 2025 23:27:39 GMT
WORKDIR /usr/src/app
# Mon, 08 Dec 2025 23:27:39 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813990653db1ebf75d8f8e5402db57b9372148e8d78ec64833c7c62150c23743`  
		Last Modified: Mon, 08 Dec 2025 23:21:45 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e84f1bc912f2cbab78f9385c9ff3a8b2c0a52bd69b9b3f98e9a24d0fa01f20`  
		Last Modified: Mon, 08 Dec 2025 23:28:02 GMT  
		Size: 29.6 MB (29583299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5ebf2c6f98430cef476aeb5bc21cb292b9ab72a2e88e0b5231414681e7c94e`  
		Last Modified: Mon, 08 Dec 2025 23:27:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a17e5a5b6051d5ca5b12c2885ba16a9f49376464d4393b6118af01dd257da31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fead4e4be404d803c5b9234b78589cd7f455777f1026968c55db46a3d39f3ee`

```dockerfile
```

-	Layers:
	-	`sha256:8eacf272326ae781ae2dfa8875c88b01059fda2be264ad0571fa8503fb5d9ca6`  
		Last Modified: Tue, 09 Dec 2025 02:50:55 GMT  
		Size: 3.9 MB (3933326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7ab348bd5db5e1fa6a6ac2ca5a4d9f3698d9ff97a19f3fbfa82bd8109d897c`  
		Last Modified: Tue, 09 Dec 2025 02:50:55 GMT  
		Size: 18.3 KB (18318 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:c7a93e5587cdf2261da26ed609444da8f7989df870c075535fa55d2dae9cf8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57094924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5469081a08082b887b9db06c986c90ada895f5a219e36d4fd38a0f8f84a066ae`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 22:50:19 GMT
WORKDIR /usr/src/perl
# Tue, 25 Nov 2025 18:21:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 25 Nov 2025 18:21:19 GMT
WORKDIR /usr/src/app
# Tue, 25 Nov 2025 18:21:19 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:099882631f3c0c5583696bbb377a83dca2faf014da28b08add3482e4678d2872`  
		Last Modified: Tue, 18 Nov 2025 01:11:53 GMT  
		Size: 28.5 MB (28513764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b493c4dd706ff3e1f6a854bdaf5feb385f698fbab243eb909adbcc5fca7e751`  
		Last Modified: Tue, 18 Nov 2025 23:16:00 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9617e115b0a0646c5263f1e004d11f8e2eee6c64b0eae1163bccff34d5a55dd5`  
		Last Modified: Tue, 25 Nov 2025 18:22:13 GMT  
		Size: 28.6 MB (28580893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d6a716060ab260097a8c04abe0510936e6e11723777f9539e9deb4a07fc282`  
		Last Modified: Tue, 25 Nov 2025 18:22:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:9ddfefb668b6b67c438294adc94cd159f6b84669dd5d3c6e83b391d0b9277074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f4aea5c384efbd183462da6034822e9f8b279a041bb11a86cb4f1d59a4f346`

```dockerfile
```

-	Layers:
	-	`sha256:a56159b4034bffe2be07b87cfc8a333b81803713ce6038a20006112d05b6c548`  
		Last Modified: Tue, 25 Nov 2025 20:39:52 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:7aad19c19f1eb290e8c6a7f776045a9abd9ec08f1c24ee4615d064ce9ac03ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63315649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2cb0b78c26d09995db3cd02bb002c61e50644063738aafaec5e6a08462c49f`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 14:26:45 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 14:59:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 14:59:11 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 14:59:11 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d408681ffbf8714eb9d0b7cb46b1ab1421ad6bcb6c6d4bed823f2b87ff6b9e`  
		Last Modified: Tue, 09 Dec 2025 14:35:07 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a475eaacc8ada4ebc8b2135468d32181c303dcba64134c8b9c98a11e7525234c`  
		Last Modified: Tue, 09 Dec 2025 14:59:46 GMT  
		Size: 31.2 MB (31246538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae384fbbdbb4a82b6a705190211126fe7f53eac35c06c836666a2b5b769fd9e`  
		Last Modified: Tue, 09 Dec 2025 14:59:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:ecf3318bf557717042894c443626fee156fcad962a82dbe7e6f8fca3bf4e1e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3943695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae8ee12ee2b2ad81f591e90ce63d5e6a508a5b72ccd1def7ae7ecdc214433bc`

```dockerfile
```

-	Layers:
	-	`sha256:f3928c751fddc71bada9e45d177dc1137f1646ef3c8380211a1f10b3a1c58a3c`  
		Last Modified: Tue, 09 Dec 2025 17:41:00 GMT  
		Size: 3.9 MB (3925312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85777d25ef45079b231148065a2d466ac4ac3a077481b99ea68e2927c64c9a49`  
		Last Modified: Tue, 09 Dec 2025 17:41:01 GMT  
		Size: 18.4 KB (18383 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:29b7d4915cba16b88956a6457c96aeedb0a72c6e1887ab0c1733d5c78dea0658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55848868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12eddfbee23559361881512799f36e3508307058d297d3c743320284374ffe9`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:20:06 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 02:55:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 02:55:39 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 02:55:39 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab0af3556c89b1de205bf1fb947bbd5199d2fcca38b366b34b8af6975fcf29a`  
		Last Modified: Tue, 09 Dec 2025 00:26:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09073b020248d4567c46e6bd04983688d82487fae9f67240dd2ef75519d34e42`  
		Last Modified: Tue, 09 Dec 2025 02:56:05 GMT  
		Size: 29.0 MB (28964173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af18508926a22d6a5aa77b20ca009134284cc82d1cab3552361a84afe425f028`  
		Last Modified: Tue, 09 Dec 2025 02:56:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:164639f7f5c08a522d1e7c7536a16b518a46c019407c4d7897338bdcadd6d2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3943001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef89d463615ba35e574b49c64da5b188f8be27698883f2cf4e6f056a3c2673b`

```dockerfile
```

-	Layers:
	-	`sha256:8560bc0511e2bf47d882286170b156e8423b90eb6cfabdd2398f3b1a31cc9fbd`  
		Last Modified: Tue, 09 Dec 2025 05:47:46 GMT  
		Size: 3.9 MB (3924657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:993f6b51e3cecbd1d25bfdc87c31b8c8b8cdba68e8e2a036519899f9c9690623`  
		Last Modified: Tue, 09 Dec 2025 05:47:47 GMT  
		Size: 18.3 KB (18344 bytes)  
		MIME: application/vnd.in-toto+json
