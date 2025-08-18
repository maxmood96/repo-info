## `perl:5-threaded-bullseye`

```console
$ docker pull perl@sha256:66589a2f285739135c2c8d374c20e7c5c1c2102cd661c399294a32c9852fdd94
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

### `perl:5-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:337b844e40fd67743c100b35105a66c7ae764171cb30bf71d50b2b7c81a78b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.4 MB (337360721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4901e83596f069cb31beb44b9fa444f21d83ca51961c3f46aa89631c0d0b61d`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620e616831b3851d274036e48fee788599fe355ea621ba7b912b9c15925e81f`  
		Last Modified: Tue, 12 Aug 2025 21:21:48 GMT  
		Size: 15.8 MB (15765318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bdf4e3059e088f15d90d719c388546de462f8152d07d724a4895907f69c1ce`  
		Last Modified: Tue, 12 Aug 2025 22:15:17 GMT  
		Size: 54.8 MB (54757082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6f7f2858f78fda61ee4b09ef4641600c64959581a56b582d6110d612850d83`  
		Last Modified: Tue, 12 Aug 2025 22:50:22 GMT  
		Size: 197.1 MB (197145445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b656af60d32969fe3a9c6aa80dc70de0292451c76192c8ae044154182a6cfb81`  
		Last Modified: Mon, 18 Aug 2025 18:02:07 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f0904778b8221239f4d3a6cf8e832dc32684101449aaec41fd95e1b35cb038`  
		Last Modified: Mon, 18 Aug 2025 18:02:50 GMT  
		Size: 15.9 MB (15937263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a7e073ada1ed0d365282c5b7f0cc9383a98ce51af740938f2a9df41b1a81ae`  
		Last Modified: Mon, 18 Aug 2025 18:02:47 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:15f42aec354ba869f229b7a2278ac93d89aeaf0cbbd115c058b0cfd7db1c6e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15482654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ed47a4d418cdaeb75e4f461ef9dffbb3a268c362257eb7ed26273fa114da9c`

```dockerfile
```

-	Layers:
	-	`sha256:85a20dbd62e9fd605b5b6fad3f74832681d5e5fa3e0a2cc8b86a6489cf7802ec`  
		Last Modified: Mon, 18 Aug 2025 19:41:04 GMT  
		Size: 15.5 MB (15464344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e0b0d3414933e80f6a3a9363d6a94dca1c7f7d8aafb43120d999f14da81a05`  
		Last Modified: Mon, 18 Aug 2025 19:41:05 GMT  
		Size: 18.3 KB (18310 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:9fbea56ef5f7ef7c797bfd093283be30fa94f236f6acaf0ecbee6bbce8835954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297140234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545660c7bc594434059e3d6e6869077591b7992edbd19c938c00536d5bbe6524`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:27a0e70a6a342a82d61d13664b90c890c24d71590db74ef7eb6f4dc1b731387c`  
		Last Modified: Tue, 12 Aug 2025 20:46:51 GMT  
		Size: 49.0 MB (49044404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae3c82b80881167fea789bb8cf043d4de732e7b062431e2c261928679dcd3b3`  
		Last Modified: Wed, 13 Aug 2025 00:15:42 GMT  
		Size: 14.9 MB (14880786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7e2d995d706697c0af2f117145d4dbab9dacbc5f34e7d500b3d99b0062c6f`  
		Last Modified: Wed, 13 Aug 2025 06:47:54 GMT  
		Size: 50.6 MB (50632440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1442f1d0f4f434d42cc2cb968a36d89906e276d8e6a54625dc785435cff2500b`  
		Last Modified: Wed, 13 Aug 2025 13:54:09 GMT  
		Size: 167.6 MB (167590147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4f638a5e4b6e665f24ec4190333dad8d705291c7a674036b4b20e6fb5e192a`  
		Last Modified: Wed, 13 Aug 2025 22:20:56 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b172d7d810ff3b9de3c51d28066bd52f1ec4742de2d62b9960a80c78d5799e`  
		Last Modified: Mon, 18 Aug 2025 18:55:03 GMT  
		Size: 15.0 MB (14992188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2642573af2d373f22e9fc69beb96a8de7cee88e1d998aae5de0f842ec2ffa60e`  
		Last Modified: Mon, 18 Aug 2025 18:55:01 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:5a3e5bb5cd324e0784fbabd3bbcba9262a349f5df362ee4c542af38cf52a9045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15282081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b8e97cb25dca120c6b9015b390b116b570b3b1439b71cdbf7670e0a6cabcb4`

```dockerfile
```

-	Layers:
	-	`sha256:13823e16486e8b95784af3abb366784f08b6a0e66787851056922bb7376df604`  
		Last Modified: Mon, 18 Aug 2025 19:41:21 GMT  
		Size: 15.3 MB (15263686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e769c4ebc9369803a10b4d479ef544f31564a110d516859874e4b51fedaaac5e`  
		Last Modified: Mon, 18 Aug 2025 19:41:22 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:5b3ca79d761af0cf60c202bdbd0b75f7afd714d0dae84be80db2426ec7805feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328753814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37121fff50dc61e5545857e46aaeb9f0b55fd71ddd254f1316d4c12a171a7b6`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25635cbca821869ea9220087d35fa6b59e758fb2dca635f36530cb5e44b7c481`  
		Last Modified: Wed, 13 Aug 2025 07:20:06 GMT  
		Size: 15.8 MB (15750676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06836ab0250fb74efa819c381a3a62f540817c74a1d0468d4e03f53c6b03758a`  
		Last Modified: Wed, 13 Aug 2025 15:28:22 GMT  
		Size: 54.9 MB (54856134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d454c8e58c4069692ce41e243c84f24682d348d8667ce5764628f03111249d`  
		Last Modified: Thu, 14 Aug 2025 00:15:27 GMT  
		Size: 190.1 MB (190058369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12014de98813cd78994506031be419d06194e2d905d98aee4938729e2cfc5e89`  
		Last Modified: Mon, 18 Aug 2025 18:09:53 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11e38ee764971e5d408ea28bc921c8d082c48a4217b83b4f1d6dc6ca5bfea0e`  
		Last Modified: Mon, 18 Aug 2025 18:40:38 GMT  
		Size: 15.8 MB (15839956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300c37d1a9671d907f0434d54ee23351a4ec17af31aaa4054fd66534f5bd809e`  
		Last Modified: Mon, 18 Aug 2025 18:40:37 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:943533aa0352ff6c0247c5196cd0d376d852542d2365125bce2bcf3ee9ed3be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df4673109703a92ff7e46ccb78e904167f15195cbcc8631e723be0c8e5736ae`

```dockerfile
```

-	Layers:
	-	`sha256:8ace0d2429e5a1cd97e27c3d5a9b4c18d02533fd8f4bdfaff70c35314c8ca0eb`  
		Last Modified: Mon, 18 Aug 2025 19:41:36 GMT  
		Size: 15.5 MB (15466325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e153f61a4179710032a1509b285eae10f66c9ca9516925e2ccc1790d53ad2bb4`  
		Last Modified: Mon, 18 Aug 2025 19:41:37 GMT  
		Size: 18.4 KB (18426 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:321248cdf8e1107445b30973e9118ef2450df00395feee39635f0107e8bf60d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342531921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da1be5faf5fe208fc191ac441698f2eb1db14d138421c9398b55e12b3715c7f`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:b148e76c29cc0ae2d2cf6449d62900f5cf24990640523768d8221eafa133979a`  
		Last Modified: Tue, 12 Aug 2025 20:44:54 GMT  
		Size: 54.7 MB (54690594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae804adc09e05ab2a1f1dda5903e8e254e92e67f845b9280059ef40044deadb`  
		Last Modified: Tue, 12 Aug 2025 21:20:06 GMT  
		Size: 16.3 MB (16268966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97464f57da439277ddfe917c8fed666dfa8bf3f7fc45105b14b6645094dddca4`  
		Last Modified: Tue, 12 Aug 2025 22:14:46 GMT  
		Size: 56.1 MB (56050296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf879d37fe4c6007eb6c3e303b759996c9275aea0fb5f70af785da18c2f07ad1`  
		Last Modified: Tue, 12 Aug 2025 22:50:14 GMT  
		Size: 200.0 MB (200047109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8b79ae3bd0963bfcb63bf0bcf75b4c1d780058a0355f730d5c53bad86114db`  
		Last Modified: Mon, 18 Aug 2025 18:05:03 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24a7d5992d9270bcaa14b25d3d9e904d63e55227ce9fee4efabad13a2ce07a`  
		Last Modified: Mon, 18 Aug 2025 18:05:05 GMT  
		Size: 15.5 MB (15474687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d9fa1ac2649aa47ddf509af05ca40b72b9e55352df5380270eedbb2a52f5bd`  
		Last Modified: Mon, 18 Aug 2025 18:05:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c43c45d694120467c8cdc567ca0420f5ff38453552c3f4e2fd2b679bd16c319c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15470618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e3da831c3588b92e2b2f1b623a3f6acf1c198986d2180346be3beff1e30325`

```dockerfile
```

-	Layers:
	-	`sha256:8875cd3c27bdc309accc4df2c1a065269847bc387e8ac8466b0547723c4242a6`  
		Last Modified: Mon, 18 Aug 2025 19:41:52 GMT  
		Size: 15.5 MB (15452344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b31ff4227f2e21fc564ed9fabff6e5bbb732b701be3700d73a2332213f3b17de`  
		Last Modified: Mon, 18 Aug 2025 19:41:53 GMT  
		Size: 18.3 KB (18274 bytes)  
		MIME: application/vnd.in-toto+json
