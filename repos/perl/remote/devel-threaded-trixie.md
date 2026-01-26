## `perl:devel-threaded-trixie`

```console
$ docker pull perl@sha256:01fd23030fe69dbd3ab00da0476bb5e1e2f4d9da9cfb3cb19e8551ef742af77c
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

### `perl:devel-threaded-trixie` - linux; amd64

```console
$ docker pull perl@sha256:cb5cfe3077bd0bdc4b48a093e0dd6bc9ce2a8beadf4f89ba001e74d351e4bf2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.9 MB (394850256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a5287eaec5a74fccaf1e2ce2fa8419da87f6c14bc8fda0eb6b290cdbcef3da`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:50:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 21:54:58 GMT
WORKDIR /usr/src/perl
# Mon, 26 Jan 2026 21:59:32 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 26 Jan 2026 21:59:32 GMT
WORKDIR /usr/src/app
# Mon, 26 Jan 2026 21:59:32 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:29 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d823e3848f3d74363d9b5b44f39f2d2f81a99a37d8c7fb54831a489a32e999`  
		Last Modified: Tue, 13 Jan 2026 04:50:59 GMT  
		Size: 236.0 MB (236001828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfc8af70604fad8c5880203c8832d5ca79d7838376a89a89852803660664b52`  
		Last Modified: Mon, 26 Jan 2026 21:59:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14ed3045cd408130b720a27def98a780b64e7e3760059680268b3b47e5b6dd1`  
		Last Modified: Mon, 26 Jan 2026 21:59:56 GMT  
		Size: 16.2 MB (16162353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed08444e7e7d6fb1e885318b28ac29de7715690a22ee562e231c98754a837ab9`  
		Last Modified: Mon, 26 Jan 2026 21:59:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:4197f1258f3f2a9b08dabed45f38ac1d26e4115e45894fa2cf6f20525038c64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17229276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5842453cdc3a1bb124a129e7063e27b7c16e0b631af6fe3a4190b9ed51788a38`

```dockerfile
```

-	Layers:
	-	`sha256:2952a7e92f1cbe29973bea205efa28f718b0251330674efeae89c8c760aa097b`  
		Last Modified: Mon, 26 Jan 2026 21:59:56 GMT  
		Size: 17.2 MB (17210664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66ffbacc14ea9326a859755914b51b790b211fabd4ef5716956dfe5c1fdb7d79`  
		Last Modified: Mon, 26 Jan 2026 21:59:55 GMT  
		Size: 18.6 KB (18612 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-trixie` - linux; arm variant v5

```console
$ docker pull perl@sha256:86a8d98685576dad6470d6f7b83bd97e436e9ed091ac7f1f84e660b8cdfc1a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.3 MB (358309151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f9169fb12f73cc2a4cdbbe7f293d3474679a729a0f3292adfee555448ca0d8`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:29:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:08:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:13:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 21:59:50 GMT
WORKDIR /usr/src/perl
# Mon, 26 Jan 2026 22:05:31 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 26 Jan 2026 22:05:31 GMT
WORKDIR /usr/src/app
# Mon, 26 Jan 2026 22:05:31 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:16d4329ceaa8dc305221873389c356e4c5bf3cdb5b245a79ff75a1b1806f3778`  
		Last Modified: Tue, 13 Jan 2026 00:42:07 GMT  
		Size: 47.4 MB (47448362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ac90147d1f1c4bc0ab2c1c245fb4105c9ad56d7e5e75726e8ec474c79f05f`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 24.4 MB (24353866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0fe9087175027e9a76a41e2c394603c9345a19f6296b58e7044e930aafb08`  
		Last Modified: Tue, 13 Jan 2026 04:08:29 GMT  
		Size: 65.3 MB (65318536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a03a66aae139adaadd8a808ca96b9e5d75cefae43a5eca814727bc64c805f6`  
		Last Modified: Tue, 13 Jan 2026 05:14:31 GMT  
		Size: 205.7 MB (205729923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7d3e0eff5e71794daa69e164bbfaa1e88ed4bccd39a18b2518b8a3a4bed03b`  
		Last Modified: Mon, 26 Jan 2026 22:05:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5af4503750dc6934e9845a982760f5d2e66c096e79042856182e0072de8326`  
		Last Modified: Mon, 26 Jan 2026 22:05:54 GMT  
		Size: 15.5 MB (15458196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554e7e76c399bd1f0f1da7a89af0b55bece1b8384034bf5e9aa4e0716e96af40`  
		Last Modified: Mon, 26 Jan 2026 22:05:53 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:878e68e1abde53e93ed97b6921472dfb2d411e30663532bb60b6d06ba0a3da27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16991596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9597ef4d3d580bb15324ee53683d364d19e569b56060ca356c2a1f5e40de3f36`

```dockerfile
```

-	Layers:
	-	`sha256:e5f5be5557babadd8990f2ef6ea52b28a3cb7ae16517271f393c1bd456d57979`  
		Last Modified: Mon, 26 Jan 2026 22:05:54 GMT  
		Size: 17.0 MB (16972886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23a631a28a7b4dec23380940e15e830a909f40056313434063b409e295ed23c`  
		Last Modified: Mon, 26 Jan 2026 22:05:53 GMT  
		Size: 18.7 KB (18710 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-trixie` - linux; arm variant v7

```console
$ docker pull perl@sha256:0ce42efe88522832f9a7b03b15ebf41a72f4d7795c89d59a0b51681f233907ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340630046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e62a61a37bc27a89d010b9dcc9f6432c0dc48ab49d346b2ea33f0cc7b9167a2`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:25:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:19:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 22:00:26 GMT
WORKDIR /usr/src/perl
# Mon, 26 Jan 2026 22:05:56 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 26 Jan 2026 22:05:56 GMT
WORKDIR /usr/src/app
# Mon, 26 Jan 2026 22:05:56 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:0f4296a8ece8abd5a409e5fbdb0cf93258815e4fec9dc768c39a63faf3c16052`  
		Last Modified: Tue, 13 Jan 2026 00:42:25 GMT  
		Size: 45.7 MB (45717820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8e700e2f18987ab9f97abcd0497d5dfc1706a8c057e685438ce3b71d8067c0`  
		Last Modified: Tue, 13 Jan 2026 02:59:04 GMT  
		Size: 23.6 MB (23626665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf6f5dfbcc297b2e354e856be84c591ec9f96e89fd8401a4d485596c43b8ed8`  
		Last Modified: Tue, 13 Jan 2026 04:26:01 GMT  
		Size: 62.7 MB (62713384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc2c3dfa2d6df259da14558beefb7cee69246c0da0fdc440a04d5af7c8fb7dd`  
		Last Modified: Tue, 13 Jan 2026 05:20:01 GMT  
		Size: 193.3 MB (193306851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5134eede58dc0fcceb83c8590a0b8388af029580144941b784a870681d8063f5`  
		Last Modified: Mon, 26 Jan 2026 22:06:18 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3badecb8dc9c0e9d066360c0ba827fc4e91df45c4dfaac23405a296b0fb7c9f`  
		Last Modified: Mon, 26 Jan 2026 22:06:19 GMT  
		Size: 15.3 MB (15265057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fb7548574ddfad257fa0212cebfec49a970c82cc60d13be7d492d8eb6dd3f3`  
		Last Modified: Mon, 26 Jan 2026 22:06:18 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:92cbe997c1e0a68a00c3af41bd4476e2df1772615f425ee208a48cf85cfa7d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16997386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7699ee66b5942a40793d914cc4b40cec54ed35ba3d82cbb9a2cc8c2fd6fb3b6`

```dockerfile
```

-	Layers:
	-	`sha256:ac1250406df4f6e893b31af8149ada10ced586f30d418d6b5da1cb7a159ac459`  
		Last Modified: Mon, 26 Jan 2026 22:06:19 GMT  
		Size: 17.0 MB (16978676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16cd73751223d013b318d233413f3a5b459c5365f6e83748706c111d4ba687f2`  
		Last Modified: Mon, 26 Jan 2026 22:06:18 GMT  
		Size: 18.7 KB (18710 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-trixie` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:7bb061869501ef087a3f4e67e06267870c4328270782b3d9a048f39ba354fced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384511092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750b47a670bf343bb1ac45b21437dfe3e166311babecbd0eebeffbb51c23eb48`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:52:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 21:55:33 GMT
WORKDIR /usr/src/perl
# Mon, 26 Jan 2026 22:00:14 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 26 Jan 2026 22:00:14 GMT
WORKDIR /usr/src/app
# Mon, 26 Jan 2026 22:00:14 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:39 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fffeb567ed4215b503f814aeaab9fa5a2e701d3efa35d4c285b3cf111e9cb4a`  
		Last Modified: Tue, 13 Jan 2026 04:53:30 GMT  
		Size: 226.1 MB (226143857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32e490128ab358be9a3b4822a742be4c5cff606c07b354e35d3da925f700a02`  
		Last Modified: Mon, 26 Jan 2026 22:00:37 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69956f0352e0891d320915f00d05a52827e8ee2fc8a2a6f7de68e93ee65212b`  
		Last Modified: Mon, 26 Jan 2026 22:00:38 GMT  
		Size: 16.1 MB (16104736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5969a4a45bd070f6b54c0bb87f4658ad5953a184895a6fa37c96049c004f9d59`  
		Last Modified: Mon, 26 Jan 2026 22:00:38 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:020bd33c00406b276759ffa293623764c810d6dc5e62b6b1aee2d784483d5b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17313734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee9e4c5c4a276223ef19488e3b16d59074fecf3a8905c2151cec67f80e2d569`

```dockerfile
```

-	Layers:
	-	`sha256:dfdcc18873afdb0ae16accb3425263171488306fd78616162e7e9c4fbfeb582c`  
		Last Modified: Mon, 26 Jan 2026 22:00:38 GMT  
		Size: 17.3 MB (17294994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84be1793a1d636bbd5c410838c9c06579fb7ce4529daa70c13247855c188ef5e`  
		Last Modified: Mon, 26 Jan 2026 22:00:37 GMT  
		Size: 18.7 KB (18740 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-trixie` - linux; ppc64le

```console
$ docker pull perl@sha256:3ae93c741af59e195b0f4d1de74d814f0426315e38398ec97343296a53e33842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.5 MB (400473474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd9944aa21ea59c9d103b6fb53ddb418fdbb03fa2d222ab33e1fb3ee2ff8e26`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 09:15:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 15:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 16:13:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 21:52:41 GMT
WORKDIR /usr/src/perl
# Mon, 26 Jan 2026 22:16:31 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 26 Jan 2026 22:16:31 GMT
WORKDIR /usr/src/app
# Mon, 26 Jan 2026 22:16:31 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21554c0ffe7aa9121703873815aca94dbbdf6352a46266dc923fc9e36d0d58a`  
		Last Modified: Tue, 13 Jan 2026 09:18:01 GMT  
		Size: 27.0 MB (26998052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb58d20828d54df35a08218c574236606c9e3ab14d0f2ddf036e12abcf8c85d6`  
		Last Modified: Tue, 13 Jan 2026 15:19:44 GMT  
		Size: 73.0 MB (73037608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e13e772271d599b914654801e760b6e090a2d2a51765f2bd85981f821d1eb0`  
		Last Modified: Tue, 13 Jan 2026 16:14:40 GMT  
		Size: 231.1 MB (231145655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb39dd0a7514b400958f46966dea9fc7970a90853ce12d3a90e0e8f7c63dec5a`  
		Last Modified: Mon, 26 Jan 2026 22:00:50 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c19db4427891cbd0cb7b88b9f133826d66b88b0bb5d1e9bda49f3594e948aff`  
		Last Modified: Mon, 26 Jan 2026 22:17:19 GMT  
		Size: 16.2 MB (16184931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295bda189682651a7337f58f812943f0396f6c24c6384f7a44c1395a50ec469c`  
		Last Modified: Mon, 26 Jan 2026 22:17:18 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:ee27184982b5a7c0ea4403d938a7f589bbded8aae9e782aae67a4d77aead8c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17214903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e72fe784e835c91b78951d2320eabe2c709952ca71e960107e2c31685901012`

```dockerfile
```

-	Layers:
	-	`sha256:82d30fa7724745d20fece193440fe73a0dec8b9dee045c3d72ea3cf2e638329a`  
		Last Modified: Mon, 26 Jan 2026 22:17:19 GMT  
		Size: 17.2 MB (17196233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9085ae04a014b78b5373873739a0fb38825f0c24ad12c3b0fe6292ea76d7e01b`  
		Last Modified: Mon, 26 Jan 2026 22:17:18 GMT  
		Size: 18.7 KB (18670 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-trixie` - linux; riscv64

```console
$ docker pull perl@sha256:f812ec049df8369b812419d3d234d0822c1c8c9604a607c454fd1f9dc266993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.9 MB (477913289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c244af4c31f152cd8e8d230ab544e9fd456a0247e0cb20e725d79dd41fd936`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:47:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 18 Jan 2026 22:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 Jan 2026 17:44:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 20 Jan 2026 17:04:10 GMT
WORKDIR /usr/src/perl
# Thu, 22 Jan 2026 15:30:55 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 22 Jan 2026 15:30:55 GMT
WORKDIR /usr/src/app
# Thu, 22 Jan 2026 15:30:55 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7f36a5fa281a3384abd9a90a26442f28edb507f1b9c537a07e1f5aaeb769a1`  
		Last Modified: Fri, 16 Jan 2026 06:49:07 GMT  
		Size: 25.0 MB (24952736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f745939b2d13a20bc5767dafb02ca8b86a288cc70e3062fa70de76ce5b598`  
		Last Modified: Sun, 18 Jan 2026 23:01:52 GMT  
		Size: 66.7 MB (66660714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e465a2a93efb7d9834b7bee31c5f96d3312ff2c13217037bf1b8e5ad263e25b`  
		Last Modified: Mon, 19 Jan 2026 18:00:41 GMT  
		Size: 322.9 MB (322922306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b87c769cb33a03e340cbcf61125aa90f130c5b0d6a72ea0f5f223e8bf5ead37`  
		Last Modified: Tue, 20 Jan 2026 18:17:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78ec4fc7546301a02a90f590106e170540a474a4bb10659d8fe9d4dc58beac9`  
		Last Modified: Thu, 22 Jan 2026 15:38:49 GMT  
		Size: 15.6 MB (15606421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5031f0f49f98161e2bfe87a2d5f806a77f4172bb00075322abd5def9602eff00`  
		Last Modified: Thu, 22 Jan 2026 15:38:45 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:b02a03bb2032fc662202a57c52e8b1dd68e1aeb0de61f309907bfcf36127a5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17285489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bca341664a5500a8c3d64878a6f46637554fb255b8882cc873b9c0ad3155577`

```dockerfile
```

-	Layers:
	-	`sha256:771d1ffbfecf0e29683b90de16dc447ecaffb58836f3fcad09fcb27c880b93a1`  
		Last Modified: Thu, 22 Jan 2026 15:38:50 GMT  
		Size: 17.3 MB (17266822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd1b31ba6a848d6ce459eb50f9e0c9e1838e979140354ad18e55751157ea0e88`  
		Last Modified: Thu, 22 Jan 2026 15:38:45 GMT  
		Size: 18.7 KB (18667 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-trixie` - linux; s390x

```console
$ docker pull perl@sha256:571d1eb16c85800554959d58147bdeb5e58209edec3d8c722d03636301c46059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.1 MB (368052069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a646e8524a2a490ec68e1138b2d1a7bec2df33ef4e830ada8b153d24c391945`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:18:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 21:52:23 GMT
WORKDIR /usr/src/perl
# Mon, 26 Jan 2026 22:04:57 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 26 Jan 2026 22:04:57 GMT
WORKDIR /usr/src/app
# Mon, 26 Jan 2026 22:04:57 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a9411869af8d59bfb1073c3573138af1f96d808896b3f2fd14cf62fca6dba`  
		Last Modified: Tue, 13 Jan 2026 02:11:26 GMT  
		Size: 26.8 MB (26792892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff54b33211ee85001fc045dcc86b026876894b17d1d6f873a415014f68cb0c9f`  
		Last Modified: Tue, 13 Jan 2026 03:16:06 GMT  
		Size: 68.6 MB (68632678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fc8348b5ddb8c2acabb8e9ca2d1b4b97457b5a1f89dd3ca04047f15644b88c`  
		Last Modified: Tue, 13 Jan 2026 04:19:56 GMT  
		Size: 206.5 MB (206530469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aa357490fdb8246d5727fc8282b74621cc942df92af07be31017e4691d2ba5`  
		Last Modified: Mon, 26 Jan 2026 21:58:33 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35eb7899dc82ada2513a5160da5d836da85a1f89da5febb1144e185ae99c6f34`  
		Last Modified: Mon, 26 Jan 2026 22:05:27 GMT  
		Size: 16.7 MB (16747057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff27928db2b464ccfd56637375ecbb89982a3f91107b8b353b0588e08b6dffd`  
		Last Modified: Mon, 26 Jan 2026 22:05:26 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:622e7fc4457d9a9362568e19fd43b032f38e8b9c22d52753b742c08261135b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17006511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badde016a75e0098fb8ead6067a8dbe57419edf8fc94d93674b5d0ed0484040c`

```dockerfile
```

-	Layers:
	-	`sha256:a0ee6bf2b0c0ea2cdb8a04d89b319b5f9e70d8f0513088b3acb98a9eab089980`  
		Last Modified: Mon, 26 Jan 2026 22:05:27 GMT  
		Size: 17.0 MB (16987897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef8ea240428c87220dd1a9319d5995ffb10cc1144d3caa27d3dc42c1e741e24`  
		Last Modified: Mon, 26 Jan 2026 22:05:26 GMT  
		Size: 18.6 KB (18614 bytes)  
		MIME: application/vnd.in-toto+json
