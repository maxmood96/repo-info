## `perl:threaded-bullseye`

```console
$ docker pull perl@sha256:bc48af4d44fa8d52a50bd8f97c24e1734966f3455a0e4638f0ed0dad79ec4b69
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

### `perl:threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:892c71a2cc27a0021570ba074a750274130f622ebba607488aba5b213a64d989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.4 MB (337431698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673850ec4afdd4c5a9bb70a9817d53ea68144a877caadd19bea796d4acf5f903`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:46:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:33:59 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 05:38:40 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 05:38:40 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 05:38:40 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:25 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24af405f2300f6988a2a2eaae4ec7393c0f9119fea3a400a1864fa5905a9bb66`  
		Last Modified: Tue, 13 Jan 2026 02:09:16 GMT  
		Size: 15.8 MB (15764316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91529b594c86b803d1ccddf4f9d27516e8577c5b27e466be4f89f3a15da8944`  
		Last Modified: Tue, 13 Jan 2026 03:53:36 GMT  
		Size: 54.8 MB (54755833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7faeb084d4ee23cb74164108fc63b81b8d1ee30a494ecc31d02fe53f3fec08`  
		Last Modified: Tue, 13 Jan 2026 05:25:25 GMT  
		Size: 197.2 MB (197217504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92427996deda717e8f178e7255ee1d27e1344edf08b3f3c9c1fc91eb6d3d00d6`  
		Last Modified: Tue, 13 Jan 2026 05:39:03 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bdce8be2290120d333e58cbc1f913493ad98a1e89c6f510ee052151ea5b0d3`  
		Last Modified: Tue, 13 Jan 2026 05:39:05 GMT  
		Size: 15.9 MB (15937334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699775ece488df0c7a509c1525711677316762ce9544ff0eb67c3c4c1ffc0954`  
		Last Modified: Tue, 13 Jan 2026 05:38:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:3172e4eed8ca7b373b35d86b8c1dafdfad982c550061f90aa4aa1c652a2d1863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15482666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97022fb3f3df0ba649f2028e2f5f52eeb5d946eb07f37f919b7d1e12a0e9184`

```dockerfile
```

-	Layers:
	-	`sha256:b12e839639aca42660722bce396ae096a956e9a8d60d886faff4f12bf053e1d4`  
		Last Modified: Tue, 13 Jan 2026 05:38:57 GMT  
		Size: 15.5 MB (15464398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b01b886795ff3285e8aa543a7ecc4f93993e280289c5e23fdbfccb8bd82170`  
		Last Modified: Tue, 13 Jan 2026 05:38:57 GMT  
		Size: 18.3 KB (18268 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:b1a2c8edffb1750a5f4469abe2fe30afd2d7c5a3ee9d705d338a44ff58235b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297193265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c15aa7cad395fad641da98f91b843a270acfd249b18d2df11ff28b7468d6013`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:57:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:15:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 06:44:17 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 06:49:45 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 06:49:45 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 06:49:45 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:5d86a038b54ede2ada385178a3a13e9fc7833f9952c07b251c404c3aa117dcd4`  
		Last Modified: Tue, 13 Jan 2026 00:41:24 GMT  
		Size: 49.0 MB (49046458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd38532089c34c92931050565b084061d36d5f2907633b524122c2d6f089b42a`  
		Last Modified: Tue, 13 Jan 2026 02:57:41 GMT  
		Size: 14.9 MB (14879656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e704ca674385fc92cb2832f27a6cfada2b1b4e440bed4c77bded017641bb11e1`  
		Last Modified: Tue, 13 Jan 2026 04:25:10 GMT  
		Size: 50.6 MB (50630568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fb78f7d484f57f4d1e2674d8385a6277b814bb5c23d2592e3dc2290d02b25a`  
		Last Modified: Tue, 13 Jan 2026 05:36:40 GMT  
		Size: 167.6 MB (167643408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f4a8440dc64d9f9b3a8877c370e7df44508b59111cb75291c3ffa85da58ab8`  
		Last Modified: Tue, 13 Jan 2026 06:50:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bdfae580124a2f4157dbd49b57cf0e40ccd3cf2f194d8077329f42e9e342b4`  
		Last Modified: Tue, 13 Jan 2026 06:50:13 GMT  
		Size: 15.0 MB (14992908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cae9286d111b21615d684991daa6019dea44b5aaa61a9b12becb37ea11b4db`  
		Last Modified: Tue, 13 Jan 2026 06:50:11 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:fda1844154ce0ec4b7be844f46cde988f9dee3c70f0eb6b3167060847ddd1ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15282096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786960717dacc68c22df1011b61768c9d20df63d65795ef777817bfc7e3d50a7`

```dockerfile
```

-	Layers:
	-	`sha256:c8f4bf508bf0cdc71e4280e53261a40a43cc245993b45d4e880e4de460e63f7a`  
		Last Modified: Tue, 13 Jan 2026 08:39:40 GMT  
		Size: 15.3 MB (15263740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8b1d195383e51ed9f51b5a492e5beb3f4ab325ac2eb63d4fe9760e4f51e452`  
		Last Modified: Tue, 13 Jan 2026 08:39:41 GMT  
		Size: 18.4 KB (18356 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:8f5efca6d9b7cbef3f301802e267a2ea5c142ff46577b6da06ab1b5dfe728a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.9 MB (328850051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3395d7a2d191792cd916bf596f47526a88b4c6223cd1d570ad99585036dcb39c`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:13:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:49:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:32:47 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 05:37:23 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 05:37:23 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 05:37:23 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:52 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6280b099c5251ca1a2b55e8af5af4da252bad1f89325ba7a8344f2dea14e67`  
		Last Modified: Tue, 13 Jan 2026 02:13:39 GMT  
		Size: 15.7 MB (15749667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735b68aa807ef231d58e7459ca83cac377da9d7f71d24a498190598a342d5bac`  
		Last Modified: Tue, 13 Jan 2026 03:57:13 GMT  
		Size: 54.9 MB (54863508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2705808e73b5ce7c5ea71a03de0f42c7ecdec94b51ae96443064253dcbeaea6c`  
		Last Modified: Tue, 13 Jan 2026 04:50:04 GMT  
		Size: 190.1 MB (190137777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff3861674eaf168a65c4f263af837d73d4fecadab8bacd8064a71f3a94bc19e`  
		Last Modified: Tue, 13 Jan 2026 05:37:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec15d6d546ec091f91df8d6b037bd5aec78b54316f32bd038684a51a367399f`  
		Last Modified: Tue, 13 Jan 2026 05:37:52 GMT  
		Size: 15.8 MB (15841063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd4038dcb4cd8e6789a2c06e3db2087ae1739775bd01df691ae82dbb887b317`  
		Last Modified: Tue, 13 Jan 2026 05:37:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:6a7492ddbb7044d3b6b0360104d2e802c0fca064e5d6e206a10600d7d5bece18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6f1844756f906225722e55629ccbd428b7f1d75282ab386b57fd77abb2db1b`

```dockerfile
```

-	Layers:
	-	`sha256:207c825c3467d40d080a0e2545d75d306b75c9359765030db6c15fe3eb97a22c`  
		Last Modified: Tue, 13 Jan 2026 08:39:57 GMT  
		Size: 15.5 MB (15466379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52bd28f307cd8b3ea4a1c95ae33a0ba550bac5a902b6dfd15b09a6bd0b47d3f8`  
		Last Modified: Tue, 13 Jan 2026 05:37:44 GMT  
		Size: 18.4 KB (18384 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:1a895c09991a605aca022d77993e2a831a7b535d8a5e83fddeb92a78e866d1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342604388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89fe932618111cac660aaec5fe1b0c3cdde852fb9364d239f3d39beb174a23b`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:25:47 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 04:30:54 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 04:30:54 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 04:30:54 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:7e115d265636fc6da528c1f4977e22baefb0bae7061ada6dba677a290e83b246`  
		Last Modified: Tue, 13 Jan 2026 00:41:42 GMT  
		Size: 54.7 MB (54699638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed43d5d71f701abde2a62df95258edf0ac9ef3046d49ca25c0f30e57af2985`  
		Last Modified: Tue, 13 Jan 2026 02:02:38 GMT  
		Size: 16.3 MB (16267780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50309e354294a6f81ebf1bf80c4203a79bc9374449993f7fb52ebf0640408262`  
		Last Modified: Tue, 13 Jan 2026 03:03:37 GMT  
		Size: 56.0 MB (56048907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad7ad875273afc9f1824115dad6d50ae84fba747da8a0b124f82d730bcb8bae`  
		Last Modified: Tue, 13 Jan 2026 04:23:38 GMT  
		Size: 200.1 MB (200113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563d78a122e6eacd6278124b76fbe26ddb56848d19cc2ba606e28785eb483c0a`  
		Last Modified: Tue, 13 Jan 2026 04:30:20 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac26e3dff3afd6c604f5268d71270540819ed59f8ccf4a609038d6ce6d83aba`  
		Last Modified: Tue, 13 Jan 2026 04:31:24 GMT  
		Size: 15.5 MB (15474660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9239fb62fd75cb61d01980a11c63591bdf44d2d6f6b7192811cae4d8122a5f05`  
		Last Modified: Tue, 13 Jan 2026 04:31:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:fa29603f604003af9156ada8f25e0536a86feaa0529a02199ab9b941417b7f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15470629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b43eb54edbfb839056ecd55a104f6f5f6ddbc2ea597fd92fe0f90046b1ed2c5`

```dockerfile
```

-	Layers:
	-	`sha256:fcff44e6c3dc627e1369e2dfe4e3a93001557e072fd16394aeeac888ce3ebde0`  
		Last Modified: Tue, 13 Jan 2026 04:31:16 GMT  
		Size: 15.5 MB (15452398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dabf317ce68cc695f6cd88b5a855d2be6de9c5c85bc3a2f7cbdfb22029502c55`  
		Last Modified: Tue, 13 Jan 2026 05:41:16 GMT  
		Size: 18.2 KB (18231 bytes)  
		MIME: application/vnd.in-toto+json
