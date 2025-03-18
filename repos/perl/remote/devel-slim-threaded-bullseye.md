## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:9718a175a9708ff54534c78f8b4acdf71fbcecd5c3760d6e2be41d6170eec319
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `perl:devel-slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:4ae009f36e8bcd4b11d9cdb9a2b741d2146cec11e72faf3852a3dd6df0d40b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56274596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba85253c21dca3489d1bee187d60484fe46df8572868656c3dcb5fafae3c5d9e`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458f669ee5aa8efa20a9e0d30ac2cac6faa23be5f242bcaee5b27911d7a09227`  
		Last Modified: Mon, 17 Mar 2025 23:28:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6571955ce5fafd842dc6d849bedfb5b605743ec4f16baf238dae26c5fa31d9b`  
		Last Modified: Mon, 17 Mar 2025 23:28:14 GMT  
		Size: 26.0 MB (26020493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a5dbe2738e6067fa638c79cc661e2d51074c98398024f71cf1f389be08ba3c`  
		Last Modified: Mon, 17 Mar 2025 23:28:13 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:82c307c17d68d4ded4203d88b78c6585fc72041ad2a3a125b62e648ed1e2a9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a2207ca433365b00143e3a4333a94cd7d8dcc4fcb1a587a1fc9d74e61d683b`

```dockerfile
```

-	Layers:
	-	`sha256:88554d92c8c37b748c07af9c2e097c8cfce9b3412b29b75558d9ea3335596c40`  
		Last Modified: Mon, 17 Mar 2025 23:28:14 GMT  
		Size: 4.0 MB (3998508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77c900dca498b2fb0d83982bc7d6d5dc2e2420ba28240c8429a152ffc1d4cbb`  
		Last Modified: Mon, 17 Mar 2025 23:28:13 GMT  
		Size: 18.4 KB (18361 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:1fae18d09ea7bad5650b0d3ca0ca464352357060efd0aff93dbcccf61bb1fe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48780750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a601e66113cb13e031256292dec74a9366bb182386183b33988fbcec83951b`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:b0ca501b624d9dae81049df15e1024733ee21141b25f8ca123d98e0d13df5d12`  
		Last Modified: Tue, 25 Feb 2025 01:31:18 GMT  
		Size: 25.5 MB (25535432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02eecd66af283ad08b114032f0c6503139d48a1f443ae51af619b70b1d8a9d1`  
		Last Modified: Tue, 25 Feb 2025 07:59:16 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ee4ce85075cdd80dc492ac5717565d2310584bb8aee46295cea91b4b70b3d1`  
		Last Modified: Tue, 25 Feb 2025 09:27:45 GMT  
		Size: 23.2 MB (23245051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f684dd4720ff163be70eeeedb14cc4abb5c96a8be1d4f71f4f02f8f4dfba40`  
		Last Modified: Tue, 25 Feb 2025 09:27:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:60bf213614c54cab9efea15a68d9e437cfb98be7ae876df7d81e4ae018d148cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d827b6f50b6f6946184134b3bb78205fabe7880c6e4d3c292a1021eedff0ede6`

```dockerfile
```

-	Layers:
	-	`sha256:f6e2f13bfb9bac8fbb66c8c3568a87f49878bb533948f9f3901ff23d93ae7a59`  
		Last Modified: Tue, 25 Feb 2025 09:27:44 GMT  
		Size: 4.0 MB (3972497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f95cc9f6b91a2cdb5c2396d931ddeaa27e72da208f6fd35db6127d6c0b8a52`  
		Last Modified: Tue, 25 Feb 2025 09:27:44 GMT  
		Size: 18.4 KB (18429 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:e8a6f6043d8ee7ae5dc824ebfd8414a6d2e5f64ffe333c0f7b710ec836b2cf04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53875678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619914d96db39041710154864bc2e3fac667006620e26f0482bb725d4a312d3e`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58491e319b39f2496349c4d9227508378814a9bc94d9337499f54401ffb59dc8`  
		Last Modified: Tue, 25 Feb 2025 06:37:40 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad555bed39a7ab87c467b3253181f26f193b9f9bb9300cacceaed0675e86f39f`  
		Last Modified: Tue, 25 Feb 2025 07:50:41 GMT  
		Size: 25.1 MB (25129422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c03d934bed982059c8984650ab710140fddfcd042191fa30b8a725f0f4e041`  
		Last Modified: Tue, 25 Feb 2025 07:50:40 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a6355f76b4d49c0056a4219e43f736041ac925d52cecc9d6cbebc24540dc7d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d814c66dc533526ab776a9c52bb76c533c4ec88b9248feeef952ddf38ca27a05`

```dockerfile
```

-	Layers:
	-	`sha256:fc565ab84b5b182a13bcee81a43d4f1dfbc9bdf86e01509f204a4a7c9b2bc027`  
		Last Modified: Tue, 25 Feb 2025 07:50:40 GMT  
		Size: 4.0 MB (3972903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6834c61398f00c8e6ab20d399590627987608bec62ed8a8bea61575d4c8bed1b`  
		Last Modified: Tue, 25 Feb 2025 07:50:40 GMT  
		Size: 18.5 KB (18452 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:0c049630d363dfae58d650b91eeb8bb7a12029f9c69ad9b3c0c1ae753d871e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58750734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41cd85b27ea493a01ba118e6581cde6e139d75747a9ead7952cf6b3bd958b8b`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e2070993e906846859ca2db1e076e7527d7657928a88e33ecd9b5afb609bd0`  
		Last Modified: Mon, 17 Mar 2025 23:36:32 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a08494fa1078b542f99492aecdfe370bf5422fbe9011f571840a3ef1ba611f`  
		Last Modified: Mon, 17 Mar 2025 23:36:33 GMT  
		Size: 27.6 MB (27570131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74a28a0f34e65e804b68ef62832a29656260d67d5286dfdfd3bbf19cdd0fda5`  
		Last Modified: Mon, 17 Mar 2025 23:36:32 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:12d0d12ccfd9c8ed3e452d032ed48990bf6b55334217a94870555be15a9af382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4021061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4609c9ebcd4f359d969261d66038209687ce8650b97240b3617848087a824051`

```dockerfile
```

-	Layers:
	-	`sha256:c81594072dc14551d98825e07568c4d1deaf2810c446a8c1873437433b220777`  
		Last Modified: Mon, 17 Mar 2025 23:36:32 GMT  
		Size: 4.0 MB (4002727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:347c0a52a6127603d6e1403648e7fc9fd6e53d5d90c1a061cd6497e1cbe17f86`  
		Last Modified: Mon, 17 Mar 2025 23:36:32 GMT  
		Size: 18.3 KB (18334 bytes)  
		MIME: application/vnd.in-toto+json
