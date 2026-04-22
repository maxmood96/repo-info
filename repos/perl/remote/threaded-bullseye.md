## `perl:threaded-bullseye`

```console
$ docker pull perl@sha256:f4b1a63e8ea841b9ee3da9bd766cbc4d9c7c5df38a6984f49bf0f3303d47cbda
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
$ docker pull perl@sha256:ef49e84f40957d8ec2705cb95969f5f9aae7f1c1c80e2dde1a08514f4a99907f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337514460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578c5af6466484bcda5fb522041db05a02fb4eb92f72bfb15dbf5a7d54f23b96`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:23:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:25:30 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 04:30:11 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 04:30:11 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 04:30:11 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d9f854f908f28a433fd2d5b08b5e68ee58c9ec953dac233ca6864ced59f24`  
		Last Modified: Tue, 07 Apr 2026 01:47:01 GMT  
		Size: 15.8 MB (15790676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14034e66ee3f8bcfd399019612c7f333cc777166161c3dee1a945ac1f0659fd6`  
		Last Modified: Tue, 07 Apr 2026 02:43:11 GMT  
		Size: 54.8 MB (54760196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067d6a857ea26ea67633cd59e0209cb6a54e70a1e95d19e8ae6c6b0a15b3d8d6`  
		Last Modified: Tue, 07 Apr 2026 03:24:05 GMT  
		Size: 197.3 MB (197253868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cea98062c4a3dc1c39d1e1817f67c48928a9e2c472ad81e37b30e49e6829d25`  
		Last Modified: Tue, 07 Apr 2026 04:30:28 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f22e004a8c1450a8c989b7137ed9e6f39df8007f3f17c8fe65ca92806e2f4e4`  
		Last Modified: Tue, 07 Apr 2026 04:30:29 GMT  
		Size: 15.9 MB (15946659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9452c2397e43a9977f208c064e7d37c3d47e9747cf2c2004704e3b4331a0a1aa`  
		Last Modified: Tue, 07 Apr 2026 04:30:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e1bd10fd973c1e329bcd45952a373097bbb9986a937119e2ddbd5a9ff7d491fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15491909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5babc47c9dca90a68f66ebab5152c4b21d61f1238facd0f85efa720d71a14609`

```dockerfile
```

-	Layers:
	-	`sha256:c48f71576d01aa7ca550d0b405655b7f66510fdafaecd2be1e4f0833aa16d7b4`  
		Last Modified: Tue, 07 Apr 2026 04:30:29 GMT  
		Size: 15.5 MB (15473641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc054ba3d46a31eae39736b00bf29bddf0232aa78aa6d20f5cd95c177a626cae`  
		Last Modified: Tue, 07 Apr 2026 04:30:28 GMT  
		Size: 18.3 KB (18268 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:26d8dc3cb6ddfe6d13067b3220fe635d1048db57c2f33f1f6b89029508f5e686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297326494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18efd06cc5edd31f27c1fdff5c2fb6b505401db3e8be9b34e16756eade91da4f`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:00:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:49:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:28:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:23:20 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 05:28:57 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 05:28:57 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 05:28:57 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:dc8695d526078f14ae00d8def0c6b77226df91b02937f7fe93806b494d0eed07`  
		Last Modified: Tue, 07 Apr 2026 00:59:40 GMT  
		Size: 49.1 MB (49053930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2f7a30a3127c8f109eb33c9b6e0a069dc1bbaf940f09c9ad55a2749c25bb59`  
		Last Modified: Tue, 07 Apr 2026 02:00:52 GMT  
		Size: 14.9 MB (14905095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4649005b124b78e09f68f36f64106a1bba3934081637a27e5d71125cf525a33`  
		Last Modified: Tue, 07 Apr 2026 03:49:27 GMT  
		Size: 50.6 MB (50640954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6122c866086b093947a61d79c835272268c5d8658470d831be42a283accef235`  
		Last Modified: Tue, 07 Apr 2026 04:28:59 GMT  
		Size: 167.7 MB (167730640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa44c5ace17b5838f2c65e8fa54eea342ced4b8acc319665dc3bebb8bde763c`  
		Last Modified: Tue, 07 Apr 2026 05:29:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5ab157a08aa7d444e25f04bdc0735f1efc1112c0b0408604b41221c18a52d8`  
		Last Modified: Tue, 07 Apr 2026 05:29:17 GMT  
		Size: 15.0 MB (14995607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e6166c4b720254e81a65c166a4ca70c650f3f2e7c2730ae2decfdd5e9c0a53`  
		Last Modified: Tue, 07 Apr 2026 05:29:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b719d9879f3523dfb5784e35ca6cb5e6a4abfb05989a92bc229e3c47b1d06592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd32e60adec16c87f2bec478a95808e8f4db75bd006884ce071f86a7137e8f81`

```dockerfile
```

-	Layers:
	-	`sha256:742e3fa90f1137e6c15848dc01a95aa76eddcb455d7df604163d8ebf4f739e5a`  
		Last Modified: Tue, 07 Apr 2026 05:29:17 GMT  
		Size: 15.3 MB (15272983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f12251d4cdcfe935da2c397ad86787ab27c5c9eaa5d7b839dda5fb1a7e7adcd0`  
		Last Modified: Tue, 07 Apr 2026 05:29:16 GMT  
		Size: 18.4 KB (18356 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:06ff226940ebc9581dce4e0c26f045147ade340a2623c3d61f4392d920281ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (328952401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cceadd34103d558b3d45431794c9344695142c90fea0c90551edce0d79e553a`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:42:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:17:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:22:37 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 04:27:21 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 04:27:21 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 04:27:21 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8876687e9899211f85cbf406fe17625833ba27c454fedd4275ac8a0a58206e1d`  
		Last Modified: Wed, 22 Apr 2026 01:43:08 GMT  
		Size: 15.8 MB (15774737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41762a69c06632f02d051591b8561619178cda30090272dff52f65c2d6157695`  
		Last Modified: Wed, 22 Apr 2026 02:32:20 GMT  
		Size: 54.9 MB (54886521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba12cf159babc02fc1c9dadaf51e2fca9d51183009dbc801190af3b460b98dc`  
		Last Modified: Wed, 22 Apr 2026 03:17:52 GMT  
		Size: 190.2 MB (190190591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacec7a33fcd0bcbabe438a890f20efc64a5a5659d38b8fe1f3284f70ce72084`  
		Last Modified: Wed, 22 Apr 2026 04:27:39 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428a72a757839a331c4d04db774ef957ccb512bb08be7e042f6573b6bf90204`  
		Last Modified: Wed, 22 Apr 2026 04:27:39 GMT  
		Size: 15.8 MB (15847285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6b3a00bf4b09ba5624927538706f076cdcfad2009ef6c3318d0b509aaf0ed`  
		Last Modified: Wed, 22 Apr 2026 04:27:38 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f8a980b474e3762955f94d034346e65b67e5c99e5c9ab3b1e5c8997d05a80de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15494006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f90b45460f3f266052aa848155dd9453006bc766c114f1b76e9821448a00677`

```dockerfile
```

-	Layers:
	-	`sha256:88c332d678250ab378bd46035576048768795e7d7ac4f5612f134fc92cbefd07`  
		Last Modified: Wed, 22 Apr 2026 04:27:39 GMT  
		Size: 15.5 MB (15475622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac193e800d2058ba246bbb25cd354bf5ccb60b21b855696a9c5a418b59e8708`  
		Last Modified: Wed, 22 Apr 2026 04:27:38 GMT  
		Size: 18.4 KB (18384 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:72f1d1f48dcea6c424ae72be143ef08f4455c3a96053861117ea004788639005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342712761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6dc9e969dce4b981a206469beded94394d54396461e787849a8c00156c13b86`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:40:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:19:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:20:52 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 04:25:32 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 04:25:32 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 04:25:32 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:17c3ebdef14b8265937ec7a01f6bd551a86fc0903b2144405f77b14942f88fac`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 54.7 MB (54702589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7d7ea2b68c41d012b622a11d60c4b7330f09ed012ac9774c3894afce154803`  
		Last Modified: Tue, 07 Apr 2026 01:46:11 GMT  
		Size: 16.3 MB (16295659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354a70b77dc85f405fa11ace8b407313b02fa39bd8320ba0a6a1e2b1c856fb04`  
		Last Modified: Tue, 07 Apr 2026 02:41:03 GMT  
		Size: 56.1 MB (56058498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0d7578290272fe386be38c96d8e837c43979560544df34b91318fabc54ecb0`  
		Last Modified: Tue, 07 Apr 2026 03:20:03 GMT  
		Size: 200.2 MB (200171747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8d214a44ec82698ab1f7b3b22300d4b8ed0bf348b71a398666fe070ce4a3f1`  
		Last Modified: Tue, 07 Apr 2026 04:25:50 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c84ff6646fe742774022749b1d1b685f8af18700303d461cb2580050999ee3`  
		Last Modified: Tue, 07 Apr 2026 04:25:51 GMT  
		Size: 15.5 MB (15484001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0cbc8696fe694e5785f28f059fc70e67b1dcb800a19c6e6ca167843e1cd84c`  
		Last Modified: Tue, 07 Apr 2026 04:25:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a49296622c7aa177ad8fc19bfda2a28eec69fed8237119bdd4df6932a21eeaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15479872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cc5503754bf000fcc9e8fa01ecd4fa96b7f7153d983ecba688e3f2ed3ce0f2`

```dockerfile
```

-	Layers:
	-	`sha256:ca92c921176519b1211db32cb083c4fea99a5a11c4e36f3b7ff2f67f54d3847e`  
		Last Modified: Tue, 07 Apr 2026 04:25:50 GMT  
		Size: 15.5 MB (15461641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68b86c386b956d5d13d8998734ab7dcd7e9c7b68d7c066b50f8f0dda4367fa8b`  
		Last Modified: Tue, 07 Apr 2026 04:25:50 GMT  
		Size: 18.2 KB (18231 bytes)  
		MIME: application/vnd.in-toto+json
