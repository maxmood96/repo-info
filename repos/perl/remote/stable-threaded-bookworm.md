## `perl:stable-threaded-bookworm`

```console
$ docker pull perl@sha256:4a2077de94ca54fb67be84bf1607e2a8977ea242d812e2258595e18056c1310e
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

### `perl:stable-threaded-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:676aa9a7cf8665b43cce648567e9c2e2c02b1b24ad7f18edb5835a003ccb7dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.3 MB (364325052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78870a399ff45dc1315ba5ff951096022718eb700acc6a8300fbf24ab73fe1c6`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:36:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:25:57 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 03:30:40 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 03:30:40 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 03:30:40 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a858b7813255a9cb57d05f02b50978e5b5965b0cfc040288fa29905cdc65ad9a`  
		Last Modified: Tue, 30 Dec 2025 01:22:58 GMT  
		Size: 64.4 MB (64396090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318d61060ae74f5254974208e92a54f807b028710293f41900249bc6033acf41`  
		Last Modified: Tue, 30 Dec 2025 02:37:17 GMT  
		Size: 211.5 MB (211466563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858c2747c59e764ca8803ef16ca614ee2eee17b47fef4c2b014ce1a2d3028fb0`  
		Last Modified: Tue, 30 Dec 2025 03:30:49 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f119344e1d17be04ad26538039feff0601dc5e99df22918c5b1ee60060260e3f`  
		Last Modified: Tue, 30 Dec 2025 03:31:05 GMT  
		Size: 16.0 MB (15951994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c64e45adc3f8b520fac7be93d8c56da530d558256fabbe01bcb6f8d66f5809`  
		Last Modified: Tue, 30 Dec 2025 03:31:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:c6be073a4c75fe21d20c4a482732ba34fc8519fb824c22abe11fa8108dc3fa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15887565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a052501b37af9dd052f1c8d8a8b2d6e08470f9d1b1ddcaeaa202e4b9c94a12df`

```dockerfile
```

-	Layers:
	-	`sha256:855988566a6bd13bee9c5a9d5b247ec64e57cb895118d3cab73f1ee59cd5126b`  
		Last Modified: Tue, 30 Dec 2025 05:39:13 GMT  
		Size: 15.9 MB (15869297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e119edfd5d0f98b3fa03493672436a8f4d425e89245348927ff970fd646b6f2c`  
		Last Modified: Tue, 30 Dec 2025 05:39:14 GMT  
		Size: 18.3 KB (18268 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:4f71ca3e5074851785f229eea812601923f2b5ff58f7c30993553383ee761267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330660015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7434ce4acf836a37c7f82f40822e98ac550b458e027b94d17b416be9f4e45152`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:28:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:50:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:31:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:16:54 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 03:22:42 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 03:22:42 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 03:22:42 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:382890ab3968ba1cefa561463cb731ea178ca7d67e9b6d5bb6fac532b4127c25`  
		Last Modified: Mon, 29 Dec 2025 22:25:07 GMT  
		Size: 46.0 MB (46015872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f922b13fca1ac9a337d28b41c5bbfa20f6d0bc0a979682648a1f6f51b92fc0fc`  
		Last Modified: Tue, 30 Dec 2025 00:29:08 GMT  
		Size: 22.7 MB (22705835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1cb899e5577dac4cbee64e78d96eb1c00ba15084be44c87f70e8eddc9dfd02`  
		Last Modified: Tue, 30 Dec 2025 01:51:05 GMT  
		Size: 62.0 MB (62010548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b61494a96eed23f241d50e46336c33d359170d4b483e90c4fad6a56b5dfb986`  
		Last Modified: Tue, 30 Dec 2025 02:32:27 GMT  
		Size: 184.7 MB (184719520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426562d46f88e9c06a5f92e43b1b5620480ed821d4c8f6c96db0a9ec07119535`  
		Last Modified: Tue, 30 Dec 2025 03:23:07 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd9eb0e8285a84a0a606e4547a621c7b5f7e90b7aba1b757997ef7d4da017af`  
		Last Modified: Tue, 30 Dec 2025 03:23:10 GMT  
		Size: 15.2 MB (15207974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acfb5ba2b0c651733596e5ad15f1f594f0f2fbbaf3e59f385ec2655596430a3`  
		Last Modified: Tue, 30 Dec 2025 03:23:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:ffa1b218d8fa781ed36df33a8406b62dbcbfb77ff8e2ae9558b57e07f63eef00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15684661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7244f8e71adbdb38788909e053da9f792b275d6a12a92193251f86777107ed`

```dockerfile
```

-	Layers:
	-	`sha256:8d87214d66e75e9a1585a811f0d19fc7f2d6d0b2673d2f8b3d0cba1c991a103e`  
		Last Modified: Tue, 30 Dec 2025 05:39:28 GMT  
		Size: 15.7 MB (15666305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dc085b55fd2b9a7b4f69a6dac76a35964e31bac34d5b03f712c57b4a2314fd8`  
		Last Modified: Tue, 30 Dec 2025 05:39:28 GMT  
		Size: 18.4 KB (18356 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:2cb2471f915698fd406ea1bcafb20a77649f86f8181b351f65f20aa6bf709ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316157073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df45513da0258f2545b0f56f7be3cd27393b25e2d4d1183ebdb7a0f889d15296`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:06:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:34:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:57:46 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 04:03:25 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 04:03:25 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 04:03:25 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7f06489595662b32227ed4939431e5099ae83a2661a5770c752a389e68e400`  
		Last Modified: Tue, 30 Dec 2025 02:06:44 GMT  
		Size: 59.7 MB (59652384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3429e4481c959b42472aeab211da596c017178158219b524e556cb5c3ee4987`  
		Last Modified: Tue, 30 Dec 2025 02:35:40 GMT  
		Size: 175.4 MB (175370783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037ac266a3f3a99689d57daaa4704ea758a2adab032704e15f4e8dd50e7cbe7f`  
		Last Modified: Tue, 30 Dec 2025 04:03:49 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d5478764f557c2a5dd91c691b72ec79800df8fde4338464504d4a6289d3d41`  
		Last Modified: Tue, 30 Dec 2025 04:03:50 GMT  
		Size: 15.0 MB (15002747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268c47e5cb30c47b3969b5265c320d85d879b89ba45acb19fa4e1d5f88d342fa`  
		Last Modified: Tue, 30 Dec 2025 04:03:49 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d45ecd4feeb959ed8e9ece6778c3d4edc6ad4ac7d7c064e23912e2ce08561e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15690137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511a8315caaeda17f15c24abd8be4efe4ca8584c49de8a0926d2fdd03d702db5`

```dockerfile
```

-	Layers:
	-	`sha256:0415f3fb3402556b56e9c16c40fb372795a751b3d587badfa7dc911b993fbcad`  
		Last Modified: Tue, 30 Dec 2025 05:39:42 GMT  
		Size: 15.7 MB (15671781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0938482906b1eeb846e7ca301fb778dc5d8ac0882e958295db6711a05e592221`  
		Last Modified: Tue, 30 Dec 2025 05:39:42 GMT  
		Size: 18.4 KB (18356 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:cc690388fe28857449b89f4ee183f208579f700eeea7c14526cda8b42355bcd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355211140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3611ca416a69e0f47d32210ed139dfe03c648b3ed007a95489f6341be4e131`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:35:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:25:02 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 03:29:56 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 03:29:56 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 03:29:56 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885a684c982cb8679ba82c9c939ec2b3cfe9c823a68d404ebbc3ac75d14830df`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 64.4 MB (64371168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e473cfa5c6fa57db72a6e347d7fc4f13909c3c9e83819127a50c0195b88eae`  
		Last Modified: Tue, 30 Dec 2025 02:36:21 GMT  
		Size: 203.0 MB (202980659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb0df6199aa6ac6998d6544bb2599e89c88110d82e722616daf7ebfba7fb3c8`  
		Last Modified: Tue, 30 Dec 2025 03:30:24 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be552631d25d4c7856256dd0685b96e7d9e3aa12227cdf2a89221b8b5f43bb0`  
		Last Modified: Tue, 30 Dec 2025 03:30:35 GMT  
		Size: 15.9 MB (15901520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebb3e4ab499c394ed9393f75854a613d40eb27ab3be6be44816f7a1e4735ec9`  
		Last Modified: Tue, 30 Dec 2025 03:30:24 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:f27da5f45eb0b38def195a8f18d287226aea0f756926c584da021e41c6b85c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15916219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03bac088a1da93791b4f01ca1abff2acad50413661de086bb7ce77a4c05bb52`

```dockerfile
```

-	Layers:
	-	`sha256:5de81ecf5c37a2f24b733598d110b899d5e864386bd515d071df97eb6d73c123`  
		Last Modified: Tue, 30 Dec 2025 05:39:56 GMT  
		Size: 15.9 MB (15897835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f867c30eb87ffccbcf3199ca95d1775176fddbb0b9d3e9b489b7d95620e89401`  
		Last Modified: Tue, 30 Dec 2025 05:39:57 GMT  
		Size: 18.4 KB (18384 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:8446d2873c54326ec97ebec37b0046e5820539cb9b98b1f23612435216636395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.5 MB (366455539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9528ee4ddb60fc5b930288c41c61d3341ddc7508938b193ce8c73b31c9d611e7`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:32:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:46:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:21:08 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 02:26:26 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 02:26:26 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 02:26:26 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:d27cc9ffb7903d292157edf3b1fb57175a2a59b66ae4855d328a6a97d9b4a6e9`  
		Last Modified: Mon, 29 Dec 2025 22:24:49 GMT  
		Size: 49.5 MB (49466879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63bb42155eb2fe3cb6496304c20382db95885b672da0e34a3fffa188861a6ec`  
		Last Modified: Mon, 29 Dec 2025 23:47:31 GMT  
		Size: 24.9 MB (24864466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10eedb7d741cb151d52259302acf62c6c98590a9a4168d4370619e890f15715`  
		Last Modified: Tue, 30 Dec 2025 00:32:36 GMT  
		Size: 66.2 MB (66233282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e51985c2f8fac19e56fa29b530e82a1e9f93bea1ea6d96cd2654ebde3370e4c`  
		Last Modified: Tue, 30 Dec 2025 01:47:11 GMT  
		Size: 210.4 MB (210391421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162316e629f39214492f536020229315124411e621e5e01b59d7a0d883eb9c6a`  
		Last Modified: Tue, 30 Dec 2025 02:26:54 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e58f26736a708bd21a35765ef970b9814d4bd05d0796930fc4242aabf7453b5`  
		Last Modified: Tue, 30 Dec 2025 02:26:57 GMT  
		Size: 15.5 MB (15499225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf09d9224fee5618ba2893e3612a42947134d58bff04bfe1b0108518cf19ea3`  
		Last Modified: Tue, 30 Dec 2025 02:26:54 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:4f38acbf6b9f55596cbb24759bad6a93bb4eeee76e85dcc4a9c644e6bbd40565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15865740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3f0193cd52b980edbbd885749e3801db6dc0f263e10ab882b713619baff539`

```dockerfile
```

-	Layers:
	-	`sha256:ab496eb9adbfd83ec33680c998b7b580ca78e1d1709772917f21feb5cbdb0dd0`  
		Last Modified: Tue, 30 Dec 2025 05:40:10 GMT  
		Size: 15.8 MB (15847509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bef54620b481e6c79e0c853f36b90bf30c3c018ecbe657324f97a89cf5bce8e`  
		Last Modified: Tue, 30 Dec 2025 05:40:11 GMT  
		Size: 18.2 KB (18231 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:16048456f37ac6f3d110962dd6ca40ac41176397376fa516e65592cf84ad39fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341081783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8136b42f05ec20578282bd25a6aab89099688cb82b03a5edebbf2bf8d4e0fb44`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 15:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 20:09:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 21:54:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 23:59:32 GMT
WORKDIR /usr/src/perl
# Wed, 10 Dec 2025 00:50:29 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 10 Dec 2025 00:50:31 GMT
WORKDIR /usr/src/app
# Wed, 10 Dec 2025 00:50:31 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:39c87c0b77499147a54de9b3e5bae714c175e6e770a910d9f420c4e6fb61ba58`  
		Last Modified: Mon, 08 Dec 2025 22:14:39 GMT  
		Size: 48.8 MB (48760897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1571bb35c4ff72a581f317370ae35a4e1c5896fc868d9d6a6a545382b80d1b1`  
		Last Modified: Tue, 09 Dec 2025 15:10:23 GMT  
		Size: 23.6 MB (23613949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7e7f53e0184cfbc8481d8bf6e3898908651f4106389843dddb844d4e45ba75`  
		Last Modified: Tue, 09 Dec 2025 20:10:46 GMT  
		Size: 63.3 MB (63309593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b092eb587173562df38ceb11d2739cc5af4dbe0fbe55d919b4b1855a889dbb`  
		Last Modified: Tue, 09 Dec 2025 21:58:18 GMT  
		Size: 190.2 MB (190228033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc27be8a57b6179661a543a2b2c28fdeb3baaa9bab22b692dacebfc96b9b466`  
		Last Modified: Wed, 10 Dec 2025 00:24:44 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025d30c36176261bec479fbecde614e4cb474f3d4c20249bbb4296c486b1cc5c`  
		Last Modified: Wed, 10 Dec 2025 00:51:43 GMT  
		Size: 15.2 MB (15169043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4697a1c7385129eef34df3d9769ea0106d1e6d5bf0a5857804da8deb746395a5`  
		Last Modified: Wed, 10 Dec 2025 00:51:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:7be140935ae778d5dc6c471af47d14d52442f96b7c54d69fddd3ab86758d70c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 KB (18128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83691c74c049b84a1fd38ab6534914bed55d729717d5a9bae9e84e5700c7b5aa`

```dockerfile
```

-	Layers:
	-	`sha256:adceed8b57599ca9a6a0119153e85db480f12fe6d762f038d4fcfcb60533b6ca`  
		Last Modified: Wed, 10 Dec 2025 02:38:29 GMT  
		Size: 18.1 KB (18128 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:1878a584df1be1396ff769323407ee8d932c8e6da020c33107270ea643682c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.3 MB (378337874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8e868d86b34d2e9ba8fd5a975693882004d8bf541e28b648a808dca6296072`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:21:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:09:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 07:29:04 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 07:36:45 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 07:36:47 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 07:36:47 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4109a037ac4c69c3ce26e6d14e10c867842083c363485abd63db45502611991`  
		Last Modified: Mon, 08 Dec 2025 22:28:59 GMT  
		Size: 25.7 MB (25672209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2b93c70c0b05a907d16ae217d77a407e9aa88f69499ffbfee4375b49ab6c01`  
		Last Modified: Mon, 08 Dec 2025 23:22:14 GMT  
		Size: 69.8 MB (69846008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc15b235f2d99c9b8cb7f5511247453daa35498d32335b3432bc90fb1d754bd`  
		Last Modified: Tue, 09 Dec 2025 02:11:48 GMT  
		Size: 214.5 MB (214498018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a610e26b9f8c1494ad48ff536c2c162fc15b6c894363f75236a5d98dc7d2958`  
		Last Modified: Tue, 09 Dec 2025 07:37:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f695aa8c43a96e2463dba95614e719fe688d860294e1803078a15101c559ae`  
		Last Modified: Tue, 09 Dec 2025 07:37:36 GMT  
		Size: 16.0 MB (15994396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635b67f02942fbc4952dd65c5dfc043d21949a05723ff9d1e1a07b1a92e2e0c`  
		Last Modified: Tue, 09 Dec 2025 07:37:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a796a32dc6ee53c88f1f8dfcf734859df9f1e043f2a603a3a1d911f9d5962c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15864084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3c65097d437faac634ea2cedf589eb224804ca8dd010446f1e53754b1d54f2`

```dockerfile
```

-	Layers:
	-	`sha256:60dab4ca2b56f658d9fda22526b701ec715fe584e8642ce83de986168f8f606b`  
		Last Modified: Tue, 09 Dec 2025 08:38:52 GMT  
		Size: 15.8 MB (15845766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb861a17ef824265915adad4dcf49fd45b71b55d4b46a9c201cc9b65d1f8396`  
		Last Modified: Tue, 09 Dec 2025 08:38:53 GMT  
		Size: 18.3 KB (18318 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:ead225904680f50e81eebac59c1359d4524d68ca1e810bdd56cc328f4110ab74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334459219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7a67f22df3d2165b24b647ddb4cea17280b5c2fcd345a2bb51f775e8d74a7d`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:19:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:23:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 04:28:49 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 04:35:50 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 04:35:50 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 04:35:50 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:ce8a6983b315f7ccc96b582192afffde7bfdc0a45f357f2cd098b4f88aab2be4`  
		Last Modified: Mon, 29 Dec 2025 22:25:37 GMT  
		Size: 47.1 MB (47137727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acc4c1479120c6249296b3550670caa7738ba389b23a7ca3973f7732c12c0ab`  
		Last Modified: Tue, 30 Dec 2025 00:42:34 GMT  
		Size: 24.0 MB (24027124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013d337299523414af9c112b1b1a1d201a2c6eaec2baa26798cdadeeaf575ed2`  
		Last Modified: Tue, 30 Dec 2025 02:20:20 GMT  
		Size: 63.5 MB (63501425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7270a2a483e4f77c88a33916d868e39275b0c406be0c8718bf3043df371c7900`  
		Last Modified: Tue, 30 Dec 2025 03:25:02 GMT  
		Size: 183.5 MB (183499888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2506b5c9d820b9793a3ce8053af2b058d1e25cf8d1d431279a27e0c0c3a7e5c8`  
		Last Modified: Tue, 30 Dec 2025 04:36:31 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b5aaa8534415bd1fbecd998152c249cec9b6bb2ad5a0e7ae22eb0774659be5`  
		Last Modified: Tue, 30 Dec 2025 04:36:32 GMT  
		Size: 16.3 MB (16292789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb694320a187b4e1dd2cd5c5b89f51b96fc79c8d86680c09ed2b3c01e00cde0`  
		Last Modified: Tue, 30 Dec 2025 04:36:31 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:c781af84f47bd3dcb6c4430fc6ed6f68b86e5248ae09f0784e0ac350f9dd13ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15695162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1b94412eda588303715e4bea336b4d14ad2581c97aa2b21e76c7f4acc88258`

```dockerfile
```

-	Layers:
	-	`sha256:433afdbe4bdae9c18e410a3830f42ab2d651832d83057aa1983385bededc7cf7`  
		Last Modified: Tue, 30 Dec 2025 05:40:39 GMT  
		Size: 15.7 MB (15676895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66423b281971797ded8d0ea74f279fe8c19d9b1b71404f587915b4bd15ec5934`  
		Last Modified: Tue, 30 Dec 2025 05:40:40 GMT  
		Size: 18.3 KB (18267 bytes)  
		MIME: application/vnd.in-toto+json
