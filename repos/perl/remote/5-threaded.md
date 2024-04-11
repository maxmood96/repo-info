## `perl:5-threaded`

```console
$ docker pull perl@sha256:bb33ca8760062b8c7edc0b14ac95e601df791229571e395959f94182321b0745
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

### `perl:5-threaded` - linux; amd64

```console
$ docker pull perl@sha256:53220353e5077e2b9fa136dc3672d23f162e25475ab787dec1114bda31cd30ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364602415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1977f5d7fb7e92b50ecb06ce019a40e0154bd9d4dac647ab2ae2b4f991a56fac`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580645a8e50b87a19330da289a9b1540022379f2c99d3f0112e3c5c4a8d051`  
		Last Modified: Wed, 10 Apr 2024 05:35:44 GMT  
		Size: 211.1 MB (211137750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289597646385d0715e0d2977cefb42f9035ca191576283943f49f230db1b711`  
		Last Modified: Wed, 10 Apr 2024 07:01:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5af91142d2a6b1a708141f3f1ee0b33c8ea9084c0e157beffdd92ed504d927b`  
		Last Modified: Wed, 10 Apr 2024 07:02:18 GMT  
		Size: 15.7 MB (15716681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7199646cd0da2985db32f279d862c9344612ec009ce8af6fbfc7340f34cebd53`  
		Last Modified: Wed, 10 Apr 2024 07:02:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:0ca13b45d05a20ff5a15b640fdb0267543a414a882621b28538c6b0f1b63046d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15388103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bb9303e58e60e05895cb054b127f3f38040c72abb5aadc070e190cc7c2b2f6`

```dockerfile
```

-	Layers:
	-	`sha256:b16f016cbeea44defd2743d5fdc9ddbfb4ea3be3c8ec6e7464262cd86961c1cb`  
		Last Modified: Wed, 10 Apr 2024 07:02:18 GMT  
		Size: 15.4 MB (15370130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e31e2247274f5ab328929114e9452bfbc511af3f66efcbfb96235086d92fd0b2`  
		Last Modified: Wed, 10 Apr 2024 07:02:17 GMT  
		Size: 18.0 KB (17973 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:6c3c2f6810e86c4de16ecf12b2a909f7c8ace42fa0267ebe3c3cf850e867c0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (330973044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78562ef080748c7206f8303628bf0ff901dbfb1bc3b476b1bb4051883820b6b`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:f3cc3d5f7d1cae45631ac2eb84f09f3bfab8fc50029f767a3b5004daf11e8493 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:5dd742eb8f72c3097f9e2af2aef94f74f93738d2c08b702932dd4bcd67ceefc3`  
		Last Modified: Tue, 12 Mar 2024 00:51:12 GMT  
		Size: 47.3 MB (47312155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d0987e351155bef4267ec491fd56aaec30a57261d0559ddd961d67e1f91099`  
		Last Modified: Tue, 12 Mar 2024 01:43:12 GMT  
		Size: 22.7 MB (22724858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f840c0f2e159cf80c44b742daea5c751f891490775e6c081415196e13e111`  
		Last Modified: Tue, 12 Mar 2024 01:43:35 GMT  
		Size: 61.5 MB (61515858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9069b8edc3144ea7c7fba8c956dedcc448fc0ba006a12c9cfe4ac23f05569d`  
		Last Modified: Tue, 12 Mar 2024 01:44:12 GMT  
		Size: 184.5 MB (184456518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea345423c0f35dddba61677d931bf109ae6b370ec39e96a5c7fb84ff5e69c9e0`  
		Last Modified: Tue, 12 Mar 2024 15:16:39 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b6c158d2a00e856f289b497c38ceb980ac1996623ad48d51bf7d0767da3c7c`  
		Last Modified: Tue, 12 Mar 2024 15:47:31 GMT  
		Size: 15.0 MB (14963387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391c842a2f4556e5c0777413267e0a3ce76d850d3ff7a5d49692142278560c58`  
		Last Modified: Tue, 12 Mar 2024 15:47:30 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:f97ab38efab0679d472b345c5c97bf81c616f1cf00b935fe9bec008da6eaec76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15197909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc68932bf6467b2521a9b155763461b258d9d20eb7014f3fbcebc642344501e`

```dockerfile
```

-	Layers:
	-	`sha256:bfc06fcd2a7d8f53adab6dbad946746d9b48ea047fc77e27f73bbfaa9ffba994`  
		Last Modified: Tue, 12 Mar 2024 15:47:31 GMT  
		Size: 15.2 MB (15180481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dea47656daf2838a9221dbc4e950a0ed939a9173f96af1112cb6309e02153dd`  
		Last Modified: Tue, 12 Mar 2024 15:47:30 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:ab8f6f2c61470217965efc7e91033ab41d5dd54d82e02062df318e4433df4937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316174920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04582a30b91b8becb5243e488861d820846411469bdf5f1ccdca709fb6163b`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b80994404300d9b15d70f0499bf342d2201561d20bd0ee4fac8c6e5db74261`  
		Last Modified: Tue, 12 Mar 2024 02:20:05 GMT  
		Size: 175.1 MB (175105976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea89ac634814fd0828b537ad8344e465a70e76436347e9ccfc80589395a25f10`  
		Last Modified: Wed, 13 Mar 2024 01:01:46 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179a32350e0a03c261884e9620bb36fb8e3bfec0be4309b7ef505c2875509a62`  
		Last Modified: Wed, 13 Mar 2024 01:49:04 GMT  
		Size: 14.8 MB (14751387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d1ef9bbfa9561f025e4d0ce59184c9abe60cf46df581ed8751803a62d1f66a`  
		Last Modified: Wed, 13 Mar 2024 01:49:03 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:02e483ae909e6ec02334aaf466e58e52e36bff80724197e4a5327b797ce57056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15203383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36457558d0fdac0c357ad4cae2b3f946d7a9a92723a38aa1df16f593cea54e74`

```dockerfile
```

-	Layers:
	-	`sha256:0a0bfe94c58d428b8b3390630bf350055635257ac75d98e47716c088214bbb49`  
		Last Modified: Wed, 13 Mar 2024 01:49:04 GMT  
		Size: 15.2 MB (15185955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:786a7d1477f2321a747637f133cc5ae4a7c4deaa1431b33d8f4c528c67969a2e`  
		Last Modified: Wed, 13 Mar 2024 01:49:03 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:8cdd5f644192d66cfa0bc1cf1fb36638bee470adca1472fa35118026df0c379f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.4 MB (355367989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08c2223022c45c599c23b889572305f96c4d9565dd371ea7436f19c336fbf48`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6faea05ead1ac9cd3244827816e2385b0d62299f7937a4574fc5a9651624c`  
		Last Modified: Tue, 12 Mar 2024 01:35:18 GMT  
		Size: 202.5 MB (202538246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77549200753f2d9ef83d1df3c80c54016724c0b1d9de2ded898ebaf1b268509`  
		Last Modified: Tue, 12 Mar 2024 22:35:58 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c28f1d82d1b6d896648cfd13e5da5cae3eb814046c3c1de9b6df45bdb8764df`  
		Last Modified: Tue, 12 Mar 2024 23:17:40 GMT  
		Size: 15.7 MB (15664702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3e5a41915939d29f83559b19b9362872087bcce36a3ff0b4f7ef701a659aca`  
		Last Modified: Tue, 12 Mar 2024 23:17:39 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:b0c40db9a91bd8acc241ea64d068ca9f1f1d7e232a787fe9725fee622a9f974d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15425926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba449aeb460ee13132f07b764c84ced229ac5d22282186891231bdd5ad792a2c`

```dockerfile
```

-	Layers:
	-	`sha256:c033e19e3ec1fe4ed0e0f7ab303f5e86899961ba79fce3096d1758781e826a53`  
		Last Modified: Tue, 12 Mar 2024 23:17:40 GMT  
		Size: 15.4 MB (15408594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700125dafd9bd19da0bc4b6f018f914a1a302289eb86f58e33bc0c9a283497aa`  
		Last Modified: Tue, 12 Mar 2024 23:17:39 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; 386

```console
$ docker pull perl@sha256:6d1cc2e6d1892597c300084b202334485fe5bf07636087900b96052e15ffb23b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366775632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798fb0d93cc34901bb999f17fe18a50e7607e04081a0447c3eadaaef9858fa44`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3845b288d815c745f12b9d8f5713e916e9d585644e3574c14b698e39da51082a`  
		Last Modified: Wed, 10 Apr 2024 08:05:45 GMT  
		Size: 24.9 MB (24884730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5c516778392288fdc27cfc451916d0d1153e04fbb6687af2b9622dea744f5`  
		Last Modified: Wed, 10 Apr 2024 08:06:09 GMT  
		Size: 66.0 MB (65987074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0cf485acf1709a8d4f069eabc7f5100b17a3a2c8e434831de60567f6d520c2`  
		Last Modified: Wed, 10 Apr 2024 08:06:59 GMT  
		Size: 210.1 MB (210058781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603be8a5850f259e1cd3d574c063a066f14e8462cb5c9953ea343210cedeeda0`  
		Last Modified: Wed, 10 Apr 2024 09:03:16 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8ff57ac9c0514810173a45c1d8a572795a258aa24ef0e80e16464e99698989`  
		Last Modified: Wed, 10 Apr 2024 09:04:46 GMT  
		Size: 15.3 MB (15257544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac65877ce5b898060cc4174d2df12b63092b7eec20ab2d1f7321fdd932275813`  
		Last Modified: Wed, 10 Apr 2024 09:04:46 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:85a9d6c8632d3c9ec585c60e8e3406505230191198f92c1c40cd9ef40dfb3e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15367080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb91f23e0a20996fbc74fabe69398f1e9cbc154585ef30e66ac7b92d772ee9e`

```dockerfile
```

-	Layers:
	-	`sha256:1be054e8ebc18eb7af2c6b2423bc4245e905579cf4e336b0c47dda2b1c5edcae`  
		Last Modified: Wed, 10 Apr 2024 09:04:47 GMT  
		Size: 15.3 MB (15349167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74510ecb1f15df3b2ecf439b091ec58f64d09dba964bc178e71fe05893dbedd`  
		Last Modified: Wed, 10 Apr 2024 09:04:46 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; mips64le

```console
$ docker pull perl@sha256:955800e08046bad3a54edf5a72ba7d20bb6258d2b815feb1f700c421e8a56f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.8 MB (340784019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6aff798d295ca797679a9ea0e4a7881f96f959eb335d7ad210ed17aae8b132`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638fdd2230a0e3b195fa0e78e24eb4739e6c5ad8a94c3bb93aedbaf4fad008ca`  
		Last Modified: Tue, 12 Mar 2024 02:42:36 GMT  
		Size: 63.0 MB (62965889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02977c85a258d317066e5a1e6febc79a4caa2a830ee66f596c866db50d3361d7`  
		Last Modified: Tue, 12 Mar 2024 02:44:46 GMT  
		Size: 189.7 MB (189698984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e408b7b8cb3719a5482c68e178858a152fb7548b871ee2a21e54534de2c216`  
		Last Modified: Wed, 13 Mar 2024 03:45:02 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178096920434cac2d2a84a13c5165619a1402ed5a3c88a05e73dbc35981c4fa7`  
		Last Modified: Wed, 13 Mar 2024 05:32:54 GMT  
		Size: 14.9 MB (14925117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a86cab0cb2378a6989610c36bfa6948b033085c674f206f909c1faaaceb9e8`  
		Last Modified: Wed, 13 Mar 2024 05:32:52 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:b2b452a90cb44bb1cfd736720e4bdcde1cfc1a8dc6f46d68711cffc3a0eca94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5209ccf39ce63ee1b75e3815de096d7c9c74973dacde6303dac7124af4eaddf5`

```dockerfile
```

-	Layers:
	-	`sha256:62eda1107a414fc4472f64da08bfd3111fe72f5e3125d5d000f62316c1850423`  
		Last Modified: Wed, 13 Mar 2024 05:32:52 GMT  
		Size: 17.2 KB (17206 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:37cd69889d74a24b2088d8d4eb4c754aa531af4d0f8b4077375fc365bcccf24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.8 MB (378770503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c5af2f5d748a775a3bf2ea00ffe6147ddf4adb1a9366148d65cb9681fcf426`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:12519205a7ecc1a9b92b9b26c967bf9f7204f2e0b9c81cb9a147b10a29b0715c in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:e6dcf23c0df5604eb9aa3050ab9c36d44dec4ab1448d2c229f4beaaf0f7fa503`  
		Last Modified: Wed, 10 Apr 2024 01:30:37 GMT  
		Size: 53.6 MB (53562477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9a49dc2918c681cd1306002e0306d198b0ab9f74366235b251cb85c930eaaa`  
		Last Modified: Wed, 10 Apr 2024 07:16:20 GMT  
		Size: 25.7 MB (25696598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7558a95a0d29869e7f316194c1d23abcbbe4d8c3340f4d3103f670b9d4af3eef`  
		Last Modified: Wed, 10 Apr 2024 07:16:43 GMT  
		Size: 69.6 MB (69581154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab0dede385435598179e3ab86d7c4094cf59880d986b82c837b42b0649d5afa`  
		Last Modified: Wed, 10 Apr 2024 07:17:27 GMT  
		Size: 214.2 MB (214172353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82b24b282bb2e235e4b3a377597eecd2e62269be1584ff5a61e734001e23412`  
		Last Modified: Thu, 11 Apr 2024 05:31:47 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41998c56a490535e2d2789c5f141093f679dbacd7034930a8d12fed1871573b0`  
		Last Modified: Thu, 11 Apr 2024 05:44:55 GMT  
		Size: 15.8 MB (15757652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add750ec020d4955478cdd604ead86265b76916d5b614c71489b204bfea66175`  
		Last Modified: Thu, 11 Apr 2024 05:44:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:951fe22c45c9d21a7207ae5167bd8d50183e6d98c678b58082dd118611f9db48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15364224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9fc94fd08657aad656990fddff31f0a0aacc4af8568146c976d0e8700d66d2`

```dockerfile
```

-	Layers:
	-	`sha256:533bd5b12b7f396450246869c5da4cbac61acfbdf40360c38ea7350c59e37fec`  
		Last Modified: Thu, 11 Apr 2024 05:44:55 GMT  
		Size: 15.3 MB (15346840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:574a1f3b58c83e1e5aeb6eacb0f2f470a2aa0fbf6c55997cc7d7fe0cf01f4beb`  
		Last Modified: Thu, 11 Apr 2024 05:44:54 GMT  
		Size: 17.4 KB (17384 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; s390x

```console
$ docker pull perl@sha256:79d9e6f7d3b0a4a7514ae5283d3d80887ad1b9ddbf740dc29fe351e1430a209d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334305131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ae2780209215341bb51a731be7bab142c007f2dcadc694a16a9ee6eb0fa83c`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:78d8ac80b1cc0c1fee1055005d9481e7bfa64e2586e84feeda25de7413892506 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:46730624c51b83b2a39f8e8dd2b4f779e9de6d2947a869347d866c219bf64034`  
		Last Modified: Tue, 12 Mar 2024 01:20:56 GMT  
		Size: 47.9 MB (47916698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddd8fd5b149ee7af1c46d50fe003e26464d37986964f535f7974aa281f5e5db`  
		Last Modified: Tue, 12 Mar 2024 02:47:27 GMT  
		Size: 24.0 MB (24043467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e216ccb0e83eab691c529b6b3db381ade89246b00d45b49aa74a6de8d55709`  
		Last Modified: Tue, 12 Mar 2024 02:47:43 GMT  
		Size: 63.1 MB (63126659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6654b38164df76c1496278c128a09a6fc9ea1d703322ccb6eb98f578047b2b07`  
		Last Modified: Tue, 12 Mar 2024 02:48:12 GMT  
		Size: 183.2 MB (183164991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72e861bb4ce86009d3ed82b0ee4ae4f028a33200978706c90c758f6bc36aa0c`  
		Last Modified: Wed, 13 Mar 2024 16:33:01 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6c795972b238751d95522b038a4492eb85b138145c4d0d6ccc72b3c1e086da`  
		Last Modified: Wed, 13 Mar 2024 18:25:10 GMT  
		Size: 16.1 MB (16053048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb14d0a85bc3d75da40dcefb2a8b2674326bfe8f5c4a30c0cbf33b91bc179ba`  
		Last Modified: Wed, 13 Mar 2024 18:25:10 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:aeb1fe1367bf1b139dad130388432bb836702d59e2d0579092bfa36ca718179b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15212069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e37fe080e0a37bb321e7f025b4572a0ce0f5e634ee86240ce3a7dbd0157d431`

```dockerfile
```

-	Layers:
	-	`sha256:01ee7a82b6afc12538ba38e43ef4e72d6da8c7af7c4dd95078ddd35d4dea3fa2`  
		Last Modified: Wed, 13 Mar 2024 18:25:11 GMT  
		Size: 15.2 MB (15194759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d3510d7c16e2cb1b0382eb037400ad1774901c1985a3eee5255c00af3e3ce2`  
		Last Modified: Wed, 13 Mar 2024 18:25:10 GMT  
		Size: 17.3 KB (17310 bytes)  
		MIME: application/vnd.in-toto+json
