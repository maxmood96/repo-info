## `perl:devel-slim-threaded-bookworm`

```console
$ docker pull perl@sha256:4eea4523a3c53ecd202365cbd8ac6e803590de7fc7b100beaf344e14a07bcc6a
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
$ docker pull perl@sha256:9c4419c972179a632edf373f8b05c543914c8bdea7b5bd76b3625251200535cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58483997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8ce03857598cb9e6ad75461ef718fc0259d26caab7a853ce7278dc2bdebd10`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 13 Jun 2025 11:40:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0889e352609f7c6de33ec0165449046fcccb0264a6b83d53eabf88144daa3aaf`  
		Last Modified: Tue, 01 Jul 2025 03:39:58 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6364d46680084a9a22dacf9d1b3199965409c7b65662500348efcd841ae9b0`  
		Last Modified: Tue, 01 Jul 2025 02:41:53 GMT  
		Size: 30.3 MB (30253588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed193b493b5f363b2098b0f3c7ed71d504eb6bc803ed0fa2b5009368287dee9`  
		Last Modified: Tue, 01 Jul 2025 02:41:53 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:66408727426eecf0807aee729880060ba736d9235ed8915a74f6dce82b1a5763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3957572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834b5e42183428fd61460d38ac6016e0b71875994b36b24efea1e5fdba637f45`

```dockerfile
```

-	Layers:
	-	`sha256:7277c3c88a0d14b8f71399f9f1511ef7379db180d7e4049a1c12780a42d7b93b`  
		Last Modified: Tue, 01 Jul 2025 04:41:25 GMT  
		Size: 3.9 MB (3938235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5bb962b12705dbd7377c37a78b8e559c24d1480b90c5eab567834b9e68e16c4`  
		Last Modified: Tue, 01 Jul 2025 04:41:26 GMT  
		Size: 19.3 KB (19337 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:9838e11741d48f5412a1628fec7590690023e8d79d4ca29f373e8bb7cca2ebf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53054096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a4478157c3ac934f0eead204ebdd571d7b71f1c47b590d59a08fabf2c91fd4`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a696d9e513599ffab953ad4b1c1cf5488587bf83c833b52b7ecaa07f842b49`  
		Last Modified: Fri, 13 Jun 2025 17:16:19 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7968bf84aaf74da89c5e24d7ef94a69609730113219deaef51f5f082fb8535ba`  
		Last Modified: Fri, 13 Jun 2025 18:53:36 GMT  
		Size: 27.3 MB (27291433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d33e1301e089b13001814e7ca23a878e5674bad005267e26750c1a4616fea52`  
		Last Modified: Fri, 13 Jun 2025 18:53:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2d69b1b515763e3862ee9a57d767987347ae59fd5e926f82fc64bb06536403ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c408fd5c1c79065228be4633069cb9f98624d86f45e8f32e80e7f4546b9f8c1`

```dockerfile
```

-	Layers:
	-	`sha256:8db2c423885f70d974ee87d081ded5b9053c171534e04ca0d18b81a67fb11187`  
		Last Modified: Fri, 13 Jun 2025 19:46:58 GMT  
		Size: 3.9 MB (3909110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eba1f523294629fc8a50fd60495cee175ada99fb4635b64a85d6b0b191b704f`  
		Last Modified: Fri, 13 Jun 2025 19:46:58 GMT  
		Size: 19.4 KB (19430 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:d7da282948531718200bec9b994fb01d9456c50b8278fdb3eb8596f325d4a16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50328588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafd1340b0daf63102f6e79990fbc56ccfc9bf92daecff3914e903a31f758052`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e92a2bf9e485711464a8f443d67f152eeb86aabc133b7b7223749f10a485c`  
		Last Modified: Fri, 13 Jun 2025 17:52:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cb4bf43584cd4c760bf989c314c62091a3a9ae1c0a91bdb10572c2f012c7c4`  
		Last Modified: Fri, 13 Jun 2025 23:16:34 GMT  
		Size: 26.4 MB (26389576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfbafe1e81a01c072364975edaa964e57521f3ac3af18600776ccc87e8b52a6`  
		Last Modified: Fri, 13 Jun 2025 21:12:26 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:311f3fec7f00299b9fd86a075057bef7538bd5225ce60eb9b5aed2565a12ad0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6902f635479b929c3fbdbf0979de6ce2ae7632c8876c875dc19791b0df8f2f89`

```dockerfile
```

-	Layers:
	-	`sha256:6e27893436f59ccd0e62279ac4f388c83568d158cb7d23a806b11fa7361fc64e`  
		Last Modified: Fri, 13 Jun 2025 22:41:17 GMT  
		Size: 3.9 MB (3908335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85ea63c7bcdb70a2be3fef1150152267278f79d362cbe7e92a2f2c5dc6fbe3b8`  
		Last Modified: Fri, 13 Jun 2025 22:41:18 GMT  
		Size: 19.4 KB (19430 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:2cecb8d30b72a7eb80e4e06d57dc2cee89f0b8bf1be84371c28427ed84def990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57135977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a06b14153f4817b2d203a8ac0c982f736bccfd34d0c063b21249e263d4ac8d`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd88fd7f20e8120596c4dc3f8f0fc3284f04a4e960c97a1ec49ae760d81fd1c`  
		Last Modified: Fri, 13 Jun 2025 17:20:06 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54531f5c08d5e82a5bc3ed0daace02e529322a75987ced99a74866ab92974277`  
		Last Modified: Fri, 13 Jun 2025 19:42:15 GMT  
		Size: 29.1 MB (29058033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4275dc513f2198258c932ef5a66199bc333270d065a9eab10668dc6c5d1c539`  
		Last Modified: Fri, 13 Jun 2025 19:42:13 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:3555d5e8fd355a50f5a6b03e8fa16de83438abeadd077e8e517307f1e0ff1e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681df43e76dc45ae9ff257471602bbb46514f026c8a77a9eb0da97848f465abd`

```dockerfile
```

-	Layers:
	-	`sha256:327290e0537672f72c8cb0c9a7360f6aaa3bb2b3b998c16040c813068a52f9e8`  
		Last Modified: Fri, 13 Jun 2025 22:41:22 GMT  
		Size: 3.9 MB (3909508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f81f5eedf8aee68f08fd5252c57c97bf5fa284b2c47401113f8729829540b1`  
		Last Modified: Fri, 13 Jun 2025 22:41:23 GMT  
		Size: 19.5 KB (19466 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:e35a4ca61dc64c43be06528c60ed37bc243c0f1f44b8ea0bfb82db0565d4c0a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58638949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb45e96823ade67df5bc7f561ab248fe207e23087258cccc7a3e430a224355b1`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 13 Jun 2025 11:40:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbd4e215878c1b07439dacaeea19c60b1eaf773ac9057037f81f9e8a3be3c6a`  
		Last Modified: Tue, 01 Jul 2025 02:35:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cfff5303247dcf29637a1b4ba6da881e48cf9dca9ef4df0e7281cba33979e2`  
		Last Modified: Tue, 01 Jul 2025 02:35:46 GMT  
		Size: 29.4 MB (29426250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aee32c8991f8d1f413bac5c7b6ebff1cd45ceba39d1e22cb09bf98f64fe093`  
		Last Modified: Tue, 01 Jul 2025 02:35:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:83b5b66e422671cbc92308b3e4b3a893ae4e47ee9f43268c74002d7af7333275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7921f3ef72b860ef8557ed14e5b2ce2f561fa2af2ad3a2678efb895fc83d9e`

```dockerfile
```

-	Layers:
	-	`sha256:285477076a00eb5f97dfd2aea5fcf492a7f1980bb7cd59736690ee588d1498f7`  
		Last Modified: Tue, 01 Jul 2025 04:41:47 GMT  
		Size: 3.9 MB (3932162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c447ce3b069e5a50c3613cd697de71f1fbb4de39712fb9fe54e39f65c39d36a8`  
		Last Modified: Tue, 01 Jul 2025 04:41:48 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:e75110ecd632e567c5961b158f920e4cab731b61e8f8ebdeef6abee2fd21d766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56937374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8319809ffd7cc858da3ebd2c31b84d812f72ec00185c68e8d4167d5860119394`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0cffea047f22d142382dff57a47a3145f4807640ec9a95a73d31c4f3366a85`  
		Last Modified: Fri, 13 Jun 2025 19:03:24 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a430b7c5f7cd8195dad360a8b1b5c8dba49f1b94164e41a3496c32c08eaadf`  
		Last Modified: Sat, 14 Jun 2025 01:19:12 GMT  
		Size: 28.4 MB (28420388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6011b12ec6ed19c2db2ffdc5f22ec56fb7a7f788f3eecb6da848cef988046d23`  
		Last Modified: Sat, 14 Jun 2025 01:41:30 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:193d5c0e586e089666e9186fd0ad8af883f1b994493fcbc0bc400f57e867c941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b87bb3d0e447cdd0b2ca0e003b0197b817660c76028aaf51aeb2270955f531`

```dockerfile
```

-	Layers:
	-	`sha256:2157cb0da92f935424d3b4c0f9b3ba1c7c62abb57f91700f0362fb625fe887bb`  
		Last Modified: Sat, 14 Jun 2025 04:39:17 GMT  
		Size: 19.2 KB (19206 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:c47e935d071eda885dbe597faf3afece65f0bfbf470b73f0fad022bf92c9f71d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63157037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbedd5d01e61cb2f1ba71e2e8d039a7c358e69b3d9e136969f4682711207310`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 13 Jun 2025 11:40:07 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e7ff39486a88d583ebdeef332f4f2d635e6d6cd422f17bd6ed0390499dde6d`  
		Last Modified: Tue, 01 Jul 2025 05:34:45 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b0eb36e838b4b8f5b21822cb3f7e6bf13402d06e20647bef37c6a7677c7ae5`  
		Last Modified: Tue, 01 Jul 2025 07:10:07 GMT  
		Size: 31.1 MB (31083952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb351989c2d29ee99fcd3b865548ec7b8f48cdcaa4e7df77decb13e7dfde16`  
		Last Modified: Tue, 01 Jul 2025 06:32:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2884ed7177cb57ed79613b12b309486b997a3ce80c2cf91a3833fdb25410d38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3943575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf14c2092337b27b60b8b8dd9dec17b840bb67cf58d4ddc442dd73265366192`

```dockerfile
```

-	Layers:
	-	`sha256:baa2580509eaf71d7300d4aa3331f3cb942f49dc7516e5d1b87e6f29b5cefef5`  
		Last Modified: Tue, 01 Jul 2025 07:43:18 GMT  
		Size: 3.9 MB (3924181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9be7e7c240d2f309c49eb193c6f7c5669121fac41f8dedba598ef8e9154a900`  
		Last Modified: Tue, 01 Jul 2025 07:43:19 GMT  
		Size: 19.4 KB (19394 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:53fa2cb0ce0136427b788c8c6a3c9ad1b1808f98d81d8c3d8919723d51dfca6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55678490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb497f31cc34f2e23d0647752ea7dc559f7edbcad2c68c3b83361e5749ac2f8`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 13 Jun 2025 11:40:07 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7022c2a575cc3a4d77de9e30c953c17d2779132b4e4d4b1f45bfa0cdc946079a`  
		Last Modified: Tue, 01 Jul 2025 06:00:04 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48ddd61892440a300067b27fc79cb72285836b7fe31f9f762cdebe912f4a11d`  
		Last Modified: Tue, 01 Jul 2025 06:44:43 GMT  
		Size: 28.8 MB (28790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb993ead791257c762c5634ec3656c43e53f55c6208de0a4cb9515a398139128`  
		Last Modified: Tue, 01 Jul 2025 06:44:40 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:db8a1713b27fb9006bcde8597d1d9b1fb2f3c136b16396afc19b38d61c0b37a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11cd23d314ebee3521941e8f3d623edaa92e9b832458fc52229dca2c3f84d54`

```dockerfile
```

-	Layers:
	-	`sha256:a66364830c659818096cdc7fb380134d47d9f9bb68cf264bd167f25817743c78`  
		Last Modified: Tue, 01 Jul 2025 07:43:23 GMT  
		Size: 3.9 MB (3923508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69756f80030122f43ee87f8e9532e48262c700ebcfcc8f8cc529ee504a37442f`  
		Last Modified: Tue, 01 Jul 2025 07:43:24 GMT  
		Size: 19.3 KB (19337 bytes)  
		MIME: application/vnd.in-toto+json
