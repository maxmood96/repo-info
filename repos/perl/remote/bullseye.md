## `perl:bullseye`

```console
$ docker pull perl@sha256:5a653fef42e859d0cf263d44f5ebec0721e492ed25d72ba67b43195dc271ae41
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
$ docker pull perl@sha256:cfeb940b07e908563beddb60e3f86178a339fef82388cafe344756afb74ee6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337515776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091c5c84503ee783854f61d7f09e51799c9ac32ae5e7b23c6679f6a539256d9b`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:40:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:20:10 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 22:24:09 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 22:24:09 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 22:24:09 GMT
CMD ["perl5.42.2" "-de0"]
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
	-	`sha256:6f73aee9b41ada94ba02c14f743b9d586c95f95094de8c37b446d20644ca173e`  
		Last Modified: Fri, 08 May 2026 22:24:25 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0cec7f4a868b1453f549fc71eda50d37c7e77e9fc95eb7f8f8fd23268cfcf4`  
		Last Modified: Fri, 08 May 2026 22:24:26 GMT  
		Size: 15.9 MB (15891046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59f3eef40016e49fcd5a9ba8b8448971c2968e3ac9d22400dd9443e2bd03f20`  
		Last Modified: Fri, 08 May 2026 22:24:25 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:06cd7b159fcc4cff0ba0cb683c0bd21385dff9ea639fda991a9f05a517531cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15491790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dcc9de7417f879d5ea3ef904d464cda1fe14af59ea8ee0a8e029b42ef5b15c0`

```dockerfile
```

-	Layers:
	-	`sha256:80987d76ed4958364c9a6cc36b7c5a9a9d71a4c75d18cda9e0eb2f28ca05af53`  
		Last Modified: Fri, 08 May 2026 22:24:25 GMT  
		Size: 15.5 MB (15473659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0451a76d704db7b34727ef29b020cf9ce14f6715ac1f50a1d205e3a339a2296d`  
		Last Modified: Fri, 08 May 2026 22:24:25 GMT  
		Size: 18.1 KB (18131 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:e49957e8f71516a5a06f6c97352789661b4fd5826048aed106b813315c14865c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297303978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d86489892877500531cf830c7ced989c112bcb95c1b7d7a81070959ad3dc0a`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:34:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:01:44 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 23:06:54 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 23:06:54 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 23:06:54 GMT
CMD ["perl5.42.2" "-de0"]
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
	-	`sha256:0af2db3b2fbc5d4c2205e8018f7ae267f9e01a0fc964f7c55076700af360a334`  
		Last Modified: Fri, 08 May 2026 23:07:14 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdace185f48a96dc38ae84f48d4c0d5c66292f70b109da99b23b1722939e2f0`  
		Last Modified: Fri, 08 May 2026 23:07:15 GMT  
		Size: 15.0 MB (14976026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991ad2108315e2f75579eb554f3bbb37e39a6033862fc59ec68ae9c710b77241`  
		Last Modified: Fri, 08 May 2026 23:07:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:dafd21bcb51d38c3bc0c63bb9d6f28a379127f59d0d8010f05631b808de2768f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc59f0a287897fa596cd24b301e79fa8127b3437e03917ab0e2082afb25196f`

```dockerfile
```

-	Layers:
	-	`sha256:d8865e64f88c86955b8d2fb6f04ad1bd70ee05d836d9fd53a2161c04ab0aae14`  
		Last Modified: Fri, 08 May 2026 23:07:15 GMT  
		Size: 15.3 MB (15273001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d052734b8f8096f68d4e47e93ea96f49decbf053b19e775b4a79706a2a1454`  
		Last Modified: Fri, 08 May 2026 23:07:14 GMT  
		Size: 18.2 KB (18219 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:484b1cdfb05f319914b03e6c446a5bae97058a719f0f10827115c7cd9c73a577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.9 MB (328944203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09e5ccd53ff0434695425f9df36753481906413120ef331038b22f71902dbd5`
-	Default Command: `["perl5.42.2","-de0"]`

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
# Fri, 08 May 2026 22:23:18 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 22:23:18 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 22:23:18 GMT
CMD ["perl5.42.2" "-de0"]
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
	-	`sha256:bf1a1f1003f37da4230542761fea8648125e30c32fa5daed31a741abf5425e8a`  
		Last Modified: Fri, 08 May 2026 22:23:40 GMT  
		Size: 15.8 MB (15820934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26196b8bb158c6007626639766adb9ae1363519fc3600d318eacc4b5bd671d2`  
		Last Modified: Fri, 08 May 2026 22:23:39 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b8fe531c6a06c885941cbaa35335ef27a97976fa5f4e07eb5c0778436f2710dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15493887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a60e6afe946278e01b7a54bc9f5758d778954e96eb21a21a3955a11f130d7d`

```dockerfile
```

-	Layers:
	-	`sha256:c129e2eaf7b9a54ef81898b2eef73afc0b264026fad4e7b40042e0d56c09baca`  
		Last Modified: Fri, 08 May 2026 22:23:39 GMT  
		Size: 15.5 MB (15475640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3943683cea3b5ae30d0fdf2cb2c2b033b42e4398c16ca06ae99f91989132f7e3`  
		Last Modified: Fri, 08 May 2026 22:23:39 GMT  
		Size: 18.2 KB (18247 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bullseye` - linux; 386

```console
$ docker pull perl@sha256:fba54cebd9c4b8af442f04b3fc60e0442342d26fc8e9f3392176c2d088ca3269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342598515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ad2de057f9ee3e50599d90c1869e1ed6423ba24788aacff72ea0adba55b9c5`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:43:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 02:26:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 03:12:41 GMT
WORKDIR /usr/src/perl
# Sat, 09 May 2026 03:16:56 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 09 May 2026 03:16:57 GMT
WORKDIR /usr/src/app
# Sat, 09 May 2026 03:16:57 GMT
CMD ["perl5.42.2" "-de0"]
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
	-	`sha256:94edc3239e5529815d70e2f26b9fb84dc00f3ddb1445c2e5d88a63ea53510543`  
		Last Modified: Sat, 09 May 2026 03:17:15 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765d6dc6165b6fd8ca25c3c540e0f3418148b576cfff9b05e8481c9c208ceede`  
		Last Modified: Sat, 09 May 2026 03:17:15 GMT  
		Size: 15.4 MB (15381706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce2d3a80515707fcfd7d970fbca6ad66af8ebb490ec9397963004a89c5a21d8`  
		Last Modified: Sat, 09 May 2026 03:17:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b4b8b1ca6cc219712f39f9eacf97c9f1193ddb9ab4b18bc8b93c016b83648d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15479753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095464df383354129e74f12c419c92405f79565c3a70a2b6ce2c671c4cfb96ce`

```dockerfile
```

-	Layers:
	-	`sha256:551bf9aeb1ff5458b73ab59ba6a47ea627bea642c507a7cf98ab6790b5f3622c`  
		Last Modified: Sat, 09 May 2026 03:17:15 GMT  
		Size: 15.5 MB (15461659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c9556a2e634738a1a2c7f93cf67389a551806f62c86c1c63df9b7d195fc6a5`  
		Last Modified: Sat, 09 May 2026 03:17:14 GMT  
		Size: 18.1 KB (18094 bytes)  
		MIME: application/vnd.in-toto+json
