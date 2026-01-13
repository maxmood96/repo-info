## `perl:devel-bullseye`

```console
$ docker pull perl@sha256:26c095003f770b223371974fb21728dedc6e7b5eb9a42e3645871b7451c91634
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

### `perl:devel-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:c2613e7a38e6eb87f108591fd0b295c4625f72dd1d6daef0269a16a083097e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337576855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d821b203585d11fe08740039f8a3679f10670da014daf59076d6c5c6bb438c`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:45:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:23:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:36:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:39:36 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 03:43:51 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 03:43:51 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 03:43:51 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac758735be4df7bbee87d37924a15ccc254964d763d0b8620fdba9dc6d6774b5`  
		Last Modified: Mon, 29 Dec 2025 23:45:40 GMT  
		Size: 15.8 MB (15764112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6512e35a226296c3166e8ce55b556c5fe6daeebccf71cdb13eccee234e17765e`  
		Last Modified: Tue, 30 Dec 2025 01:23:49 GMT  
		Size: 54.8 MB (54755226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a02f77a11e56b83bcea519986069889a0de4be2bffa5e238ee4e26de179464`  
		Last Modified: Tue, 30 Dec 2025 02:37:38 GMT  
		Size: 197.2 MB (197218457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab2a5684bb4a8b674c24e1cdb9ad2a834a12f2c794a07308c722542f63274c3`  
		Last Modified: Tue, 30 Dec 2025 03:44:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc581a125cd681d0ec75e2c58ba79b49d38830239c012fa822532ad396530cc`  
		Last Modified: Tue, 30 Dec 2025 03:44:33 GMT  
		Size: 16.1 MB (16082353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad0e442cc2bd1bf9d80f771313b19e3c9f28bc98878db2ad528811e834f0b03`  
		Last Modified: Tue, 30 Dec 2025 03:44:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ffd72de42dd8b0c9bc63851424cc1af4373c42d17279b8e262c1bcea885be47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15481305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad522c205b0c717b8f6698f588341341c2e8b275e057bf6f7577403be8b56dc`

```dockerfile
```

-	Layers:
	-	`sha256:6982b8e7779de2273afc3b631b62f1c93e284b533d7cd9e0ea9b3bf0578e28a1`  
		Last Modified: Tue, 30 Dec 2025 05:47:28 GMT  
		Size: 15.5 MB (15463706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a981ed1de866ce857e2cef6a4c50a7e132a594b5d5ce814c0ee6417a7e6d57`  
		Last Modified: Tue, 30 Dec 2025 05:47:29 GMT  
		Size: 17.6 KB (17599 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:b72a37e2ea7c10baa5c1d44be6189a15d60367522797ffbb551d863ec731af6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297368780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d7b44a9f8ee1d310090d3a662d37e29493c32d0bafaa0828ebc3e044f4b560`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:06:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:35:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 04:42:41 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 04:47:43 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 04:47:43 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 04:47:43 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:b46683c1e86f7a120aca01c56dfafa77513b188a88759ff45f42ce118f9a337c`  
		Last Modified: Mon, 29 Dec 2025 22:25:41 GMT  
		Size: 49.0 MB (49046401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf8c40ad8b4e8cd6362fd57fbf345b792e3a334f7cfacc579cfaeef4447f6`  
		Last Modified: Tue, 30 Dec 2025 00:34:10 GMT  
		Size: 14.9 MB (14879533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318980c2ab1381876582d11a8701c769d018a68765de938c093203d5fb485b94`  
		Last Modified: Tue, 30 Dec 2025 02:06:57 GMT  
		Size: 50.6 MB (50628825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e20ad9034e29b862e54139afb5ad3088a0eaa66ff57507e0c966b81af518ed`  
		Last Modified: Tue, 30 Dec 2025 02:35:52 GMT  
		Size: 167.6 MB (167646297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979d45dad450b563e201b4b3b450593872b4a2fcaf6ad2bc28079347ea871c1c`  
		Last Modified: Tue, 30 Dec 2025 04:48:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e3e46d1ab5a70e7dff08fdbc23d195e53ce41e707f8d0fcf4d1d886c658e2b`  
		Last Modified: Tue, 30 Dec 2025 04:48:12 GMT  
		Size: 15.2 MB (15167457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f09191d4ceef28853f4f8cb1f473718c64dd99f1d3f08e774b24f0666ba753a`  
		Last Modified: Tue, 30 Dec 2025 04:48:09 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:d413862ebd9c103400ab97fc7045284c252919c163fea7887fbc75712ce986ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15280703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fccc5e70cace65bb853399eea95793875bdb81a3f90fba138ad7c897791ecc`

```dockerfile
```

-	Layers:
	-	`sha256:5adbf80764a4c847d16bdf13d5f075485a28c65155e04249cf4cbad1dffb15b2`  
		Last Modified: Tue, 30 Dec 2025 05:47:45 GMT  
		Size: 15.3 MB (15263032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55972096cee1584fa448b00dfa83f732b737b9a948a3169107bf678d8d396ac8`  
		Last Modified: Tue, 30 Dec 2025 05:47:46 GMT  
		Size: 17.7 KB (17671 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:28b6a84293dd5328f0566329f66aa319471d73b429e1dc9e66de2766f9534144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (328993172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28a34a2212bcb865d2af8b289303db8f925a4ebe392996c037751543d2fcbce`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:45:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:25:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:35:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:24:25 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 03:43:57 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 03:43:57 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 03:43:57 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9549a4595c672d6f3151acb8314dc1cf09736bd0b263013f6ec6856c4c63f19a`  
		Last Modified: Mon, 29 Dec 2025 23:46:10 GMT  
		Size: 15.7 MB (15749381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890aeb16c8cc7bc154fba2dfa61907bbdbcc96a5a7b348a6376fb17c7ab1fe61`  
		Last Modified: Tue, 30 Dec 2025 01:26:00 GMT  
		Size: 54.9 MB (54865435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821c1c97ed0c0b535fe64f1b97780f9f62fe5ee7181cf3046d79708952fd6a6e`  
		Last Modified: Tue, 30 Dec 2025 02:36:37 GMT  
		Size: 190.1 MB (190111646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b032cb11d1c1cd7045de2de6d2dbd7c9bd616f9ae2299ebc90d5e575fe49f506`  
		Last Modified: Tue, 30 Dec 2025 03:29:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b87cf8ecd676f23c990caf7a04cf7713941f27205f4cb33098d805d2eac924`  
		Last Modified: Tue, 30 Dec 2025 03:44:36 GMT  
		Size: 16.0 MB (16008673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42360ad75ad104022e2d2c258ef213e0ddb54052dbc4b8237b80d6613809e5ab`  
		Last Modified: Tue, 30 Dec 2025 03:44:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c8ca4222ea8286ff3a2f8cc4415b40f6ea04abe7613ac7bae2fcc6e040a60950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15483354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd91ab7f875aa5d2e96ad18629a3864ff8dc52fe14041445b3d6953aa322424a`

```dockerfile
```

-	Layers:
	-	`sha256:5430c7229d70ca0d45eeb88ada280cfdf2d70c9a54f97f982b14e61fe2a2e146`  
		Last Modified: Tue, 30 Dec 2025 05:48:04 GMT  
		Size: 15.5 MB (15465663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ed5501b447091ced7f767593ae41f2048724b38e75691c81e402fcfccd4e42`  
		Last Modified: Tue, 30 Dec 2025 05:48:05 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; 386

```console
$ docker pull perl@sha256:af2df8020a3193e2cfa1cb9e9c4b846eebcfd52e2b682849635f80560ea0093d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342697821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f63144bbe8af67349ede2405ab29d14d71bb68dfde0d9c39131cc1f0796769`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:32:07 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 04:36:49 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 04:36:49 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 04:36:49 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:7e115d265636fc6da528c1f4977e22baefb0bae7061ada6dba677a290e83b246`  
		Last Modified: Tue, 13 Jan 2026 00:41:42 GMT  
		Size: 54.7 MB (54699638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed43d5d71f701abde2a62df95258edf0ac9ef3046d49ca25c0f30e57af2985`  
		Last Modified: Tue, 13 Jan 2026 02:02:38 GMT  
		Size: 16.3 MB (16267780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50309e354294a6f81ebf1bf80c4203a79bc9374449993f7fb52ebf0640408262`  
		Last Modified: Tue, 13 Jan 2026 03:03:46 GMT  
		Size: 56.0 MB (56048907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad7ad875273afc9f1824115dad6d50ae84fba747da8a0b124f82d730bcb8bae`  
		Last Modified: Tue, 13 Jan 2026 04:23:38 GMT  
		Size: 200.1 MB (200113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcc096fc287a10e92eddc7a2d2703d0c2568dc06506d9debb7c84ff1d4fd7f6`  
		Last Modified: Tue, 13 Jan 2026 04:37:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bb03bee098c954245123a959074316f711b00449c0836b4bf4da3d82389b5c`  
		Last Modified: Tue, 13 Jan 2026 04:37:17 GMT  
		Size: 15.6 MB (15568094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee9bf4007c3b76219c40c392a8b9800e59398d8053b870ecc94bc4ce994240c`  
		Last Modified: Tue, 13 Jan 2026 04:37:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:92469a01bc65ef963e70238c2c387f31f7e58da085815dd467498c4b039acd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55fef59c784839ba3f88d0e97f87a516379624bb485519877a8bcce2fb70e27`

```dockerfile
```

-	Layers:
	-	`sha256:9e335bba04fe682452250d0d887e03e4ba172f25cc3964ec14151fa1174baa5f`  
		Last Modified: Tue, 13 Jan 2026 05:49:06 GMT  
		Size: 15.5 MB (15451716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc7db78843b8b0bbc53731ab7466e72b531b41727b00c26032a641d2d08e120`  
		Last Modified: Tue, 13 Jan 2026 05:49:07 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json
