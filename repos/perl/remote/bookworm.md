## `perl:bookworm`

```console
$ docker pull perl@sha256:476785af8ec7de8633476a4789f353080717116d7ebfbcd4f938ffb107624ca1
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

### `perl:bookworm` - linux; amd64

```console
$ docker pull perl@sha256:2aba67d6537575c803ef8953f50e4643da1711d401ade6fb6786a182edd43662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364942180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4a7a7570ee43969d99e4eb606db686e4d22939e4eb5a1cba927dfa7cfe25a9`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3873416e6a335157d669c6193a256dfb289331d669d87f200e4eed1f19f9ebb9`  
		Last Modified: Thu, 13 Jun 2024 03:49:40 GMT  
		Size: 64.1 MB (64142031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a142b8b0e695954ed154c13c098ede4e217dcb99aa7158e34361604191822bd`  
		Last Modified: Thu, 13 Jun 2024 03:50:15 GMT  
		Size: 211.2 MB (211206915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e9650f84195f1e4c78065dfb6fe7aa3414a88175c5e389117c7a539d086269`  
		Last Modified: Thu, 13 Jun 2024 18:37:16 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480da13203564e2c68f72cbbb4e67d758df6389657f6c6973ff0fd89473bd7ad`  
		Last Modified: Thu, 13 Jun 2024 18:37:16 GMT  
		Size: 16.0 MB (15966312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb11c197442b296edbdc5b2eb06bf0d8e983e68e7cff769ef1b0b61fe1cfa8f`  
		Last Modified: Thu, 13 Jun 2024 18:37:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:fd32e3ad6e7dd61c98a77486a17b7fca5c0b82a5428928ab0feba83845acd516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15387654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3cfa312bd584b898f049fbc62d62b3ca0d43d3598cab39bfa1cef3d790d9ce`

```dockerfile
```

-	Layers:
	-	`sha256:1fbb669ad5d052ca9726889b758017c881540d6586c986da334c86200ca3c2fb`  
		Last Modified: Thu, 13 Jun 2024 18:37:16 GMT  
		Size: 15.4 MB (15370509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a04a609c5caf0eb78cc53f7484cc59d7efac9f4739e670a1eaaa1cff1b7c8bb7`  
		Last Modified: Thu, 13 Jun 2024 18:37:16 GMT  
		Size: 17.1 KB (17145 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:cc2e700479e169df0bc45488da815d0966653e3a423f4fc787d5ccd43152dd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.3 MB (331349198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887aeef3b431fb6334947cd16d3c43cada34c39c038a9361c93d5472e49bf461`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:ce7f1a42beaf6b57d9cd3b9b043cd6434d5b8da1315fee8cac2cd6fc2e7cc981 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:ba68704cd532bca61f763f11a4142906ee2aa565b2583052f6ddfff3fdf96b74`  
		Last Modified: Thu, 13 Jun 2024 00:51:14 GMT  
		Size: 47.3 MB (47338510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb056c8f4290f2ae7f12204b417f783b3346fe7fee14a5916fed571483b57f89`  
		Last Modified: Thu, 13 Jun 2024 01:24:01 GMT  
		Size: 22.7 MB (22728300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f981a74b01c05f914b1f13564a2cf75fc9471592be602f7b699412e5a62b8d`  
		Last Modified: Thu, 13 Jun 2024 01:24:23 GMT  
		Size: 61.5 MB (61517456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0475d9394b70464b90e234102b87625699171564d5f8cad8ec2f1d4de8fae2`  
		Last Modified: Thu, 13 Jun 2024 01:25:04 GMT  
		Size: 184.5 MB (184522344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6e6134f0eb07c4d391eda6f1d703f51d140816d7fe5fb51a7ecd0630a0635`  
		Last Modified: Thu, 13 Jun 2024 15:50:27 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ffc7f7c3d251f8d4881437ad36b8543d889d4726a02d3a4c87a567d2735686`  
		Last Modified: Thu, 13 Jun 2024 15:50:27 GMT  
		Size: 15.2 MB (15242322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3c571e5a8f7ad462eafe83d5dd00a30939beb7735c5e7ad62db225dabbb3b8`  
		Last Modified: Thu, 13 Jun 2024 15:50:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:e4b81c9fd48b067b464bcde37cd16cac68a3b3b0ec519d93c0391a95498c2c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a923c470d607e2769012f0439f99da552af55a3e2433bf0ed91662cde8b3627`

```dockerfile
```

-	Layers:
	-	`sha256:89921318f5167e28a10250fbbe394810438e4fee9ac543803f1134472e4ff920`  
		Last Modified: Thu, 13 Jun 2024 15:50:27 GMT  
		Size: 15.2 MB (15170919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ab49e0d975d796dcd161d34cfb33316d6fc0125990360754960cb82ea8a1bc`  
		Last Modified: Thu, 13 Jun 2024 15:50:26 GMT  
		Size: 17.3 KB (17263 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:325fd727ba6f9af8b3b76eee6d454769ee9c99150a6ebfa842d254734b89f1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316553837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f72facc7665b8dac864cc039f15a2a95d2f17547830fb882cd42c083732131c`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba09d7f8a9b10217e3ad0b9a640e8644b91701e59675c4e2443e6e4f8eb69c72`  
		Last Modified: Thu, 13 Jun 2024 01:33:24 GMT  
		Size: 59.2 MB (59217226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21d8970e0ba89fca18dc8a8432adc4570843d9db8e5e79d0ffb8099ce62748f`  
		Last Modified: Thu, 13 Jun 2024 01:34:03 GMT  
		Size: 175.2 MB (175175030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5497d94fb712f3ae4038c6a72f46a641a93311b7fe781255b11231bdb6231a63`  
		Last Modified: Thu, 13 Jun 2024 20:10:03 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0eba1b3fc76ab25f7ce7a4e74aecd4de413b625e77888c8afb285377e136cc`  
		Last Modified: Thu, 13 Jun 2024 20:10:03 GMT  
		Size: 15.0 MB (15032496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf1fb37e466c3d0652d43a8310c2adade45193e85a4a9774349e8f83b473e0e`  
		Last Modified: Thu, 13 Jun 2024 20:10:03 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:78aab3e1b8bfebaa87f96c657037857a86b7bddde6bd1b7e173f410dab09c931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15193656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131fb6d90218720218c2c0f49e7a561c57f4b6db38cc08f7d46439f6639e5381`

```dockerfile
```

-	Layers:
	-	`sha256:4110f2d06cedb8fb9e024de251c6a2fc5d812a0a7e6c60e44b816491dae26902`  
		Last Modified: Thu, 13 Jun 2024 20:10:03 GMT  
		Size: 15.2 MB (15176393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:784d342fcf5fe64e26e51fc11ff0f404cfaa22cd6ea4252629e50278f8adf248`  
		Last Modified: Thu, 13 Jun 2024 20:10:02 GMT  
		Size: 17.3 KB (17263 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:1fa47ff7ef0fe8bf884fa5fb2158f2e50b0b41759cb9dd7194e1035d00d5c42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355710058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9408736b653df8d5ee99404ea5bd2517c279fe13aef00235198622d1b8ceab8`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cd5f8f608f832afd85dc82fbac4aea05183fd7fccf555dd4a53a4bbe06b013`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 64.0 MB (63994737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222cb3bce424c387cc9f91f975242473b8be06d3426252fad4895105c051ad28`  
		Last Modified: Thu, 13 Jun 2024 01:31:02 GMT  
		Size: 202.6 MB (202593329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d267ab3eaff8be5ffbb0d28a1110a335d7368c1cbf004158756d6bf9fca2bf8`  
		Last Modified: Thu, 13 Jun 2024 20:07:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6eb86b9a4765401777aabb15c1984b34b3f79efabcc02b80314274c9db06a0`  
		Last Modified: Thu, 13 Jun 2024 20:07:14 GMT  
		Size: 15.9 MB (15921753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b459eea700903b42be3de65cc1387a8557f6a9fce1375046b041d2c4247f5dcd`  
		Last Modified: Thu, 13 Jun 2024 20:07:13 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d3494a7f8065d2fb3d80cd67f3b87a8ca4ff7ca41c3c4f41fd39313fddc3a1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15416665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1a4dfd80fc08c178c4286da38bd68be948528160be7ae16b0dcf3a5db037fc`

```dockerfile
```

-	Layers:
	-	`sha256:a63c8928e6f6de8f4ca981da38658d84b7504d732b81f58a9294e9312f89cece`  
		Last Modified: Thu, 13 Jun 2024 20:07:14 GMT  
		Size: 15.4 MB (15399137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ea11b27755ab0cb8d6595388ab9a266718895ad91dea595c1b665c60bc1b4e`  
		Last Modified: Thu, 13 Jun 2024 20:07:13 GMT  
		Size: 17.5 KB (17528 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bookworm` - linux; 386

```console
$ docker pull perl@sha256:3985e3ec7aa1a5b435c0627549138dca705811fd23359419bf7ba79c7842b9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.1 MB (367068688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7185fc16d9143d1382b17a77e25f80ff2ae087e39847025d7cdaf3515d7b3734`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cee71c1fc4977c82dc6f4660b13a8b8f1be5e2c7784dc4f73433486837241c`  
		Last Modified: Thu, 13 Jun 2024 01:18:48 GMT  
		Size: 24.9 MB (24888472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a9e5ec3fb52acd5155f108c6f26d0a120522c7123cc28a08b50ccc21286f53`  
		Last Modified: Thu, 13 Jun 2024 01:19:13 GMT  
		Size: 66.0 MB (65989018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba812ec2feb1a698e5c5b1fda0a47d8bbba6cb3f887e520925c9fc376b01836`  
		Last Modified: Thu, 13 Jun 2024 01:20:01 GMT  
		Size: 210.1 MB (210128099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66726c5ee63a9ffb897f37dfd77664ad2b58186068a6da852ec433f1bf0ec281`  
		Last Modified: Thu, 13 Jun 2024 02:08:04 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdadf4a50df0554801304ecbffbe00b3e05a00be244fe1fab59b9991971376aa`  
		Last Modified: Thu, 13 Jun 2024 02:08:04 GMT  
		Size: 15.5 MB (15460385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023a5c6860168a40679c37a5ccb0a239566d957e5fb911ac36c469cf4dd5c973`  
		Last Modified: Thu, 13 Jun 2024 02:08:04 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:541ce7a1f0905bc84c37d7adf242881a019f318a9c4c509013ee49a699ad27ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15366632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1eed7dbbc78a08c4c66ddff616e30d246529a310ad0c4987396530a81aeb3c8`

```dockerfile
```

-	Layers:
	-	`sha256:340c313f862aca9da88db80aa31ab4249aac087e26543dacaa202fc1af3ae084`  
		Last Modified: Thu, 13 Jun 2024 02:08:04 GMT  
		Size: 15.3 MB (15349546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8beb4d59067efd64c0af38151e66d6461d1afa868172b6defe5927cb0ffd5f1c`  
		Last Modified: Thu, 13 Jun 2024 02:08:03 GMT  
		Size: 17.1 KB (17086 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:d4dc0f5470bbe4008a6259db79e10adb7531b96e6c6d6efc6aac561d85bd2d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340929199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd82fa0f06ea87033b9a211853043c70e6190552a5ca3f33392abc119cb429f3`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:c1871631a2828ac765a04bc2cf8d2d9709cd81730d4ce46e403f4d0dbeff9dbb in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:6cf4285917f60eb7d02ed62b32504e18b0ca84bfd90c36a0b39f6eb520741b6a`  
		Last Modified: Thu, 13 Jun 2024 01:21:11 GMT  
		Size: 49.6 MB (49582735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adc1137b694767cc0d09b98cc14d61f1a91b811b596506348d0673d092435b4`  
		Last Modified: Thu, 13 Jun 2024 02:36:03 GMT  
		Size: 23.4 MB (23438130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1c3c99bf43fc1ee7e418fa6f18cd0021306408228bbe2acf6511535380acad`  
		Last Modified: Thu, 13 Jun 2024 02:36:56 GMT  
		Size: 63.0 MB (62968443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4fa6ba322c491003c606d39495f780d3353477768a903cb773ce91522ead7b`  
		Last Modified: Thu, 13 Jun 2024 02:39:05 GMT  
		Size: 189.8 MB (189770239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9ab427fa93e2d6e7ef5f7e0b838fe580d253ee1062ae5b37040039cb58337b`  
		Last Modified: Fri, 14 Jun 2024 01:38:20 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8186479053aa08904076db509994ba524f5fcc92892b3b82aa72de7f22d7bcdd`  
		Last Modified: Fri, 14 Jun 2024 01:38:22 GMT  
		Size: 15.2 MB (15169384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1878c307d433b26cf99844ad760c66ca381d7cf98cb48931442f6078d6a2eb89`  
		Last Modified: Fri, 14 Jun 2024 01:38:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:16007c7a72e8c11b52567448552f4b70138c356564dc6b01654aea85b3f7fdf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568d6bf35b713c5243e39008c9d6df799635c446f71ff844ff499b393ac85a5f`

```dockerfile
```

-	Layers:
	-	`sha256:e30a7018a409043e58063c066fdb12d6fa569de68fccd6f94d8f8834c9de8411`  
		Last Modified: Fri, 14 Jun 2024 01:38:20 GMT  
		Size: 17.0 KB (17036 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:22fa5d9fbcaeac2066e67fd15d1167435e90b0b8e7e2c6a33a42dac61fcc7c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379063385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0bb3a7393bc680906cfa9451d149668f9631adb02b3a0c9bc3c29667a17ef9`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:5b31953e08477fa1771514ef5fd326ae78b7c4ad417cbb64755ee493634ab392 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:7e04e800a5f6b106e3f1cb53c3677b55297b3841c160edc0f657f7a27ffb9ad0`  
		Last Modified: Thu, 13 Jun 2024 01:21:03 GMT  
		Size: 53.6 MB (53579678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4148242bae3618c54f03447132a7364c4a46c509d204908b4d8b569f2cbbf18d`  
		Last Modified: Thu, 13 Jun 2024 01:59:41 GMT  
		Size: 25.7 MB (25699643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0038ae14b2277791270ea7736f896040def15b2cfcc8a74ca0cfd14349e968`  
		Last Modified: Thu, 13 Jun 2024 02:00:03 GMT  
		Size: 69.6 MB (69583876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb32bd190e0cb532461d35afe27a691f4117106df93f8222c22c3c037b8b006`  
		Last Modified: Thu, 13 Jun 2024 02:00:56 GMT  
		Size: 214.2 MB (214235513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561b4f5e8980caff7dfbe370a498c1e9cab930b0149613afbeafe3780bd74938`  
		Last Modified: Fri, 14 Jun 2024 01:21:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb465ecb2802ecd20b52b5f3a5c3477e5e8452ba70fa459f78f1775f8ae8917`  
		Last Modified: Fri, 14 Jun 2024 01:21:43 GMT  
		Size: 16.0 MB (15964408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecec3f7754f07ec2a2cab809270bdf5ec772fc461b3148d2e983b56b111f187`  
		Last Modified: Fri, 14 Jun 2024 01:21:41 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:b4322110a16e56aee5a1d610cbce88155cf5a71365d3ee649f240172919d3db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15364438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8846dd890293c27ae74cc58504e1f379541a8f56e0d0998beb0c40785c5ae668`

```dockerfile
```

-	Layers:
	-	`sha256:0de42c60e5dc559198daca80a1214abcf3b4ca0902de125b141d18955756712d`  
		Last Modified: Fri, 14 Jun 2024 01:21:42 GMT  
		Size: 15.3 MB (15347219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c3ed1164f7a395fd22ebb2af6682f4d4cf625aaea1b65077cf245509d6544e8`  
		Last Modified: Fri, 14 Jun 2024 01:21:41 GMT  
		Size: 17.2 KB (17219 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bookworm` - linux; s390x

```console
$ docker pull perl@sha256:e3dc2fff0a5b3293d0192b351ff09938fbff641de05f7e4f7efa5707ef1cf67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334655738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1ae719d91aaec6cb53620d12b4270cfa7ba40d4947bdd9acc5ddbaf626d1b2`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:42:19 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 14 May 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:20:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:21:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c304d55d9ae47fcef54a6044634995ffbdbd5e4d3e409198127615b4043fa8b`  
		Last Modified: Tue, 14 May 2024 01:29:23 GMT  
		Size: 24.0 MB (24046857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943219d44d0b66fa3c53413ccd4b689951925725722eba1e47eec984778d3640`  
		Last Modified: Tue, 14 May 2024 01:29:39 GMT  
		Size: 63.1 MB (63130182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dd19c695c401ade3f0a1af6a11007c474b68b17b925095492dbfc5a8f2a538`  
		Last Modified: Tue, 14 May 2024 01:30:07 GMT  
		Size: 183.2 MB (183236787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1096c1a2e6edba763a77cd4c09fbaf0ac50d71260f9babadd07a09106bd365`  
		Last Modified: Mon, 10 Jun 2024 21:09:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53106f63d9a8af32aa860fc8d7882de98bdd3c1217107ab327967131d43f148d`  
		Last Modified: Mon, 10 Jun 2024 21:09:13 GMT  
		Size: 16.3 MB (16299455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75621ffe87d4c51e649c65648c95ea2f955f14c3f4e1fbd1befe269ec81dd194`  
		Last Modified: Mon, 10 Jun 2024 21:09:13 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:69511592b4714d36de08792e437b9b789a891d1eb92b39585dba2f50e43b0d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15202335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e887c73b36142440d3caae6eaa2215a140380e9e227a8dc2e51a6e43d23840`

```dockerfile
```

-	Layers:
	-	`sha256:ac621a9e9d3e816c7e214564887282ab0d0599e2a4af7a7379f0131032adfea6`  
		Last Modified: Mon, 10 Jun 2024 21:09:13 GMT  
		Size: 15.2 MB (15185191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3e0a2063fc629d03b31a92c0f3d488d69607b016a47b614053cb6e976bad478`  
		Last Modified: Mon, 10 Jun 2024 21:09:13 GMT  
		Size: 17.1 KB (17144 bytes)  
		MIME: application/vnd.in-toto+json
