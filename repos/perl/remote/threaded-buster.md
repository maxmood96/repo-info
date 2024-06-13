## `perl:threaded-buster`

```console
$ docker pull perl@sha256:43a8e76363442b8d2eeaea3c606e34e812e0ba0183582617af303815e3aae39a
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

### `perl:threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:0d3cd80ec530cb5c17dc73695626c9d0cfe11235191985260eb2b9e6709aaf42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.1 MB (328121601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e147ee6da5f7b80cd3cae1b135938df13bffd8e620f00de09c8172f7d40cbc11`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:82f06126089fd0ca482c29baeb90ef37ac3a9f5f6a0f2f5c968a605846627d47 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:3892befd2c3f36ceb247ba7d906de12601d69b806597e65c4c837cf3d93df119`  
		Last Modified: Thu, 13 Jun 2024 01:26:34 GMT  
		Size: 50.7 MB (50657373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ab8bed435ee0e35413bb45d14dae2283dc0841644d881be35089debdc88cc3`  
		Last Modified: Thu, 13 Jun 2024 03:51:25 GMT  
		Size: 17.6 MB (17586423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a567eb2264b60aa779a5bc8f8f4dc7a6d3e1e01d8f5d1bcd039ed444d91a408`  
		Last Modified: Thu, 13 Jun 2024 03:51:40 GMT  
		Size: 51.9 MB (51895667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be81a73cfb7b45f4634965206adaa318a889f15cff6ced0ffd70f7c2d851fe4`  
		Last Modified: Thu, 13 Jun 2024 03:52:10 GMT  
		Size: 192.0 MB (191957999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02cfedd8624a78716a985373d3896f7ac801513051a89824f730d2171fb7893`  
		Last Modified: Thu, 13 Jun 2024 18:24:28 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fccc84f47627efcd72d8b8d62012d0bdf72a6b5f026acfc8262ad226f85817`  
		Last Modified: Thu, 13 Jun 2024 18:24:29 GMT  
		Size: 16.0 MB (16023873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23ff7c6b73700a29f055e94f7044899bdb57e565867ff517db0d577638e0d61`  
		Last Modified: Thu, 13 Jun 2024 18:24:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:7c960c40016243e066e1b52511e28082213918e186e417c197f834f6ba0b7360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15982285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea01dd3e950e4bfdb26b2e1705b722cdc2f53033b7127d813055cefbed67a56`

```dockerfile
```

-	Layers:
	-	`sha256:809625c993d9634547052e81f72ff4d07541795ae477919307438b389fa3bb4f`  
		Last Modified: Thu, 13 Jun 2024 18:24:29 GMT  
		Size: 16.0 MB (15966491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc745effed5a376598cc04b4a189f71dcefe2d81b9a96a64c3142760320f58fe`  
		Last Modified: Thu, 13 Jun 2024 18:24:28 GMT  
		Size: 15.8 KB (15794 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:b5e0af3b7fd888f88e7ce5dfe0eb271452ac7340b920b09067dca3c8fc12b6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (293024515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154a2e6288abb0d72088d0c362740410c2b354bfee28ec7ca115ece57b14c46a`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:a412a8d68ab5b47e51cbbb8ae3797bc960802ae45716dda9d517985663677bd1 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:36ba9c8baad7d50b1a4b523006966a56ab736274cf5108a528d21b65d3e5927b`  
		Last Modified: Thu, 13 Jun 2024 01:02:44 GMT  
		Size: 46.1 MB (46129853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde0a02dfec0ceee2c7c23d86d1a306cffd3a1c9b4907db8b4fa768c14abd3ad`  
		Last Modified: Thu, 13 Jun 2024 01:35:26 GMT  
		Size: 16.2 MB (16216998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38716c4e5c9c098df6d6fe31c91df92948117751c7c1013c686dbf50412911c7`  
		Last Modified: Thu, 13 Jun 2024 01:35:42 GMT  
		Size: 47.4 MB (47411218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dab4bbcbf00be5a105a2cebda6ada1b414a3d28291fd966b1738ab058d8851e`  
		Last Modified: Thu, 13 Jun 2024 01:36:16 GMT  
		Size: 168.2 MB (168170017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2260ff5dc3fcbaee3564d05baeba7024b97903388c1a82ee7545fa3a2624023`  
		Last Modified: Thu, 13 Jun 2024 20:23:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4389822efd28e6b6b094041729c7e3a9c348858bdbdf2318e1da782bbedaef`  
		Last Modified: Thu, 13 Jun 2024 21:03:17 GMT  
		Size: 15.1 MB (15096163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a76eb707c2779f9b305e6a6ade9ac8ce4661ea98a7e6936a8cc770646bb93`  
		Last Modified: Thu, 13 Jun 2024 21:03:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:cfdf9b5a4a9a77b735abc7653991a5f718343325ba3e2265a2ef97602d4269e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15784521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b374253480336d5ae291d39efc4b6ec7655aaac3f473b12341b5e6380ae17ae4`

```dockerfile
```

-	Layers:
	-	`sha256:f4b8e8100d2f463a8f0af4f2e224871f88ad5e65657a2d4db777c8ca2099b0aa`  
		Last Modified: Thu, 13 Jun 2024 21:03:16 GMT  
		Size: 15.8 MB (15768649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcb68074265d389ade155a03de8ce837722be71b075415f49653d00a6954f2a`  
		Last Modified: Thu, 13 Jun 2024 21:03:16 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:ac7da9e007a0b3a6fc7ea65f8abfe2aa057d70434c298053290f5b0073feb6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318616078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685b41c3a0adeb34e23fbede518dc80a4c07412e34c8437cf00b44e400048354`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0606e294c7cef3e3fc7bdc4e83c5d17bd0ef8ae487db37628efb49fb6a03ed2`  
		Last Modified: Thu, 13 Jun 2024 01:32:04 GMT  
		Size: 17.5 MB (17457043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afdcf6433347dce5e44f4ff0bc3de90b44a9fa538fa39a22d9b21f9ee5365d4`  
		Last Modified: Thu, 13 Jun 2024 01:32:18 GMT  
		Size: 52.2 MB (52231551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d462078a4e654dfe4d03086b828f77c76e47c0d5d14062aab137912bd0047683`  
		Last Modified: Thu, 13 Jun 2024 01:32:42 GMT  
		Size: 183.5 MB (183534120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352f4767cc10fe7b5671ba3cf475623d3ba044e75f977ebb3e3485543aaa5aff`  
		Last Modified: Thu, 13 Jun 2024 20:17:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548354ed1085f77107fa275808569cafd134c90417e588e73e959ae6d43340d8`  
		Last Modified: Thu, 13 Jun 2024 21:01:10 GMT  
		Size: 15.9 MB (15939839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216fa5d2cb1d12ce4d7bd70a2986f960df9e7dbc9a2795d2a44c77ee9a06fc43`  
		Last Modified: Thu, 13 Jun 2024 21:01:09 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:03c6130a46e50bee3a2bdff8806a8d17c25e17b3e2bc37b21e8da776241efc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15973521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa7834c5daf114908a84b09e20627e9db75ee53620c0eda5e759566bf9ec74b`

```dockerfile
```

-	Layers:
	-	`sha256:3bffe4007a1381d9bdc973b3e1f8a1d8c45f373da6dc69035b9b73a30380b69a`  
		Last Modified: Thu, 13 Jun 2024 21:01:10 GMT  
		Size: 16.0 MB (15957405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84b2e66c4b8a6d4d56a21870822a45335d707ea630f9702afe781f227578dc0c`  
		Last Modified: Thu, 13 Jun 2024 21:01:09 GMT  
		Size: 16.1 KB (16116 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:9a5be491732f1759585bd87571c83997d89b4b2301d4cedb50ec40a7fa7a7796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337076389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3fb235104a0a64fb617c73746226b60431a3b57c18274e90e24bf166542095`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b199b6fd9cf013c26330a6ba185ef8be1adf3ec49220a3d9f496e533501402b`  
		Last Modified: Thu, 13 Jun 2024 01:21:27 GMT  
		Size: 18.1 MB (18098294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8cbd7f32e12d211b1f55f9163945f9210759618d50cbf096e4b934b9cfb2b`  
		Last Modified: Thu, 13 Jun 2024 01:21:46 GMT  
		Size: 53.5 MB (53491704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40f693ac8434364b7489c467dd31e0263396e4e0f3102204854d8530f11116f`  
		Last Modified: Thu, 13 Jun 2024 01:22:28 GMT  
		Size: 198.5 MB (198491652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bb0a153d80d1465ff627880d972a12ee63acc8c2f921afdcd58d6d9e17b72f`  
		Last Modified: Thu, 13 Jun 2024 02:13:42 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f389ef6e657e38409bc665dc16adbd930909862d9413ff07bb9e258cbe8bd78`  
		Last Modified: Thu, 13 Jun 2024 02:13:43 GMT  
		Size: 15.6 MB (15574559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ee83c45c680cc1347356515f3c89aad9f3275e08a584a543b535a708a65825`  
		Last Modified: Thu, 13 Jun 2024 02:13:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:0b3e6767e545c95e4d88af9dbf75be8d2b1d7cc79a7f2e776d22fcb4c7f54385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15987832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13e1522eb3624458462e049836a9f0bc6bd5f4819d086075a080484b35b22a1`

```dockerfile
```

-	Layers:
	-	`sha256:c4f3ec80beae34f095458199f4626840f4d89f1aaf82423c282b319775e690b1`  
		Last Modified: Thu, 13 Jun 2024 02:13:43 GMT  
		Size: 16.0 MB (15972073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22aed7f088003c982ab87d6304e9d7eb5eb8b9e43fb945f2c932dc6139eb07f8`  
		Last Modified: Thu, 13 Jun 2024 02:13:42 GMT  
		Size: 15.8 KB (15759 bytes)  
		MIME: application/vnd.in-toto+json
