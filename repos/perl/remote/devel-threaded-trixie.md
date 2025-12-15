## `perl:devel-threaded-trixie`

```console
$ docker pull perl@sha256:54d5a50c1a76e71c2cb87d1a7b934dab26bf2953136225a7ebffcb84ed20270c
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
$ docker pull perl@sha256:43ade1c86117f8b3a8ceacb2de8979ec87cd4a77ecbe6242e8fde5a6e623048c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.8 MB (394757979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c545bfd917b632814554041fe8d9b7051cd5291b8fe9f12ece60df33aebec251`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:46:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:34:28 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 01:54:27 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 01:54:27 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 01:54:27 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd420cee8193b72cf70974a80e88896c8e58d925edd1cdc515b203ff7aa65550`  
		Last Modified: Tue, 09 Dec 2025 00:47:38 GMT  
		Size: 236.0 MB (235974801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d0b1e2016a76c3522f5a6d125b74184cf1617c682eebd13c99348f39251a8`  
		Last Modified: Tue, 09 Dec 2025 01:39:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686b09b94a19550c9cf71b626a50456a70b96bdc1f1457768e6f6d733252680d`  
		Last Modified: Tue, 09 Dec 2025 01:54:53 GMT  
		Size: 16.1 MB (16100881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724e44125d37d61959be6b6afe2825314839a654b021fe9c93d5f28635a9475b`  
		Last Modified: Tue, 09 Dec 2025 01:54:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:71bbaa7a5ee684b13bbf45d12ec08f9ed4b6d34ce428077b9bee5e2083264bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17228094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ddef652d1226cca353592954f89da0593b5c88f91e56fb22d1da69f605aab1`

```dockerfile
```

-	Layers:
	-	`sha256:d026248982b11a7ee6649722cb8b9c29d717f06c98f64c8f516b2a9ce92a6416`  
		Last Modified: Tue, 09 Dec 2025 02:49:49 GMT  
		Size: 17.2 MB (17209481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc47d495aef9be6b8d6389a8417726edb3136fa81653ae42589851e99705f4e9`  
		Last Modified: Tue, 09 Dec 2025 02:49:50 GMT  
		Size: 18.6 KB (18613 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-trixie` - linux; arm variant v5

```console
$ docker pull perl@sha256:ca8c1bcce4dce95ba098911533f701ade52c48944db7939163a65302c587c2d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358214547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd4b43c0821f36f948002780790e76ecb9c6ce6675f20cc0845b6133e57168d`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:55:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:18:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:15:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 03:54:53 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 04:00:37 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 04:00:37 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 04:00:37 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:123c232a33b986aeccb984e885244b48200c4eb4f9a811e3df109a416dc71f80`  
		Last Modified: Mon, 08 Dec 2025 22:16:56 GMT  
		Size: 47.4 MB (47448721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbaeb213e9fa41da55c6b895ce8273281464b3351c9fcf26aed8d0fc7484a18`  
		Last Modified: Mon, 08 Dec 2025 23:55:26 GMT  
		Size: 24.3 MB (24345927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4936999457f9b45cd7af5bc334afc3525d9cd25bc796f9420e78292f7e4e6d8`  
		Last Modified: Tue, 09 Dec 2025 01:18:47 GMT  
		Size: 65.3 MB (65318096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbe24d4bd7124e2e25624c6cb817a4ea96874b5b05fa82ee85e637d69cc11d3`  
		Last Modified: Tue, 09 Dec 2025 02:16:29 GMT  
		Size: 205.7 MB (205708128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ca774682ce4f5d21f67ba912cf24c5c2e5157c6d7b83076701ead6559b2798`  
		Last Modified: Tue, 09 Dec 2025 04:01:04 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3664337ba267b66ed4aedc64c25a4c572b0c6c3a88151a3629807be0a157bccd`  
		Last Modified: Tue, 09 Dec 2025 04:01:05 GMT  
		Size: 15.4 MB (15393410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a632378186bacde45f1d5dd5e441c36f85a0dce1e4eb4a22ab20f59650fa86`  
		Last Modified: Tue, 09 Dec 2025 04:01:04 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:c07d0bab8a90c3666e5af5a50497f72dbbb4ca733c3c932ae47a3d1362cd2456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16990413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b575571af97d4b32c9a41661c496ab9004efd0013ee3b10ad58a3cb31659597`

```dockerfile
```

-	Layers:
	-	`sha256:3aa3a7bdd5d3734ac6c31dc951c35f1109c3b12f64728338817e106803c8ed07`  
		Last Modified: Tue, 09 Dec 2025 05:48:06 GMT  
		Size: 17.0 MB (16971703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a645a70065333f04cc9717d771f54d6c3164a7ea4f85ec9afbf14872b075b096`  
		Last Modified: Tue, 09 Dec 2025 05:48:07 GMT  
		Size: 18.7 KB (18710 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-trixie` - linux; arm variant v7

```console
$ docker pull perl@sha256:7baed68aaffa90bce663e0bbfc3cc6d4bd88bb0860a29d6ce3187e4da37d6dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340511859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec66faac8d9ad8041e3639d0a6f742ccb348bc2eee9592dcbfd2250f39d0935`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:33:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:19:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 04:36:28 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 04:41:54 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 04:41:54 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 04:41:54 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:c4eba7a08ba9825cabd599d8641314a004d500b627e05a38640b9d3c0bf389ef`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 45.7 MB (45718282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6ad1d8bb6e8d2c91990f13409d4d822c19a3b9fb5463aa9033cd860aaa4822`  
		Last Modified: Tue, 09 Dec 2025 00:07:27 GMT  
		Size: 23.6 MB (23620171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067e549495a4594bb4406cebf8990f1500f9fbae204461f2b793444540c774bf`  
		Last Modified: Tue, 09 Dec 2025 01:33:43 GMT  
		Size: 62.7 MB (62713415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10f0a24772dec0e72cc1a314a0c6613a5577b09b7b6c8368604b9a163a31aa5`  
		Last Modified: Tue, 09 Dec 2025 02:20:05 GMT  
		Size: 193.3 MB (193258585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c819572111c41d1560d92aa01181300deb8e53e4a828e35a4c4885ebad6ed9a`  
		Last Modified: Tue, 09 Dec 2025 04:42:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91777dd51412bed9365d63303cbdbab91aeb8665cce234208f0fe1c0b170623e`  
		Last Modified: Tue, 09 Dec 2025 04:42:25 GMT  
		Size: 15.2 MB (15201139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6804e1c98555cd1d934ed7ba28a401700ef422c70b9f6956a80f755cdd18f9`  
		Last Modified: Tue, 09 Dec 2025 04:42:21 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:68a93013ced3ed09384dc4a691c9baf871d0dbcd1fd65844da8bdb34d1a9b0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16996203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d7331de8fc0877893e93207287c92fca8e64bfa49e02acbdf1cb5e1bf0678a`

```dockerfile
```

-	Layers:
	-	`sha256:19c61e99081266e6fa09d5354fb030343eef2d8a57388b6e03b6d1edaf176b08`  
		Last Modified: Tue, 09 Dec 2025 05:48:20 GMT  
		Size: 17.0 MB (16977493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b270e6e66fd7bd6f4b440feb80c15cea45fba7295205575f44f60ad763a0a42`  
		Last Modified: Tue, 09 Dec 2025 05:48:21 GMT  
		Size: 18.7 KB (18710 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-trixie` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:4f2653f1e8e8033212c3ed368e260eeb2e4277f60fbc5fa8d6fca296819b2108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384407522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b4ecb17de811d3d87636ab784d6ae849bc921f257bad592cc912aee65f4884`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:16:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:23:17 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 02:43:16 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 02:43:16 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 02:43:16 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2b4af09d0743acafc293109ad1b191f5a03a36cd1dddf8454458ced3631f5d`  
		Last Modified: Tue, 09 Dec 2025 01:17:36 GMT  
		Size: 226.1 MB (226108094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524834ff7f669762223ae8ce753b95facd462ff828207bd6a3f9a09cc96fdaf7`  
		Last Modified: Tue, 09 Dec 2025 02:28:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e4f7c9d739ab7c45ee0a0b487214f20abba5f8932507e59b5b72bfbced566d`  
		Last Modified: Tue, 09 Dec 2025 02:43:44 GMT  
		Size: 16.0 MB (16042983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd892a6a116e90f3347fed4cbb9d76d458c7d095357ca6bbd6342b00e8dcdc5d`  
		Last Modified: Tue, 09 Dec 2025 02:43:43 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:b91fce7e21a4be68f48340f93239db87267e0b8a481a1aab8b6c213a19623f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17312553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af65bbb20bb1eb9364eae066e03f20bfd5a021d8bbba029e34143adc7305a11`

```dockerfile
```

-	Layers:
	-	`sha256:1eaa786c91d04ea9b8758ef66496db35a545f7e34a9353ff7a957933c6eab98c`  
		Last Modified: Tue, 09 Dec 2025 05:48:36 GMT  
		Size: 17.3 MB (17293811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d1a45660888b749439ca7bda7b5d9c64ac0115a83df20cfe68e46bb5ec15e33`  
		Last Modified: Tue, 09 Dec 2025 05:48:37 GMT  
		Size: 18.7 KB (18742 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-trixie` - linux; ppc64le

```console
$ docker pull perl@sha256:7297570c88a772282cdb4fd6e79cc91d5c76e41fd0f12754e0a15d6644aff0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.4 MB (400357543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757597eef7b8abede134653902d861a8e162f46a02eb9130703da7057e1927e9`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 04:34:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 11:08:36 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 11:16:55 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 11:16:56 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 11:16:56 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e79cf54a8287f03b9105a7213ef3a99e05832db0bdcaf506dd64b872bddfd7b`  
		Last Modified: Mon, 08 Dec 2025 23:23:25 GMT  
		Size: 27.0 MB (26996775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbdd943d24ee93fc3b0013d3315e9ace0f4529c7fcae39b318579723e579b6d`  
		Last Modified: Tue, 09 Dec 2025 02:13:21 GMT  
		Size: 73.0 MB (73022086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc59b593a33ee8746f94dd61c3d4d2abec3c25d3c7e93e36a9043ee716aacde`  
		Last Modified: Tue, 09 Dec 2025 04:45:03 GMT  
		Size: 231.1 MB (231106988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49689c8b8ed1c8a959815b21a854a40f4c81efa6dc51495258af9f789b63044`  
		Last Modified: Tue, 09 Dec 2025 11:16:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc579082c9b517297f433fde879eec8a5f703af5e5b168dbe0e6a62d7a3337d`  
		Last Modified: Tue, 09 Dec 2025 11:18:04 GMT  
		Size: 16.1 MB (16122950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4069acd83adfd0bd4fdd75efda4722450de1ee9d2815958d41cc7de3675b9074`  
		Last Modified: Tue, 09 Dec 2025 11:18:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:66051e1042cb6cd369bd9a67b0d7fa984dfd38f6a9fe06d2fcd4087a60569e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17213718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fae5ee900872b6bbffadbc1a6156421d4bb28cedeecae586849a869ca6299aa`

```dockerfile
```

-	Layers:
	-	`sha256:24c25e606b4929be8665f1627ccb7a40207e6925a81e50e0076a42b597ae65aa`  
		Last Modified: Tue, 09 Dec 2025 14:40:52 GMT  
		Size: 17.2 MB (17195048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b6c9edb4387663cc7fc8c213c861e9eb9ad5e0201f1241759048a16900a4c2`  
		Last Modified: Tue, 09 Dec 2025 14:40:53 GMT  
		Size: 18.7 KB (18670 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-trixie` - linux; riscv64

```console
$ docker pull perl@sha256:7940825b9a8f4fe0a04c1218169f03e32bb438ac5be8910474c969acb88454a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.8 MB (477814786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499f1fc628cb16ea40dd2f8ef139a8da1fe962eb2ed1549084f25ab213380412`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 08:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:46:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 06:42:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 08:53:25 GMT
WORKDIR /usr/src/perl
# Mon, 15 Dec 2025 19:00:44 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 15 Dec 2025 19:00:44 GMT
WORKDIR /usr/src/app
# Mon, 15 Dec 2025 19:00:44 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088c9d98910c38f13b1907a28647a9e78cc7ea821df93ab45af07ce2813dcab`  
		Last Modified: Thu, 11 Dec 2025 08:40:59 GMT  
		Size: 25.0 MB (24953834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a60a42ed8727e43dc5cd180abfcc19a18468941394808f724b1f4dc00352352`  
		Last Modified: Sun, 14 Dec 2025 08:50:41 GMT  
		Size: 66.7 MB (66660499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89b1e152c7f5b34657f3a6e97a87170ecf850bc400696de74b3929bc238f0d3`  
		Last Modified: Mon, 15 Dec 2025 06:59:37 GMT  
		Size: 322.9 MB (322886042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23b426781cb6a695d490240262f612651ac55b6f15d68dc12eaf3dd5ee792c`  
		Last Modified: Mon, 15 Dec 2025 10:07:38 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2f95bc6898dc703cf59e9d9c5b88dc854537cead051223e20a096de0a7ef17`  
		Last Modified: Mon, 15 Dec 2025 19:09:03 GMT  
		Size: 15.5 MB (15543008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e032ab9ea556b3b72f6e40e77335cba987087fb958ab90b26ac6692502203ce2`  
		Last Modified: Mon, 15 Dec 2025 19:09:01 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:8509e72b3da2b7c1b61b862eaf3244062d0073b41fb336b57daf842aa41b73f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17284361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:330523f9c4ef78729d99ce36ba51f0bfdd7f9192d397d45023a27950e49a6add`

```dockerfile
```

-	Layers:
	-	`sha256:0b3c06a75c93ae8daefa69d298a4b6b4043fac74ee8d96b84929826abce7a672`  
		Last Modified: Mon, 15 Dec 2025 20:40:51 GMT  
		Size: 17.3 MB (17265691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612005c61793fe6497f18b7cc0ab3caea54919db46809e55203d6c7a01d54d71`  
		Last Modified: Mon, 15 Dec 2025 20:40:52 GMT  
		Size: 18.7 KB (18670 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-trixie` - linux; s390x

```console
$ docker pull perl@sha256:8a4954aa8f4bec633c3fc71aecc2dcac7d250619bc625bc6f9be1b3f602f3fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.9 MB (367922564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6d593447307865283c80f1e2365bc024eaed588d955c647d4d680f03bc0256`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:57:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 05:05:50 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 05:39:51 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 05:39:51 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 05:39:51 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98c145469a927f8321c172bcf0ed7919725c5f02b2fea3f4d05ea5083b4b8c0`  
		Last Modified: Tue, 09 Dec 2025 00:12:09 GMT  
		Size: 26.8 MB (26786516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a105dbf5cfcb4e2c38a6c33b07d696009c0c1ce742a7404e87b258f0914a1424`  
		Last Modified: Tue, 09 Dec 2025 01:47:55 GMT  
		Size: 68.6 MB (68624346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d6b6af65161fdf6adbca5b49fba0d0a414708fb199521ee78075952e4ba4ca`  
		Last Modified: Tue, 09 Dec 2025 02:59:04 GMT  
		Size: 206.5 MB (206478489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f3f4ec628fea5c138297fe3c247821519c5ce2d8a15a78cef1d0e506d7595e`  
		Last Modified: Tue, 09 Dec 2025 05:11:33 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a9bcb63c92332ab474b7eb818e13e2614278890de1de369398cbb91873e55b`  
		Last Modified: Tue, 09 Dec 2025 05:40:29 GMT  
		Size: 16.7 MB (16687038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033dc5efb631472e9946b63badb89fb94142a1dafaef09e8443b442da497725f`  
		Last Modified: Tue, 09 Dec 2025 05:40:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:78b8080714a5d2252dbebd507b681f21b095473902b50b5a4846c697a7fe63a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17005328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f214b1bbe225a90316759fad29a1aae1fe0e35b4911f456f74da8d330dfb79`

```dockerfile
```

-	Layers:
	-	`sha256:151a381dd1e241003b61bd5421e8d8986c723eeca449c3619e0de85753c5676d`  
		Last Modified: Tue, 09 Dec 2025 08:43:32 GMT  
		Size: 17.0 MB (16986714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:907c7a604c2bfdaafd205e30b9cf978f48c80180b25c5f79e035495e3877ea54`  
		Last Modified: Tue, 09 Dec 2025 08:43:33 GMT  
		Size: 18.6 KB (18614 bytes)  
		MIME: application/vnd.in-toto+json
