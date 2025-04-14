## `perl:latest`

```console
$ docker pull perl@sha256:73e29cfe12b0495d769cc53da2ebb60a9e1aa56c410a7ea9e1e0d9686cf96e98
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

### `perl:latest` - linux; amd64

```console
$ docker pull perl@sha256:1b4def4dc470617248a3b070f582314441d43853298cc34918472f8c177ff07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (364039457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbffe45ee5660e5e06a841866a7ac8dbf7c5f3e52f9cc9eb7aef964b3e45dc6`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b617a119f8a27982374d94ec6eb3738ae3d38d6fc2c34c865813926cf596a621`  
		Last Modified: Tue, 08 Apr 2025 03:16:47 GMT  
		Size: 211.3 MB (211331550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d3721eebce24c46caaaf40952dcbdab93cea83f3e6b10c649c4433c42ff5e9`  
		Last Modified: Mon, 14 Apr 2025 17:48:28 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbc38f92afe5d0f62d294dd612df853dbb198ca7d4bcac0f5bd037cd90d895b`  
		Last Modified: Mon, 14 Apr 2025 17:48:29 GMT  
		Size: 15.8 MB (15809542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa945014fb9a7a00e3f33fd650c891864b653d3c3ee0160eccf6044391bdcb9`  
		Last Modified: Mon, 14 Apr 2025 17:48:28 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:d957bcce4fc497f2e85d9104e9b4766dc6521790ed23b92a737aec647cf48e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15491475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe07fb237e74f2e59ed68e9cc4c81c01d13a63c6216eafc66a420a150030415`

```dockerfile
```

-	Layers:
	-	`sha256:829c2a05baf79c017c9208243c302503c3ac02907bc7247fd7f12f34481e0633`  
		Last Modified: Mon, 14 Apr 2025 17:48:29 GMT  
		Size: 15.5 MB (15471867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e8be3d938e611c4884f32b41223e3bf4097aa3a3f0b4ec08db96d86a6b181e`  
		Last Modified: Mon, 14 Apr 2025 17:48:28 GMT  
		Size: 19.6 KB (19608 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; arm variant v5

```console
$ docker pull perl@sha256:908588512f7229de8d44514cf0ac6f223056bf422029fdd3f88191c623606663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330448323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e3de07ea616ceca446db2023aa24a6f5d0e96d873a82d094c31035fb42440d`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:444a58715eaf0dfd1bf39e8ed2c8a7ca67bc95fb2e8d072811ba720753b5bdd3`  
		Last Modified: Tue, 08 Apr 2025 00:22:50 GMT  
		Size: 46.0 MB (46026188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475fd0c8f5bfbbc214449bab28de187a71afadbad78b3fcf3ab5a380454a0d52`  
		Last Modified: Tue, 08 Apr 2025 05:11:56 GMT  
		Size: 22.7 MB (22689768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a439b8dc553dd972e806fbe1e6609bc57221e66dbdd1f511c50afda48bb3355`  
		Last Modified: Tue, 08 Apr 2025 08:37:37 GMT  
		Size: 62.0 MB (62008221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca9cd06f1a9db5cfff9c325784dc0f41fc6a767263f6a8aa490157957bfe774`  
		Last Modified: Tue, 08 Apr 2025 10:14:56 GMT  
		Size: 184.6 MB (184629675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1216fad5b77a4637a5c6948125e08636b955da9a83d2f32d18a1621afdaa755b`  
		Last Modified: Tue, 08 Apr 2025 13:44:46 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748714a39e7cdfe198a089e0a00275d60bb51185925bcbc6f338cf8875b7c581`  
		Last Modified: Mon, 14 Apr 2025 17:47:20 GMT  
		Size: 15.1 MB (15094203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf82436c2c31d5c0c328f9b2ab764bd4c59ae22c57b536e7051a38f1003f08`  
		Last Modified: Mon, 14 Apr 2025 17:47:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:6c142b3d1935092032d680104d379cc37405506c59044f7f3a7c73a1ec5574f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15290574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee3a2208ac36614e6f4d6687e551c658453348ea5d2f06dc4e85ca2ed5cf59d`

```dockerfile
```

-	Layers:
	-	`sha256:03286543686250589fa62d52eaf1fc5ddd7a6ca8915a49a112587155bef87714`  
		Last Modified: Mon, 14 Apr 2025 17:47:20 GMT  
		Size: 15.3 MB (15270841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b5a2af9ed4c98cc3fda7f6c79af43e95704b44db83fc1394c0e34227e24583b`  
		Last Modified: Mon, 14 Apr 2025 17:47:19 GMT  
		Size: 19.7 KB (19733 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; arm variant v7

```console
$ docker pull perl@sha256:bb58714891d40cad8a02a9fd4e901b219b457ad5b5446cc6fc102cb9657b590e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.9 MB (315945407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214b832cdb171da301e99cbce11f4e5fe203206e6b4c85af03bd5be75c83a1e6`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd5426bd57bea2caac0e0e87b98c0988fb39decb07637e76311bc28b01e6b7`  
		Last Modified: Tue, 08 Apr 2025 20:34:20 GMT  
		Size: 175.3 MB (175297229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ef9d00dadf3d75d2447577ee1e4941a621f585ecf6e56c81dde7a717ef4b75`  
		Last Modified: Wed, 09 Apr 2025 01:13:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d64867b83251d64b3b4459a90115465a9695145eb1d9cfd30296d8334a3be53`  
		Last Modified: Mon, 14 Apr 2025 17:46:56 GMT  
		Size: 14.9 MB (14893472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5bba1492e1743b84c239cad0a90110f3314e1d3b779266ce81281b2f9c9949`  
		Last Modified: Mon, 14 Apr 2025 17:46:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:3c7c8746c411e7fa88c706bc88cbc0e757ade1644abbc99e5026d8e14f13383f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15296048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07ce0ec9f447d0398fa1a569580a83f722d9ff66e8aa621850d3140f16820da`

```dockerfile
```

-	Layers:
	-	`sha256:9f41062cf58c78fc329050ef5946a8b4860178d6e32117399f73a6cef0ba1104`  
		Last Modified: Mon, 14 Apr 2025 17:46:55 GMT  
		Size: 15.3 MB (15276315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:372d6147c0fae8d8c8f4db493344174da4d35bdd15fad812d9f9ad772afabc84`  
		Last Modified: Mon, 14 Apr 2025 17:46:55 GMT  
		Size: 19.7 KB (19733 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:3039d19348d5debf44bf2c11366e40599249e45b1948eb30e9cc5567138a5534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354733155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521c6ac71128238bf97ac8aff38f1c1f714e7ee751952388c07518b10c3d3f53`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002e18bd5659ca9d155e99922678788bec836a3ac4964d8a9567ce59e2154de9`  
		Last Modified: Tue, 08 Apr 2025 15:52:42 GMT  
		Size: 202.7 MB (202735307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f600ef1fe5f8519bc507f7ff4eb810f784c1e3492c5cab05e5876e22beb6768`  
		Last Modified: Tue, 08 Apr 2025 17:42:42 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c55ebc9652387b3d698c24ac876730b89614797d368766d924701a9accdbcd3`  
		Last Modified: Mon, 14 Apr 2025 17:45:07 GMT  
		Size: 15.8 MB (15769992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bd00d227984aaacde72f149a7e74dd69821d819e5a7cdbb898a3e1385dda74`  
		Last Modified: Mon, 14 Apr 2025 17:45:06 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:ef873db7c850310814c2ab79e98d6e736cdc632528ee47deedc9dd57184bc968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15520249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbfbba8408912a4ab160fd8e0474246009ed1e16e0cf7e7f8d5b9d559f216f4`

```dockerfile
```

-	Layers:
	-	`sha256:2e143916c7606bc8c8df1f00d712fd4ea4bb1efc211cac7695f58ceab8572dac`  
		Last Modified: Mon, 14 Apr 2025 17:45:07 GMT  
		Size: 15.5 MB (15500464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda61c29ef12c23f481c09fb12c789d5734ee6a9a7e24d197fd026ad0f6b5235`  
		Last Modified: Mon, 14 Apr 2025 17:45:06 GMT  
		Size: 19.8 KB (19785 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; 386

```console
$ docker pull perl@sha256:5708313d6871b0347d835631684fd60ed438d83070bac2edf1d4265e08ce11a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366136966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba910b71ba1baaa958af537661b186ee6a619dc5826a9b44a0d9c08b596ab520`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ffc3e6085548412ccbe96cfa7c6e138ccc7724d5a764a6a99e732fca48b289`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 66.2 MB (66237424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8471ab4232bc51e32c08f3c8fae6e33670c6c77fa4a3359a48d05453051f93e`  
		Last Modified: Tue, 08 Apr 2025 03:17:21 GMT  
		Size: 210.3 MB (210267336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2372f95154bb527998a6375e1db3ebdb7f738f3b5decf491302bb41d1fbf1a66`  
		Last Modified: Mon, 14 Apr 2025 17:48:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e48f2bf2ca747c692437d72b0f82fc3321ab5827e245026a6f8fb487e8eb83`  
		Last Modified: Mon, 14 Apr 2025 17:49:36 GMT  
		Size: 15.3 MB (15306605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caff9e7094b2b0212afef4e25213dedfebb78d930ac4144f65a16cb2b603c3a`  
		Last Modified: Mon, 14 Apr 2025 17:49:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:c71fafa95c11ce2d62504249d5c54c0251d80a03cd83387dfac1c880673236c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1070db00390746b7280dce9f87d8faf81a51239c0bf001a45d05b5a4d0558492`

```dockerfile
```

-	Layers:
	-	`sha256:c588d6d667ae41a87dc471d6d4ad4b686394980e4d26e2bc80feaf9850e2e82b`  
		Last Modified: Mon, 14 Apr 2025 17:49:36 GMT  
		Size: 15.5 MB (15450425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaad8fc1bdfd7c1f99ac43fc7aac395bdb7540114033ca3bbda350cc7bdb8bde`  
		Last Modified: Mon, 14 Apr 2025 17:49:35 GMT  
		Size: 19.5 KB (19547 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; mips64le

```console
$ docker pull perl@sha256:c8ab24a6cc0daa404f65b5178e110b95822605eb17d815cea5e5e9057813e477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340626712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60994421a3f42ceb03b6bdd86712fe38b61241162e9d17d0f4093255f1cb5a1`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:f5e7682657f9515783d77fb7efbdd12ea81bbe4c750080727193e5396dfa344f`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 48.8 MB (48774861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca83e3505dc809d18860248927308a5c27c298583b9da5817d702111bdd65622`  
		Last Modified: Tue, 08 Apr 2025 16:31:05 GMT  
		Size: 23.6 MB (23595612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89ecdcc124054ab515f88e8a0bc5260e578fb23450a3ca215363db6cf689231`  
		Last Modified: Wed, 09 Apr 2025 00:38:14 GMT  
		Size: 63.3 MB (63308311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7549fb43869784332073d59495afe808b54bfcee1761b7a0bb69ce5a525ab5e8`  
		Last Modified: Wed, 09 Apr 2025 07:56:22 GMT  
		Size: 189.9 MB (189921312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79408d275227d46adce50e9aef83189eac80f610d7cbd0a1f9a25f09f27d50aa`  
		Last Modified: Wed, 09 Apr 2025 10:47:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffbe8e7d9f52e2e7a5f8d0db86c60f3b3b53e2dddff351b2cb4afc86fb2c5d1`  
		Last Modified: Mon, 14 Apr 2025 18:05:13 GMT  
		Size: 15.0 MB (15026350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a2380ed3a05067f9bfb2186496f52f01d939fbef0e09f838f1ecbad5ca94b`  
		Last Modified: Mon, 14 Apr 2025 18:05:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:17c54ffea71c2d531c95d8990af8bc7ef2695c0e39465685cea19bf7f8543f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e85f9d736eea0590803a44f0332a2c64e2392579f08e5e47e01975e17812782`

```dockerfile
```

-	Layers:
	-	`sha256:bfa643fd4bc9deb898e956ef98cb47b87e41bcb232994eab60a8bcdbe7a5a0a9`  
		Last Modified: Mon, 14 Apr 2025 18:05:11 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; ppc64le

```console
$ docker pull perl@sha256:658f26c58bfdac493845658cda53ab588ff988262610ae1604ad71e2319c5d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.0 MB (378023209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ca6424c32468a259efc3d3baf528dbf11ad765e02cbd7322c4df557759385a`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675af5e5720aa9e9d4f74b056a7b58aa0a84a5b3cc2c23272c361e473b9c5b8`  
		Last Modified: Tue, 08 Apr 2025 15:34:04 GMT  
		Size: 214.4 MB (214387209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0648a20768d67c4ed45e40185b406e19df63fe72b755895232eb0f37a9e48d`  
		Last Modified: Mon, 14 Apr 2025 17:47:17 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaab6939a57a45ef6885bfb7c491f26e345423cff1b182f89bb21deffe5dcde7`  
		Last Modified: Mon, 14 Apr 2025 17:47:18 GMT  
		Size: 15.8 MB (15809986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202c49e3db1df05e5c6b7a1eb1a2e401b2310e8e40b2831c049ea3b0b2736f98`  
		Last Modified: Mon, 14 Apr 2025 17:47:22 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:c0f339fb1f4961bae80a4163c288a3d7ff6a06ca1175166606db103a7c591408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15467971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26a0355ad74b9e1e95d92672ef0aab2e8062bd17ae2a4f54a7aaba0aff708a9`

```dockerfile
```

-	Layers:
	-	`sha256:7bb1783701cd6e0b3ecd141063c7db5a56810761fcbcd1439f52481f2482b990`  
		Last Modified: Mon, 14 Apr 2025 17:47:18 GMT  
		Size: 15.4 MB (15448282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eb710de9adf3c0327397f87126f9702127c95d71b4571f00138891a15c23bf0`  
		Last Modified: Mon, 14 Apr 2025 17:47:17 GMT  
		Size: 19.7 KB (19689 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; s390x

```console
$ docker pull perl@sha256:b121eac24af103ffe388d9ad396ff4845a86bbb610f9de5a904b1ba828e7a7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.2 MB (334196902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c122e58236427a43fd2c48e31af82bd9387e8607de5d67fcb074da53f51f18a8`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d2c4791b14ffb813f2bd4d87d95e9030a5939b65f31722bc2c223f845ecf8`  
		Last Modified: Tue, 08 Apr 2025 10:02:09 GMT  
		Size: 183.4 MB (183388438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21326c96e3160d5ef491c711edc6c2d7f3367e387591cb94b06cd0971a87f52d`  
		Last Modified: Mon, 14 Apr 2025 17:50:37 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082af456c43a471bb5b81d447ddd03ddfe3f9aa48024650518f9bcb65b2f86ea`  
		Last Modified: Mon, 14 Apr 2025 17:50:38 GMT  
		Size: 16.2 MB (16150489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0ec24c5e4b24acc7399bb6a2a8373a113220dc743fe09cf7462ec8aa48e79f`  
		Last Modified: Mon, 14 Apr 2025 17:50:37 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:86a0af46e3f668bf2252cc34fb74859d2e595d1addb107d14a9836c8c27792a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15304166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e004efde61cc449ccca34850a9096a15af2eb2355eb4426c0ba70a955f92cc`

```dockerfile
```

-	Layers:
	-	`sha256:6be05355f71765a0c8748e8aec5429a5c308390850171869a37f7c76720b4a43`  
		Last Modified: Mon, 14 Apr 2025 17:50:37 GMT  
		Size: 15.3 MB (15284557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702270b8cb2cf3491d243442b81226db7596ad7b9949306912c698f980dd8cdc`  
		Last Modified: Mon, 14 Apr 2025 17:50:37 GMT  
		Size: 19.6 KB (19609 bytes)  
		MIME: application/vnd.in-toto+json
