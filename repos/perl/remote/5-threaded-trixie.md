## `perl:5-threaded-trixie`

```console
$ docker pull perl@sha256:867cf66eac093cac3da2c988818a84a958c41a142e4556ca1f04bfd58b13a0f8
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

### `perl:5-threaded-trixie` - linux; amd64

```console
$ docker pull perl@sha256:7898974cb9542d63984a21b870d80e37d70114308289431059e6a9a154d5b312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.8 MB (394761087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b84547cf87476dffe82467e36e68c009ea6d3f28b4b8e59a3cb008c3b0a8a34`
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
# Wed, 22 Apr 2026 06:19:36 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 06:23:50 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 06:23:50 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 06:23:50 GMT
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
	-	`sha256:d5290c2c7a940ec916da64b2393cbff55cdf42f0ce860c5fed8c4af985ba07d9`  
		Last Modified: Wed, 22 Apr 2026 06:24:08 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5083ce753d6e30c0377fd94adeae25e50f1c4c9d1e2bc07bfc35321f1a5ef020`  
		Last Modified: Wed, 22 Apr 2026 06:24:09 GMT  
		Size: 16.0 MB (15971377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f531b9647fb13e26a0dfafe7f248add0bf6ed382045bbaa0c29943f0117ab614`  
		Last Modified: Wed, 22 Apr 2026 06:24:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:c1e5f8a414acfbb0347c23c4805b459448714434f7e9dc203dfe9ae45177e765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17231980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d40b17ee88a3654890b87d51e1d515df9c7430483978cb61de5aefeb537657`

```dockerfile
```

-	Layers:
	-	`sha256:b2e7ff82d5f9fdee15713fcb82f900b2902b8c0527500ab3246e4f89e197eae0`  
		Last Modified: Wed, 22 Apr 2026 06:24:09 GMT  
		Size: 17.2 MB (17212206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b2d7809dc4d8f9672638cfefe0f0bf06a6dd4c4a302c457156b877d1c30d5e5`  
		Last Modified: Wed, 22 Apr 2026 06:24:08 GMT  
		Size: 19.8 KB (19774 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-trixie` - linux; arm variant v5

```console
$ docker pull perl@sha256:9b42a96bb87c1c42eac0d0dee8b789e1225b0ce68871103f149f3ca2d9d1bc35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358198800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e805c0816fb1717203b11e6f08acd4b48866937d02ccb257876677b251d02dd`
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
# Wed, 22 Apr 2026 06:21:17 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 06:27:03 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 06:27:03 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 06:27:03 GMT
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
	-	`sha256:431cf3866262285948b54813cb8dc39dc955ac29edf565998c9528a71d3b2bfd`  
		Last Modified: Wed, 22 Apr 2026 06:27:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be158e12c44d8a8d3ba74373f67cde0873fe750211ac2bf1936d3ac9cbb8cdb0`  
		Last Modified: Wed, 22 Apr 2026 06:27:26 GMT  
		Size: 15.3 MB (15251228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1cb52c0ecd54d69e2e9a9c1f6b575d63838c18669d367844b4c611176aa93a`  
		Last Modified: Wed, 22 Apr 2026 06:27:26 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:6c44a1d099c2fac1f899b3900b6aac673c69e05d714739b7a437613ed9c1992e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16994361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b7ade5f77b0cca3064e7e3499db6e13ef6ccb8dd90cfdd74528a3cc87acb29`

```dockerfile
```

-	Layers:
	-	`sha256:5aaade5959209aad872b917d46a97ef8a4d24e7511aa8c5debe35ab2010f670e`  
		Last Modified: Wed, 22 Apr 2026 06:27:26 GMT  
		Size: 17.0 MB (16974460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63dddc5863898cc1ba6ac61e4ed1490a7476bce064a26ca8f86b1d169cd58067`  
		Last Modified: Wed, 22 Apr 2026 06:27:25 GMT  
		Size: 19.9 KB (19901 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-trixie` - linux; arm variant v7

```console
$ docker pull perl@sha256:f2dc31639a6cb03f2942a7faaff2764580b34b31bf0a56df688cec8dd20fdacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340551268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484a0981971a42894f389733ebd4fba830c3cd8a1905f55297777c0a91788bb0`
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
# Wed, 22 Apr 2026 05:21:46 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 05:27:13 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 05:27:14 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 05:27:14 GMT
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
	-	`sha256:f4591e00f3ff0f2d5fdc41c1603582b43927fdac41f6c6dbaa6ceff4c7f51001`  
		Last Modified: Wed, 22 Apr 2026 05:27:35 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5964d84e12b01818e74040e4a8526a946b5a606dfc1a7f4b882b4db36a55b604`  
		Last Modified: Wed, 22 Apr 2026 05:27:35 GMT  
		Size: 15.1 MB (15067014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c7e9b0d13e458f259f70e204e3573dbe88a9b7c0d5df1f8179c9ef91d18368`  
		Last Modified: Wed, 22 Apr 2026 05:27:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:7761e0f5ab1361e0c6788e111e37136d652e94f31fc02862989dd97aaea03003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17000151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e30b8a426271cc3212ac9090a902748b642a289470dbc19537e84ec9fac0ede`

```dockerfile
```

-	Layers:
	-	`sha256:c5b317408ce1037c4b4945abedcdaac17c1ca5bee2ab826d317b22f7bc18ff3a`  
		Last Modified: Wed, 22 Apr 2026 05:27:35 GMT  
		Size: 17.0 MB (16980250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f9e1f0367de650eef66aa2dc00349276074e5e2427e994df44f7c178d6c7938`  
		Last Modified: Wed, 22 Apr 2026 05:27:35 GMT  
		Size: 19.9 KB (19901 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-trixie` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:2f97b925aba86eb804edc1015b1742769ebe58a46a039cd47cbb0fbdaaaccf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384394982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6da08ee38a93813f6b572c12b5db11505f3ea5e67042e7a58e076e0845e445`
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
# Wed, 22 Apr 2026 04:14:26 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 04:27:04 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 04:27:04 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 04:27:04 GMT
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
	-	`sha256:977fc6d67c3abe05a190f670c7c8a82e68b792d80cc01286e7036db22e9ea21b`  
		Last Modified: Wed, 22 Apr 2026 04:19:20 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a604db1fc7d674c00a7a626504275023a12b0684605bc4bd3dcc1f338547fc`  
		Last Modified: Wed, 22 Apr 2026 04:27:24 GMT  
		Size: 15.9 MB (15907767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaa11bb407a80d4a4f2af45eeec99ecd777118d78b6f33c585795e665552816`  
		Last Modified: Wed, 22 Apr 2026 04:27:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:933caab6489017b1e80acda973dd6d13a7e4d8cf09b88a0f552563688d8fa534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17316533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b4dd6099d78af880493d466c9fd8c8b4d1e7bb2d3c4d85bc3510cf20f12d24`

```dockerfile
```

-	Layers:
	-	`sha256:f0507326ebf68c62fcdde6fdbed22555654ee49ccc20ac022c468d493fdd6cae`  
		Last Modified: Wed, 22 Apr 2026 04:27:24 GMT  
		Size: 17.3 MB (17296584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86320aa2191e89ddf47544e01fe37e047e3a4a9720afe8ffe327042ba9c3856b`  
		Last Modified: Wed, 22 Apr 2026 04:27:23 GMT  
		Size: 19.9 KB (19949 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-trixie` - linux; ppc64le

```console
$ docker pull perl@sha256:957842f0440cd118bf8dedc41aa814e169632979f4fd42797c159a40adad64b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.4 MB (400372454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60a1b8622a98d6244e0be0b6537146c06e675df0b6a87579ae60ffec8ce5a00`
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
# Wed, 22 Apr 2026 16:45:23 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 16:45:23 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 16:45:23 GMT
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
	-	`sha256:15584b7b980855a354577366c24b708b476876a5926a1b9c4106546aeb0d6fe1`  
		Last Modified: Wed, 22 Apr 2026 16:46:02 GMT  
		Size: 16.0 MB (15985076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f73babc3f8574d0d9634029589aa79a2de7afb19da19869b2eec9f590119108`  
		Last Modified: Wed, 22 Apr 2026 16:46:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:ffa7e6439658d2ba5b50af321eb059e32912e019b404fc5335f598255bedce4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17217653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c294a7252ee5c249313b63979392ea2a6c0153afa4f42ccabdb4f577074ea64`

```dockerfile
```

-	Layers:
	-	`sha256:4035129b50c91faca1c83e6a8b889fb36658bbffb039e2a9ea9116a24a1bb497`  
		Last Modified: Wed, 22 Apr 2026 16:46:02 GMT  
		Size: 17.2 MB (17197799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21804827cd2134137fe26e3b17671448b662f6a9169e7299104212e586ceda45`  
		Last Modified: Wed, 22 Apr 2026 16:46:01 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-trixie` - linux; riscv64

```console
$ docker pull perl@sha256:b3d33cd4d9d54b46291b6496c4286f389d49ab8fa80b41bf40198cb5428793ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.0 MB (481013868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bb4753cfbeee238c052ce5235ccdd186e3552c348c9cd6cd3d41578a2c4038`
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
# Mon, 13 Apr 2026 05:45:06 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 13 Apr 2026 05:45:07 GMT
WORKDIR /usr/src/app
# Mon, 13 Apr 2026 05:45:07 GMT
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
	-	`sha256:44ba15cb590f582108964e1827afe23bffee923943642b495246e4cad17d9c3e`  
		Last Modified: Mon, 13 Apr 2026 05:53:03 GMT  
		Size: 15.4 MB (15407412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3139f9d2feb56390032d9fd7243a678c5b256e0a868c99abb533c09a099680`  
		Last Modified: Mon, 13 Apr 2026 05:52:59 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:87070beccf92747bd160bc8060c449270d76a6f81138a8a69feaccd446b8aa95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17288188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef4229d0177d6b7b29bb290b51064700c082fd93c6e43b65b218e47cc644f0c`

```dockerfile
```

-	Layers:
	-	`sha256:445d9dd3dd3c4be75a4417d972845b0f009584b7f70a95daea84cec7e67d8e93`  
		Last Modified: Mon, 13 Apr 2026 05:53:03 GMT  
		Size: 17.3 MB (17268334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f7ba941687389f6abd348dd9da415bad2f330d49da49da1d3408b184eb35ce3`  
		Last Modified: Mon, 13 Apr 2026 05:52:59 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-trixie` - linux; s390x

```console
$ docker pull perl@sha256:171f95aa74fdbb7f049b4908133893a060477963dd8ae3143a374bd0aa63d965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.0 MB (367952131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1095e908c674d00528603f38300be94b999608bd35a389feca1549c78a9a53bc`
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
# Wed, 22 Apr 2026 08:34:16 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 08:34:16 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 08:34:16 GMT
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
	-	`sha256:9b9e4a4d5681a2c41ee161e5bf6f5917aa818fca39dfd1bcc4ab007fd065d22b`  
		Last Modified: Wed, 22 Apr 2026 08:34:52 GMT  
		Size: 16.5 MB (16537882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48caa852bfc4bc54125b586491addea0173e56754bd2ae600befa806960946b9`  
		Last Modified: Wed, 22 Apr 2026 08:34:51 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:425b0bfacb74c5c368ee9725b7ca3e89dfb543bf19d8a0468cfdeee5dc6ab9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17009211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a19feb696c0474af122247fae3c8f1f81319cdb0a6c004a39f98820a7839d1`

```dockerfile
```

-	Layers:
	-	`sha256:54b5f71beb049efb7828688956baf612f7ed2e4e579f3e28244bad19a835be73`  
		Last Modified: Wed, 22 Apr 2026 08:34:52 GMT  
		Size: 17.0 MB (16989439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d96c2bd49942b25de4cdaf239c77192492c962ca56c25e67f398060099bd48d`  
		Last Modified: Wed, 22 Apr 2026 08:34:51 GMT  
		Size: 19.8 KB (19772 bytes)  
		MIME: application/vnd.in-toto+json
