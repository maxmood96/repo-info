## `perl:stable`

```console
$ docker pull perl@sha256:a954cab65a6c8c27833b4f91964a0c2fa946cbe89f1190b932b27fa50d04e193
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

### `perl:stable` - linux; amd64

```console
$ docker pull perl@sha256:15192b4ab549a1623285f50a95811fc1690a9540587dd7b7afff4374bb2cf4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.8 MB (364804545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e6c1be78635a7753b27a32ad393e00acf11d78993579753434ead0b54562b9`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 01:24:49 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 02 Jul 2024 01:24:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:48:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:48:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:50:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbed71fc5444cf6889a21b002de3e7805e810aa88f91a9ca941b4e3880246d1`  
		Last Modified: Tue, 02 Jul 2024 02:00:35 GMT  
		Size: 64.1 MB (64142928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae70830af8b64968596022cd9041ce522f0c77eab5419b19e169b53582c69e3f`  
		Last Modified: Tue, 02 Jul 2024 02:01:09 GMT  
		Size: 211.2 MB (211225279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bff36fc8b2334af32a5dc53c1a0192c121f7f888f19d5a6d3fbe8b1252dedfb`  
		Last Modified: Mon, 22 Jul 2024 20:06:20 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a68ea494f0c9cdb9476aa9291f7383a4df116cf2f3338f26e103ba11d8647`  
		Last Modified: Mon, 22 Jul 2024 20:06:20 GMT  
		Size: 15.8 MB (15832213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f9d102fe933daff29ff412751a575f41103e4693411911d9ba4bf287d30843`  
		Last Modified: Mon, 22 Jul 2024 20:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable` - unknown; unknown

```console
$ docker pull perl@sha256:8226d7ea4a6835f3ddffd9a5f83edf0518da40cc39fc4e03ae22e7fe1b1d9cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feddcf85eaa4e994ae41bf57146e321ff80e41d4baa0f19e499c24486f0560a7`

```dockerfile
```

-	Layers:
	-	`sha256:a4778191f03d3f40d45ce7639943be612c36160248cad5b460feb35128f46914`  
		Last Modified: Mon, 22 Jul 2024 20:06:20 GMT  
		Size: 15.4 MB (15445475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8660b329cc75f931cf5121d81f9c06011f77a0b028149e591d5baf6fb96668c7`  
		Last Modified: Mon, 22 Jul 2024 20:06:19 GMT  
		Size: 18.8 KB (18799 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable` - linux; arm variant v5

```console
$ docker pull perl@sha256:0685440284858a9c650faae00418fc00d5649673c76a49373993a664d006d13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.2 MB (331187765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949d134f0dcbd5a3541f8b63041b8c6fba1ac5f05783bf978a43ddfe659f45ac`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:18 GMT
ADD file:e0c33927a1af62d353710ab02fe9345a8805475ab99685993742946d38302465 in / 
# Tue, 02 Jul 2024 00:48:19 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:12:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:14:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:f1ff7b6851f56d19040d12cd1d8757075037a3e51cd0d20ddfedfe600e399be6`  
		Last Modified: Tue, 02 Jul 2024 00:51:07 GMT  
		Size: 47.3 MB (47320358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ec281dca54581a50ec4a927c64bebe7b6ef47dad0b260009c44ae5a8feddc`  
		Last Modified: Tue, 02 Jul 2024 01:22:39 GMT  
		Size: 22.7 MB (22727504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c366b742114f1b314834ae656bee5e41f5e30629107aed4bd693207e1ed0df`  
		Last Modified: Tue, 02 Jul 2024 01:23:00 GMT  
		Size: 61.5 MB (61520104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec006b2fd0fa59480156cd480431866e4136d69ec003c1c9a01cc6cf74b4a11`  
		Last Modified: Tue, 02 Jul 2024 01:23:39 GMT  
		Size: 184.5 MB (184511793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db45ad905715b1863cb840be29800e600578efafdf6ed915a3198e08cb6e3747`  
		Last Modified: Wed, 03 Jul 2024 16:09:37 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e465e4edc5756ec80a38909115c7be6f0702e73e7da6e7bcb017bc3fcad53a`  
		Last Modified: Mon, 22 Jul 2024 20:05:36 GMT  
		Size: 15.1 MB (15107738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b3075c490fbc12960b45aaa6edd8ba9b6450d917410e5c7b8c707305c3596`  
		Last Modified: Mon, 22 Jul 2024 20:05:35 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable` - unknown; unknown

```console
$ docker pull perl@sha256:a96916b378a3766e6feb16e6fd4274a78683934efd245c3615d30cb6d2f55309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942e5f993d22033464b344d05fca97ac803b16c814e5f6088c7200984eb9cd5f`

```dockerfile
```

-	Layers:
	-	`sha256:3ae81fce90a6764deee278228afa1454d14429de208eb19c5cba38edb84ee27b`  
		Last Modified: Mon, 22 Jul 2024 20:05:35 GMT  
		Size: 15.2 MB (15244884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c182d75044c7413eb5d07952df273d54a0a0a57aad0f8f77393798884aff4396`  
		Last Modified: Mon, 22 Jul 2024 20:05:35 GMT  
		Size: 18.9 KB (18917 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable` - linux; arm variant v7

```console
$ docker pull perl@sha256:7618b7e6ce1266e6215e4506aa89f677ee947c542383c91908dc9ed254bf0c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.4 MB (316388027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f373ba0ec598d40ea469473eee0f36b76c587e8973d5cca928493bed20cf6e`
-	Default Command: `["perl5.40.0","-de0"]`

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
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
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
	-	`sha256:85754ee8352992b725147e0e20d731e73a366738cde91063265a5a9c8a21d834`  
		Last Modified: Mon, 22 Jul 2024 20:05:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da419e13b45d54afce3e64ee80dec7d4c16ce548f174a00b53509319e1d8d99d`  
		Last Modified: Mon, 22 Jul 2024 20:05:06 GMT  
		Size: 14.9 MB (14898469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4504e357bbe02f4e096fdde8791a1e71144efb53b65c098a63f74f9b39ea50b4`  
		Last Modified: Mon, 22 Jul 2024 20:05:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable` - unknown; unknown

```console
$ docker pull perl@sha256:c0b173f7fb7f349e7e040b4e348c0192bb313f669612ce15e74072162bb4e8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15269275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c09b3a3e882bcdf88f3f442b89f3eaad8861b173bfeb35baddf2e5ec76dd6a0`

```dockerfile
```

-	Layers:
	-	`sha256:826d22bbb144e67f93e119d3b151c5c646f77dd6faa1e7e91570b4797ece16fa`  
		Last Modified: Mon, 22 Jul 2024 20:05:06 GMT  
		Size: 15.3 MB (15250358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe9ff0f613800782acb82da7833828c9a1c04b7824b825b7bff166330e08543`  
		Last Modified: Mon, 22 Jul 2024 20:05:05 GMT  
		Size: 18.9 KB (18917 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:a36048f5431696de00d2cfacdd567fdf1caf2928d3cb86c0f0b40233aa008cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355572734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b683b69cf6ca76163613ea9a0974392c52692846933857640f1a2752a4c8897`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:51:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:52:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6ab51b82df5ee608db374a16686eefb99bc53834af17064184653121729b3`  
		Last Modified: Tue, 02 Jul 2024 04:01:58 GMT  
		Size: 64.0 MB (63994637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f8241ab9fefcedcf3f5b57b6b8b870d07c8ac5d8e37b6c24189ae5b084f48`  
		Last Modified: Tue, 02 Jul 2024 04:02:26 GMT  
		Size: 202.6 MB (202610801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57b4f5958685128b24a566e71db9d638eeadc0e453088a1f4c69f69b4391657`  
		Last Modified: Mon, 22 Jul 2024 20:03:06 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b7699ec3b320598a75bf37c12c8a566a076e35f04361ec8891219c2c2da360`  
		Last Modified: Mon, 22 Jul 2024 20:03:07 GMT  
		Size: 15.8 MB (15787436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491060b404aaf81f4c7fa8874bb6ae0d96f7981f1d9055183ed989edef69cda0`  
		Last Modified: Mon, 22 Jul 2024 20:03:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable` - unknown; unknown

```console
$ docker pull perl@sha256:083d7af8bda111b91429412800632410253c87328f0f3343719a612ee0127a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15493286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd092af23036e2d4de5f7600783d938d7cc3214b4abc91b46dd56ec794478c8`

```dockerfile
```

-	Layers:
	-	`sha256:aa92f20af350f45e2704f1af17eee7db839f4c196717ad25302dc486708fc95d`  
		Last Modified: Mon, 22 Jul 2024 20:03:07 GMT  
		Size: 15.5 MB (15474103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e741611647204b18c19aee9ecfa90cbf6a0b9598a9f3ff74e0f485e435b0e9`  
		Last Modified: Mon, 22 Jul 2024 20:03:06 GMT  
		Size: 19.2 KB (19183 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable` - linux; 386

```console
$ docker pull perl@sha256:353a551f81400c8eab8c78f6b52b7f387eabc02eb59a68174314382f1440df92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.9 MB (366924366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1dfb93276981aaafd93871c8390823e3a4d8c25de57be5fc94a982161f23caf`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 00:38:40 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Tue, 02 Jul 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:05:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:06:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fc07fa7086d431c647128f1beada8efce9ea5808c01b2bf497e7e85b1fda1b`  
		Last Modified: Tue, 02 Jul 2024 01:14:02 GMT  
		Size: 24.9 MB (24890132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bff6c9a28c036769727a4cf9dbe067b96273c0352a50922f6e950491245fc03`  
		Last Modified: Tue, 02 Jul 2024 01:14:24 GMT  
		Size: 66.0 MB (65988734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517d78d8993f755e32d16bdd9d852de52b88366b9799e3015e185a4a9b88f991`  
		Last Modified: Tue, 02 Jul 2024 01:15:11 GMT  
		Size: 210.1 MB (210139446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a44713c4bf2df886b3515927f99ad324ced0c4a639e06001b747fa1310e21f5`  
		Last Modified: Mon, 22 Jul 2024 20:05:47 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ab6bd80bc54effb159b3779d378ea1a317e1b968c25727d0f2f5360e449a29`  
		Last Modified: Mon, 22 Jul 2024 20:07:11 GMT  
		Size: 15.3 MB (15326480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f137a1f5cb58abcb8697953185aa965fa44c4ff872de2bc8d232fa54c5fa3761`  
		Last Modified: Mon, 22 Jul 2024 20:06:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable` - unknown; unknown

```console
$ docker pull perl@sha256:84cfa07ea0ab573fc7ceb8c0354acd7cd5761ab6b33a229dcf5bd5d2a1921ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15442971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e09e55391c761d567a2eaddb62b1521d95b0b39dbb6879187e00b71c2d5c5f`

```dockerfile
```

-	Layers:
	-	`sha256:c75573c19e029a549cf2cc0236e451ab0d35de6f39f2426b671b448004d6079f`  
		Last Modified: Mon, 22 Jul 2024 20:07:11 GMT  
		Size: 15.4 MB (15424231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:704b51aee0574d3758e4e0b7e7b4f8e9894ddda7d850dfa126b1977654d2abe0`  
		Last Modified: Mon, 22 Jul 2024 20:07:11 GMT  
		Size: 18.7 KB (18740 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable` - linux; mips64le

```console
$ docker pull perl@sha256:22b96a32d6a4c06cd885a05ace8950557e554400139d76054e88ff09204e74b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340981478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7648a70dd01ee9481a11bee23b5e21f5c1a416a47e80e3b6fc43565cd87392b7`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:7b6bffd1620df34613432d47a9414e641286a0c24330c40763ea2925fae3ff07`  
		Last Modified: Mon, 22 Jul 2024 20:24:33 GMT  
		Size: 15.0 MB (15035286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c2e5fef992eea7f5fb8ba4b33053b12df65c0de2f5a2a6718472ed60bbcc4`  
		Last Modified: Mon, 22 Jul 2024 20:24:31 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable` - unknown; unknown

```console
$ docker pull perl@sha256:93862a0227d72a390075636393bf9d6faf0a1f3e123e38301a3dbfe68ca27b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5b01fe339c1d59c58eae64d6afaa040a83613dcb19feff2cced74d51b2bb6a`

```dockerfile
```

-	Layers:
	-	`sha256:05634b8ceef0d42d1cc8aabc77492809d199ab12158664d0ee835404ed04945f`  
		Last Modified: Mon, 22 Jul 2024 20:24:30 GMT  
		Size: 18.7 KB (18691 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable` - linux; ppc64le

```console
$ docker pull perl@sha256:6b80610eb9c164d6ddc8d3fe950c4e1d5c6d6d9d8e2e899e72d856f1fa948b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.9 MB (378917613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26ab3d95ae2166ddc718bee90a21a59cb5b8ee7b14684025011ed398b7b70b6`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:20 GMT
ADD file:a02c311ba745dd8d5b3cc5585e2fe57a4aa9807b1ca2005815257da116010b54 in / 
# Tue, 02 Jul 2024 01:17:22 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:47:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:2ebe64104880a6a83eee169b12fbd82da8a0ddeac711670e50f30e975bcb92bc`  
		Last Modified: Tue, 02 Jul 2024 01:21:30 GMT  
		Size: 53.6 MB (53557015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf317c43d118e9cf38efabf9b1e93b406add8c26e307fde367e39a47a1c5821`  
		Last Modified: Tue, 02 Jul 2024 02:04:25 GMT  
		Size: 25.7 MB (25695092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f1c93d43f65ddb5b49fa7540ab263862ed9868139cb0bfc51bd8dffe47f60`  
		Last Modified: Tue, 02 Jul 2024 02:04:48 GMT  
		Size: 69.6 MB (69582302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3851398057330b42908d94c58bef25257d4970fa040c693d176d2cf32992a715`  
		Last Modified: Tue, 02 Jul 2024 02:05:34 GMT  
		Size: 214.3 MB (214252411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61648c767023e0aa37a16992cf6e076d7d1b1db58722041f3796122eed32d180`  
		Last Modified: Mon, 22 Jul 2024 20:04:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709248f2e558d1423cf6325857cf4defc9b0d78e19b89a397a73fba64f9445af`  
		Last Modified: Mon, 22 Jul 2024 20:04:45 GMT  
		Size: 15.8 MB (15830526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d1efbedf424edaf0a8d399d442865526ff39681fab42d970e563f93794801d`  
		Last Modified: Mon, 22 Jul 2024 20:04:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable` - unknown; unknown

```console
$ docker pull perl@sha256:ca88d3e665ab54dbb40cfce82b2a39b5e198da7fee64151ab398b1117ad9444c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15440905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c99f73e8b37c4f1ccfb74f5bf60349bd9e13aa5737ec9ae1f9fc847987e0ec1`

```dockerfile
```

-	Layers:
	-	`sha256:21b8af5a5977fc6f9333633df0d1f6a39f78c73dbc412f4d6ef98dd9f4a52c09`  
		Last Modified: Mon, 22 Jul 2024 20:04:44 GMT  
		Size: 15.4 MB (15422032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc0204aeb64847592389087bc7a686ec82e87a27d5e3b4350c13f756c79fb81`  
		Last Modified: Mon, 22 Jul 2024 20:04:44 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable` - linux; s390x

```console
$ docker pull perl@sha256:b48f7e09e4a269ca8bc766382b8f1823f28250b0632edca1da5fee6d3126df0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334525247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889e42eb66f646537a36208645c71ce6089494a4f74539706e471e098de872e5`
-	Default Command: `["perl5.40.0","-de0"]`

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
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
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
	-	`sha256:7b51f8c7e363058c7e97645a010b54e6cbf6c4b780c0868038b12dd3c3d69c8a`  
		Last Modified: Mon, 22 Jul 2024 20:05:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fd4d1eff7151974ae869dc790e20b80fd9647054a1bf5e59195331f70f4a4d`  
		Last Modified: Mon, 22 Jul 2024 20:05:51 GMT  
		Size: 16.2 MB (16165718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3faefffad2d3e41ec068cc8119245e9e9e686bde8da1941f9e9ee3fc85e2c915`  
		Last Modified: Mon, 22 Jul 2024 20:05:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable` - unknown; unknown

```console
$ docker pull perl@sha256:e85a4dbd12b6108636433643f1611aa824a98820912dd44f429c8e71e81f60c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15277669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7246b62103ccf315f069907b13cf805f4c2936da6d02a48f9d09361ae131fda3`

```dockerfile
```

-	Layers:
	-	`sha256:7902e77b37d8221eb948df79c5393d4740de85cdff5143f83a2c13d3c3c004c7`  
		Last Modified: Mon, 22 Jul 2024 20:05:51 GMT  
		Size: 15.3 MB (15258870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429d191b274fa9f4746a2afd44e3ce63778aec0b04b691908902e174e6144253`  
		Last Modified: Mon, 22 Jul 2024 20:05:50 GMT  
		Size: 18.8 KB (18799 bytes)  
		MIME: application/vnd.in-toto+json
