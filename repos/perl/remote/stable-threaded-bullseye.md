## `perl:stable-threaded-bullseye`

```console
$ docker pull perl@sha256:5dd7bf528796ee7b27f33400572f745dec31c5c944a565d3992aeba33b8b057d
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

### `perl:stable-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:1546ab2ce49c8096122298b83a4446fe372065af55d49289f06f7656869d839e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (336963962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84529ef03631900c701a1a91db4e0d2e9d239c3ab5493565468bc727be77558`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.1.tar.gz -o perl-5.40.1.tar.gz     && echo '02f8c45bb379ed0c3de7514fad48c714fd46be8f0b536bfd5320050165a1ee26 *perl-5.40.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.1.tar.gz -C /usr/src/perl     && rm perl-5.40.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.40.1" "-de0"]
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 05:19:08 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d32181a1ed55cf7269c27a7a18858d7a4679d9fccbc616d5d878b6ddded25b`  
		Last Modified: Tue, 04 Feb 2025 06:14:22 GMT  
		Size: 197.1 MB (197072749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b66f058cf64a92ed8420888a35a697a12654ea27f46ac6e0a68f405bc3b64ef`  
		Last Modified: Tue, 04 Feb 2025 07:20:29 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b6f0f551c38703a95dd488708e1cb1d93746d00d4486548eb98c984a9fba01`  
		Last Modified: Tue, 04 Feb 2025 07:20:30 GMT  
		Size: 15.8 MB (15841886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51385796f07a8803f6f985640737ad5cc2688d3cf522622dbfb45143d7bc998`  
		Last Modified: Tue, 04 Feb 2025 07:20:29 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:62ae5fe40aaa04d1ae47fc46d0a7bf8a676ec78f7e52f333c076fccea29a4851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15091996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f758beec9d4d9fe673091c953597affffbf9862ecd4a2fbb0aa11555cdea07`

```dockerfile
```

-	Layers:
	-	`sha256:1dd829fce21a120b087830e33d93e885593929eb97e3d3808600f398968a254e`  
		Last Modified: Tue, 04 Feb 2025 07:20:29 GMT  
		Size: 15.1 MB (15073706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64b29bd37255060c5ae387946306a79fae6b41546804ebd251dd592184c41f65`  
		Last Modified: Tue, 04 Feb 2025 07:20:29 GMT  
		Size: 18.3 KB (18290 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:2057e76e8788328e8dc8a751d3abc9dc9d20bd0b157df3847068a0f35dc82179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296756499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e51cb95cd8d8bbf242e0d4e58faae2f1615355bd80c314712d9a305bb7167e`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.1.tar.gz -o perl-5.40.1.tar.gz     && echo '02f8c45bb379ed0c3de7514fad48c714fd46be8f0b536bfd5320050165a1ee26 *perl-5.40.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.1.tar.gz -C /usr/src/perl     && rm perl-5.40.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.40.1" "-de0"]
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526075af1d9c0b728ff0e8888d46f79edd8fb9bacc975b1eb824b9bca2c06ee2`  
		Last Modified: Tue, 14 Jan 2025 21:56:34 GMT  
		Size: 167.5 MB (167525487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e4a92e71b155f8fe9896ed3812a2fd6d9e2029a8e82696c44717ec51f6680`  
		Last Modified: Wed, 15 Jan 2025 05:07:24 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad5d7ce205e61e4a423503e6c15da454f9d94d4f8c7af3f80cb757d2f02005`  
		Last Modified: Thu, 23 Jan 2025 02:18:30 GMT  
		Size: 14.9 MB (14891204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914be7b78c92e0a77e81a4b144b87f68c153a6b2b7fce01097271fcd156bb283`  
		Last Modified: Thu, 23 Jan 2025 02:18:29 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:194309429888766c6255ebe192215aef4ec04fdb7d1ffc22d453bc70a4028559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c2dfcf40b7ab8eb98eb7634a0da41048e6d9d513f91170c4dadf6f0e58de9c`

```dockerfile
```

-	Layers:
	-	`sha256:a16cd068ec938c298b4cc69c32e6510e88502c3206c61577e14d715cba235f9b`  
		Last Modified: Thu, 23 Jan 2025 02:18:29 GMT  
		Size: 14.9 MB (14874477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7aaca2e412eb4f8d70d6b2e3856954d28cc452460ff7850f893076c59351ac`  
		Last Modified: Thu, 23 Jan 2025 02:18:29 GMT  
		Size: 18.4 KB (18374 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:9177c6ae54ddd14556b617fd376457986875fd525f6262c7265f439ca5b215af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328373333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e68ec786d7eaae99af78e1f4778d91fd7e4c356cd24b9d261fc5e75e79027a`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.1.tar.gz -o perl-5.40.1.tar.gz     && echo '02f8c45bb379ed0c3de7514fad48c714fd46be8f0b536bfd5320050165a1ee26 *perl-5.40.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.1.tar.gz -C /usr/src/perl     && rm perl-5.40.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.40.1" "-de0"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5936a36467e76a2d54993295f16ff38dd2c24f30cf89a1f83a922f2440b869`  
		Last Modified: Tue, 14 Jan 2025 17:09:53 GMT  
		Size: 190.0 MB (189980217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4b9ab80f66e24837140e850189db5d516f8cdbd29428ef81e4bd9dd2b521ea`  
		Last Modified: Tue, 14 Jan 2025 21:29:37 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23896d61cc851ebd3b3ba1dec92a0118f84098ee5d9de4c4061221279be6751`  
		Last Modified: Wed, 22 Jan 2025 21:51:47 GMT  
		Size: 15.8 MB (15750095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7813c5e022381315972e1254a1f76dfea572d52f3c82b787b63dfaf05a886e69`  
		Last Modified: Wed, 22 Jan 2025 21:51:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c8b12189dbb4a61eba1ad86a461a89df0078b2e75e8662d2843080bf8989c7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15094364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfb3a71210f6d522db1695fa8aa5163261eaf3111758c8ee715d39902383276`

```dockerfile
```

-	Layers:
	-	`sha256:038a3986e0cffc61aedaf52fc27776af1e78eed2c6ceb2273d55035b9a2c426a`  
		Last Modified: Wed, 22 Jan 2025 21:51:47 GMT  
		Size: 15.1 MB (15075958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44188e45f5086c44258c8ed6d64b85081e1656e015aa461012855c2d9ffd9fe6`  
		Last Modified: Wed, 22 Jan 2025 21:51:46 GMT  
		Size: 18.4 KB (18406 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:1c638b1410665897997ea54ff766cc283e3dc7823d140dea2176b940b12c3152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.1 MB (342126325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535e1103a665ce1a99b539822bb1b7dd9704b7aee450f168cd642d174b490767`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.1.tar.gz -o perl-5.40.1.tar.gz     && echo '02f8c45bb379ed0c3de7514fad48c714fd46be8f0b536bfd5320050165a1ee26 *perl-5.40.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.1.tar.gz -C /usr/src/perl     && rm perl-5.40.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.40.1" "-de0"]
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 01:36:38 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 04:23:38 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4520e7fd9b17628990db3e961c2d7570421849af1fe255937c0a9e48cf49a48f`  
		Last Modified: Tue, 04 Feb 2025 05:15:33 GMT  
		Size: 56.0 MB (56029876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b370f45f01968d6de3175fc994cf545ece88435b9abc17f2ed4705ac128c8d4`  
		Last Modified: Tue, 04 Feb 2025 06:14:51 GMT  
		Size: 200.0 MB (199980423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbc7bcfd7942adb0b1be8084872453f54c036a2d467abf8f0e2662551acf29b`  
		Last Modified: Tue, 04 Feb 2025 07:20:58 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d257062a0490daa3b09a3a71357d1073ec612b77e8b5c9f41fe89819a5660b`  
		Last Modified: Tue, 04 Feb 2025 07:20:58 GMT  
		Size: 15.4 MB (15377750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fddf48c445cc8cb4c4611a36c6254d91762f1a52f930e7a2b6e6bbff49d2905`  
		Last Modified: Tue, 04 Feb 2025 07:20:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:0d92610bed7701bc951b1e3aa6075e65cec9cb978bdde23cb44e60f35a344d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15080284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6f6f50279d9fa6cb62bf8caed1487d21eee3a80043b00ffe890bdd883bf941`

```dockerfile
```

-	Layers:
	-	`sha256:f6fb45bf1135785418744ba03bd1545d6e5768a15fcc79f95c9b04c699a3374e`  
		Last Modified: Tue, 04 Feb 2025 07:20:58 GMT  
		Size: 15.1 MB (15062031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:976a339cc93a1e0e9e8fb8df62e7cdac634ff960c36741394e8c5fdeb2ae8c5f`  
		Last Modified: Tue, 04 Feb 2025 07:20:58 GMT  
		Size: 18.3 KB (18253 bytes)  
		MIME: application/vnd.in-toto+json
