## `perl:devel-threaded-bookworm`

```console
$ docker pull perl@sha256:8243c272af4c09f27add64baba9f66a3adea485602d843ab1b947b31dc5e80c8
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

### `perl:devel-threaded-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:d58e66539cbcf7d28b77eb2366799f9a86c1f1c8082bf16d116b2647be61ad91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.2 MB (365175383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba0fea3eaeb56a16b36a1658148124a581b301d9113e2fa53b268aacedf97ff`
-	Default Command: `["perl5.41.4","-de0"]`

```dockerfile
# Fri, 20 Sep 2024 18:57:44 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["bash"]
# Fri, 20 Sep 2024 18:57:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Sep 2024 18:57:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Sep 2024 18:57:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.4.tar.gz -o perl-5.41.4.tar.gz     && echo '402b2e10dc1a6249685f0cda5897959bfc079fc324b551a1c4771fe401563896 *perl-5.41.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.4.tar.gz -C /usr/src/perl     && rm perl-5.41.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.41.4" "-de0"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1948034bc47af8404d0a0bc828b7b406721b5e839ef786d8e4a13fb1d3b42e1d`  
		Last Modified: Fri, 27 Sep 2024 06:19:18 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8395ca22418dbc660d027b5fe52b2cdc70932712470713ee421108d2eb76b58`  
		Last Modified: Fri, 27 Sep 2024 06:19:19 GMT  
		Size: 15.9 MB (15909053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3249964e76619200da37b730bcda56518804a225131a20812437f7099bfef7`  
		Last Modified: Fri, 27 Sep 2024 06:19:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:0016b1d5e42b8f33e3c0deebe43c8b1146510ea4249adbf86aeeff94dc7b5f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b574acdab02bf8b9f5e62f9eb926131096459b7da5aa15bbf6994e935777b13e`

```dockerfile
```

-	Layers:
	-	`sha256:fc628980a75f9925cce533f406755c2493ba3719883ebb91433a9d4b3a702b3f`  
		Last Modified: Fri, 27 Sep 2024 06:19:19 GMT  
		Size: 15.5 MB (15451409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adda230dd5e1c92a037690dbc80a0c28065af6c3ffed0e55872fe7c4e12476c2`  
		Last Modified: Fri, 27 Sep 2024 06:19:18 GMT  
		Size: 18.5 KB (18532 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:f63aeb9be9d5d459262883907af24ef82397e26b3b73979eef432c138013979c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.3 MB (331297413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37416953a342529d9261ec5487557b4468fc9ca6d130ac7ae8a11e874ef7a7b`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:22 GMT
ADD file:7ffef6fd95a7091f8058ff29f285ea1ff980523eddf5b8cbcd5ced08753075c5 in / 
# Wed, 04 Sep 2024 21:48:22 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:16:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:c9500290eb8f2377c9935666a66a6f2f71959169f4c4c62904bd950e7f1cb1cf`  
		Last Modified: Wed, 04 Sep 2024 21:51:08 GMT  
		Size: 47.3 MB (47333195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e56608de2d5e6deacba9620abd7b9b042cd77c62b1371a3f75f13a4c692e9`  
		Last Modified: Thu, 05 Sep 2024 00:23:55 GMT  
		Size: 22.7 MB (22729234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5184f06fda15989d5238dfb3324d258330643f00fd09e6f81fab9cf6e46340db`  
		Last Modified: Thu, 05 Sep 2024 00:24:18 GMT  
		Size: 61.5 MB (61526797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bcb55460b2c2b07856962a4787935d0468bccb7c9dfa177433fa022f264f26`  
		Last Modified: Thu, 05 Sep 2024 00:24:55 GMT  
		Size: 184.6 MB (184553262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e3ba8d208b54110d235a915e5311e3e81e0014a23fd9f4110543a983e36d65`  
		Last Modified: Thu, 05 Sep 2024 22:44:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680c00dac6ed2842e951abd123f4905cd548c2895a4718f44c7850cd015a1a5d`  
		Last Modified: Tue, 10 Sep 2024 02:48:20 GMT  
		Size: 15.2 MB (15154663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25061fd19432582d0fbe4cb39edb8b1bc7c6954c85e1f95a4df80a21a3b4f37c`  
		Last Modified: Tue, 10 Sep 2024 02:48:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:ae2e98b4bb09d9c6afee6e07b5a6cf487909ec1b6f9e12814133bbd68dab5c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15261816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a52db97e327ee32d2d0bc7b64e29a428b109f3992de2567fc192a932c6cdcc7`

```dockerfile
```

-	Layers:
	-	`sha256:1794d3c2cb4fcbe59fc53a52ca1cf7e2073090660b86228a049c7d01f03e622b`  
		Last Modified: Tue, 10 Sep 2024 02:48:20 GMT  
		Size: 15.2 MB (15243203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6793242a4a54d0f99c9e4a3a1e38e5202f36d0a83fcdaafa1204121b5ab36b50`  
		Last Modified: Tue, 10 Sep 2024 02:48:19 GMT  
		Size: 18.6 KB (18613 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:fdf92deb6ae1490a5cdd03a4ddb2872368d52a55c8093a3158f75eb558df38f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316487927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b81aed83b8921e33bd65be5eb3d397b2fbce3004b61e87453c4a5a0fabb36a`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 21:57:56 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Wed, 04 Sep 2024 21:57:56 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:29:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:30:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74af1f53669444d39cb60af3d8b27682f29cd813798990f2763c4a3e13530631`  
		Last Modified: Wed, 04 Sep 2024 22:36:19 GMT  
		Size: 59.2 MB (59228610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaf1b5402e12f0e97f96b3da218271b7caf2abf4a321ce82a42bedc2d72eb82`  
		Last Modified: Wed, 04 Sep 2024 22:36:55 GMT  
		Size: 175.2 MB (175209450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad618838a84324c00c7f7b428900ec35a2b687d1cdf924213ebf39fa5c17492`  
		Last Modified: Thu, 05 Sep 2024 23:48:41 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ffaad2f753950d475cf96586176160feee9f548a4ab5b6f8635eee2c0302eb`  
		Last Modified: Tue, 10 Sep 2024 04:26:19 GMT  
		Size: 14.9 MB (14943915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb1cf428f89d9dcea8f5e8f78c450ec5f3032a71b3c68144f08faee56b8b940`  
		Last Modified: Tue, 10 Sep 2024 04:26:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:59c1c5ec88ce197b6f8b1e8e6fca804ecb5cc6199c66e88fe914d00620ecbbe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea6bcd6c3c7733d87b83e88f39d24c66f20d76b0c50dbd4a68b93b3abbf5093`

```dockerfile
```

-	Layers:
	-	`sha256:e2a25b1bf80888697efee62d13dc02ec652a5e08426d26ba3f8269f9b0a6bb11`  
		Last Modified: Tue, 10 Sep 2024 04:26:19 GMT  
		Size: 15.2 MB (15248677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30cc711555f922b12824bbff3899ce56f78840c22f8e053a284318f0d79dac8a`  
		Last Modified: Tue, 10 Sep 2024 04:26:18 GMT  
		Size: 18.6 KB (18613 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:bf26569032064476c27cee6cc3d76f3e1b198bb940e7018d4fa4c87789222f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355688096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46bf5e4a249876c34fabc4989ca5ab14ca89b6a789d1d0f56f91919400c0449a`
-	Default Command: `["perl5.41.4","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:01:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:02:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.4.tar.gz -o perl-5.41.4.tar.gz     && echo '402b2e10dc1a6249685f0cda5897959bfc079fc324b551a1c4771fe401563896 *perl-5.41.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.4.tar.gz -C /usr/src/perl     && rm perl-5.41.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.41.4" "-de0"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843b1d8321825bc8302752ae003026f13bd15c6eef2efe032f3ca1520c5bbc07`  
		Last Modified: Wed, 04 Sep 2024 22:08:14 GMT  
		Size: 64.0 MB (63997467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a348c2a8d94613f34ce7d0ac4fd4e51800d8f4aa8a0bc9347fe5c8436b4c3bd5`  
		Last Modified: Wed, 04 Sep 2024 22:08:46 GMT  
		Size: 202.7 MB (202652028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ea2e63c1386fe6bfe84d9f99788c7ed834f803bcba3b688893f9d778620795`  
		Last Modified: Fri, 20 Sep 2024 20:02:18 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4678c8e49e7765ffd74c128fff70fc5071edf2e788cf932877fc7bc73fb1db95`  
		Last Modified: Fri, 20 Sep 2024 20:26:11 GMT  
		Size: 15.9 MB (15858431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fab74d5902dd8be547332cf752ab3c20b0faa78fdc87a8f4b5c2e53e317fcde`  
		Last Modified: Fri, 20 Sep 2024 20:26:10 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a2aabbacfca162afa09d57b8a6d9f02d0432a9c20d0eb6587843253c62ad4aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15491274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c89d58b2d802a8df078da72443841e8e2eafdd525185a53bdd30b628c0a8a04`

```dockerfile
```

-	Layers:
	-	`sha256:e159786d2b741ea9322f41702593ccc373f2cec94e415fe3817ddf6feaa73d95`  
		Last Modified: Fri, 20 Sep 2024 20:26:11 GMT  
		Size: 15.5 MB (15472406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a4d414bc9f954cd41446e182b2d3e81d356c912735e04531b72031168734b1`  
		Last Modified: Fri, 20 Sep 2024 20:26:10 GMT  
		Size: 18.9 KB (18868 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:9178bf78378a4d5da81c91086f14304b69ed3e7e00a57fbe586955190854f7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.1 MB (367087781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a30c60cb6f2b8bb03c4de6aba3d0f5822ffbb00c5d991b6002e0378e03cf2dc`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:24 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Wed, 04 Sep 2024 22:44:25 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:13:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a7648037128b800dbf0363e27e6092c0253e0bd9beeb38a8aa572225934be`  
		Last Modified: Wed, 04 Sep 2024 23:21:06 GMT  
		Size: 210.2 MB (210181614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de19dfda11a60aa2238d1c46f7f0608c1cd209a8c06a80079838a459a24dffb`  
		Last Modified: Mon, 09 Sep 2024 19:19:04 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d85214af413c60dd90fe5e43e0960e9bd470f4f0afa36ffa9b6f4b6c7822515`  
		Last Modified: Mon, 09 Sep 2024 19:19:05 GMT  
		Size: 15.4 MB (15444947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8647296e6a52e04bdaca911bc77de27fd64069d49f541ec92563b41f9a3c74`  
		Last Modified: Mon, 09 Sep 2024 19:19:04 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d9b00738de63542b67d6e4c2f26c8ad39d7356d0eeb89af1bf40269be540d81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15441090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9c0dd159ec4564bf114918ee6e83629f2741b52f0531cc403c3ef03d65523f`

```dockerfile
```

-	Layers:
	-	`sha256:591f655f02239ff7b9747343390b0a9e5661be55378444994e1353d243be12ca`  
		Last Modified: Mon, 09 Sep 2024 19:19:05 GMT  
		Size: 15.4 MB (15422602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e437a2b94ac107a9d0478f4b8adfb985a77db10fd1c35407c7c0813870ddc962`  
		Last Modified: Mon, 09 Sep 2024 19:19:04 GMT  
		Size: 18.5 KB (18488 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:6d50041ee287edb2bbd41d38f00691e1c4ba55cedd0deadea39ef7522cfe086b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341139523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4acbc8df6fd11b5477db7fa926ac94204502a1799904a93d945d7a5d0b0aa3`
-	Default Command: `["perl5.41.4","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 22:14:59 GMT
ADD file:7a12db48c47f9e4ffb57061ade21f94ff0eb0791886ef60b56a9820f096b39a2 in / 
# Wed, 04 Sep 2024 22:15:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:48:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:54:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.4.tar.gz -o perl-5.41.4.tar.gz     && echo '402b2e10dc1a6249685f0cda5897959bfc079fc324b551a1c4771fe401563896 *perl-5.41.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.4.tar.gz -C /usr/src/perl     && rm perl-5.41.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.41.4" "-de0"]
```

-	Layers:
	-	`sha256:15bebfb1ce6517765581a89c1270a3039857497f5393a3a53eb55a6cf6c3b9e9`  
		Last Modified: Wed, 04 Sep 2024 22:23:29 GMT  
		Size: 49.6 MB (49562002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2220e2c6ab360be293a3568d8fad1b242e41ac727fbfd337305f9bda60d806`  
		Last Modified: Wed, 04 Sep 2024 23:12:52 GMT  
		Size: 23.6 MB (23647328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18258835940e3a6a6470cec276b968942cf166572cd7df8b709c75a6ae95f76a`  
		Last Modified: Wed, 04 Sep 2024 23:13:44 GMT  
		Size: 63.0 MB (62967111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f8cb8fc9c5f50bae748d45f12febe8141263b15997a428733fa15f9121148d`  
		Last Modified: Wed, 04 Sep 2024 23:15:54 GMT  
		Size: 189.8 MB (189827045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a923bef1e3951d9f99c0c83d4e12b06f4ec35c3f7b3e5dc98a07bd91429ae22`  
		Last Modified: Fri, 06 Sep 2024 02:10:35 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c35b7e720b91545c0bce376f86c3de7aa9063e734b542466f3703606da07c`  
		Last Modified: Fri, 20 Sep 2024 21:16:27 GMT  
		Size: 15.1 MB (15135771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea1f296ad5b27c1892f6f045b8f722acdf94e25e9a4abe33f0a8787349a571`  
		Last Modified: Fri, 20 Sep 2024 21:16:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:28b80516b6f7f8c86ae3f2cee600b139ca64c46baa146b86376b35e4182b10d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdebb1dadb96c03a19073c8b2ac7dbb5735faa3acd5938074736f37bc462fa8`

```dockerfile
```

-	Layers:
	-	`sha256:1dfdf00e0d9e5b131b96fa456a6f90180785119dbe203de79cb9d44ba23cf0e0`  
		Last Modified: Fri, 20 Sep 2024 21:16:25 GMT  
		Size: 18.4 KB (18389 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:6ae68ccd8385574cf7c06aba286b9b212c1f9eb1ae73f375182949ec54bc05b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379091168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956746a11f8531aeebcfc6ae122d917438d8187bb2d2ee1d38a8c6e68cd45337`
-	Default Command: `["perl5.41.4","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:38 GMT
ADD file:c5d3aa6402ede77c4a443935fc6572b655c0144f8f41a2967e2e2b55b4c3343e in / 
# Wed, 04 Sep 2024 22:25:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:03:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.4.tar.gz -o perl-5.41.4.tar.gz     && echo '402b2e10dc1a6249685f0cda5897959bfc079fc324b551a1c4771fe401563896 *perl-5.41.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.4.tar.gz -C /usr/src/perl     && rm perl-5.41.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.41.4" "-de0"]
```

-	Layers:
	-	`sha256:d0634fe6314ffdff41b21ba805323138b719229ae2c5a32bda44147f688ed49c`  
		Last Modified: Wed, 04 Sep 2024 22:29:47 GMT  
		Size: 53.6 MB (53553949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928db16ca296d9db3172ad8a2c21f034d363ea47bbebd05e5c085f52a9cae60c`  
		Last Modified: Wed, 04 Sep 2024 23:13:36 GMT  
		Size: 25.7 MB (25710210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39a679766d4a9f2fc4813eab194d4b11ed292163911e303c4f21bebad4be350`  
		Last Modified: Wed, 04 Sep 2024 23:13:58 GMT  
		Size: 69.6 MB (69588450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161dd3959faa2f30fc05f50f11de2ff1ae36632b37e08822b40bdd9e596b6ad`  
		Last Modified: Wed, 04 Sep 2024 23:14:38 GMT  
		Size: 214.3 MB (214285993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9acf5692a24b211db767cfd82b58c02670357ca48918d180cb764fd8490307`  
		Last Modified: Fri, 20 Sep 2024 20:03:58 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6a7259695b3b0c51542fb18d54d922f2189a211a5edc7967d569c0b0f381a7`  
		Last Modified: Fri, 20 Sep 2024 20:20:07 GMT  
		Size: 16.0 MB (15952300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9d16e37ab4a63bdc18fd3d133f5ff7d2510181b7aa242847b8042b4488d452`  
		Last Modified: Fri, 20 Sep 2024 20:20:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:827b53ed8ef51f2efda47dd7ccf0a4dbe11d3b3655c54ed5ca0df2fae6e3c2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15438942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbddf5ce1f9e5a47d7e534151a9c4f181772bbd5b0953af2898952e415a86fce`

```dockerfile
```

-	Layers:
	-	`sha256:57598c912e204ccac60723f21498ae817d899f092a4e93176d069ce95f88f747`  
		Last Modified: Fri, 20 Sep 2024 20:20:07 GMT  
		Size: 15.4 MB (15420359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9456b5f4a84a785193e7fafa7dd0d8205a5fa954137ce003d84df8c3699fd85`  
		Last Modified: Fri, 20 Sep 2024 20:20:06 GMT  
		Size: 18.6 KB (18583 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:e4cb73c0cf67226f0dec59148be459d80d9225ee06afed37333f35ff2b8845c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334673821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b091bfb19b496ef89911015df566e15becf4c47bb393e6a2bf252bcaf97eb3`
-	Default Command: `["perl5.41.4","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:25 GMT
ADD file:61b2bf58d4b2b852e6903b24131c8a331d7a1afe2cc99c4dd08ddffc91545071 in / 
# Wed, 04 Sep 2024 21:42:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:51:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:52:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:52:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.4.tar.gz -o perl-5.41.4.tar.gz     && echo '402b2e10dc1a6249685f0cda5897959bfc079fc324b551a1c4771fe401563896 *perl-5.41.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.4.tar.gz -C /usr/src/perl     && rm perl-5.41.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.41.4" "-de0"]
```

-	Layers:
	-	`sha256:1f3378e3b07f08dbf0b6ce13220a2997d788ba77fb8aa9394ce275771f49ec7a`  
		Last Modified: Wed, 04 Sep 2024 21:47:26 GMT  
		Size: 47.9 MB (47939277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837216ffc2cad6e5167bbe28293d10e21f258e3d8c77b1249ed4cd57246d0f7e`  
		Last Modified: Thu, 05 Sep 2024 00:00:03 GMT  
		Size: 24.1 MB (24052111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894819abf6316f9b38eecbe542cdc236074b267f2f7b83410ab1057aac88398b`  
		Last Modified: Thu, 05 Sep 2024 00:00:18 GMT  
		Size: 63.2 MB (63150669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18612060b30c9f1db538f5e79e46ea0534fafb1c79e714e74e11a1b56e69c56d`  
		Last Modified: Thu, 05 Sep 2024 00:00:45 GMT  
		Size: 183.3 MB (183289806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4854a659b81d79c1d50f3460306c700973d8046c2b4595542ceb1ba4c2b9bd`  
		Last Modified: Fri, 20 Sep 2024 20:03:07 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95eeb5c7ca264da8ad52e115fbbfa91aea5072d008dd6096f6128923a4ab8a9`  
		Last Modified: Fri, 20 Sep 2024 20:17:21 GMT  
		Size: 16.2 MB (16241690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf7d03d0d0f2a3a463b1d2072d83c88d9dc1e60ca1c2b8cd8698c46a8db5702`  
		Last Modified: Fri, 20 Sep 2024 20:17:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:90e4f6e78f6e58352668e1f4a50d88b5ebd6101f7a8cad67d94607513c33bcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15275754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cb2f123114cd1e69b00f3cd5a498ffa2d9fd88c227211d27f698ad44774419`

```dockerfile
```

-	Layers:
	-	`sha256:bcd06193977e575d8108063a237f8607f3f7584d20e8d0a90952656d9c15b965`  
		Last Modified: Fri, 20 Sep 2024 20:17:20 GMT  
		Size: 15.3 MB (15257221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fafe66556678cf9d78d589f238d2dd2942264e591a662eb13f72e4479a3a15`  
		Last Modified: Fri, 20 Sep 2024 20:17:20 GMT  
		Size: 18.5 KB (18533 bytes)  
		MIME: application/vnd.in-toto+json
