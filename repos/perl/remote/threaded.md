## `perl:threaded`

```console
$ docker pull perl@sha256:c2bb6ccda33c874be91cdd371f55a703cd9a2160af004a227d42706d12b48c07
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

### `perl:threaded` - linux; amd64

```console
$ docker pull perl@sha256:9d61a982e0cb12045c03840da7fc00ee0a3571f3f9b61c4e33f62ddda8853a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 MB (394616103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b187729a62394810850ed0024a59079216db74a3886821ff664fcbcd6c33f95`
-	Default Command: `["perl5.42.0","-de0"]`

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
# Tue, 09 Dec 2025 01:38:54 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 01:38:54 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 01:38:54 GMT
CMD ["perl5.42.0" "-de0"]
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
	-	`sha256:29e6ea88c1f125ec30efea3bf962d0d11be22c22a206ed7b605bfd1ef7a32319`  
		Last Modified: Tue, 09 Dec 2025 01:39:26 GMT  
		Size: 16.0 MB (15959006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c69a9aab0a6d63f3c6830f5d056e9dc000f14b5710904350c608f6906a2fc0d`  
		Last Modified: Tue, 09 Dec 2025 01:39:21 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:bae51585b3e74d1eacb288caa03059b4532497aa15a1857d76e495c0256edc4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17230487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15055fad44733d3db81f41b9b822bbc92bf9376503963b4f8ef608dfef8bc06`

```dockerfile
```

-	Layers:
	-	`sha256:7e9903d7f5935ee8cd4afbbce9df06e66bb4f947f3c586920e3751e63028597d`  
		Last Modified: Tue, 09 Dec 2025 02:39:20 GMT  
		Size: 17.2 MB (17210713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec751bf790c4163ab7e9698376d8c50c1fd0ac5e2ea88e0fc56b9e1570283a06`  
		Last Modified: Tue, 09 Dec 2025 02:39:21 GMT  
		Size: 19.8 KB (19774 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:c4847f469f9e454a518973344b1aab522605cf149e51b18dc75c61f1b6bc0699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.1 MB (358064924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc2b4ad4810ec85faa7e4f9eadd20362c18926afda3b42989da15c1dda9a6cd`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:55:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:18:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:15:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 03:24:24 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 03:29:58 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 03:29:58 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 03:29:58 GMT
CMD ["perl5.42.0" "-de0"]
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
	-	`sha256:57df105e96fa537422d1a1ae056b9f63532fbb651f740ac8b5d9ea46db82d43b`  
		Last Modified: Tue, 09 Dec 2025 03:30:27 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523e2d3ae2641a9b0d33e16a22efb947501038768b180b8cb916b475a93c6cc3`  
		Last Modified: Tue, 09 Dec 2025 03:30:28 GMT  
		Size: 15.2 MB (15243786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15efdc72e868244262cfd73c2bcab4dc9b257fca8b068eea5f79a57ed20b38b`  
		Last Modified: Tue, 09 Dec 2025 03:30:27 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:69fbda0cf03da890402f592a8f8426ce34829f39a3000a950051f8d8098c3549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16992868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be0f8cfcec41009f9cba35fb9840ceeebb235fade514de4c33f873bcfaf0e6e`

```dockerfile
```

-	Layers:
	-	`sha256:8ea320d7537c8701a91eb955bc323ec64a3ec137a67bc8eb8c6545ec557c929b`  
		Last Modified: Tue, 09 Dec 2025 05:38:52 GMT  
		Size: 17.0 MB (16972967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2bb7c71bac62785e956943406522d24574203463fc418f3db341652ef25ed14`  
		Last Modified: Tue, 09 Dec 2025 05:38:53 GMT  
		Size: 19.9 KB (19901 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:6a08f16563b9c42e117174911566221357dff7dd4b0b19ac7b8ffb158d296096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.4 MB (340356962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b85775e0595e40d654f713cb3d621e4d4969b3c071ee4afd1768e9f36a2939a`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:33:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:19:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 03:44:17 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 03:49:40 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 03:49:40 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 03:49:40 GMT
CMD ["perl5.42.0" "-de0"]
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
	-	`sha256:300b17f1f9aa1402188cc2cb3f5f813f2be40320ab8c107af0429053e26b056f`  
		Last Modified: Tue, 09 Dec 2025 03:50:18 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76c8058eee96c735b0a92340c9628127303f5dead7d739a2a6d9670d75a904`  
		Last Modified: Tue, 09 Dec 2025 03:50:22 GMT  
		Size: 15.0 MB (15046244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8b5836e64b700a4c6aa4d3235f73ff3041cdfc94a6409818578eab944f8afd`  
		Last Modified: Tue, 09 Dec 2025 03:50:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:4e93229e469520fb2fe42b16d7564df1d5b5ae198ac0a1edd0452462755d5065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16998659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c993673451e5645720f5075cad957106ceaca648e69ad87ffc3e6ff87ea9fc74`

```dockerfile
```

-	Layers:
	-	`sha256:5498f9cbe384858c0e75626f26b9109a219979eb1409d1bdeebc8f5e4fa3e07d`  
		Last Modified: Tue, 09 Dec 2025 05:39:06 GMT  
		Size: 17.0 MB (16978757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c6c54aa9a4c0f266d25a4ece91c4f72e666ed9ed7fe41e296ca9b38f83edb59`  
		Last Modified: Tue, 09 Dec 2025 05:39:07 GMT  
		Size: 19.9 KB (19902 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:09036b6e0ad6eadaaf68f8591d684fe69286314f8d4a1231d320cfda532fe2a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.3 MB (384264141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2b73c60f85a0cbc824c1bf1936753e915245f738825ae95c991111c86a5db4`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:16:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:23:34 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 02:28:24 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 02:28:24 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 02:28:24 GMT
CMD ["perl5.42.0" "-de0"]
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
	-	`sha256:c8432ba81733db946ea2a2af358a301fd98d4cf54169491f39f497e2981dd386`  
		Last Modified: Tue, 09 Dec 2025 02:28:54 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dac93e26cefe54e81472ebfd716608d70e4058292d58b90e5b40dd1c0e3231e`  
		Last Modified: Tue, 09 Dec 2025 02:28:55 GMT  
		Size: 15.9 MB (15899603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9690081cb91de308c2f4e30f8a4908622f4d77ee6a39404952dca8556c07b14c`  
		Last Modified: Tue, 09 Dec 2025 02:28:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:88b6187543e4fefaff5aba47882b39f69d0003ff92389ba6de1011d267f83546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17315041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98849659de6a279c6b0b0ad6398ff445ebe98628904e27c56fcd3e7458a85f97`

```dockerfile
```

-	Layers:
	-	`sha256:53da082b256f008e310ea788d1f24936d3e26163c71da59e8d15c884c37c9b62`  
		Last Modified: Tue, 09 Dec 2025 05:39:23 GMT  
		Size: 17.3 MB (17295091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4227c0ee01c1ae2581fa9b3d8e2307c034f0343e33e49c7158903f413f081a9b`  
		Last Modified: Tue, 09 Dec 2025 05:39:24 GMT  
		Size: 19.9 KB (19950 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:7736f53807a12ae1a242663a07ecc5dfbbbb5effc866e0a864b1b6e92afc7e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.2 MB (400209913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e75ffce87ca22240f311fbd7319c19d11539b7cc651f0321f87933a6e6ba4b9a`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 04:34:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 10:47:23 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 10:55:55 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 10:55:55 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 10:55:55 GMT
CMD ["perl5.42.0" "-de0"]
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
	-	`sha256:7584510ac60c4ae9b342f91c75c34b25079272eaa7380f0fc290a1495022c7b6`  
		Last Modified: Tue, 09 Dec 2025 10:54:39 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b0377cefef0e40fba2fb77acf91cee6fc58ea46073a8e87b47fe3a9d10e82b`  
		Last Modified: Tue, 09 Dec 2025 10:56:45 GMT  
		Size: 16.0 MB (15975321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df99a84adce47e2423ad2d39b85a8f48c8bd3ba5b04e361d4a80f954ae884b9`  
		Last Modified: Tue, 09 Dec 2025 10:56:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:41d8f6918c7643ab388fb726f2c6e4ffada5ef572229787830ab619eb609c531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17216158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f707a05c765d10273f74b9b194fd8db4ec01c304d3fc060762bb6a27f9e350`

```dockerfile
```

-	Layers:
	-	`sha256:6141d0170593bd936278fd67b25ffbb9116df84b03742eadcc144f206a59c641`  
		Last Modified: Tue, 09 Dec 2025 11:38:22 GMT  
		Size: 17.2 MB (17196304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0db4acb4b821b63056a9f83f3f62b81890ee05d58f74e80192c75dabdacfa43`  
		Last Modified: Tue, 09 Dec 2025 11:38:23 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded` - linux; riscv64

```console
$ docker pull perl@sha256:9443b6f6257163fb0ee02cb184d32dc9f57b2054ab762b75507c95863f29c7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.7 MB (477670063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff22bd30cdcaaad6b08c98f60400ed841bea9d60edbf66de058024d4f93a7771`
-	Default Command: `["perl5.42.0","-de0"]`

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
# Mon, 15 Dec 2025 11:18:47 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 15 Dec 2025 11:18:47 GMT
WORKDIR /usr/src/app
# Mon, 15 Dec 2025 11:18:47 GMT
CMD ["perl5.42.0" "-de0"]
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
	-	`sha256:78bf458a4eacd3b0f5c2b8fda6a66ac498510e9d88d823dfd92e9ad213b36de1`  
		Last Modified: Mon, 15 Dec 2025 11:27:10 GMT  
		Size: 15.4 MB (15398285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa2def0827b7e66a35a80966f4810605bb93c2d4646e0248c4f4861c5312cf7`  
		Last Modified: Mon, 15 Dec 2025 11:27:07 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:f5f66d417e25b3aabd0068fd8d84402b9072fa36e9054329f607e733ec779db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17286799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70c2b12521e54f2d5c6d13acbd7fc602710d4bb51406bcc368292fdb8a60027`

```dockerfile
```

-	Layers:
	-	`sha256:5a2f743c83cbe691496231da8f75053945b68e8b67d1c1e21096bc56463f19fb`  
		Last Modified: Tue, 16 Dec 2025 01:34:46 GMT  
		Size: 17.3 MB (17266947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e35d76525e6d7c06bdd7ea65d48127b90b3aecda499969c62d7bbc2ea37161c0`  
		Last Modified: Mon, 15 Dec 2025 14:39:26 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded` - linux; s390x

```console
$ docker pull perl@sha256:1c413d40b08c28847b39955d3f7d803ebee6ccaf018e58bdd77de70558424a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367765895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0c7737b0bdc11bb995d8b78fb6c9c8e2040983d710910b75e8677e5f900474`
-	Default Command: `["perl5.42.0","-de0"]`

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
# Tue, 09 Dec 2025 05:18:33 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 05:18:33 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 05:18:33 GMT
CMD ["perl5.42.0" "-de0"]
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
	-	`sha256:f24b5b8f58ed61abf0e8a4902d922a8307a4b8cdbf3538740cf7edc729a73863`  
		Last Modified: Tue, 09 Dec 2025 05:19:20 GMT  
		Size: 16.5 MB (16530371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f30837451d8782a59bf33ca0c674b28c3b5748ad2cc9a9ef7b5611745046d32`  
		Last Modified: Tue, 09 Dec 2025 05:19:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:5fa628e9cb21bf4f8c521a373741c6f903616bc0aaa811cc5b4a9f7161427ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17007720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d1e94d1b1b7bdb36eaa45108e8ea5114dddc6961ef22a4d5cf35423cf498d6`

```dockerfile
```

-	Layers:
	-	`sha256:d824192f84f1bac8be6ebf85f7eba4b8330100cfea72d17fcc4c8a1a9ebd04f2`  
		Last Modified: Tue, 09 Dec 2025 08:38:57 GMT  
		Size: 17.0 MB (16987946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c310c03d2dce03f1eb47e17808ba473e4f3fd1e73b6d0d5b0512e0ca96238c5d`  
		Last Modified: Tue, 09 Dec 2025 08:38:58 GMT  
		Size: 19.8 KB (19774 bytes)  
		MIME: application/vnd.in-toto+json
