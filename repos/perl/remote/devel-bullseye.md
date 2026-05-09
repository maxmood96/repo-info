## `perl:devel-bullseye`

```console
$ docker pull perl@sha256:ee4fd73211f225d088f65688caad67a931089f327b5287987d7b3762c4f53b68
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
$ docker pull perl@sha256:f494fba9fb45f96d48eb26fb314650f610b1d3cc541af62eb2aade89c8c55af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.8 MB (337776379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f4d25965875ca270db3bb1ab8d1961e85c300ca59f96f4061ce6fc5698a4e0`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:40:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:20:16 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 22:33:58 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 22:33:58 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 22:33:58 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9888e096307133d2fbd60bcb00b491486db0aecbd10ad65207abf37059a9af`  
		Last Modified: Fri, 08 May 2026 19:40:30 GMT  
		Size: 15.8 MB (15790695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f960812f05fbc5416b446a8fd445ccdc345be2a630ee73fbe4b2644bb91848`  
		Last Modified: Fri, 08 May 2026 20:26:40 GMT  
		Size: 54.8 MB (54760810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeed64561784d1cd96dfd78f461b7eaf16af77b6bfca7c0caf1278729e02a05b`  
		Last Modified: Fri, 08 May 2026 21:17:48 GMT  
		Size: 197.3 MB (197309613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8cebbc7ddb20b9816aa50de1760c1d068493d26219579bef3264e33245942e`  
		Last Modified: Fri, 08 May 2026 22:25:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaa56307a9de9d487ac67285f57eb39814a46f49f798966c0c89001964b29fd`  
		Last Modified: Fri, 08 May 2026 22:34:16 GMT  
		Size: 16.2 MB (16151650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496cadc9a5147f14cda1af3454ddfc1083351d182830ec60f7d0c20cbd4b1f6`  
		Last Modified: Fri, 08 May 2026 22:34:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c367017f5e176728c9a1bff50745711af7a7f6ca8ee5024de454cd431d5d9d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446b034c03d29f95239043ec09ffaf9559c76340b5bc69fd269ed4b7dcf39e95`

```dockerfile
```

-	Layers:
	-	`sha256:4b68e78222ad3c8f52fddd9e369072b6ec193396def2dc70e938cf45d2c589c9`  
		Last Modified: Fri, 08 May 2026 22:34:16 GMT  
		Size: 15.5 MB (15473057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8a2127c1821b6fc4c404c09b6845c1bd5c74788893a5a4179df114fb2f3ea0`  
		Last Modified: Fri, 08 May 2026 22:34:15 GMT  
		Size: 17.6 KB (17606 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:8dbab71511151518e2047875874c4e9dafd67b75f2dbef598df327b350f1f992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297556393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b795bc1dffba67a97101760ade75c0e218f9b74b5dd06e24472e54427ccdb623`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:34:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:14:16 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 23:19:27 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 23:19:27 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 23:19:27 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:4cb33fa51e00f2c5cad3e12a59f701c1cb73526295425e2f64b4cb13b9375c4f`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 49.1 MB (49055106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba52e9af1266c17416a17c315f698fb07fc71701dcf95b70a57e9d0f65c70ea`  
		Last Modified: Fri, 08 May 2026 19:44:47 GMT  
		Size: 14.9 MB (14905070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd446ccde0d71af76f958e25aea6b705f55351a4c8727e3397b0e759244004a`  
		Last Modified: Fri, 08 May 2026 21:35:04 GMT  
		Size: 50.7 MB (50651505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f862bea187cb46c212aa6da5f355ebf4c26db2ef51b6fb3a6bdafc2d503f34`  
		Last Modified: Fri, 08 May 2026 22:13:23 GMT  
		Size: 167.7 MB (167716002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4caae19fca617650b6e2db0a593d0bee93620ed57855d676be413b0b400c22`  
		Last Modified: Fri, 08 May 2026 23:19:55 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62580de28e6854fe28cd8f505cebe0b76c8b248c961ecfb1732ce8c62594bbd`  
		Last Modified: Fri, 08 May 2026 23:19:56 GMT  
		Size: 15.2 MB (15228442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d970f610ee4f815e06210b0898e665f4bd0ddb53a84a3d5a5cc74a26fe68668f`  
		Last Modified: Fri, 08 May 2026 23:19:55 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:2defea8c8ae1f9a69f0a059e1b478fb510a981393d4554e0ef3d83f60f11dcd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15290060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5dedbde76fe18bf91fbefb7604734ffc00321fa620e4628cea12adb9aaa844`

```dockerfile
```

-	Layers:
	-	`sha256:cce0655aa4a528f2dca8206df8380f213292232667e857dbb99422633a557242`  
		Last Modified: Fri, 08 May 2026 23:19:56 GMT  
		Size: 15.3 MB (15272383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd1970aa8d3d6817d1f76d25bfa4f967ab0af49191fceff6a9a1630a26f1e1a7`  
		Last Modified: Fri, 08 May 2026 23:19:55 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:1669dbaef11ab7b86b4fafc7b648abc7cdd06d7254db4b68e46dca7f3a1795f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.2 MB (329198219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c4e6f6211585d9a9af518a99b0cf9e298fb14df2620db365b2a3c6269fbf29`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:42:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:18:57 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 22:33:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 22:33:00 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 22:33:00 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d20a72a3ae72af0f6239652b45dcc6f5eda87bb797e4c05972c586c32afca3f`  
		Last Modified: Fri, 08 May 2026 19:42:32 GMT  
		Size: 15.8 MB (15774834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de92af39e07f00fd21cc384e0f5108a74acadedc0acecf16d700d606eedccd3`  
		Last Modified: Fri, 08 May 2026 20:32:13 GMT  
		Size: 54.9 MB (54886410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc943fbfcf4513ea392f60742ca835596dbac2f1542abbf52e3b28b25333c14`  
		Last Modified: Fri, 08 May 2026 21:17:50 GMT  
		Size: 190.2 MB (190208547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658aacb65c0523d6c4c84d1d6f9e51bdb74a031eef2c1dfa340716489762f98`  
		Last Modified: Fri, 08 May 2026 22:23:39 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917510528f61b2ba206befce338c7fba83ef4f2afdda2c0b678d40bd39238a12`  
		Last Modified: Fri, 08 May 2026 22:33:19 GMT  
		Size: 16.1 MB (16074950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d299815040928ca0164c5f975b09984ce4e2cf5000e75d8a9e9707008da59217`  
		Last Modified: Fri, 08 May 2026 22:33:18 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:0416db47d2145324b46ee97fa26c9c90216bb18b05edb4b13918e4bf61d1e96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15492711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7da21a1efb8a7ae22c4e3e98b17c2e469e15c2d8f5d225db236754dc1eb0e59`

```dockerfile
```

-	Layers:
	-	`sha256:e74cb002f9eb628f2899a2f18613712f9133e5d6003b11807c173276ad2836d2`  
		Last Modified: Fri, 08 May 2026 22:33:18 GMT  
		Size: 15.5 MB (15475014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:934a27f181a7884aee6bd64110e94c3565bf9cdc0d49ad93da601f3c7f3013e7`  
		Last Modified: Fri, 08 May 2026 22:33:18 GMT  
		Size: 17.7 KB (17697 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; 386

```console
$ docker pull perl@sha256:388153cf1f700391a993bebd01229632986f1172726fd626ef9f8011b8ff5430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.9 MB (342860376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b202232254e49aaa87d7015ffc793878b013e04c8f2e69b29bdd2eebb7bf8b`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:43:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 02:26:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 03:20:30 GMT
WORKDIR /usr/src/perl
# Sat, 09 May 2026 03:25:13 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 09 May 2026 03:25:13 GMT
WORKDIR /usr/src/app
# Sat, 09 May 2026 03:25:13 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:caf67df8e858ea1242ba8175484d5f733d658c733fcfe8f173a3140308e3ffa5`  
		Last Modified: Fri, 08 May 2026 18:30:59 GMT  
		Size: 54.7 MB (54705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bebb3bb20b05d30c1a5354688795bd554c50c12bfa7e9190aa4a54c7dce2a8`  
		Last Modified: Fri, 08 May 2026 19:43:41 GMT  
		Size: 16.3 MB (16295597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5882cc2f0705ce8b109017f0de582bdb1d4e67ec5740dba7f8635d30c4b832c6`  
		Last Modified: Fri, 08 May 2026 23:05:02 GMT  
		Size: 56.1 MB (56061157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7226b1417fe6d33d44e75557d981eaed1351a54abf2e427ded180dbac85c616`  
		Last Modified: Sat, 09 May 2026 02:26:58 GMT  
		Size: 200.2 MB (200154443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95763679d93a46113fd0f4699547e3b81c2ae8ba4e449596d06be1fe72621c31`  
		Last Modified: Sat, 09 May 2026 03:25:29 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ad02d96626de685e99ea2f1fdd174d013afa87f501cb0bb5db5ed6e2dacaa2`  
		Last Modified: Sat, 09 May 2026 03:25:29 GMT  
		Size: 15.6 MB (15643567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b634b0bee036251c83b9ab90f510e4643e35c7e567997d58546aedecac1b7f3`  
		Last Modified: Sat, 09 May 2026 03:25:29 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:51fbb782f95234281b50a695e203315130754435d5c2d071842147bae7697267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15478645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8eb6e86fb5d37191f3099f6bfe71b474bab125a4326baa37f827cd58b398f65`

```dockerfile
```

-	Layers:
	-	`sha256:38903be6e3ea11a81432fb7e5b4b7b2b745ff1378a9c2a4bfec03f3e479fd625`  
		Last Modified: Sat, 09 May 2026 03:25:29 GMT  
		Size: 15.5 MB (15461067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58921f35589869c9dc664d8eb3308bb162d43eef9377bfbeebc91be57872ed9`  
		Last Modified: Sat, 09 May 2026 03:25:29 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json
