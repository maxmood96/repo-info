## `perl:threaded`

```console
$ docker pull perl@sha256:2ca9649459f7db3f3bf38ae492365e658f7044d46928ebe320ab31f21e7deeb1
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

### `perl:threaded` - linux; amd64

```console
$ docker pull perl@sha256:3960dd8d72d32993a6bea6a3b0f5489ef49d3e3ca8063190fc1dae9b2b230b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364112213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6a4b5ec7235fd65ec1e7019a943158446cac75db7f66cd9fb52107032d0cdb`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 05:19:13 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7576b00d9bb10cc967bb5bdeeb3d5fa078ac8800e112aa03ed15ec199662d4f7`  
		Last Modified: Tue, 04 Feb 2025 06:14:28 GMT  
		Size: 211.3 MB (211328049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9e44959f0c03feecea6252b1d89446da4646654206a5368b67e5853766127a`  
		Last Modified: Tue, 04 Feb 2025 07:19:37 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67b044bfb755ea766049bae744bc17000e8c80143d83ada7d5ccc1c482dc5f6`  
		Last Modified: Tue, 04 Feb 2025 07:21:07 GMT  
		Size: 15.9 MB (15851564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5459ad4bf237e1f205a6ecd4520ea8430daa4b67552411ab2a5689fee2119b1`  
		Last Modified: Tue, 04 Feb 2025 07:21:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:07163c142a11a9b939bbede12dd7a03d303d9680b02b94ef310d5ca4767f7a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15494722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d654e6eb91ffed1b039682f49878fe049b0be0e882e0412629e6a3732d525cb6`

```dockerfile
```

-	Layers:
	-	`sha256:d056e176768a8ae164b54ca63930e1e3e1395cf49e0cd883a2792178a0f76a2d`  
		Last Modified: Tue, 04 Feb 2025 07:21:07 GMT  
		Size: 15.5 MB (15474901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70381fefb3a5e0f1006371ec3bd1ddc250b52ec5a4a8de2eb4ce25dc10312f07`  
		Last Modified: Tue, 04 Feb 2025 07:21:06 GMT  
		Size: 19.8 KB (19821 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:8c9d416c648aea2c75f4daf980dbc2c5fc9ec30d7af5a0584a420587f37beb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330481214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d30f8729fa60669cdea155800b69c39ae445f2ee4a5d36305eb8afed6208eb`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 01:38:08 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28060e71ea1173228ae8eefd6f5fb4296e8c1c73672a593f2d0d8e6e5483072`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 22.7 MB (22733102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f77895e90931fefcb9b0f936aeec6e8c95f160c764c504ceb6084ffc29b46c`  
		Last Modified: Tue, 04 Feb 2025 10:20:41 GMT  
		Size: 62.0 MB (62003807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1293092f82d991d58072eac031a86360954b6f4021cae9377a435006dbe3bc7`  
		Last Modified: Tue, 04 Feb 2025 11:42:01 GMT  
		Size: 184.6 MB (184615729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23abcce17ec04db148c6b0580e5a69f4c5d4daa7be00f6eff67bf3c3f4170bc`  
		Last Modified: Tue, 04 Feb 2025 15:58:15 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4e06d431e620709412a71481608c5ab622f156d599a6fb00275c7783f1587f`  
		Last Modified: Tue, 04 Feb 2025 16:05:21 GMT  
		Size: 15.1 MB (15121736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afef0bdf11743f58c72e62dbd7c0e528c31c49c74561c980333599704d0b722`  
		Last Modified: Tue, 04 Feb 2025 16:05:20 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:229bc378e61b969e858a6f007d805e2e16501ad6fbf2d94b5aed8e509f0e44a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15293820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4a0f2d19aae3b169ac7b9e1ecb08be915fa0a8112747c4f5062dd492789050`

```dockerfile
```

-	Layers:
	-	`sha256:69e1c3520c27efa9608f4567f88e443672d6329d4b2eee90e43beeb5a90d0651`  
		Last Modified: Tue, 04 Feb 2025 16:05:21 GMT  
		Size: 15.3 MB (15273875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39b2da9f25280705851b6687a5b61a22650947b543bb84dc5eaa935930da0f43`  
		Last Modified: Tue, 04 Feb 2025 16:05:20 GMT  
		Size: 19.9 KB (19945 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:02fd5701cdebb4179a901c8ac1d303509847c3c08bec5ec79e44fff2c0cb2f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (315962104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a5498d9b3bb74d05013e72ffc13433fc52626e7438a37989e3bea4ef18e7d5`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66806698bb37ab9f15c9072a66ade0dcacacec8794e48afd7fdc2e801ccb928a`  
		Last Modified: Tue, 04 Feb 2025 16:20:53 GMT  
		Size: 59.6 MB (59639147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb08f2dfbcde333a583952948ebc4e632dcbb5e80617adcb1cf802d99c434d0`  
		Last Modified: Wed, 05 Feb 2025 00:17:42 GMT  
		Size: 175.3 MB (175281303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e810d845c4281a6bc894667aa1e6873bc04cdc601cfc0caa650df42c9595301`  
		Last Modified: Wed, 05 Feb 2025 07:47:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e052b444cf0040f8b84dc8654cbf396b981e0c85a31f0c78d27050b93cdb12d`  
		Last Modified: Wed, 05 Feb 2025 07:59:45 GMT  
		Size: 14.9 MB (14897252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1d5530b313fd0368684ff255bbf60e5db20e5a88d6105e2c039aca1157c4d6`  
		Last Modified: Wed, 05 Feb 2025 07:59:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:999770a6779a8ebf4b81d9ad840e6073f68a9f5d963b928af8c5ea07962c779a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15299294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b053b36df6a4f53d2a45dd6e5ecde4fd4152a202f6f0d209c71daccb5e3946`

```dockerfile
```

-	Layers:
	-	`sha256:b95c98f58f6749935b8df17b0bc066e756e6b068ce51b31f28f76bae9bcbd0da`  
		Last Modified: Wed, 05 Feb 2025 07:59:45 GMT  
		Size: 15.3 MB (15279349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4affefe6b26361db687e1f6bcfba6e6efc3c162d5bdb43bc225d24c14f64fd`  
		Last Modified: Wed, 05 Feb 2025 07:59:44 GMT  
		Size: 19.9 KB (19945 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:cba9a276622fe63bfb1498be402d6326dbf86c427fcf443b578d122aed2d6b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.8 MB (354785651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fc4efecad9183fd47e1f736b87874776609edb65a003b35318ab9a059cbbd4`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Tue, 04 Feb 2025 09:00:06 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d3572a68af0b860060b7ea84adfa8406fa20cfd1337c947dfb661aa965eee7`  
		Last Modified: Tue, 04 Feb 2025 19:01:50 GMT  
		Size: 64.4 MB (64357505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9611c2b713640ce0f9156445b244c4da5e621183b56c0901d97a8b6d54ce10d7`  
		Last Modified: Wed, 05 Feb 2025 01:38:07 GMT  
		Size: 202.7 MB (202718404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac515b63bbb62379af840bef0450b1ac84bb63f4bd6aa9a02f1a7e3c931cf1ce`  
		Last Modified: Wed, 05 Feb 2025 09:41:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07a3dd2ed4662df0576dd95d8ab45fe07284b19ce5b7f0bc8b0ff19af2d05d4`  
		Last Modified: Wed, 05 Feb 2025 09:51:57 GMT  
		Size: 15.8 MB (15804494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c9defb3eba689429893e2d1075749b786a3e0b163efde1143300111f9fc06c`  
		Last Modified: Wed, 05 Feb 2025 09:51:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:4af20585762146f898eb2600d040c798706103df543139e3327f50a14ff23798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15523496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5205eec847f482db2a502895f57f7af3edaf384aa37d4f3c1caa72d825009c`

```dockerfile
```

-	Layers:
	-	`sha256:4a54c8df88e20155322c339a4f70270a76a04608d8f513d434af19a060c45562`  
		Last Modified: Wed, 05 Feb 2025 09:51:57 GMT  
		Size: 15.5 MB (15503498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c6f5c207f7c7cb5831b1e55282646696ede1d3f88ba5e2e1bb8c72e43de68cc`  
		Last Modified: Wed, 05 Feb 2025 09:51:56 GMT  
		Size: 20.0 KB (19998 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded` - linux; 386

```console
$ docker pull perl@sha256:f2fb241650412405d4464345dbdc2f34bbe77583da472afa162f3d10d88434a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.2 MB (366243845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac4795ffe1a13f01b12cea8c984193b1c019f1ac3704a81c63b5abee73032d6`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43394bbbaab482132a05c8eb702c9ebbbf5ecccd558ce05fdf40c651b7fbfa10`  
		Last Modified: Tue, 04 Feb 2025 05:15:47 GMT  
		Size: 66.2 MB (66236925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a443d7b60dbf868d9542c672117d7e30786e753c999878424f61b36b47cb37e5`  
		Last Modified: Tue, 04 Feb 2025 06:14:56 GMT  
		Size: 210.2 MB (210244226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889ba634ba5084b6d59a4399a5e04204831ef365b9d32bbf2baa8fb65df686f8`  
		Last Modified: Tue, 04 Feb 2025 07:21:42 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4ef0f68bda04da54e6793973b919e98cee642e876623568e16bd7a9539ea51`  
		Last Modified: Tue, 04 Feb 2025 07:21:52 GMT  
		Size: 15.4 MB (15405636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3439321fdf91fd5be5c3afb4b217b81259d761b20c24ddbd8d3bf64bb20a3da5`  
		Last Modified: Tue, 04 Feb 2025 07:21:52 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:f54a5f0ee9ead88d2f83906890fdc8e2ceb6dd4041de5c9cd586847e33b62fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15473216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa1f3b054440613a367776aa268613b0cc2aedaaeaaae3e7c2420deb15190be`

```dockerfile
```

-	Layers:
	-	`sha256:bf29847aade59113f3cd5d82d3c22a625f077f40e1dd8852622548a28f1be184`  
		Last Modified: Tue, 04 Feb 2025 07:21:52 GMT  
		Size: 15.5 MB (15453456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9344c871c122068dae8b17216aec3f86c667962add80367f8b6ca49604b85b`  
		Last Modified: Tue, 04 Feb 2025 07:21:51 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded` - linux; mips64le

```console
$ docker pull perl@sha256:0521f27c89dc425d09eee895b143914df3474a0813dd8140136c9fb906b12b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340702160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72401395f79f2bea40f8636476d8ad02f2016d78698eecbfe57304189c88613`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:467081b053e1cbae3c04ca1529cea6d968f9b38249f5cdd15b07f60be084dd00`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 48.8 MB (48757800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7faf65582b7e0fbb4eea14df7537078630b3bff0936e1fc964a494519326b5b`  
		Last Modified: Tue, 04 Feb 2025 19:25:23 GMT  
		Size: 23.7 MB (23652224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12393adfa37a97fbcfa8d29955e04828c6bd657b4d83082cf837413910af04a1`  
		Last Modified: Wed, 05 Feb 2025 02:53:44 GMT  
		Size: 63.3 MB (63306362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63804284b8ce6a2c44bc7e10737c5060fcbf1ae87b2f923d57cc93f3f65b661b`  
		Last Modified: Wed, 05 Feb 2025 07:48:12 GMT  
		Size: 189.9 MB (189907614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac66c6918eda6e1f8c7ed1d2f4ccc156c3da7b1780281fffc8f71f87e1d6c6a3`  
		Last Modified: Wed, 05 Feb 2025 10:18:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9758e8851dcd751aa70afd76f0e20ed7f955f9245ac2c4bf0a361c61df5e719`  
		Last Modified: Wed, 05 Feb 2025 10:45:27 GMT  
		Size: 15.1 MB (15077894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba22a0875a11d97068222cf200bb57346fcf7a7dc80d4c344ea40bd1ece0e0d`  
		Last Modified: Wed, 05 Feb 2025 10:45:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:df821f9d4a59b7ce33aca168313979459d298a675432adef995738c6d4315512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba766536c0cb1aed2c9e0cf54873ed95bfa23b32efe377e527b6b2277bf0b13`

```dockerfile
```

-	Layers:
	-	`sha256:5e22903aeba561004cda4c7202bae4937ec5f4f62dba2c52cd34d28491078964`  
		Last Modified: Wed, 05 Feb 2025 10:45:25 GMT  
		Size: 19.7 KB (19726 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:f302657850ecaffe9856fc05def115715d8f35d79a7807668929d8bdcf437ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.1 MB (378138418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6af11b5fc9d3d35470505dbb202c0fc893585fe1883c8ab56b9d8d549e1755d`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 01:37:34 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f161b1ac6fcd1e84495441a30458604c921f0c00816d0cd0926964e56d9717`  
		Last Modified: Tue, 04 Feb 2025 07:24:32 GMT  
		Size: 25.7 MB (25717668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7451c2aa1d936ee2bec4ea4db323da11f1dc2694095c250c16b70763100f29cf`  
		Last Modified: Tue, 04 Feb 2025 15:46:48 GMT  
		Size: 69.8 MB (69842739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556dba2526850ef13f84af87d0289a40f2451777be07098d04c55f33c7f76b83`  
		Last Modified: Tue, 04 Feb 2025 21:55:09 GMT  
		Size: 214.4 MB (214366038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9767988e88d50aa74fb637e1bcce7003b88ca10b7885dc9ec89fdae83c1209c5`  
		Last Modified: Wed, 05 Feb 2025 05:17:37 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c753ff2ff57182e366967549e3ba0351fbb947de68f3a45788a84ed47972c7`  
		Last Modified: Wed, 05 Feb 2025 05:24:14 GMT  
		Size: 15.9 MB (15898851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c6c0e5c0eed0d0b3c1c9585ef843927bd9cfccbfbe185a5690536bb8fc0d53`  
		Last Modified: Wed, 05 Feb 2025 05:24:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:8eb535f37afe2e2f8776fbda04e2d85cafa70f63f9a4d5f4c9cc2d96f3a3cdf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15471223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd6dcaf64c6e2e5939f0ad4d8c08b48a7575bceac8bc3275c2bb7b79ad51466`

```dockerfile
```

-	Layers:
	-	`sha256:daf839f46197398e09782f540b8ac53a411c4a950aa8ece0dd660bad0ccc6af5`  
		Last Modified: Wed, 05 Feb 2025 05:24:14 GMT  
		Size: 15.5 MB (15451322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10ece2c9bdef93f37db2d330d72609ed3cd599d1bbc6a386df93cec67f450859`  
		Last Modified: Wed, 05 Feb 2025 05:24:13 GMT  
		Size: 19.9 KB (19901 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded` - linux; s390x

```console
$ docker pull perl@sha256:ff4e902fff73ba66fbced6399169ed17d5f1524b5976c69dcdb4a66ead242a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.2 MB (334243893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0bbb70771dfd0d4e3823a451775e6c1870a7ed424a63f652223b4b95e70462`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959543dffffce198d7241bd6958a549b695b11519fad12fc54ebe4df4b49bea4`  
		Last Modified: Tue, 04 Feb 2025 17:51:50 GMT  
		Size: 183.4 MB (183365325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0079b8c9bb26c424b839fbc393c06a5b0001ab62eec368a5b2bd5e49d2f5a3`  
		Last Modified: Wed, 05 Feb 2025 04:08:27 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2763cad3474e746b65de891f6ba38a1fdd69fe4ef441ed698ea80a22660b9f00`  
		Last Modified: Wed, 05 Feb 2025 04:16:05 GMT  
		Size: 16.2 MB (16189776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d3741dbb30c56cda4f05f95565db2b5d9e6d94697cfd849a2f73821ff0d2d8`  
		Last Modified: Wed, 05 Feb 2025 04:16:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded` - unknown; unknown

```console
$ docker pull perl@sha256:6725942bff7c12e678ea48831a283165da098e75503361c4b8d46517a4a79ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15307413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb36af80ebcaac43b2b8060ba4414b760232ed2a9c6f105c62bb07bd7ea0c588`

```dockerfile
```

-	Layers:
	-	`sha256:6556e02a16e4c13afba698b39a14ac6dc0553ca38ff1627dcd66f731a4f83d35`  
		Last Modified: Wed, 05 Feb 2025 04:16:05 GMT  
		Size: 15.3 MB (15287591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0577e6ff29e545a4558e77fa1184a00d5e0cdcdea4fa8d313e45fd4a776d7a3b`  
		Last Modified: Wed, 05 Feb 2025 04:16:05 GMT  
		Size: 19.8 KB (19822 bytes)  
		MIME: application/vnd.in-toto+json
