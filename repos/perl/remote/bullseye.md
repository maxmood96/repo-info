## `perl:bullseye`

```console
$ docker pull perl@sha256:53c02d18764c6de6a3b709cdfa8aac87d3e0f6da480ca1a19a3fb2b646a22883
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

### `perl:bullseye` - linux; amd64

```console
$ docker pull perl@sha256:0b7d6732c328f068023a6ba82cf3cab66ee4e688d9f48eb6ae7c0d680e6ef1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337507772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd0a33117c73de71436c8650f5dc3b97a9a6f171bbeb31254a3f27b258a2514`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 05:00:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:12:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 06:12:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 07:17:27 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 07:21:33 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 07:21:33 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 07:21:33 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1210b2030df8684a29d3d6bdd62a8d151c73a23016c72c44011c839c8d24c516`  
		Last Modified: Wed, 22 Apr 2026 05:01:06 GMT  
		Size: 15.8 MB (15790675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ff843d7c842f57820ba127a5b3e0c2594fa7af32413d9bed6b12e4f5d03214`  
		Last Modified: Wed, 22 Apr 2026 05:12:17 GMT  
		Size: 54.8 MB (54760733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef54c4cd462cf7307ed3d2be8d877a54db3b7430a955e1ddcc641790dde70a2`  
		Last Modified: Wed, 22 Apr 2026 06:13:22 GMT  
		Size: 197.3 MB (197301898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485cb64c209f256a240689d96b68029391c5ea32af4fa89e05f8b41de07fa3ff`  
		Last Modified: Wed, 22 Apr 2026 07:21:53 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8b3e07e820e0f1c4f14813a7113cd69d0604826a591cf9eebf659e102e01a5`  
		Last Modified: Wed, 22 Apr 2026 07:21:54 GMT  
		Size: 15.9 MB (15891048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224f94055b8e4c0bc9e1bfcff83463966046d5604de4fa122db60ed6253e1505`  
		Last Modified: Wed, 22 Apr 2026 07:21:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:9b621d59f682d33dff234bc4a7f115283253e5bd208a43193cbf820f08cd2403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15491682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a1fc2ec9b3e5208cc9f36abc147e7ed1b742c89eda72cafdd6749001478935`

```dockerfile
```

-	Layers:
	-	`sha256:c287b7bfd5a70649fa318bf00142f6ae97f7ec27c7b2fabd5c8badd3e66b2edf`  
		Last Modified: Wed, 22 Apr 2026 07:21:54 GMT  
		Size: 15.5 MB (15473551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fcabb7af7cc571a63e39a0c638a42b45902fa05bc2443976222c7798fb0a11d`  
		Last Modified: Wed, 22 Apr 2026 07:21:53 GMT  
		Size: 18.1 KB (18131 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:afa92e2648e3d41fb73495dde19fb3f37b0068398c9f696b025e2198a29880f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297304680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b167284bbe0b274804494afb0612631202cd8133ff29ea81645ecba4f66d8480`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:15:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:21:40 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 05:26:46 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 05:26:46 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 05:26:46 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:b7f7b3cfb222580c94a933dbaaabd959ea960847c9aff9c5d4daa21494eea44d`  
		Last Modified: Wed, 22 Apr 2026 00:16:47 GMT  
		Size: 49.1 MB (49055006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2698f04c927addec960608562122b5f1c50ad262b50810e813b3046303555106`  
		Last Modified: Wed, 22 Apr 2026 02:18:42 GMT  
		Size: 14.9 MB (14905103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a451edd267f2ece592819d45854d958b47c98b8c4b25b1c98edd54f76d1bcc`  
		Last Modified: Wed, 22 Apr 2026 03:52:30 GMT  
		Size: 50.7 MB (50651590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954c2c739d513064642e14c7fa1d4873e1e96ff1538ad1bd0b4769a3ea4bccc7`  
		Last Modified: Wed, 22 Apr 2026 04:16:18 GMT  
		Size: 167.7 MB (167716786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09c436b6eaf4451346103feb3e398208e258757a73eb5f9fdf27dbaf9c5eb97`  
		Last Modified: Wed, 22 Apr 2026 05:27:05 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551ae7e576b2606fad180f821740b56e9bd7cfa377cf63656cce69cfae56722d`  
		Last Modified: Wed, 22 Apr 2026 05:27:06 GMT  
		Size: 15.0 MB (14975930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0024e049fcc1d00655abe6114f7d1b97c6dab334aa515d6d510968eea9566f38`  
		Last Modified: Wed, 22 Apr 2026 05:27:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:81c2073766ea8f80439ea7fa7ecca6373b09e9f0e4a36e30a1ee6e4906b2969a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1915792c2956ba5256b062aa1949be10fcee8699dfe6840e0436d2630a1fd83e`

```dockerfile
```

-	Layers:
	-	`sha256:e90a6485b1876580ab677208b96a9e3597afbd2daec5b756cbe7751fab325fd6`  
		Last Modified: Wed, 22 Apr 2026 05:27:06 GMT  
		Size: 15.3 MB (15272893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee36ab8b0545cbf04734fbc78e433ecc199a79535e4b5daa7e6ae1e1969a65c`  
		Last Modified: Wed, 22 Apr 2026 05:27:05 GMT  
		Size: 18.2 KB (18219 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:2ae978a960805e4f59325baad0ac77dc3b6285fd50bf0d1a27d90ee781e18b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.9 MB (328926111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068002b1f92deef32c8515364f65d10755a5846649d5b5fe5ffd3d762249946d`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:42:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:17:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:21:52 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 04:26:09 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 04:26:09 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 04:26:09 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8876687e9899211f85cbf406fe17625833ba27c454fedd4275ac8a0a58206e1d`  
		Last Modified: Wed, 22 Apr 2026 01:43:08 GMT  
		Size: 15.8 MB (15774737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41762a69c06632f02d051591b8561619178cda30090272dff52f65c2d6157695`  
		Last Modified: Wed, 22 Apr 2026 02:32:20 GMT  
		Size: 54.9 MB (54886521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba12cf159babc02fc1c9dadaf51e2fca9d51183009dbc801190af3b460b98dc`  
		Last Modified: Wed, 22 Apr 2026 03:17:52 GMT  
		Size: 190.2 MB (190190591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dbc43bfa2b76dcb9942177ea0db35f92df6574175b93dd403e574fd58eb350`  
		Last Modified: Wed, 22 Apr 2026 04:26:27 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7d4b0a6c11ea6212d77ac1008071d7600b30435f3e71e991075a536453ce0f`  
		Last Modified: Wed, 22 Apr 2026 04:26:27 GMT  
		Size: 15.8 MB (15820994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf1c622358aedf423b82628790e0e8e9d87da6b73a6b86923a465f719dfa18f`  
		Last Modified: Wed, 22 Apr 2026 04:26:27 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:02bb535cf86f1c3d6a03394fd0a119468f2c2be8f61ebbf1f7cd75aa943a68ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15493779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de337dad73c4055fdc2e58cbf2f87cdca72f043828a6000b2b7a3f26423f4d2f`

```dockerfile
```

-	Layers:
	-	`sha256:2ab8e2d15173d0e163ad60160d15f00bc8f0dd477c3101acea9a450933a2c798`  
		Last Modified: Wed, 22 Apr 2026 04:26:27 GMT  
		Size: 15.5 MB (15475532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:313677e507455ab7c52aa9ae91b1d09e91c8ffac978e10619f77443dd80b395a`  
		Last Modified: Wed, 22 Apr 2026 04:26:26 GMT  
		Size: 18.2 KB (18247 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bullseye` - linux; 386

```console
$ docker pull perl@sha256:b0047d9b839294d1b670c0785c5446c6ad7c28b68e86ca6aaca0c30048395923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342598777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92a5dbdfd12f0901470bb67edd6d519ff0b2d9020e29f90a79939649a4bbdab`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:42:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:02:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:20:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 09:11:46 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 09:16:07 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 09:16:07 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 09:16:07 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:737d996bc05c156425b11be5deec8366db5d7a009f49d85b480b1daec555cf4a`  
		Last Modified: Wed, 22 Apr 2026 00:16:40 GMT  
		Size: 54.7 MB (54705161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f313e1ea7e09266848088c3a09b07b715bfc6a8bb9980dc9b80da0fb20132694`  
		Last Modified: Wed, 22 Apr 2026 01:43:07 GMT  
		Size: 16.3 MB (16295616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae525ab0fbeb04dd4bb1d8468feefde68ce73f1bb5bc987c27f9283ecf43104`  
		Last Modified: Wed, 22 Apr 2026 05:02:53 GMT  
		Size: 56.1 MB (56060834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f654f3bca96d1c4170a39f9bcd55aa6b780c844f1780f920483ef6e6d9c71`  
		Last Modified: Wed, 22 Apr 2026 08:20:44 GMT  
		Size: 200.2 MB (200155364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a840c818c1a25fee8e56924dc72d235f1817ad35369bd07218c094baaa0be416`  
		Last Modified: Wed, 22 Apr 2026 09:16:25 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76ebb66d28a0895e1f31e6712899d7de4d86c4bcd5759a4e566f20838fa1c2f`  
		Last Modified: Wed, 22 Apr 2026 09:16:26 GMT  
		Size: 15.4 MB (15381535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e0a66e49a7ef742f7aedba8618d6c16f271a9fc38c1818bcc0b4f8149b8c71`  
		Last Modified: Wed, 22 Apr 2026 09:16:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:d3a3e55eacb2b5a7c1b23ab3c0a50816af7858e2607dae41f90854809dfd9828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15479645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fbd63f7e73e2ca500f3fac7e87b7c32e01572322c73d88db1bd3c3db55ea14`

```dockerfile
```

-	Layers:
	-	`sha256:8164e8192d6da92b94669e44a89b31ce85068f88660c60378921ecd065b63968`  
		Last Modified: Wed, 22 Apr 2026 09:16:26 GMT  
		Size: 15.5 MB (15461551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7452ed877dcbafa36e1929653a39c2bb1ad0b29b3684103acaed9be8c367d72`  
		Last Modified: Wed, 22 Apr 2026 09:16:25 GMT  
		Size: 18.1 KB (18094 bytes)  
		MIME: application/vnd.in-toto+json
