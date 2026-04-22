## `perl:trixie`

```console
$ docker pull perl@sha256:a3135bdde85c868a77180b01f9754b1979b59ef1941f6975f8f5dfcf52f80520
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

### `perl:trixie` - linux; amd64

```console
$ docker pull perl@sha256:fc04eee20b9b35e45440fe3d66727ed9e02e00b97855051675513a8ddbeec49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.7 MB (394702159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efbf0457c8c1a04a08f2cdaeed7172411a76e97eb153ca9e2a5a8be156e58eae`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:13:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 06:19:33 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 06:23:45 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 06:23:45 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 06:23:45 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f93954cfe1451f4333422086d00bd066cf33f42112b531804ffe06f0a929`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 25.6 MB (25622443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d12c8f3f3fbb5bd2b8369adf3213e09d6b33f975462543ddfece85b2fe85e5`  
		Last Modified: Wed, 22 Apr 2026 04:45:50 GMT  
		Size: 67.8 MB (67790089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1bb20756a85e159dfb7908a2a5c860ac2f2254254a915d8c047e02cb2b0259`  
		Last Modified: Wed, 22 Apr 2026 05:14:09 GMT  
		Size: 236.1 MB (236074811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e5b8be477fddae10c36fe7c86a6cbcf4b5ea6c43e5779299fb72b2089a644a`  
		Last Modified: Wed, 22 Apr 2026 06:24:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38184837014bbb53c1d206b8c6517e832ef3c8b9d1016dd8c90ba36d5847a5e2`  
		Last Modified: Wed, 22 Apr 2026 06:24:09 GMT  
		Size: 15.9 MB (15912447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21a26da59181741a74128f94278aa3d58ed5026690d27096ff871e6aedb060e`  
		Last Modified: Wed, 22 Apr 2026 06:24:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:trixie` - unknown; unknown

```console
$ docker pull perl@sha256:203ba3a8d8145f7d23ff55202d1cb01af36875ffa2c4760f1654faa8e2edf8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17231597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f94b588de14a0d490914d31ccf51aa1988d82dcb2d94265b32d7655b643cd67`

```dockerfile
```

-	Layers:
	-	`sha256:b38c0369111ee69dfb07fba9795786b67dfc8a44bfe3a23781c92ab0287217db`  
		Last Modified: Wed, 22 Apr 2026 06:24:09 GMT  
		Size: 17.2 MB (17212040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:893f4490440a9dbeddf09971bb6526d28afe96dfeef4a42a4d3804429dded89d`  
		Last Modified: Wed, 22 Apr 2026 06:24:08 GMT  
		Size: 19.6 KB (19557 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:trixie` - linux; arm variant v5

```console
$ docker pull perl@sha256:23aa2173ffede18a92ff5d521f096c14de56ca4c9d02e914c5fcba4b0e6bad0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358180814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc869a4dd5fee005ff8b768a728f1d3767375e85b451687fb11e2afbf9374e8`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:17:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:08:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:14:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 06:19:55 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 06:25:14 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 06:25:14 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 06:25:14 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:2a20d1d425bc7f9412bd28183d8c6af38f835b7563f035cf6476381816d73dd3`  
		Last Modified: Wed, 22 Apr 2026 00:16:22 GMT  
		Size: 47.5 MB (47466106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850bd1c760e36c64cea860128e609cb23ecd251d01c38d67fa6179d5cca0da73`  
		Last Modified: Wed, 22 Apr 2026 02:17:34 GMT  
		Size: 24.4 MB (24363601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ba959356b2294f9c3156bf888a9b762bdd922efa57422268742976c4c2656b`  
		Last Modified: Wed, 22 Apr 2026 04:09:07 GMT  
		Size: 65.3 MB (65324567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f8cb5cdebca7286fe39255749ea619a9ca772b211e66a28194a1d29bc920e9`  
		Last Modified: Wed, 22 Apr 2026 05:15:22 GMT  
		Size: 205.8 MB (205793031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9572ba0941ac9bfd76ab8e64438a9e902ed03ef90c0cd4a0ac3ff5d5e9eba0d`  
		Last Modified: Wed, 22 Apr 2026 06:25:33 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a1b328a70198c593ee3fa98bcd2383f78f62c114494aee2dee2ea2769fd178`  
		Last Modified: Wed, 22 Apr 2026 06:25:34 GMT  
		Size: 15.2 MB (15233243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b66a9472384f1233b3c3582a0d8cde3e80ad4e71e678cb222f72fd9cef85340`  
		Last Modified: Wed, 22 Apr 2026 06:25:33 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:trixie` - unknown; unknown

```console
$ docker pull perl@sha256:c810b2d1638be6f1b034ca9b469509f710d2c6ba9605d684a6095145ca6cc279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5d6f16fc0fe79164f72e4414be47e026380e3e68f0d2ac1e300241665ca760`

```dockerfile
```

-	Layers:
	-	`sha256:190362bb6ac7965da7f99f68249428ee4a83aa343acad0b5e9b2542a43e31241`  
		Last Modified: Wed, 22 Apr 2026 06:25:34 GMT  
		Size: 17.0 MB (16974294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3d056f0154942307003ebee58b8fc410623734a8ffd81f73f0a24bee3bb6fe`  
		Last Modified: Wed, 22 Apr 2026 06:25:33 GMT  
		Size: 19.7 KB (19685 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:trixie` - linux; arm variant v7

```console
$ docker pull perl@sha256:72fca360efe1767714f9e6e55268156516dd52ad0f2dc5d21a9e6c9fb7fa29d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340528955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614e76f5e5f1d27d5dba20b8763e7de88701d927bce8e53c66b387f3b6334cd`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:52:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:16:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:21:18 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 05:26:25 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 05:26:25 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 05:26:25 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:cc74239df6a59971739f1b7a0758f97ae57e6ab4f74daa64d264ec77db24169f`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 45.7 MB (45738193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f411318175ae51ff20f60969311f63c366288f8aad04eda4d0389d8b016c9`  
		Last Modified: Wed, 22 Apr 2026 02:19:59 GMT  
		Size: 23.6 MB (23636616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341da7892f7aceb1342cb554bdaf16f78292d5247e1ef9fb0f351c24aadb1f0b`  
		Last Modified: Wed, 22 Apr 2026 03:52:40 GMT  
		Size: 62.7 MB (62721455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ab603b07acf826bbac9a62308beed40392f03d30c6911af4cf6fde3264b31d`  
		Last Modified: Wed, 22 Apr 2026 04:16:39 GMT  
		Size: 193.4 MB (193387724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf472d47df0b8479f822f1d36add1a6ccb5bcc7f4de61e21500379a674de63b`  
		Last Modified: Wed, 22 Apr 2026 05:26:46 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa9705ef0370a01e0340d607fd3155708b853cdcf94f77c24d1e75a159e11f2`  
		Last Modified: Wed, 22 Apr 2026 05:26:47 GMT  
		Size: 15.0 MB (15044702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e2392062621098655dc04298b91e4d3c50c0f84c94584d2b5d30233ad175b8`  
		Last Modified: Wed, 22 Apr 2026 05:26:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:trixie` - unknown; unknown

```console
$ docker pull perl@sha256:8d2c0ba7d940055afe6de1df963e0619b41395e8149808f884d02049dff1b3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16999769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8a6e987b4e478f56777b38222e864b8b56edab7f6027b688be7ea8a67ad8dc`

```dockerfile
```

-	Layers:
	-	`sha256:759f6c8b4acbb657dd53510be6950d5243c6e3077b94e4825ae617bc677ea495`  
		Last Modified: Wed, 22 Apr 2026 05:26:47 GMT  
		Size: 17.0 MB (16980084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac5e8fb396d8c2710e09bdb037f5f11feda7efb1f845e34f37b4f5995005fdb`  
		Last Modified: Wed, 22 Apr 2026 05:26:46 GMT  
		Size: 19.7 KB (19685 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:trixie` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:4e20951997399b8699771f901f5ff00d00626f90e107ef646e579d53f08c412b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384353228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55432ce22b3a6a205f41803783aff3b63545e812437975e7a193b0f7ebb7f0ca`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:17:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:21:38 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 04:26:11 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 04:26:11 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 04:26:11 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f67984ab3d0b84dba0bf1b9e75bc42547713ab962aa5b392bacb0e61fa68b`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 25.0 MB (25023409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c17e454c787ef19107fbea0250c33a4b6ca95fe0319ad68539a7bae9d9cad57`  
		Last Modified: Wed, 22 Apr 2026 02:32:52 GMT  
		Size: 67.6 MB (67584735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5461f2dc96dbc8b34faf5c31d5312e44d27b85e81fffef565438663f34f538`  
		Last Modified: Wed, 22 Apr 2026 03:18:16 GMT  
		Size: 226.2 MB (226209559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab089875866ee7eca2bfb18d5f03919681cb3b3ffa1e766884f42bd1c792091b`  
		Last Modified: Wed, 22 Apr 2026 04:26:32 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6316ce31b712ad17eb9649ced638f3da65d55109f42a1816f9cdd0b758b67cec`  
		Last Modified: Wed, 22 Apr 2026 04:26:32 GMT  
		Size: 15.9 MB (15866013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b72bc08d2fd1115648794452ca36a938ee237021723e04bf84e0c3ba5e9e3eb`  
		Last Modified: Wed, 22 Apr 2026 04:26:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:trixie` - unknown; unknown

```console
$ docker pull perl@sha256:8cac76172334075946ec4c329cc4fe6aa5d183bb54ac11e8fd5fe65bf6b15372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17316151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f60217a1b815cac8433759088c50d5817a1f08a50f83e699d135711b45d88c6`

```dockerfile
```

-	Layers:
	-	`sha256:80b4e02513cf2537609d832a2acfe877312284cab75807d7f1fb2a86512b0fb5`  
		Last Modified: Wed, 22 Apr 2026 04:26:32 GMT  
		Size: 17.3 MB (17296418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06f16a8b1c81849615cbb74c5aa6e85ff287b5da592203922523dfbc83e9125f`  
		Last Modified: Wed, 22 Apr 2026 04:26:31 GMT  
		Size: 19.7 KB (19733 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:trixie` - linux; ppc64le

```console
$ docker pull perl@sha256:501c42860ed0e0a7b3caa7edac5d634fd928cbbe2846aa60dd8ed27771db27ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.3 MB (400274218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71bdadca11af69015455e4e0dd85a488e4ac3288bc4eb94ab72bf8ba35377d0`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:40:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 09:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 12:17:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 16:29:06 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 16:36:41 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 16:36:41 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 16:36:41 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2454d511c21492888baf49902a298f334e8095ce0fe93b53b274ab3f39febd31`  
		Last Modified: Wed, 22 Apr 2026 03:40:51 GMT  
		Size: 27.0 MB (27014616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f9e1a80821bce13187cd275a074ab44791a07c4796e61afbcda3a692b97ac4`  
		Last Modified: Wed, 22 Apr 2026 09:39:58 GMT  
		Size: 73.0 MB (73039689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee24d1527042fdf5416c0f176e46ee07a4162716bc3c579e21e2b5b37cf0dc3`  
		Last Modified: Wed, 22 Apr 2026 12:18:28 GMT  
		Size: 231.2 MB (231209822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19404befc9815eae9c2365be7c9d31bd24655ff639e0e8fea5c4488851b28986`  
		Last Modified: Wed, 22 Apr 2026 16:37:25 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f688fea26eb87d1771874f1d0e07837e812999191ebc08b1ae9f39b6e32d0`  
		Last Modified: Wed, 22 Apr 2026 16:37:27 GMT  
		Size: 15.9 MB (15886841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccb9628fafc8d803d3d54d65849779b81da066bb81726e40e467a21f1a1c3d1`  
		Last Modified: Wed, 22 Apr 2026 16:37:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:trixie` - unknown; unknown

```console
$ docker pull perl@sha256:655c0e1a4a4bdeef37bc4ea3f9c2aa09f3868067d1294ed123db12b344b9edbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17217270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742c434c8ac5820879df0799f32155bfed1a684a57a7b7956a6f62834da95066`

```dockerfile
```

-	Layers:
	-	`sha256:0a1144a2bf450660d396675f7c0eedde67f918d6bd4460bc493e0dc59e7235b0`  
		Last Modified: Wed, 22 Apr 2026 16:37:26 GMT  
		Size: 17.2 MB (17197633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d794054fbe94136e3418ace7db71c3cb7f7f7980dde8cbb0c5179926dc62367`  
		Last Modified: Wed, 22 Apr 2026 16:37:25 GMT  
		Size: 19.6 KB (19637 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:trixie` - linux; riscv64

```console
$ docker pull perl@sha256:2960e6e3b4fe6d3b74ffd1e62339fc41c018f9e93d8902ae0d3980b414ef8200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.0 MB (480988290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672eacee770837fb6efd7e4e68cbaae9b5071529c9408a23bc6994d5bc657ed4`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Wed, 08 Apr 2026 00:44:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 02:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 09:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 13 Apr 2026 03:18:32 GMT
WORKDIR /usr/src/perl
# Mon, 13 Apr 2026 04:24:59 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 13 Apr 2026 04:24:59 GMT
WORKDIR /usr/src/app
# Mon, 13 Apr 2026 04:24:59 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b086e95c6ca0165102a5ceced9274da65d6d9a865b88c14f181ecba94652bd75`  
		Last Modified: Wed, 08 Apr 2026 00:46:07 GMT  
		Size: 28.1 MB (28118765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacec47fc648b6d60a98d7ff6fd4e23039ac63553f44613cd15e968e674616e6`  
		Last Modified: Sat, 11 Apr 2026 03:02:36 GMT  
		Size: 66.7 MB (66662977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200a11642b21f83b32d7a1e5b3d3152a43e4108b937c8957932be9a3bd5c5cc8`  
		Last Modified: Sun, 12 Apr 2026 09:17:59 GMT  
		Size: 323.0 MB (323031820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170404f38d42ec5079ff76a52644c029ff2eaf90e941706ba995ccb7c0e74a86`  
		Last Modified: Mon, 13 Apr 2026 04:32:52 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1246c86b6fa3cc1689cb29d06b0675c8e5efa3a4e856e990827e39f79a3eb6`  
		Last Modified: Mon, 13 Apr 2026 04:32:56 GMT  
		Size: 15.4 MB (15381835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26163a972894951738709dcc407e402b8d1c27a94e7957f8128ba7d1b5af7947`  
		Last Modified: Mon, 13 Apr 2026 04:32:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:trixie` - unknown; unknown

```console
$ docker pull perl@sha256:4e1cdc388b4a9de04219427b977e27e21928bce6a47746227bdb340505a2a77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17287805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27f593f89d9d8288c05ffda6940301e1042ba451cb9f42c554e1d888b406c9a`

```dockerfile
```

-	Layers:
	-	`sha256:594e6777ec8877843119dbf3f2c8149fbf3850ac543701de3ec107c2e49e6403`  
		Last Modified: Mon, 13 Apr 2026 04:32:56 GMT  
		Size: 17.3 MB (17268168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df35082c0d44fdf5280a9a4bcf0fe5f4a6a791f22797cd017238f494a26e9c01`  
		Last Modified: Mon, 13 Apr 2026 04:32:52 GMT  
		Size: 19.6 KB (19637 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:trixie` - linux; s390x

```console
$ docker pull perl@sha256:2654587415da4c1026c4ac24ccde4f02166d1c40a8ae3b3ff3b89133cdde4e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.9 MB (367890123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c393b552f2f48c70390ac949337405c6437dc29bfd8b4265757d508c5e45ea`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:21:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:13:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 08:16:55 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 08:24:35 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 08:24:35 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 08:24:35 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c2a3da428dd91e4b5df556514e279e6a571eec116b1f2b3ed1bc95489fcee4`  
		Last Modified: Wed, 22 Apr 2026 02:32:51 GMT  
		Size: 26.8 MB (26802425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c81397603fbb04688ca83ea8697469c3a01388a59e003d38dd37d22beb13789`  
		Last Modified: Wed, 22 Apr 2026 04:21:39 GMT  
		Size: 68.6 MB (68636900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9797d445faaa1f9219c6d6ae09f17025e8f5995b4cec1bfc6cac2d3adf9581a2`  
		Last Modified: Wed, 22 Apr 2026 05:14:44 GMT  
		Size: 206.6 MB (206602552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656e4f0e94fcff0c1dc29ebe5d4d9a3a3924e906782d01ac5e340ba226160c09`  
		Last Modified: Wed, 22 Apr 2026 08:25:17 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443a958ed8352c4e2cac870f5e0518b0f61d6cfbce2764eb78df985bd88b7ad2`  
		Last Modified: Wed, 22 Apr 2026 08:25:18 GMT  
		Size: 16.5 MB (16475873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7c3fed7daf05a20b974c02f03c7a9d136eda50bf91a2f8255b95f02b346959`  
		Last Modified: Wed, 22 Apr 2026 08:25:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:trixie` - unknown; unknown

```console
$ docker pull perl@sha256:8d1c72e358e8347fbfed325b3848301d94b0e434673f6802a86ca4f216c77588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17008830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f5155a370c89ae2a3b781172ef41b03ef2374668353161c01438bf226677b2`

```dockerfile
```

-	Layers:
	-	`sha256:bda45e30c997897c52e8c87562dc242cb173f35d7e8a660a238a46dcd70103cd`  
		Last Modified: Wed, 22 Apr 2026 08:25:18 GMT  
		Size: 17.0 MB (16989273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be376e580ddd261172414728585ef12310ac98ed820e800452839b429884c57a`  
		Last Modified: Wed, 22 Apr 2026 08:25:17 GMT  
		Size: 19.6 KB (19557 bytes)  
		MIME: application/vnd.in-toto+json
