## `perl:5-bullseye`

```console
$ docker pull perl@sha256:870ec10a1fe77b2ada4743bd9c1662310aeb43a2004412e3e26b85d2f7ed7e5b
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

### `perl:5-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:a77280598c7a1257327d95d7a81e9036a694584f5228090a9ed9ecb533e85430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.4 MB (337373420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13df2ea1341a294fc53319c9916f6cf67aef9ad545707eb561728bd4d1c3246f`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:45:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:23:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:36:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:25:00 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 03:29:03 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 03:29:03 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 03:29:03 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac758735be4df7bbee87d37924a15ccc254964d763d0b8620fdba9dc6d6774b5`  
		Last Modified: Mon, 29 Dec 2025 23:45:40 GMT  
		Size: 15.8 MB (15764112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6512e35a226296c3166e8ce55b556c5fe6daeebccf71cdb13eccee234e17765e`  
		Last Modified: Tue, 30 Dec 2025 01:23:49 GMT  
		Size: 54.8 MB (54755226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a02f77a11e56b83bcea519986069889a0de4be2bffa5e238ee4e26de179464`  
		Last Modified: Tue, 30 Dec 2025 02:37:38 GMT  
		Size: 197.2 MB (197218457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f7a2c4a0abea9544d1198155591cd74320c287fffd2a1d5a58c3806289dca8`  
		Last Modified: Tue, 30 Dec 2025 03:29:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2b7a4e03c58ed194651221faf07440c15e18882fbb0e91f983d72d0ceab2e0`  
		Last Modified: Tue, 30 Dec 2025 03:29:27 GMT  
		Size: 15.9 MB (15878918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09e8fd40fb84a560be9a4da45bbe68f9d22d02ca4be876761969b4bd88003b`  
		Last Modified: Tue, 30 Dec 2025 03:29:26 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:07d39025810fdc348940761e9b22689f7a18a77843d84af52b5ee2ad3b0a1978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15482439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731cc3bfdb1c8d8e23581b52651bbeac4e2ec8b2f39679c50974f83adcca4f49`

```dockerfile
```

-	Layers:
	-	`sha256:7227ad604a5fccbc4372af01cf576d33fc2c59a4e7a879cfa04b6b872c2cb067`  
		Last Modified: Tue, 30 Dec 2025 05:38:15 GMT  
		Size: 15.5 MB (15464308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:110876bade6093fb1d9912926137e1c9a3d6f0b1cac359bb9c9efb9d7044af45`  
		Last Modified: Tue, 30 Dec 2025 05:38:20 GMT  
		Size: 18.1 KB (18131 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:d0122150dc9d65922c66fa9042dc65d752d09e04135fd870b68cbed60a34403d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297172244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b312b1b4e7f5ec980692803030df3b2d99367d3d395352ccf2bd3e6dca9e299c`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:06:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:35:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:49:33 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 03:54:37 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 03:54:37 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 03:54:37 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:b46683c1e86f7a120aca01c56dfafa77513b188a88759ff45f42ce118f9a337c`  
		Last Modified: Mon, 29 Dec 2025 22:25:41 GMT  
		Size: 49.0 MB (49046401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf8c40ad8b4e8cd6362fd57fbf345b792e3a334f7cfacc579cfaeef4447f6`  
		Last Modified: Tue, 30 Dec 2025 00:34:10 GMT  
		Size: 14.9 MB (14879533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318980c2ab1381876582d11a8701c769d018a68765de938c093203d5fb485b94`  
		Last Modified: Tue, 30 Dec 2025 02:06:57 GMT  
		Size: 50.6 MB (50628825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e20ad9034e29b862e54139afb5ad3088a0eaa66ff57507e0c966b81af518ed`  
		Last Modified: Tue, 30 Dec 2025 02:35:52 GMT  
		Size: 167.6 MB (167646297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d457f952c732ae5a4a6385165c2c2b4cb02f9e3f8f49d7243e9d22e780e0d`  
		Last Modified: Tue, 30 Dec 2025 03:54:59 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62fd72c604178df79168c3ba425fd90c813e7f4f5f511eb9fd8525d9641146b`  
		Last Modified: Tue, 30 Dec 2025 03:55:00 GMT  
		Size: 15.0 MB (14970922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625b4225b4784107b94b156f64890e61bfa62b78150f5f7ee74af203453ce30f`  
		Last Modified: Tue, 30 Dec 2025 03:54:59 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:11b034bc274d5af53cdf1d7aa1b879d093257f71937cea4ef8bd8bc16478eba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3efa6e635cbfeb2389951b3674c42bc7bb94445d2d9e96be46ed5c7fce6c33`

```dockerfile
```

-	Layers:
	-	`sha256:c517ec1055b5dd7fa73146460b344ccb369d32476c3579e1a62386513996e08c`  
		Last Modified: Tue, 30 Dec 2025 05:38:33 GMT  
		Size: 15.3 MB (15263650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b5294eb6f687b6c5140960ce97be631e0779ec639540d6fdf0319d42e5fa527`  
		Last Modified: Tue, 30 Dec 2025 05:38:34 GMT  
		Size: 18.2 KB (18219 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:3001b6a461559efb411fa148c976b4641ce01c33fe91eb5ed605344436a82cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328793094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2a78720b0d2993de57ebce5b98e2b88d4f74cddea7f90ce7f9c06dd6402240`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:45:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:25:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:35:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:24:25 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 03:28:44 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 03:28:44 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 03:28:44 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9549a4595c672d6f3151acb8314dc1cf09736bd0b263013f6ec6856c4c63f19a`  
		Last Modified: Mon, 29 Dec 2025 23:46:10 GMT  
		Size: 15.7 MB (15749381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890aeb16c8cc7bc154fba2dfa61907bbdbcc96a5a7b348a6376fb17c7ab1fe61`  
		Last Modified: Tue, 30 Dec 2025 01:26:00 GMT  
		Size: 54.9 MB (54865435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821c1c97ed0c0b535fe64f1b97780f9f62fe5ee7181cf3046d79708952fd6a6e`  
		Last Modified: Tue, 30 Dec 2025 02:36:37 GMT  
		Size: 190.1 MB (190111646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b032cb11d1c1cd7045de2de6d2dbd7c9bd616f9ae2299ebc90d5e575fe49f506`  
		Last Modified: Tue, 30 Dec 2025 03:29:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47cab169383f39754bcbe330d804421f0d12ed9f9baeaff1c2a3e08d9a31f85`  
		Last Modified: Tue, 30 Dec 2025 03:29:09 GMT  
		Size: 15.8 MB (15808595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2aadef026515ca6c9426e25b0875af1c9543a6b1b4e7454f075d58d1db74996`  
		Last Modified: Tue, 30 Dec 2025 03:29:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:3dbc2fa48750175be8d7db609a52e45c240ab0d68c304c2b36a6c32068c5b7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce67a280da7abcf2902c82fc057f612c6b4538725c0adc255253221878091b10`

```dockerfile
```

-	Layers:
	-	`sha256:9a042c862cd428ff2422dd63bbf95a5f6fcfd66988142a3faa29fdde1943362d`  
		Last Modified: Tue, 30 Dec 2025 05:38:48 GMT  
		Size: 15.5 MB (15466289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd973629f3bde269781a30ed1a6f9ab026ecad9d37b9c8a7854f976e622ef97d`  
		Last Modified: Tue, 30 Dec 2025 05:38:49 GMT  
		Size: 18.2 KB (18247 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; 386

```console
$ docker pull perl@sha256:5aff9486b7a3223a72f084636727b02a28956e983b51f2f7a0de329a16dc609c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342508544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c5b43f76b6076d7be94faf64aa5d48eb665346e3e1f4f84d85df12497c0611`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:47:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:32:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:48:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:20:08 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 02:24:24 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 02:24:24 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 02:24:24 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:025f128203ca36b1f5bbcf71b38334a935a5d6b64f4bfdd4dee99a843a623eb2`  
		Last Modified: Mon, 29 Dec 2025 22:25:07 GMT  
		Size: 54.7 MB (54699587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3022123a59bc3e9201838d9bb8187e2c0436e8d72f121e714ce751ebf40452d6`  
		Last Modified: Mon, 29 Dec 2025 23:47:31 GMT  
		Size: 16.3 MB (16267837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704bcf14b5c7689619866c7dc5f71300d1fa1b4363f9b2dc0af3c7d5404cad9`  
		Last Modified: Tue, 30 Dec 2025 00:32:39 GMT  
		Size: 56.0 MB (56048904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5695083195baa6a81207ae78bc1a8b4f92244fd260e0462a239c3413cf5d2513`  
		Last Modified: Tue, 30 Dec 2025 01:49:02 GMT  
		Size: 200.1 MB (200116362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfbfa8ed90a9fb7f25d8b0fad5e213321121d1aa0bbe26f94998b9a6c0667d6`  
		Last Modified: Tue, 30 Dec 2025 02:24:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b88ee74934c6618159e54a54ce3a4b5cede6830b1d259f0fe9a9d35b2a56340`  
		Last Modified: Tue, 30 Dec 2025 02:24:51 GMT  
		Size: 15.4 MB (15375587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bffb1d1003fdf8b01acf14e2e5bc1f6475cbae810a0528d13b069b52be207ac`  
		Last Modified: Tue, 30 Dec 2025 02:24:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b23c4870b9e7fde037f5e3f13b175dfa9b38064e85f280998f3ec39b63d433a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15470402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3b486f85982a7119371c23153e82ea2812e93deab56afbcc5e9a05456e635d`

```dockerfile
```

-	Layers:
	-	`sha256:168ff4751d5d43ad0244341a12ebb0e3928c30b6429ae6671663e2617453418c`  
		Last Modified: Tue, 30 Dec 2025 05:39:02 GMT  
		Size: 15.5 MB (15452308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bef4d0cf9bacc0f5ce810c25cac0d5a3362b98db1d03c69a61a76220d82a947`  
		Last Modified: Tue, 30 Dec 2025 05:39:03 GMT  
		Size: 18.1 KB (18094 bytes)  
		MIME: application/vnd.in-toto+json
