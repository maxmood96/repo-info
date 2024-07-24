## `perl:devel-bullseye`

```console
$ docker pull perl@sha256:6dec448253b99bd166c1aed52ff2343eb8ec349a198c5c9848943b6954fb316c
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

### `perl:devel-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:008c50461c11bb48452094c13bef9ae605b6b6b1c0b1c854cada3068028952e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338290101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecb8f8fc88a789b983b9c1754111c2226f098aa5874f1e5e8b971a591896847`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8ed7043ae24342affc9e27ba2f362a3d02c164d6f2cc7b837f33b475f4ef54`  
		Last Modified: Tue, 23 Jul 2024 06:14:32 GMT  
		Size: 54.6 MB (54588538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c6efb0908b76d25c6355b6afc739337771c5a9f3a556c262cb1d0c767b6604`  
		Last Modified: Tue, 23 Jul 2024 06:15:02 GMT  
		Size: 197.0 MB (197039174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28337586d327bd05962630e9f3a051868f2bdc301b41b0ed1a43a9aec33df569`  
		Last Modified: Tue, 23 Jul 2024 07:28:42 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54da1018bf4a04c6a2f44eb97c670a43456c7f6e21ca4899fe74163dd8ace888`  
		Last Modified: Tue, 23 Jul 2024 07:28:43 GMT  
		Size: 15.8 MB (15813260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092ea7afbbb135a4394818ef4ad560e38ce684738bd81bd45517b9f678f4a22a`  
		Last Modified: Tue, 23 Jul 2024 07:28:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b96a1c8209b6c4b0a1fa28e811a9533dc48976a7a352feebf071031c07dfa88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15068020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60366eed32724fe9322ba43b0465b143088c116328ced930f42606219dd65154`

```dockerfile
```

-	Layers:
	-	`sha256:8436b0e1b7540a05a2488757b5a4bad7bf415a96a8b10fa225d9a70b903b0936`  
		Last Modified: Tue, 23 Jul 2024 07:28:43 GMT  
		Size: 15.1 MB (15051209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f54592a160105c52ad4a28bcbc7a165c68116ac8bacc5da954cc0d7d697b64`  
		Last Modified: Tue, 23 Jul 2024 07:28:41 GMT  
		Size: 16.8 KB (16811 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:790c71933f6903a461282dfe76636257eee539fc82c3347c9c2ff9d72a4af392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310644324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d6463c72922c19fb3a8637cdefbca5e7ccb835b95343025a1e9c7b04fb0823`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd35925e7431e8e36d2900def8d6954e5c811ce7a1c205db5d4cc183c4696b67`  
		Last Modified: Tue, 23 Jul 2024 03:53:27 GMT  
		Size: 15.4 MB (15375348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b062df9eea8fb3b005e76c03f7ef72ba9331888f68b2b9dd6b1f7afaddd042cc`  
		Last Modified: Tue, 23 Jul 2024 03:53:50 GMT  
		Size: 52.3 MB (52329700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5972ef34abc8f8302675fa051e04d2b0db7995a024a1f4298f5a462fcabd0d`  
		Last Modified: Tue, 23 Jul 2024 03:54:35 GMT  
		Size: 175.2 MB (175246775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e2f986e3d39c9333d00ca329638a370e4c1068b110261294858edf3ee3d954`  
		Last Modified: Tue, 23 Jul 2024 22:09:18 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455c48fbc52277e7ef55816a6c0b9677a1ed2405fed89b504ff9e26a81dc60a8`  
		Last Modified: Tue, 23 Jul 2024 23:48:13 GMT  
		Size: 15.1 MB (15103271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98024d95d21f9a8437c40b9092b2d3bdaca570dffae7569196c704bc9ad2ff6`  
		Last Modified: Tue, 23 Jul 2024 23:48:12 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:23a8c9000cefa35888ea0940e17fbd2e1f7688a47275e5ecb7161bb62c555a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14863726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de66a0b5c79ec3c6785e6ddf267d447ba8041c34b6bb0a9b6048ce1f7ec621e4`

```dockerfile
```

-	Layers:
	-	`sha256:99574cc4a483b2a1adf1cf59b7cbea36a087eb554b60bceb2c9a5fedd21eb253`  
		Last Modified: Tue, 23 Jul 2024 23:48:12 GMT  
		Size: 14.8 MB (14846854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ff4113539b08c9f5646df8e81b07874d4ac37ad4f2b2b429efa8ae4aab81b88`  
		Last Modified: Tue, 23 Jul 2024 23:48:12 GMT  
		Size: 16.9 KB (16872 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:754acecbfe0484f0734239c746e993d59429bc7bf9d45b9d5bea603fe9c32d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298769038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38202dffc68375ee741249eb692f89d18cc270f9d2ed5cd3ea965e90c2f20d08`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:11 GMT
ADD file:6e828fd5dbd54f949f96129ea922c27ff88709484119faef51401e338e900e6e in / 
# Tue, 02 Jul 2024 01:00:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:26:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:27:35 GMT
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
	-	`sha256:a0610bbe9cb80952dba5ef5efb55f03668fd4f8ab63ade3ba30e22a4c03c42da`  
		Last Modified: Tue, 02 Jul 2024 01:03:38 GMT  
		Size: 50.2 MB (50238998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c595e4d8c2d2c7ad66ab723b54c73c6a0aa876b01511358ec8af1aed8c8b94`  
		Last Modified: Tue, 02 Jul 2024 01:40:13 GMT  
		Size: 14.9 MB (14879331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577c5fe1f5243a6910c54b7b4a338cc9cbae0cfeba74a350b011d2a467e49daf`  
		Last Modified: Tue, 02 Jul 2024 01:40:31 GMT  
		Size: 50.4 MB (50358262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53a04feb4a55b8a4920c0ad42332dddf76ad9bb3bd19eac2f580036953cf88`  
		Last Modified: Tue, 02 Jul 2024 01:41:09 GMT  
		Size: 167.5 MB (167478798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3996e1d55536d7f0fd72e159b2b4789726b0b353fe5a4446bbe60d9336a467`  
		Last Modified: Wed, 03 Jul 2024 16:22:53 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd16b407ffafd972e7cd90040d4436ca8495017c7951cdf25961725a0934c3d9`  
		Last Modified: Wed, 03 Jul 2024 19:04:56 GMT  
		Size: 15.8 MB (15813381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ec33f67c64f4762bf98b1f8ebd0fe62a0ad607189920fdf6686510ad2ae4b1`  
		Last Modified: Wed, 03 Jul 2024 19:04:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b3e053d116b8775c69a5b8867ff857a91226f1ad90a589a5aa9f35099247a575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14792604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d76a6ae8d587d88947ecfafed0da80c188fd0d4a8a2497565e2c873b9fc50df`

```dockerfile
```

-	Layers:
	-	`sha256:2568e51c44e85bde91226c252cf293d50f589450df2a5bfc020b651f29676846`  
		Last Modified: Wed, 03 Jul 2024 19:04:56 GMT  
		Size: 14.8 MB (14775851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f0b4e9fd10bd994186488e8ab7cff11392220476749474238bd54c26ed5a7de`  
		Last Modified: Wed, 03 Jul 2024 19:04:55 GMT  
		Size: 16.8 KB (16753 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:becca62c30b0bcf44b4b389b25c6fb68811242e12a0371994ecc9049fcbbda7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329887519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649ce7bc50519a821d4b5d9afdd4a1b5a1d9b2647f116975187ef87f0a91322a`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27a83c76abd51a72277b6a74eb7f88e560054e0d04383f64e2886877a20dd5`  
		Last Modified: Tue, 23 Jul 2024 08:11:04 GMT  
		Size: 15.7 MB (15749501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac540a55631c4cba93c7e4e4bf634300076d45e71db5f34f3c0d770eb826303`  
		Last Modified: Tue, 23 Jul 2024 08:11:17 GMT  
		Size: 54.7 MB (54694822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df233b2a5328fe9ae508771678b5a4faaefca18e64196b4ac65584baa5c8aa9f`  
		Last Modified: Tue, 23 Jul 2024 08:11:41 GMT  
		Size: 190.0 MB (189965935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011e3e6dec28352ce61a35ec709fe4dabc2ff6bb907c60dbbd213e31a9b9e392`  
		Last Modified: Tue, 23 Jul 2024 22:21:18 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc8eea5f73847975ca25c3247a36aef77e0dd7daae88472882ed562a55bd7b5`  
		Last Modified: Wed, 24 Jul 2024 00:27:34 GMT  
		Size: 15.7 MB (15747006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8598ffaa3109f06fd030413147a11f3926e908bff94bb5382e3d7563fce2bc0`  
		Last Modified: Wed, 24 Jul 2024 00:27:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:1fcaf2fc942645570ea06d5fed0d8a702a67f615137b850eca9a3b7350a5bd0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15070674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2618919db82dc30b2102d01f2990cd826478c97cbcc212bde31a80a0eccbfd`

```dockerfile
```

-	Layers:
	-	`sha256:6684b0ca0498f88f4751a026987dcd1a2e8351d2ddae483c5720cb608a0254de`  
		Last Modified: Wed, 24 Jul 2024 00:27:34 GMT  
		Size: 15.1 MB (15053563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f108c2ca78f5d370efea05de23e2b9735962bac8344dcd592cd4434561da4cb4`  
		Last Modified: Wed, 24 Jul 2024 00:27:33 GMT  
		Size: 17.1 KB (17111 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; 386

```console
$ docker pull perl@sha256:4cb97d91fc44903818cbecce89b88456066ba909f1d3760f698b378be0f6bd92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343522326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8523e30e8f219bc038777a731c5d1177413ecd06e1ec1880ffe302cf65a05f42`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4dc1000d9e0251c16eaa821d62c15a6b192ccf2a5a7ca1f418356c9510042e`  
		Last Modified: Tue, 23 Jul 2024 04:50:03 GMT  
		Size: 16.3 MB (16267809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb2358914d635fc6784c6b2db8c1b20149653f26b9311bf6d676476a452297f`  
		Last Modified: Tue, 23 Jul 2024 04:50:23 GMT  
		Size: 55.9 MB (55927780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30928a030df8a953adc83c67e2ab17a4c5048cc04287762bc9e03e269fe7c3dc`  
		Last Modified: Tue, 23 Jul 2024 04:51:04 GMT  
		Size: 199.9 MB (199944219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd199f5498f738dff5ce515de5c77213653d15ea5d67fb30f78658092e7f75c4`  
		Last Modified: Tue, 23 Jul 2024 06:17:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8546a44e7e0490d64efd0dd32375d74a8afd0b152da373263b28369485a3946d`  
		Last Modified: Tue, 23 Jul 2024 06:17:53 GMT  
		Size: 15.3 MB (15308081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d744aeda9123633c6ef8d9d2b0a24e0e5e3dabcf2898540209d664407eabaf5a`  
		Last Modified: Tue, 23 Jul 2024 06:17:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b23b2bfe5819ce2e5dc19bacc64d4e784661e71a4cbde0e917775c7e89b213d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15056543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5da129b2a469b97e445c6f90883e96ca95c5804cd6b2a41894f1102c879887`

```dockerfile
```

-	Layers:
	-	`sha256:a4c1964cfa967cb939fbd793fd1cbf0a3d85603422d26a29f448659be11f1f26`  
		Last Modified: Tue, 23 Jul 2024 06:17:53 GMT  
		Size: 15.0 MB (15039757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3131bbc3bd16a5ba8213578b1c5c4ca2a1edf9ffb3a2174f8f74bf75257b64`  
		Last Modified: Tue, 23 Jul 2024 06:17:53 GMT  
		Size: 16.8 KB (16786 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:81fab7d5b2671862ce151ca0161be841197ded67b6763386fe21240b89cdfb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.4 MB (317425235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b10d2f65f7560bad8b2e9bc79f78c215c7cf10ba04d1ff8104a8edc3b8fd21`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:58 GMT
ADD file:c27c9e3b89ea2f05df44728fc1fc46f994aa335600846cab7240fdd415afec7a in / 
# Tue, 02 Jul 2024 01:19:04 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:05:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:11:03 GMT
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
	-	`sha256:47b1b1e48b458e7bb52034561a02c3a9df945540ee55d2b8112f6501aaad6d66`  
		Last Modified: Tue, 02 Jul 2024 01:30:13 GMT  
		Size: 53.3 MB (53306204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca902fb3ff705493024175dfa7b750ecd6b69939807e1032182d84553f4e2b8e`  
		Last Modified: Tue, 02 Jul 2024 02:32:52 GMT  
		Size: 15.7 MB (15734714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b25e341950d66380e7def2b99a1ad6804e2693911e88a6f3fb36c897514564`  
		Last Modified: Tue, 02 Jul 2024 02:33:35 GMT  
		Size: 53.3 MB (53311036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534425da9587d5d3e3a5e6047e9990019b07b4b673145ec12e939ebc9f59f83d`  
		Last Modified: Tue, 02 Jul 2024 02:35:34 GMT  
		Size: 179.1 MB (179135389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2abc58c95e90ff3dee94d503caa25012a0f964e599668d06b490f1f3f3332`  
		Last Modified: Thu, 04 Jul 2024 11:20:26 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6235614d07539341cf88cc91a1f39ba8a1dbea963373092a3cb1a21d4471efb9`  
		Last Modified: Thu, 04 Jul 2024 11:20:28 GMT  
		Size: 15.9 MB (15937626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f1b77df8318be86a322f05da71a4506bc4c079615e177b51447a63476312ff`  
		Last Modified: Thu, 04 Jul 2024 11:20:26 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:0953571d7a262f37300a5948da3b90e903257d3457b146b174d773fb5c5c2385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 KB (16521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc81e253e061d16d3ffa128b7b845d4e98a0c08a5b85b4778a1f072412e71afb`

```dockerfile
```

-	Layers:
	-	`sha256:2983eeffebeb9322fc4d0498a131c76626136df1a54756bad2005445b4ca61a8`  
		Last Modified: Thu, 04 Jul 2024 11:20:26 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:53a9cc61a09da36a555677066a50a97520039142dc2fcfb719f89811a8c26363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 MB (346790825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038f843dbc5b98a8620195a63faaf423d6c62d79369bb20e479a15a95ad220da`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3543cad9c41f9c9127d1adde535bc13ac5b446330727c5083aafa4b8d005c62`  
		Last Modified: Tue, 23 Jul 2024 02:43:26 GMT  
		Size: 58.9 MB (58872667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8d0e14af4e3c68b0eae63b664f02cecf25bea995af2d28db767811530400f5`  
		Last Modified: Tue, 23 Jul 2024 02:44:02 GMT  
		Size: 196.4 MB (196396379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf61b6b9b3a54026c09c3cbf0a4ff98b423797c2b882f49a74813c8fc142fdc3`  
		Last Modified: Tue, 23 Jul 2024 19:53:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d114e78db85a6c91084c395de867b183dbf35eb00ddedfe95a126fcc4c722`  
		Last Modified: Tue, 23 Jul 2024 22:31:17 GMT  
		Size: 15.8 MB (15801010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af5ba3628381e4e82dadb324d8ba043b8ebddcd6a1600addf34dd03880618b8`  
		Last Modified: Tue, 23 Jul 2024 22:31:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:489c0ef1d243632aa19c3d13e25fa76cf8caeeca4143b8f8ecd21db9993fbbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15037347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa9fc04f737a6001edb635334c83436e797d7b315c18144ad4f8aedbf36796f`

```dockerfile
```

-	Layers:
	-	`sha256:d27e12592e70caaac4c20e07afb384b992d273f31cdeb2b13c7ec5d7e6ab03cb`  
		Last Modified: Tue, 23 Jul 2024 22:31:17 GMT  
		Size: 15.0 MB (15020506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:887dfa0b5fe994ad6de7c1f942cefb081370f7ad1ec3bb093120809c3b989fc3`  
		Last Modified: Tue, 23 Jul 2024 22:31:16 GMT  
		Size: 16.8 KB (16841 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:05f8c9937bd8371c6a27d56cf90bf495e21f3c11e8323fbb5ca0b8d5e3581103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.1 MB (313147350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9c32858c95e124b483d945f616b13bc3a1ba5b8f6fd3e4749ef624d370d6ec`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:57 GMT
ADD file:5752d26037cbb262eeafd1819ecd77ecf8a8cd0019683c05fb92c50c6a458861 in / 
# Tue, 02 Jul 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:35:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:36:05 GMT
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
	-	`sha256:aa9549a3d8effd17bc1f93fd40d83261d2505d37791c5aa837c9f7c0fff5c9e3`  
		Last Modified: Tue, 02 Jul 2024 00:48:47 GMT  
		Size: 53.3 MB (53319825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7860b53e214213e98b388ade5c0d289331e291bb4e43197e4a14a4e8a111583e`  
		Last Modified: Tue, 02 Jul 2024 03:45:25 GMT  
		Size: 15.6 MB (15641817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b8db73130bc88255a98f66627e7258a074a0223eef8b550e6c1084068d24d0`  
		Last Modified: Tue, 02 Jul 2024 03:45:38 GMT  
		Size: 54.1 MB (54075315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afac5d5564136a413fbebb4f4ab7b85f2fa277f71f996d27bc1d7e24b307c5d4`  
		Last Modified: Tue, 02 Jul 2024 03:46:03 GMT  
		Size: 173.0 MB (173024898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6eb53b43cd2f55ef6a654adc7cf49b0eaec2f7bdb613e82a0ebd131220c7b4`  
		Last Modified: Wed, 03 Jul 2024 16:18:35 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d0770ac3643d86e4f91ad2e2003d114dd31f0e01f90a461961ce5fadfb4df5`  
		Last Modified: Wed, 03 Jul 2024 21:10:41 GMT  
		Size: 17.1 MB (17085228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f60ff01a29298103a8caea6f390eba57b41c268d423dab243aff29ca4ee0685`  
		Last Modified: Wed, 03 Jul 2024 21:10:40 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:2a1b8de4c109870ad7b5ce810a38fe016bfd0f8cc9ef96a6e8b9dbd3e1c4bc36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14812338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c114b385c3cb14d802d3f4c3d91bed9cafb98dca051e385f6425a61de13197`

```dockerfile
```

-	Layers:
	-	`sha256:34ad54317d61216988a5ac576bd9c0ebfde5aad9ae7ce8028c6f84fe009f5055`  
		Last Modified: Wed, 03 Jul 2024 21:10:40 GMT  
		Size: 14.8 MB (14795646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20eda7e15d1fcf4d3b952964074626f39514ab38d668d15ff0bb5e4fef2c3a25`  
		Last Modified: Wed, 03 Jul 2024 21:10:40 GMT  
		Size: 16.7 KB (16692 bytes)  
		MIME: application/vnd.in-toto+json
