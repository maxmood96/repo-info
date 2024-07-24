## `perl:threaded-bookworm`

```console
$ docker pull perl@sha256:493ee80d24dffbef87a32229558979e49636155b1a80390a4856423f9ee621d0
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

### `perl:threaded-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:3e030480c06afa86ab1281c1305bd2a9a99add133e1e2aa93f5d870546035390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364871199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46536db8928580e93093c4a20f327a0f672fa194987a5ecffe95a3b6af816f8`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d643a5fa823cd013a108b2076f4d2edf1b2a921f863b533e83ea5ed8d09bd4`  
		Last Modified: Tue, 23 Jul 2024 06:13:33 GMT  
		Size: 64.1 MB (64143199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dc1019d7935fe82827434da11bf96cf14e24979f8155e73b794286f10b7f05`  
		Last Modified: Tue, 23 Jul 2024 06:14:07 GMT  
		Size: 211.2 MB (211241610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4543b083040f43b97fdc8766e0be00fa1bb218ad9b53cd752423e2bcea43da`  
		Last Modified: Tue, 23 Jul 2024 07:28:46 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f6510c1083296672755e4fac9799b1ddeebb3cee50b38bbbc2cd3cafcb1787`  
		Last Modified: Tue, 23 Jul 2024 07:29:03 GMT  
		Size: 15.9 MB (15881253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9ab5d8590399a1d872455dcfa42a0540464380a0f1bfb1b82a8d93ada7fa90`  
		Last Modified: Tue, 23 Jul 2024 07:29:02 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:b36ca51daf03107849ffde1814999e38cac54ad55e157e94a2be538359a0b46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3fcda368a019aa1aa6b0bb3be1242f25ad9a201d41080e6de52286c9e016e5`

```dockerfile
```

-	Layers:
	-	`sha256:9e7e7d1323da52a62c86e70634859d9b8cf29e583fe8e21db29d64c3f629eee6`  
		Last Modified: Tue, 23 Jul 2024 07:29:03 GMT  
		Size: 15.4 MB (15445641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c8c214cebddfbe0b158a14eea09de81d76109e58e309e0959eea2773ac0fd6`  
		Last Modified: Tue, 23 Jul 2024 07:29:02 GMT  
		Size: 19.0 KB (19016 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:1d4734db6729f077b34ae6a7798a48ad1f611f34611de8c9f1b1be61d9cca5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.2 MB (331238443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3611c64d28ba58f8f28bdbc68c742f1498a9d4f93429d4aa9f16005e2c18fd5c`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:983ad82e1f35e444cad37dc64834e9c9e172d4335ea328a24fe5d009d70d58ae in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:a2103702bb8398b16f1bda2e89255e26b7a0141cd10dcf946690d760d4402196`  
		Last Modified: Tue, 23 Jul 2024 00:00:53 GMT  
		Size: 47.3 MB (47320379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ee1c099139cbe59b1878b46c83329d4cf446719eb18cc9d218c3a093a7a059`  
		Last Modified: Tue, 23 Jul 2024 03:51:58 GMT  
		Size: 22.7 MB (22729513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6419549a75691f5f64e23ef19b8b237b75cd67d7c0b8efcb141d58481ae8f1b9`  
		Last Modified: Tue, 23 Jul 2024 03:52:24 GMT  
		Size: 61.5 MB (61520180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f383f84306b6f41c3ed73bdfceb22befd854a21432eeb20e66606aa7f0de1a3`  
		Last Modified: Tue, 23 Jul 2024 03:53:14 GMT  
		Size: 184.5 MB (184529578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5869ddcc0be7f20129b8ab03f3653f151092c7df0e4321b9927cedfaca4a926`  
		Last Modified: Tue, 23 Jul 2024 21:59:30 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b99ebc2ac72a626aeffa9bbb1eb3a7b81980f32faf8f7895d31a6c5c11b235`  
		Last Modified: Tue, 23 Jul 2024 22:16:36 GMT  
		Size: 15.1 MB (15138525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d72ba50437d0dae3aa81392e873654053ee221be64700ab1553653b461fe34`  
		Last Modified: Tue, 23 Jul 2024 22:16:35 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:7e3546e04a9cade5a84002cae8bf23cd531c16c1bc7596a4bc99593800ef85ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15264184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00324d06356da0be1066ac4efeda66ac6f6c4d1ed80d6d441638785d74e2561f`

```dockerfile
```

-	Layers:
	-	`sha256:b1d6cbc32dd4bad53978288426b5223661a3d309f6bbccd63cd9ceed7d621478`  
		Last Modified: Tue, 23 Jul 2024 22:16:35 GMT  
		Size: 15.2 MB (15245050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaadb8f4c247f77e97a266323e5868b9f981bc11a0a05010c78ba7b626da8063`  
		Last Modified: Tue, 23 Jul 2024 22:16:35 GMT  
		Size: 19.1 KB (19134 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:a15e3983d490d25bec6b1e65f6015ac6d6b4109475fc95f9803d4ec24bc2e535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.4 MB (316428416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62b4c0fef428943d62ef161a0550f7762f971ab545dbe819fe8a3ebc4920a4a`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdaec64288ad5c82e3a7f27432ae79c4867ba6c8f1a77e1dc0389e784b1c6dc`  
		Last Modified: Tue, 23 Jul 2024 03:48:08 GMT  
		Size: 175.2 MB (175182891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc49d2585b5f6cd53f7b8a88054531f6ef71a57b73ae4bd98b8f3d60d76e1c4`  
		Last Modified: Tue, 23 Jul 2024 23:29:24 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996ac87a1aabaee50d118e007942ce53c3af606673d041019a0893c4ba1e3dee`  
		Last Modified: Tue, 23 Jul 2024 23:57:02 GMT  
		Size: 14.9 MB (14919656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ca5d81d8a61c06cac2b66878bd60d59d0c04a095b218a79f2632f381f7dbca`  
		Last Modified: Tue, 23 Jul 2024 23:57:01 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:91f39d05d948844da5ad067b714db5d6d3ec81bb69ca03aa91aa0a21678a9805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15269658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b641acd4c9e9945692e67138be2c7d54637bc6c4e1953534896192708af47bb`

```dockerfile
```

-	Layers:
	-	`sha256:8e6e49d20fce36ae8144060e62990bdb9791707830db252956f78e91695313e1`  
		Last Modified: Tue, 23 Jul 2024 23:57:01 GMT  
		Size: 15.3 MB (15250524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcd650c921c067d5d70b5b4a81f18e3852ab5bf2075d95762e962b9d0879c250`  
		Last Modified: Tue, 23 Jul 2024 23:57:01 GMT  
		Size: 19.1 KB (19134 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:9fea39e2628e197169b26ec1ccfd5fb5c65a940a9e85a1407ee8d67f2c2986f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355626376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78083448b401c37713d0084c4383321fda15dd4a5860b27ce3d514a76437ce7`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e903e4e709d192e5547602a5978c79692063228a98585f33fb02d343bc15719`  
		Last Modified: Tue, 23 Jul 2024 08:10:20 GMT  
		Size: 64.0 MB (63994288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adacb995432c92df6de0b5690abdd064e095988fac45631ba8fc0a0ffa9be5cc`  
		Last Modified: Tue, 23 Jul 2024 08:10:47 GMT  
		Size: 202.6 MB (202624227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d863165631ff387b2edb7851205f0cebd6439d47c79ddc4c9474ee2164e512f9`  
		Last Modified: Tue, 23 Jul 2024 22:16:17 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2640e58b273340fc7cdd614ce91042027716b1b3d87753ff8fef56c82f10542f`  
		Last Modified: Tue, 23 Jul 2024 22:38:04 GMT  
		Size: 15.8 MB (15826699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039929e6726c54d142294e2361aba39beb2e620f5f61aa4ad045564a034254b7`  
		Last Modified: Tue, 23 Jul 2024 22:38:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d8c1eab44af252a277b73319eb0e0e86363ea7b58e9977a174513af48910b407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15493669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073199723991789ee7be7a80188b29cf54da113a9d16c09ebcf792e5c0a0446c`

```dockerfile
```

-	Layers:
	-	`sha256:e9c1b16aa2e2de4dd20e35ad9eef4793024a47b170c49239dece9758fc1e8a5d`  
		Last Modified: Tue, 23 Jul 2024 22:38:03 GMT  
		Size: 15.5 MB (15474269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e134ca785b81cac963c99d7bfd42739bfb66daf024734a48b4c8d605c1436ab`  
		Last Modified: Tue, 23 Jul 2024 22:38:03 GMT  
		Size: 19.4 KB (19400 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:d54d91cee865d7c9fd30e1ef31a7cb19eea77412b5894dd7f6f5cb7545761dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.0 MB (367046930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0751c5183b1810dd73777a6c992051499b24222019a6162064b9a14cc93ed7a9`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe9de7929eb5cdfbf61ec571a39b7279b074e89cbd4a3b2ca99e81badbd5dde`  
		Last Modified: Tue, 23 Jul 2024 04:48:40 GMT  
		Size: 24.9 MB (24891462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8378865fc9e6569272faaefe1da81649f1839f35e7c990fb8ab8e8279a807ac`  
		Last Modified: Tue, 23 Jul 2024 04:49:03 GMT  
		Size: 66.0 MB (65988807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4a7c31652ee354c7323f3315523d185b07416d8cb4bc316907ce5389dbee90`  
		Last Modified: Tue, 23 Jul 2024 04:49:51 GMT  
		Size: 210.2 MB (210156525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10aad516600153173fcaca3daa3a027fb9344b510400a741499af7e2cde32512`  
		Last Modified: Tue, 23 Jul 2024 06:26:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263ea7999373fefe866835626beeda33fe6eab844a7f028a30274750c958bd49`  
		Last Modified: Tue, 23 Jul 2024 06:26:54 GMT  
		Size: 15.4 MB (15430449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c720b7da768b53e3d1bf3c07048f91738c40e7243d9d4826e1b42362750b6977`  
		Last Modified: Tue, 23 Jul 2024 06:26:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2ff8f922cbea7ce4b6d105a3609654a4f1a37917ac2f6a5e65619d1b21770d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15443354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01734c7ca4a36bc6c28c51360e77339564ff5fcb640375a2bccff10f50583ad`

```dockerfile
```

-	Layers:
	-	`sha256:f7652b8950b21fd052363d3d5fed776ed9ade82f7c39a9a6572e6a4dc76791f4`  
		Last Modified: Tue, 23 Jul 2024 06:26:54 GMT  
		Size: 15.4 MB (15424397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8af5509ba051b39e2e35bd7f75c9e6e93d25e1242285d03579a18a462731fea`  
		Last Modified: Tue, 23 Jul 2024 06:26:52 GMT  
		Size: 19.0 KB (18957 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:1a66bf6c41d918e82caad2278820feb2ccb71ff9a7f8bff64032316df7b7e4e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (341036719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e14efdd895604e8b095a9466cf28d52fa4f1a06f2e40fcc10478a2f789f9e27`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:40 GMT
ADD file:7398b3272eb97d7c196f6072f2a25952abf995169e82ecb85361b7659b2fb005 in / 
# Tue, 02 Jul 2024 01:17:47 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:55:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:56:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:02:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:827f475650f14eab4a6679f0e49d9155db82de1d5209a3817922c689f46adf08`  
		Last Modified: Tue, 02 Jul 2024 01:28:47 GMT  
		Size: 49.6 MB (49563118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c410c8d28a38525afd5f655d0e2d89727c34a9099ce124494526fbe8c30ef52c`  
		Last Modified: Tue, 02 Jul 2024 02:29:31 GMT  
		Size: 23.6 MB (23634676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0277124339cdea065e75bfae0dd207bb4e1d178268d7e5611472c2f31474deac`  
		Last Modified: Tue, 02 Jul 2024 02:30:24 GMT  
		Size: 63.0 MB (62965735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ca9a10b60cfae11fc4e8ad7a3257aab07a5904e898e4c6be273b066d5cd88b`  
		Last Modified: Tue, 02 Jul 2024 02:32:32 GMT  
		Size: 189.8 MB (189782398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55c21941f81aa8c3d9b8c9715d4d7f5cbb0ae1d1cd2d23f687c04365a242867`  
		Last Modified: Mon, 22 Jul 2024 20:24:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54472a974bd24901a795b44aede234143396c80d10b8da0a46ae7d0f37c8ac2d`  
		Last Modified: Mon, 22 Jul 2024 22:42:52 GMT  
		Size: 15.1 MB (15090525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a455c91ee4000e755a1d48da0729064bff1e4352fe5fdf155fb3e1989bc8290a`  
		Last Modified: Mon, 22 Jul 2024 22:42:51 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:4f7234e156142e345f73359ed49794349296d08a8bd05980991ce48b87c04a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361875e293f406ee1befcd065ad807bc18a93f1ed7f7d5b7597e02b9f62523e8`

```dockerfile
```

-	Layers:
	-	`sha256:0a3f839e7958051db727a83393b6d129a6a09f36cfe720b58b9fbcccc65538a9`  
		Last Modified: Mon, 22 Jul 2024 22:42:50 GMT  
		Size: 18.9 KB (18908 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:cccf73939e96e4873bf5ccce176813f1730dc04ff58091fcd4c79a497753f655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 MB (379020016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8a31b8c69138a1e164f1c2104ed0345dbaaad44bf387e971fb5f7b8cc84b4b`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98b19c7a350c0cd13610a34d9ca7ecb2491895327b24e7a8aa6c8e93c31678e`  
		Last Modified: Tue, 23 Jul 2024 02:42:57 GMT  
		Size: 214.3 MB (214264729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1b53a97dc18032a6a51fabde03c1ff03c9371f6abfc944ef79f39957a8ab6`  
		Last Modified: Tue, 23 Jul 2024 19:46:57 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f67a5a9c3a5dd8adf525fac9ae147ebe278ef68a5d732d6454e57a3d4764aa5`  
		Last Modified: Tue, 23 Jul 2024 20:14:15 GMT  
		Size: 15.9 MB (15920215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56ddb7e978df33a05ff4a04a1ca5eb221cb29c248d3005a8b65de7e33b3aba6`  
		Last Modified: Tue, 23 Jul 2024 20:14:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:7d96e9d963ab8560db091a0b7feb8e94d220679ed2658c0cd5ee0007311e1670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15441287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc3bf54c2d7538f6786854986502daa34cc98c4d3e3c063db4004ce0e5960b1`

```dockerfile
```

-	Layers:
	-	`sha256:ca47f98b643a78a56905506ed468e79465377b96b65e5cd4c29999c255a92d4e`  
		Last Modified: Tue, 23 Jul 2024 20:14:15 GMT  
		Size: 15.4 MB (15422198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab3de38e5b30421ee30426d49b5eac2c9dabaef6037146e7c664c38dfbcd1ab5`  
		Last Modified: Tue, 23 Jul 2024 20:14:14 GMT  
		Size: 19.1 KB (19089 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:f9d6cfcb42535312bb3eabed8e72753b603d18e072775434afd1e165c46317dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334590331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e6b56cd54d32e49f3b90dcf8f2ae3dde268bf2becc197d673356b35d8765c1`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f11437a649236e2e47148907f7f8038ee2ae1c54cb67398c9bab566828b04`  
		Last Modified: Tue, 23 Jul 2024 03:15:09 GMT  
		Size: 183.3 MB (183265308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda389e8329e5a63b88bb9676bb65ba5ea9a92ce7534390e0ea64018a7ab3eba`  
		Last Modified: Tue, 23 Jul 2024 22:23:31 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9547b163435b10e85c09cd1161616c990ccff879718c23da58278725eb17c1c`  
		Last Modified: Tue, 23 Jul 2024 22:53:35 GMT  
		Size: 16.2 MB (16219330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea35144623dede2015ddd94cf69054e6fb833a6a22144ab54bd50f55e007d65`  
		Last Modified: Tue, 23 Jul 2024 22:53:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:dd5ae6a49ee6565dacf623dee9260faae882c04189ed9217e27756e65bbab387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15278052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb286d440fffab563c205b41a82d0d6c08b348df7cf3d6f6466a157a3204316`

```dockerfile
```

-	Layers:
	-	`sha256:c133f73aebb7602d1471b6a56c4cfe1ee84e3a2f9ad367b11dc49e3b08a4c24f`  
		Last Modified: Tue, 23 Jul 2024 22:53:34 GMT  
		Size: 15.3 MB (15259036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b19d8f5f75825287863bafb2236b435c00ffc7b6a1c1eba6eed7cddd3918ccb0`  
		Last Modified: Tue, 23 Jul 2024 22:53:34 GMT  
		Size: 19.0 KB (19016 bytes)  
		MIME: application/vnd.in-toto+json
