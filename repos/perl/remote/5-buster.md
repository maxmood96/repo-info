## `perl:5-buster`

```console
$ docker pull perl@sha256:3b1767dfcc93f78f7de598560a788a642fcb452906050679d9fb8073c9da9b70
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

### `perl:5-buster` - linux; amd64

```console
$ docker pull perl@sha256:07c1d90caf772f828a8be788fd459ed1b99353cf12e5ab926d5128a6876251d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327763679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96733cd90a5c71f31428f2955c787f08e0172a1b707f739050ac466e21fb8f91`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44f61bacd5268a0f7dbd851e763d6ee101c21d0af21e649584357d4443cd709`  
		Last Modified: Tue, 14 May 2024 03:06:14 GMT  
		Size: 17.6 MB (17586437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e7d6cb6a5235443faadc8d241ebb270739fd828ca9f0b78c63a1e7f36f8405`  
		Last Modified: Tue, 14 May 2024 03:06:29 GMT  
		Size: 51.9 MB (51894320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc40752dd2cf0f18dcf07e73c1c85269734230ce7b22f18f4a4d120f54e608`  
		Last Modified: Tue, 14 May 2024 03:07:00 GMT  
		Size: 192.0 MB (191957446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea33eba33a9d9286dc6569e7b2421b91133c199a90593603ecfee71f1ed9c411`  
		Last Modified: Tue, 14 May 2024 04:04:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbf5108fda89fdb08157aeff1cde1d99fde2141cc536f62b78566da9e4ec9db`  
		Last Modified: Tue, 14 May 2024 04:04:23 GMT  
		Size: 15.7 MB (15668301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b8a848acf06343dca9f5766f3fa6476774a23a4e3f65c5d6696c639d167b0b`  
		Last Modified: Tue, 14 May 2024 04:04:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:f526b2797937e3b3c1368635c0cd77c587787e86b5a213336dbc02bb299ce9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15982674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e401859c72175cc5b4b87da9bf1da5d5a6f31f8e5b5d1fcf952858a26d2de90d`

```dockerfile
```

-	Layers:
	-	`sha256:ad52fe0883b59059210e364bd227cbd895196db0b47437e9973389752e30622c`  
		Last Modified: Tue, 14 May 2024 04:04:23 GMT  
		Size: 16.0 MB (15966402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32efa45ee6062c4a9b05ba1a339e9fb8a1caee6850f94f0db61fdd123322c109`  
		Last Modified: Tue, 14 May 2024 04:04:22 GMT  
		Size: 16.3 KB (16272 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:588d5c3c90397ecf6ce23eb890e3a2bc0d5686a0a33f2d65f297f5ad066782c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (293004631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9320dc8623ef17a0ec4b9e40273b24f992b1f364ada8bd12fbf0ed434c6dc63a`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:09:12 GMT
ADD file:a05edfdd56e92b1814d8e812ef81e814accd29893888392076dbc26b33b5ae41 in / 
# Tue, 14 May 2024 01:09:13 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:39:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:41:03 GMT
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
	-	`sha256:66d6e1b7bddcb1c893c2c3e9b1ac8f5fca7c047037ed836079c97c9a917cd989`  
		Last Modified: Tue, 14 May 2024 01:13:47 GMT  
		Size: 46.1 MB (46129793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e36c6c43e23d017283e609c78ad3425681f38a7cec50832f329aebf9f45a45`  
		Last Modified: Tue, 14 May 2024 01:49:06 GMT  
		Size: 16.2 MB (16217024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d070dbdc44447a3c019b1076d14827afec1e3d9f53f0941c341dde2f5b674`  
		Last Modified: Tue, 14 May 2024 01:49:23 GMT  
		Size: 47.4 MB (47410306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeab1a68b064abb317c5afc7a68fdc8b46b5c9f37a1fad3e3d9664777a761c11`  
		Last Modified: Tue, 14 May 2024 01:49:55 GMT  
		Size: 168.2 MB (168170028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac4d78312c91d8822482c2c42f3864f1f9ff99e42a8ff015cc21c64e2788515`  
		Last Modified: Mon, 10 Jun 2024 21:15:29 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c0af1e38d39139ede81cbbe9110d893f667098a8ce67678ed51badb2169a5b`  
		Last Modified: Mon, 10 Jun 2024 21:15:29 GMT  
		Size: 15.1 MB (15077212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c5d269bcf928ec1f63ece77e073dabc957b25dcd8588734a03d0a1d7b461d7`  
		Last Modified: Mon, 10 Jun 2024 21:15:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:412d857228db58429025cae9d5251c9fb4e7053f12bbffb71b18f15a0ffc9e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15784294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de755b45f19fb9f90ebdcd9d5f6c5224bba073e80d76971027bbc8e611e1258`

```dockerfile
```

-	Layers:
	-	`sha256:49553ede56dc6b12386b50d406f41178906273a3c4ff4c375fed81893cc34d3d`  
		Last Modified: Mon, 10 Jun 2024 21:15:29 GMT  
		Size: 15.8 MB (15768559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60974f963b54fe27fb005803a85fb993a272fa4e5d893ceeb77f225b7925efa4`  
		Last Modified: Mon, 10 Jun 2024 21:15:28 GMT  
		Size: 15.7 KB (15735 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:487242f98b250af1d0e7dcb94bd6ba49bd56861b699a3a1b63e16b8f7c79707e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318585868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00df7a34df984b8c54243cce66d0656e623f74bce60d41ef77638e5dd600aaa2`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:40:02 GMT
ADD file:da8c3a2d966487a4e1bc0646a771d18df585d75dc24f095a1aaa762ce0841747 in / 
# Tue, 14 May 2024 00:40:02 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:48:35 GMT
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
	-	`sha256:0a8090f4fec79fd213192f5f5c31c70546878a20b6c7ca023ff9001fb788f828`  
		Last Modified: Tue, 14 May 2024 00:43:49 GMT  
		Size: 49.5 MB (49453094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e540eb6c9fa042a5d3f1166ea6b4d3806d751dcc600baff113c7e2b711719d`  
		Last Modified: Tue, 14 May 2024 01:54:42 GMT  
		Size: 17.5 MB (17456998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334249e7f4554ad45c3998bd6a23aa8d7ecc535422903784fb251e6345d36f9a`  
		Last Modified: Tue, 14 May 2024 01:54:57 GMT  
		Size: 52.2 MB (52230498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019b2124bd151541dda5ef935a2883293321b124587270f4c0c28495c25a1ca4`  
		Last Modified: Tue, 14 May 2024 01:55:22 GMT  
		Size: 183.5 MB (183534368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c2bbf8cd4ab2410cfc37c445a08eae53ab94b2a1b12e94567f24bc0bbed466`  
		Last Modified: Mon, 10 Jun 2024 21:20:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3040fb3e4b7d27178308ef417c2fa637acba4d7a8bb88b269c0ff96dcc883c06`  
		Last Modified: Mon, 10 Jun 2024 21:20:14 GMT  
		Size: 15.9 MB (15910643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00fd88c57a5a5ca4569740f9179ddfebf2fbbbfa19564853ddbbde421abc8a2`  
		Last Modified: Mon, 10 Jun 2024 21:20:13 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:c0214145243011b5cb6c5e55f4b96f8375bfc3781a897bc637521fb5f4bab680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15973270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6966dbde74e3666af07f252a5e79bc7d51869b83aa342d444571d6054700507`

```dockerfile
```

-	Layers:
	-	`sha256:cb4552023276133fad9eb39e5f39362e49881d3044ecf63b2846abc433202f60`  
		Last Modified: Mon, 10 Jun 2024 21:20:14 GMT  
		Size: 16.0 MB (15957315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:847bb2bb9f20578037b2db64c9111bb2c2721695e696d7634a5b47baee9f1959`  
		Last Modified: Mon, 10 Jun 2024 21:20:13 GMT  
		Size: 16.0 KB (15955 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-buster` - linux; 386

```console
$ docker pull perl@sha256:55aee9fc6815f243c8ad7c9e60995a14ffd0cf3f40a2e832d6ad91854465a14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (336973251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fadafe885b2ec2bd49eb986bf15fe8226e287107c0664e844728eab50451ba`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:47:45 GMT
ADD file:5e59addfe8663b7c16cce40874c2a3c8601e20e80f5a0897c86b64ba463c10e9 in / 
# Tue, 14 May 2024 00:47:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:05:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:05:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:07:14 GMT
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
	-	`sha256:1a892f56e4b10aaecbb51b3219d90bd0d8a1e955acd0624a6ef27ed086ba168c`  
		Last Modified: Tue, 14 May 2024 00:53:06 GMT  
		Size: 51.4 MB (51419713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df672f2f18886bf928d6070d3311b71a33f94ce9708b67ade8e00ea0ec6cf25c`  
		Last Modified: Tue, 14 May 2024 09:15:53 GMT  
		Size: 18.1 MB (18098325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20019971ec9aacb9b7c64eb51f32f35360675176e10007625a27813b8a8cd124`  
		Last Modified: Tue, 14 May 2024 09:16:13 GMT  
		Size: 53.5 MB (53491794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a3d64f2a6cfb08d0e101f8b79c83a6035104799f3de7058346a363aa6a09f3`  
		Last Modified: Tue, 14 May 2024 09:16:59 GMT  
		Size: 198.5 MB (198492126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ea30008a582a72ff1d0287abbfec68d7eb9d7d6e93ef747e95f5d1b16a9124`  
		Last Modified: Mon, 10 Jun 2024 21:03:34 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df66085690b97ef3628413481eb5680558994bdef4ba9769bf87b0dba31c4a20`  
		Last Modified: Mon, 10 Jun 2024 21:03:35 GMT  
		Size: 15.5 MB (15471025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0163e24dd3fca6e9251c68d847232bab22a4cc95d97d66ceaa936743b6681afa`  
		Last Modified: Mon, 10 Jun 2024 21:03:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:9b9ce0d30beed9c785a2c71ed64e893b7ced4dc7e81adbfeb0240b1992cb37ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15987606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a299ca4c8fc701e8c39e250012dcc9f16cfc6e96eaa3fbf0fb9d2e777d9114e4`

```dockerfile
```

-	Layers:
	-	`sha256:01c34f5a20f5e0a0f8d5ec5025f96e351200744c137842b648510c1a4cc1b936`  
		Last Modified: Mon, 10 Jun 2024 21:03:35 GMT  
		Size: 16.0 MB (15971983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8d7830dd9d517e6253e9af4761ff791965538a4339b535450b7b0909b449a8e`  
		Last Modified: Mon, 10 Jun 2024 21:03:34 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json
