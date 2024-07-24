## `perl:devel-bookworm`

```console
$ docker pull perl@sha256:8dbeedbdf5f9c323af756a83d65a251332b1154632d4b444adaa0b080265fe39
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

### `perl:devel-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:656f654af4805dda957508f19199db787d24e4a6d3da50229f8125f9c6fff417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.8 MB (364816050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6949c2f7cb7282d4a0df1e4731dd04b33ad0b5bf22356c1e20cf5307c0bb60`
-	Default Command: `["perl5.41.2","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
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
	-	`sha256:a26016228cef6751dde4b7d108a34e5ea20809e0ee38f788bba3e6bda9d777d5`  
		Last Modified: Tue, 23 Jul 2024 07:29:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d1e0c68884d51224bc9b11f5d5356f5ae8e60a157231306ae93350122ff1ae`  
		Last Modified: Tue, 23 Jul 2024 07:29:04 GMT  
		Size: 15.8 MB (15826105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2037662b6df7b07708599db16965763cc788fac130f4bf522efe89693ecff3ea`  
		Last Modified: Tue, 23 Jul 2024 07:29:03 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2e4ef27fee616c174b4e6af5e687069f526fa4aacf5a0b8fc6e9702172d79e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98983d95949af43f9cb44a7c0b3c47ead803713741bfa19c0bc85072140dca0`

```dockerfile
```

-	Layers:
	-	`sha256:fa134b6150831941e2f584b70667c374ad637bab816615344828b891395f0f1d`  
		Last Modified: Tue, 23 Jul 2024 07:29:04 GMT  
		Size: 15.4 MB (15444293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ccdac1e186ae4a7069900f2c66da00c440666ec04bff05e1ef004b8e3c9d423`  
		Last Modified: Tue, 23 Jul 2024 07:29:04 GMT  
		Size: 17.7 KB (17687 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:2c91cb4cc69de52b089bf2ff5ad1ba9126256b4c828e41f2afce2e00c6655ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.2 MB (331205097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63340be0e59d7ade61b843f6209f23f6a6c6313ef72bbc28457460fecde170e1`
-	Default Command: `["perl5.41.2","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
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
	-	`sha256:6e4ab772f0879fc32359a8c741913d0faf784072cf3a9797e66941d37378cbfb`  
		Last Modified: Tue, 23 Jul 2024 23:41:35 GMT  
		Size: 15.1 MB (15105179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e4252c37512d3bbba01118d7edbcabe3dfbf57dccf24f8e2cc2ab60a89788f`  
		Last Modified: Tue, 23 Jul 2024 23:41:34 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:5d3bc8596a20d85f6619677cb93516660603e4cb53b054ab4d4f7424794c9710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15261443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be94ab95c2f785e355a21ac92bccea1b8256496b82364d9e60f09b07fa7561d9`

```dockerfile
```

-	Layers:
	-	`sha256:82864abd3372cf1ec0f64cc4755b5e31ad9643967f41ce7d5a9a0dd9eb557fa5`  
		Last Modified: Tue, 23 Jul 2024 23:41:35 GMT  
		Size: 15.2 MB (15243670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8b0650f3ad6b30dc9958dde4cdc5adc9164e1329adf14187fc0d51cccafa30`  
		Last Modified: Tue, 23 Jul 2024 23:41:34 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:37ba853566c14e9d269a62ab453909bd5a72fb14bc7779de24d4410da887d0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317305416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0ada94190268953abde9243ca64b71f216f4b9477873cdacda565790fdab65`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 00:59:52 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Tue, 02 Jul 2024 00:59:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:24:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:24:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:25:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/perl
# Wed, 03 Jul 2024 14:39:46 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.1.tar.gz -o perl-5.41.1.tar.gz     && echo '7dee38af601b0ba3f3730cb812cdbc799c921da440cb0ce96dd7a4f508b1a6f8 *perl-5.41.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.1.tar.gz -C /usr/src/perl     && rm perl-5.41.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/app
# Wed, 03 Jul 2024 14:39:46 GMT
CMD ["perl5.41.1" "-de0"]
```

-	Layers:
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa30b2bcbde45c2fc67abf425197af3af3e67d55296f168143343ef1b0e2d3e`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 22.0 MB (21954038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4650a14deed524a46f7f7b410ff5d81e5ff66e51c7345e2b05887b6e3f4030`  
		Last Modified: Tue, 02 Jul 2024 01:39:24 GMT  
		Size: 59.2 MB (59222408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ceb3cc12c0338c85a0602b703f838a13aa2e232ffde0c008b8db42bec79a26`  
		Last Modified: Tue, 02 Jul 2024 01:40:01 GMT  
		Size: 175.2 MB (175164748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4569fc74283819352c34c392776cb2b376d56ce3768e7ca1150d980c753ee2f7`  
		Last Modified: Wed, 03 Jul 2024 16:16:06 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fa7013a4a5d1b23d9b3ba4b0703fe713e41d87606633d44104154bf5ac3022`  
		Last Modified: Wed, 03 Jul 2024 18:57:30 GMT  
		Size: 15.8 MB (15815857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10356331de6d4959072f20bc50c201cd937ad02b375d82a198ccb1380d28270`  
		Last Modified: Wed, 03 Jul 2024 18:57:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:0405f457ce0113fc792a4039598ae9cebb02597375b5a434585f5168b859e9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15189064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65c563588eddf5ca847ec07e78af3d1a89b197e2c228df290e6f1db319675d8`

```dockerfile
```

-	Layers:
	-	`sha256:39b4d6d05de6f761251f918af95a9cc1dfce198d85225127154c56cfca263ad7`  
		Last Modified: Wed, 03 Jul 2024 18:57:30 GMT  
		Size: 15.2 MB (15171410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d71e591dc75ee7e4e1d8d4652ccbf0d815e20a80674405e722d9d64121e6b189`  
		Last Modified: Wed, 03 Jul 2024 18:57:29 GMT  
		Size: 17.7 KB (17654 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:0a605311632189ce8f06d94b15243dd3e211b4bca505b3a8a6b15a830873f254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355582048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bbb21b98609a9c804d1d064bdf7382dd33cdd6dcd17758da8a2b4b216c7e7a`
-	Default Command: `["perl5.41.2","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
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
	-	`sha256:360f1ef9d25e9740801aad3d7f2ddb051db7629c705a2ebcb49a71edacf44c6f`  
		Last Modified: Wed, 24 Jul 2024 00:22:46 GMT  
		Size: 15.8 MB (15782372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294a7f2769447a0a5bd773c4ee114d71596b441f6d5da6b50ada32a3d1e28f6f`  
		Last Modified: Wed, 24 Jul 2024 00:22:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:bcf5a12a930f14005994c70158506aab33b1a3f3720341e17eff410f4f0c858e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b542c794c1d69f82c9975faada796969c4c6dc86432fdeeefd1a17150adc150`

```dockerfile
```

-	Layers:
	-	`sha256:e139cdb2ccfaf4c806579bc62d68c86b31d61e83788a5db003e9c7a5dc75598d`  
		Last Modified: Wed, 24 Jul 2024 00:22:45 GMT  
		Size: 15.5 MB (15472873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da57844b19c44ef8f313a44af2e76a918e70fff80f15a068b8ac8e839a6f2f1`  
		Last Modified: Wed, 24 Jul 2024 00:22:44 GMT  
		Size: 18.0 KB (18023 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; 386

```console
$ docker pull perl@sha256:57d42b5892ce9baa83cfa92a7bed41a890aff73ec2d059ad87742780ac914dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.9 MB (366937681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741342abfcde14b81a4210c14ee63624ef4ab02233fa00caa4114ee83f8e476b`
-	Default Command: `["perl5.41.2","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
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
	-	`sha256:114b6133e5e430589e7aecd5c67bf67e5dc6f78d8c053eaa47f66e63a5401e00`  
		Last Modified: Tue, 23 Jul 2024 06:18:39 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4f3fb362317ff27dc687f2a341a916c773ca7b8c9ed082bd22eebb167e909`  
		Last Modified: Tue, 23 Jul 2024 06:18:40 GMT  
		Size: 15.3 MB (15321201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee755ed4a4b8e290ccccd88edaafbd5c3b8c09fcbd7ada70da3cc287d3f2c7cd`  
		Last Modified: Tue, 23 Jul 2024 06:18:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:00036373383f3cbb6710da7bd0c7fd9dace6d74c67e09974d454ca72cc16213a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15440717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf29bc575ee7a24a2d88d05e495a8fcd12b2a71ce4d4239706156e09428478e9`

```dockerfile
```

-	Layers:
	-	`sha256:7caf53a8e9b24800df55866a210470c49b61cbf8359bcc50ff3a4f096d91063b`  
		Last Modified: Tue, 23 Jul 2024 06:18:40 GMT  
		Size: 15.4 MB (15423069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:748f15577e2cff84071073e282c7edaf64242dfee4b66e48212f91bcb8e07caf`  
		Last Modified: Tue, 23 Jul 2024 06:18:39 GMT  
		Size: 17.6 KB (17648 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:bf97a4cce223e6652d1a3424c2186454a0c04fb85e27f8e59e6221191985356f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.9 MB (341901800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14084373fce32f7ba1123c7cdd6abc09c43258eadf110128c27c361440e6932`
-	Default Command: `["perl5.41.1","-de0"]`

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
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/perl
# Wed, 03 Jul 2024 14:39:46 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.1.tar.gz -o perl-5.41.1.tar.gz     && echo '7dee38af601b0ba3f3730cb812cdbc799c921da440cb0ce96dd7a4f508b1a6f8 *perl-5.41.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.1.tar.gz -C /usr/src/perl     && rm perl-5.41.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/app
# Wed, 03 Jul 2024 14:39:46 GMT
CMD ["perl5.41.1" "-de0"]
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
	-	`sha256:0bda7217957229eae68e3089b29c15682988d592ceee26f8380772fdf3895363`  
		Last Modified: Thu, 04 Jul 2024 10:54:35 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a1c3c9bbc0f9f9d07402455f40cae5a342e5bdfd4f754fb0fdd3b6c7c8014c`  
		Last Modified: Thu, 04 Jul 2024 10:54:37 GMT  
		Size: 16.0 MB (15955606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e260784607b4f24b2da33b8ea464b52d85fca52ba9cdfe1e2e0eb873cebca7`  
		Last Modified: Thu, 04 Jul 2024 10:53:56 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:fe0bd2f64a591355ef072cd988919941a6ad99d5d01607f5a2630549d4a70cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007bc1795483af2e2a85aab96c27a3c719e932077467b8f6dd81e65812c227fa`

```dockerfile
```

-	Layers:
	-	`sha256:a3da8596b4452e017587b5da5bde2ff18a321075ec70eea559baee189241cefb`  
		Last Modified: Thu, 04 Jul 2024 10:54:34 GMT  
		Size: 17.4 KB (17424 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:2323529f6a50388a04695a597f9a61d97ef0987e3cf7eb06d87447373b7b3d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.9 MB (378927501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87732f182fb9b3de4c3734c84595f4e5306d763671b90de37dc1d61df59a1b71`
-	Default Command: `["perl5.41.2","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
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
	-	`sha256:30ae977af44d17f08a5953e75cd7a0e629e36a404ad53132bfab0c71c616bbfd`  
		Last Modified: Tue, 23 Jul 2024 22:25:01 GMT  
		Size: 15.8 MB (15827699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428967a1492af41923db814c57a80e48c2f501fa589636da85641a6543f6126f`  
		Last Modified: Tue, 23 Jul 2024 22:25:00 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:7b01bedc7888be6d5ebfce6bfbbbfca7f38ce50ad8e928ac7f4e14053ce9219b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15438563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab579a458c4d7eccda792836e6c9dae5c32812ff210526b31a7f8087efe1c502`

```dockerfile
```

-	Layers:
	-	`sha256:55332cedd2d07f7955723f9d590882e45161c54405e538319e1c66554b820dea`  
		Last Modified: Tue, 23 Jul 2024 22:25:01 GMT  
		Size: 15.4 MB (15420826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ccdf3d0fee37f88e5eaa070fc54a79152f2442991d52727756ce7d5ed371d1e`  
		Last Modified: Tue, 23 Jul 2024 22:25:00 GMT  
		Size: 17.7 KB (17737 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:e2b9511fc548b24ce4547a053e84f6b22e3638efd769116ecead77fb78f759ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.4 MB (335447032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30762134aaa37e3b6fe0b4c3eabc76c15274b82c5c566fc9fc25635108c078c4`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:28 GMT
ADD file:397aa43721bc5ca67ab359263843a05c62e131f07114e92f39927f59790c9a5b in / 
# Tue, 02 Jul 2024 00:43:30 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:32:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:33:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:34:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/perl
# Wed, 03 Jul 2024 14:39:46 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.1.tar.gz -o perl-5.41.1.tar.gz     && echo '7dee38af601b0ba3f3730cb812cdbc799c921da440cb0ce96dd7a4f508b1a6f8 *perl-5.41.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.1.tar.gz -C /usr/src/perl     && rm perl-5.41.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/app
# Wed, 03 Jul 2024 14:39:46 GMT
CMD ["perl5.41.1" "-de0"]
```

-	Layers:
	-	`sha256:1b8bfe08588d8939b4d39134c5c614351649e3890ceb7c234b7542f58d7bcc28`  
		Last Modified: Tue, 02 Jul 2024 00:48:16 GMT  
		Size: 47.9 MB (47931511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37bf3d98ae5de59851adab45daeaaca9d29f76110a2923bd8937c4ad2e8cd52`  
		Last Modified: Tue, 02 Jul 2024 03:44:34 GMT  
		Size: 24.0 MB (24048872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6cb3bef78d7b20f095bd16b5a39e3ffec90c96f6d1307f8672edb9deef1c5f`  
		Last Modified: Tue, 02 Jul 2024 03:44:49 GMT  
		Size: 63.1 MB (63125178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e457fb781c30f5a251f0251b0cafc815abfed65652bdecac052b60618b497a23`  
		Last Modified: Tue, 02 Jul 2024 03:45:17 GMT  
		Size: 183.3 MB (183253702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f35273966b80956490120e7c46c217ca18f1d5d5d79881d34c861652d948cb`  
		Last Modified: Wed, 03 Jul 2024 16:08:08 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241ac843b188a69913691a33929665d48cb5dc68da8ff604e4e826bc94ea2d38`  
		Last Modified: Wed, 03 Jul 2024 21:01:18 GMT  
		Size: 17.1 MB (17087501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62641c3fa0e6c6d3b5079e8bd5aea9a42a5c0d999d679ec8309a23d34d1c7faa`  
		Last Modified: Wed, 03 Jul 2024 21:01:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:762a423c5bb97d7db411ac14dcb27a9573c1b8686c50c2d0655bc10c850544f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15197808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3086f0b224d273ce2cc47b08c8506a227642de42b3ee39b5c56da62948e31f7`

```dockerfile
```

-	Layers:
	-	`sha256:dc70ff1bb6c661152de51fb59892b58203ee462e411ac1c3e6a6108efa5a87fa`  
		Last Modified: Wed, 03 Jul 2024 21:01:18 GMT  
		Size: 15.2 MB (15180240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13cfe2836fe57a35704accac005034b1e2deb7440ebbb45cdb562d2f6addd7e9`  
		Last Modified: Wed, 03 Jul 2024 21:01:17 GMT  
		Size: 17.6 KB (17568 bytes)  
		MIME: application/vnd.in-toto+json
