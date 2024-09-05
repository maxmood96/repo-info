## `perl:latest`

```console
$ docker pull perl@sha256:77363017cfffc0df22a13c2e0996eb4d031e08a40c7858aec0ac4a3ed0767cba
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

### `perl:latest` - linux; amd64

```console
$ docker pull perl@sha256:57cfcaf9ba7433fdd90def26f3c322c396aa2e0989fba35150071f4623d2e2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364857174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1550a4ac7e16340a8fdd47023e16efa1b1861e6c8b17419d2c3211e33415f6`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Aug 2024 09:24:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Aug 2024 09:24:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ff076d818ad6b8557e03e10c83657cc716ab287c8380054ff91571c8cae81`  
		Last Modified: Wed, 04 Sep 2024 23:02:08 GMT  
		Size: 211.3 MB (211266623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50e6b55e2b231ba28015b8402d6e4c07ddd993778a98db6fc054f8151e17e8`  
		Last Modified: Thu, 05 Sep 2024 00:24:39 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274bc7803e47e75c433737c37a5a903dd58ce54c6bee392f12ed1a577bfad99e`  
		Last Modified: Thu, 05 Sep 2024 00:24:40 GMT  
		Size: 15.8 MB (15832413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1041ace35d0d123c9a7232be74095ea44b1efb1a5442214ae91d7eac9fe4248`  
		Last Modified: Thu, 05 Sep 2024 00:24:39 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:7dfcfed089deffee70e62464b71f5724514e1bdfbebfc1b0bdfde1d7f522afa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ba94abfb4bdd9a3647babad0b0b847fd5da2711dcbbb54f738a1796affd293`

```dockerfile
```

-	Layers:
	-	`sha256:be0ffb1f3d004705e900c9700f5c2cffb63412d1eaef844a7578493947ecc5fe`  
		Last Modified: Thu, 05 Sep 2024 00:24:40 GMT  
		Size: 15.4 MB (15444900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d4b4ca844a7bfbbbc2428b40693cad30aaae1de9f07e0c87e255cfc9193645a`  
		Last Modified: Thu, 05 Sep 2024 00:24:39 GMT  
		Size: 19.3 KB (19287 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; arm variant v5

```console
$ docker pull perl@sha256:f6e8b566a075b24178f0c89c539ed6add3bc5ca9afd635959775e5c96cbd5bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.2 MB (331208152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4346cb7320edad33b3beb61a2f4e2129af371d566fde1c0536bb61f28ac368e`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:20 GMT
ADD file:d0d1a7bef1e6f926632190db50e475c494faeae7f507fe25bbc44d83e4cacf61 in / 
# Tue, 13 Aug 2024 00:55:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:19:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:20:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:7b23500f0d545573a069afd72bb54ddd68dc094fc52cede45c3d6d99ab4ce614`  
		Last Modified: Tue, 13 Aug 2024 00:58:03 GMT  
		Size: 47.3 MB (47320194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9b6b6feffde625468b578ba2210c9f0d6883023349fb0f1f7e6eacd4734f28`  
		Last Modified: Tue, 13 Aug 2024 01:29:38 GMT  
		Size: 22.7 MB (22729369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed69be726be2aaabc7cbd7778afcd3159b9bae3aea862563ee95cb6c84dbdf2d`  
		Last Modified: Tue, 13 Aug 2024 01:30:01 GMT  
		Size: 61.5 MB (61520228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29df05d41a6c52dd0e5bf38b1bd02aabd071cdfc47e5db769d4f8027cbce9b07`  
		Last Modified: Tue, 13 Aug 2024 01:30:40 GMT  
		Size: 184.5 MB (184530610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0058464ba7b32190484b2d74c7b8a4dbf864429a28253a5c1739276067f5c7a8`  
		Last Modified: Tue, 13 Aug 2024 11:11:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c81530cbcfb96befd7511cc0123f3f2d4e42d723303faacc7b928d813a34dd`  
		Last Modified: Fri, 30 Aug 2024 18:05:13 GMT  
		Size: 15.1 MB (15107484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad10bbcd771c346550935c92d41415762f2b53e6500186573da4313092c61cd`  
		Last Modified: Fri, 30 Aug 2024 18:05:10 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:ae9bb05e0d9bab8fa11f14a40af47e104c7b44eb893ed2fe4303c28932c6fb75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15264289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5c9148e18fff022d5546f3038f19866773d4447ad01b829f8b1ab56ae2dbc8`

```dockerfile
```

-	Layers:
	-	`sha256:7482ce83c6c05b619ddfbc2f4fcfba708035d653122f60af90807e0da8d545b1`  
		Last Modified: Fri, 30 Aug 2024 18:05:11 GMT  
		Size: 15.2 MB (15244884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc08117e9e418b516caa9e3c5df2ccc1f9a058f610a35613d79deabb2bc368dc`  
		Last Modified: Fri, 30 Aug 2024 18:05:10 GMT  
		Size: 19.4 KB (19405 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; arm variant v7

```console
$ docker pull perl@sha256:78bb7dc8310b77ce01b217d199534113a16253ce6dcce07ebabc388a814a92cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.4 MB (316405970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5163554e99a7043ed10b8005419106cfbb78043fee30419c92c3c90c3b8a8ee9`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:26 GMT
ADD file:e3c71ceb3b7032e8a78ea70e306ec97b152570eeaae849a0c97bb61b2b12287f in / 
# Tue, 13 Aug 2024 00:57:26 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:24:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:24:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:25:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:fe61db625a1b529903f1126ded0caa9e4e1c247503d524cd43bc15454b6bcc2f`  
		Last Modified: Tue, 13 Aug 2024 01:00:32 GMT  
		Size: 45.1 MB (45148160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06599d70e5763853acd56f8e4938729e068e7942382f335f96ce0ae3bc5a63a`  
		Last Modified: Tue, 13 Aug 2024 01:32:20 GMT  
		Size: 22.0 MB (21954622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3af44a3c0ce16617696528373b53738420f91f3383cda1666cc673cbf6fe50`  
		Last Modified: Tue, 13 Aug 2024 01:32:41 GMT  
		Size: 59.2 MB (59221928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dd2b78206591edf08b24f09f26f742a3d689be108f6e3cf74538c78a14b7d8`  
		Last Modified: Tue, 13 Aug 2024 01:33:16 GMT  
		Size: 175.2 MB (175182857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332aa183c908a7a7416d25ca604825cb09706e74c6ee8d527e967b31fd515f04`  
		Last Modified: Tue, 13 Aug 2024 12:31:52 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9eed760ee1479d00ef16a3e67a9dd95370a1522e8da999807f802de05d660e`  
		Last Modified: Fri, 30 Aug 2024 18:04:49 GMT  
		Size: 14.9 MB (14898137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac53c6a61f074b3878cf48619ce6140dad6d93aa904e0a66a6492839a76953b`  
		Last Modified: Fri, 30 Aug 2024 18:04:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:47f7c6449195d5453effafc7d079fd8dfaf1b18b2b74af743e9f437c1e1784eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15269763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787593c7119eba8c503377aac4cfe89f6df84cdf3d8b594a2616a1de696f4995`

```dockerfile
```

-	Layers:
	-	`sha256:9ae502c1e51c9d0294d377bba8ca2353fbf8ac1a82978dec66b73f2f2f678327`  
		Last Modified: Fri, 30 Aug 2024 18:04:49 GMT  
		Size: 15.3 MB (15250358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4430ddb246c9a8fbc426b250f3356f2aa14a476770014021c0b053c652fdd4a6`  
		Last Modified: Fri, 30 Aug 2024 18:04:48 GMT  
		Size: 19.4 KB (19405 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:c61b3263a5a8c91e50d11950e1715df944ae484ee423a5fc041c9150f88ef78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355587814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a4050f61f46e509a33d75bee0a568aa8cace3569591b40f47e0877104da6b4`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:42 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Tue, 13 Aug 2024 00:39:43 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:02:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:03:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275677961327bd0cf394699228e29d7caf27f171c627899a20ebc9eeb550e209`  
		Last Modified: Tue, 13 Aug 2024 01:09:34 GMT  
		Size: 64.0 MB (63994880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46e144614e1ae9b82b5d89d16a31a506542733eabceebfac041e0192dfafcf4`  
		Last Modified: Tue, 13 Aug 2024 01:10:06 GMT  
		Size: 202.6 MB (202624176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b2fa6e8c30392edc043fb6e0b449c2e120da2938b0dd759d51b07e05a037f7`  
		Last Modified: Fri, 30 Aug 2024 18:03:36 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eaf15088f47f58bcd07387cbe242e63ebd7166fd17db4667079410c322519b5`  
		Last Modified: Fri, 30 Aug 2024 18:03:37 GMT  
		Size: 15.8 MB (15787471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c5f25ea1197e788c18c8297f0e20aaa595f1bc3b03b5de743d2918b84b326`  
		Last Modified: Fri, 30 Aug 2024 18:03:36 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:4f8bebfb98472622eae19e56656b29548a70a1216b708af7a4fe1390dfc254f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15493773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe85f95efd9025695b645b03a2a60905a299254dc03450314b7edbe6d8139151`

```dockerfile
```

-	Layers:
	-	`sha256:929489bd2d2129f41bf5734ae2153fa5449a7420c368b4c0da7564f2e44ae4d8`  
		Last Modified: Fri, 30 Aug 2024 18:03:37 GMT  
		Size: 15.5 MB (15474103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49d462485f580477502a73a911420f82b3c6af848ebb8a539356dc7d16c1ea0e`  
		Last Modified: Fri, 30 Aug 2024 18:03:36 GMT  
		Size: 19.7 KB (19670 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; 386

```console
$ docker pull perl@sha256:dd436794159a16e56d6253cd25a02a9042f121f5a387182cb45b701adaa4adfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.0 MB (366968096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97280a25a5d72b5952ed3b263d8df05baac4a31c3739a55c257d03bd717d2ab`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Aug 2024 09:24:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Aug 2024 09:24:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
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
	-	`sha256:a65494a2b4584b27391660c4de18963664e05d4508624139536273517a07c1c6`  
		Last Modified: Thu, 05 Sep 2024 00:25:43 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b30314fbbd595908db7512adc1a0c6ff0f51116e06fd1b6081a3cf8c2f48e48`  
		Last Modified: Thu, 05 Sep 2024 00:25:44 GMT  
		Size: 15.3 MB (15325266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65adec843049ea3699bb90dcdfa37e459040821694ec7ae2b04ad5ba1b8ad190`  
		Last Modified: Thu, 05 Sep 2024 00:25:43 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:ba1ec5ed4e6da97237f74710bba8c088a7253719cebb6940b56bcb7de380a9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15442884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c05e557d7c7501c3479a92528a856f97f2063d472801667f104dd9fde53e11`

```dockerfile
```

-	Layers:
	-	`sha256:0a211569888c44cf80c6da03a20c40f0e6ee5467c43bea57c77a2efc288f58b7`  
		Last Modified: Thu, 05 Sep 2024 00:25:43 GMT  
		Size: 15.4 MB (15423656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541d82240d1c3240b52ac8bcf2445f47d6d6cca3f0a6d2cd3b8891a6b2d423c4`  
		Last Modified: Thu, 05 Sep 2024 00:25:43 GMT  
		Size: 19.2 KB (19228 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; mips64le

```console
$ docker pull perl@sha256:86e08001676ca6bbd751f10a3d89b5a0d694672a811929e151ac1e3d8e1cd29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (341004096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc1e25a7bfa1e85a569f9dd0cc5901d8cba2e44dfe7fb1b2b99ca3aafedf8bb`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:10:27 GMT
ADD file:42b5546fc536a0937c9332001326b56edcfad5a5db46bb873f84f73c3bda9b67 in / 
# Tue, 13 Aug 2024 00:10:33 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:02:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:192d8664ef287a4c7c8030bb7f9fd54f06a0ee665114437e01bd957247249b59`  
		Last Modified: Tue, 13 Aug 2024 00:21:46 GMT  
		Size: 49.6 MB (49563201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f290e8d96661528fcabadb467014984544fb262f562d178e8eacd4c2b72d7bdf`  
		Last Modified: Tue, 13 Aug 2024 01:31:16 GMT  
		Size: 23.6 MB (23636644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada0a2437b401a0a19336dc670ab8d52dc4c37912787524de56c1c95a6bde7cf`  
		Last Modified: Tue, 13 Aug 2024 01:32:08 GMT  
		Size: 63.0 MB (62966082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93661e8bade5668baa650e17db139abcf2b722965a5fbccb9f55952cf3a58f`  
		Last Modified: Tue, 13 Aug 2024 01:34:16 GMT  
		Size: 189.8 MB (189802742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04290dc0bee72dac963db1c1ebe9501056440a74062fd232c307d3c22467329f`  
		Last Modified: Thu, 15 Aug 2024 02:54:33 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9102af76ea4466a8936c4209570df2295227b7f37e89b580fb4ef4b8457dc5`  
		Last Modified: Fri, 30 Aug 2024 18:23:38 GMT  
		Size: 15.0 MB (15035160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6232b59001ff18b1c9cdfeeef4f4c7383f17772fe58cee685af0fda61be2854`  
		Last Modified: Fri, 30 Aug 2024 18:23:36 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:c35fc618854c369188e02e453bf3225b483db8d9dbd2134d9a9e25709cbb979d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8c6d931cc815276aed244cc6ae3eb8ed8cbcb408204b9ee6deabe5e6f945f3`

```dockerfile
```

-	Layers:
	-	`sha256:a776a04cce5be1befc829a772c18886b72a529098b14add84df15e8032cbfdb6`  
		Last Modified: Fri, 30 Aug 2024 18:23:36 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; ppc64le

```console
$ docker pull perl@sha256:da7ecebd2d5915effd91951ccc98a6729f56a1c590ea8bd1871f43f4f975e4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.9 MB (378929725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4fdf66a48b3c37e78ae7d8ebbdc8739cb66e817b0eb042bfe30301be352a2e`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:45 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Tue, 13 Aug 2024 00:21:48 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:22:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35476fbf45cb5153abf5ea2df7487a74d0cd0de327ba5e9e970713f9e385650`  
		Last Modified: Tue, 13 Aug 2024 01:35:51 GMT  
		Size: 214.3 MB (214264660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f938761b67c4431b432588d6f82b6178280c0c5d9b28583343e9eb8c588aa5c`  
		Last Modified: Fri, 30 Aug 2024 18:04:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccce94f1c178b224b98b0900633f8be4e9ba95937e98c521e54f0111e50e7417`  
		Last Modified: Fri, 30 Aug 2024 18:04:52 GMT  
		Size: 15.8 MB (15830572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2476e308f03563ac77903bd048b1f3af6de384499bbc1b2aabfac5fc4b12a2`  
		Last Modified: Fri, 30 Aug 2024 18:04:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:04f684c94c346e4dffbab7bee0baa3515fe3f2b6e0a1a744ab6b3af3a1371cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15441393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d917c76e0b37742176e44e9dfe4fb786a5afda166ee490331465443c35ed399f`

```dockerfile
```

-	Layers:
	-	`sha256:379c23640e0e34a6b201cc508bf2a783a97cdee3bdbff1079cf3085515297f94`  
		Last Modified: Fri, 30 Aug 2024 18:04:52 GMT  
		Size: 15.4 MB (15422032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79828cf258e879355d2ea5e500d981d46ffd538739e5bba62b9c8d914cb6f9a6`  
		Last Modified: Fri, 30 Aug 2024 18:04:50 GMT  
		Size: 19.4 KB (19361 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; s390x

```console
$ docker pull perl@sha256:333d16f7fff621890fd9bf93838fa2d81af16494e87d1044f90ff4af129ced97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334536764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb4436e01ca92b5133d0595182e59a4a88652bd459a96764c651d842d49717b`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:19 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Tue, 13 Aug 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:17:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d84b8bb13cbf61ae13e4c378871c52c3e9b521657a5faa02f0159e1be542a05`  
		Last Modified: Tue, 13 Aug 2024 01:25:25 GMT  
		Size: 183.3 MB (183265629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2829b4d92c3d06a1177f26aad9af8d9118a5da7aef95be8b058562b783a85e5`  
		Last Modified: Fri, 30 Aug 2024 18:04:42 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda8039bc47a42b76076b3712bb7a5431e4874cdac40f00c2c5275b5df1ddd8f`  
		Last Modified: Fri, 30 Aug 2024 18:04:43 GMT  
		Size: 16.2 MB (16165646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac53c6a61f074b3878cf48619ce6140dad6d93aa904e0a66a6492839a76953b`  
		Last Modified: Fri, 30 Aug 2024 18:04:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:22046e696f2038b84d1ac4a9919827f3ba1ebf6d2507d41f6a7cf674cdd4b7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15278157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c62ec3b8dc260fcde6835a1e6394a90653431a3fa5a60c16070372cef20cb5`

```dockerfile
```

-	Layers:
	-	`sha256:fdcb9daa9d0d1eb7a17c2e652e334a7589299da5153feba1fa25b0cf5b166d21`  
		Last Modified: Fri, 30 Aug 2024 18:04:42 GMT  
		Size: 15.3 MB (15258870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad8278206e41f8437a112f5adeb23cbf11220948306c971f9da010399b71aa0c`  
		Last Modified: Fri, 30 Aug 2024 18:04:42 GMT  
		Size: 19.3 KB (19287 bytes)  
		MIME: application/vnd.in-toto+json
