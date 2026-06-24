## `perl:bullseye`

```console
$ docker pull perl@sha256:4b75609df245cf139bf319023ce23fd35c2ad768418ebaae67e010a96053327b
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

### `perl:bullseye` - linux; amd64

```console
$ docker pull perl@sha256:6f3619d37fb3f2829d6f7a6a5243ec2849ad68c82b278273b1c71b596ab2734f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337533218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3c3b55556b77406a3e4f6045fdee87f008f632946171cddba1ba389f96ca78`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:41:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:28:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:17:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:22:02 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 04:26:17 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 04:26:17 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 04:26:17 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816526a6d4acf81b392ec5a1e6d8d402fbc4bf0460323c5ad45b376b247ca6fc`  
		Last Modified: Wed, 24 Jun 2026 01:41:36 GMT  
		Size: 15.8 MB (15790805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3cf50c221acb61e259a7ecd20caf425597eca7d93e329dde2640ca7ec8aaf4`  
		Last Modified: Wed, 24 Jun 2026 02:28:36 GMT  
		Size: 54.7 MB (54742897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a160e6d2c8242d5f49a2c1be818ab0f47647e5cc5cf1fcb068e6618846d778`  
		Last Modified: Wed, 24 Jun 2026 03:18:13 GMT  
		Size: 197.3 MB (197335039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54ee2447040a47e32cd0da14f43b6ef0d4466a3df120e86257e8943f0fc0a5a`  
		Last Modified: Wed, 24 Jun 2026 04:26:34 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12446aa0d70ff729de0e2ff75a247e45fa0f3cdbf524dbdad9c757b6db84c91`  
		Last Modified: Wed, 24 Jun 2026 04:26:35 GMT  
		Size: 15.9 MB (15891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825fb9a1b4e2fb215b9583f8654bf03c3426f1a5543f941837db40c4c96ac424`  
		Last Modified: Wed, 24 Jun 2026 04:26:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:2d542f8a389002995b6a1997610cfb50ce74642e44803d084db858f7cd9d0ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15491797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da242351ce0136303360efdcbb3d12fa030fc67c0d59e86fbeae27802500cade`

```dockerfile
```

-	Layers:
	-	`sha256:74c1d067c35f444047672b1ae6b5ae6679745ff752523ad2400e9eb0253799a2`  
		Last Modified: Wed, 24 Jun 2026 04:26:34 GMT  
		Size: 15.5 MB (15473667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f14d1f8b199e2fa336ecdc72264584245b35bd8b737bd540d3fb54e0c185ded2`  
		Last Modified: Wed, 24 Jun 2026 04:26:33 GMT  
		Size: 18.1 KB (18130 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:416edd6ab07b80d35948f83c7ac805b72a3d59978a4209228a4f2561bf90c1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297384188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538af0d3d6aec62196e24ef0a0721f6ddb5883a406d6464f826c1d76276a7e79`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:54:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:17:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 05:20:12 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 05:25:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 05:25:19 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 05:25:19 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:fc5ae1e57bd12fc3393aea9c4c883b87d2ec58e18ce0892f8effba71fbfcd039`  
		Last Modified: Wed, 24 Jun 2026 00:28:02 GMT  
		Size: 49.1 MB (49064073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354f5593b138af5d5b60d8e82c822aa52fd74f6a603db24886e0573d60561397`  
		Last Modified: Wed, 24 Jun 2026 02:23:28 GMT  
		Size: 14.9 MB (14905363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf4cfcfd51cd63cbc0a86a0ed17f661e5157a3b24f24a750cdb7ac4191f84c2`  
		Last Modified: Wed, 24 Jun 2026 03:55:06 GMT  
		Size: 50.7 MB (50659165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd7e6cd4f6193c57c8019ecd8089fc02e4912acb7efee4fe62122766c0d5356`  
		Last Modified: Wed, 24 Jun 2026 04:18:24 GMT  
		Size: 167.8 MB (167779320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f201cef547f5953bf1f0269926f71c556a857b363537179eed4f19854fd2a828`  
		Last Modified: Wed, 24 Jun 2026 05:25:36 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281bd7694a23fd8f07af3e722b6081a79fd5c07e8ae004a4f53f4f973958c3dc`  
		Last Modified: Wed, 24 Jun 2026 05:25:36 GMT  
		Size: 15.0 MB (14976000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0d0abbfad041f5486fc6f1bdae220bab3ed1c514d7064d5153552836f8f3f9`  
		Last Modified: Wed, 24 Jun 2026 05:25:36 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:2e9e6642d1267d1e9266f1d6ea9f5ec865cc5b431d15829afa81767865981e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9362a4c9d60ebb040a7b693fae6ce39eceed3b21dc28f273280232dfa449bf10`

```dockerfile
```

-	Layers:
	-	`sha256:9392d428b659915a26a2be652b542574090841969493b56d33cb53f8085a255f`  
		Last Modified: Wed, 24 Jun 2026 05:25:36 GMT  
		Size: 15.3 MB (15273009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1421065257fcdc659fa7794c2be0e396aee4256eb6cd96b564e847ee0e13e029`  
		Last Modified: Wed, 24 Jun 2026 05:25:36 GMT  
		Size: 18.2 KB (18219 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:c0d690dd3f6fe2ffc622f55a304d631c589e1fd59480bc2aede7f1680ad72c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (328962187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6400619a74ee8958fcdaa346d5eba3c464d80f5d9c9b08d02935d307404ffca`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:16:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:22:04 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 04:26:27 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 04:26:27 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 04:26:27 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf305d6ad7bad47ee0696c3db8b8fed8e9c2a42c53b57d047f8ab32f5d9b546`  
		Last Modified: Wed, 24 Jun 2026 01:44:59 GMT  
		Size: 15.8 MB (15774954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f37219bba62c0b4908476dc3cf7f0f98f1c87e8908c188797b1dc1f610c77`  
		Last Modified: Wed, 24 Jun 2026 02:35:29 GMT  
		Size: 54.9 MB (54879567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e939dc6537087193b54cb28550f30706346c9eb7faf3f1da018845a5675ef09`  
		Last Modified: Wed, 24 Jun 2026 03:17:29 GMT  
		Size: 190.2 MB (190229454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0303ffbabfa7869a04b6e8d63cae2fdb6de5c667e215fd44998a158fe7af1c44`  
		Last Modified: Wed, 24 Jun 2026 04:26:45 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166d34601326fd5f6421957dbe01e631522fcb81d44b2663263ce6d7a05965fa`  
		Last Modified: Wed, 24 Jun 2026 04:26:46 GMT  
		Size: 15.8 MB (15820727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73487bb90e42ec59180bfb54ae6be5583869e3df40374b508f09ea86da1d23b9`  
		Last Modified: Wed, 24 Jun 2026 04:26:45 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:7e66c8244f1ee19248c4a0978bd62fba3056f0c286dd61dcd01ec249801286f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15493894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55a944e03f118d0839f1e7f413734dd67efdf8a31a3a6854af37f44fef50007`

```dockerfile
```

-	Layers:
	-	`sha256:dbdebd9c4e9463463a76e76494fb0f92c864902afa7a84d5c7418c4ed74cf0f3`  
		Last Modified: Wed, 24 Jun 2026 04:26:45 GMT  
		Size: 15.5 MB (15475648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be47407b6a62af609ff90050f339728fcf2ce35951d54717fe4b3aa888bb08c5`  
		Last Modified: Wed, 24 Jun 2026 04:26:45 GMT  
		Size: 18.2 KB (18246 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bullseye` - linux; 386

```console
$ docker pull perl@sha256:5009de1797e9fb11b3594d8a49da32bd622cb6d9a1c02d4dddaaff9e1ca589ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342681875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dad7ad4dc909c1f90c1c6c06c33168ff02522f655edaf37c89984f8ac51394`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:44:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:17:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:17:37 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 04:21:54 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 04:21:54 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 04:21:54 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:508ffc251196056212d40e318af0b7425af79fd3069a3f9ab15fd6220917ec75`  
		Last Modified: Wed, 24 Jun 2026 00:28:09 GMT  
		Size: 54.7 MB (54712884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f059b391cd2cd82464a697d38282bb9c5437ac5b83e7b92cde4d9a0644a137f5`  
		Last Modified: Wed, 24 Jun 2026 01:44:13 GMT  
		Size: 16.3 MB (16295718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18472033acd6c573e081fc2a3814994e7ab4e4ca2f812052bd6f7c4b0286c5cd`  
		Last Modified: Wed, 24 Jun 2026 02:35:09 GMT  
		Size: 56.0 MB (56047273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6beec4254dd6d9d54bec111217bc6634d6c5d7b5ceaa6029ae996278552695`  
		Last Modified: Wed, 24 Jun 2026 03:18:33 GMT  
		Size: 200.2 MB (200244154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d21e237d41f8cf54521d979fd0347799599c9c85abab83d56ad0949b0721519`  
		Last Modified: Wed, 24 Jun 2026 04:22:12 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27cbea24cf6933810049ded7c20ca4ad83ce81a9043ad7fb125fc2a97e64acc`  
		Last Modified: Wed, 24 Jun 2026 04:22:13 GMT  
		Size: 15.4 MB (15381578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb28f4ddb9f4b3bcc9beda0b9cf705735ab4e475dce062233c4f97e015813b30`  
		Last Modified: Wed, 24 Jun 2026 04:22:12 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:036da023a8d83116a950c3ebf6440600efa4af271889366b77c9f6adcdbf42e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15479761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d316edee572865530b311283864c7c96c6bbe50c488ca39c861de7c1f7c14c73`

```dockerfile
```

-	Layers:
	-	`sha256:1ef80beec3c22ed6be61223c1f0c4acadf7cdf375df5dfba2b976491b438a3ae`  
		Last Modified: Wed, 24 Jun 2026 04:22:13 GMT  
		Size: 15.5 MB (15461667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e00f55f59c74d45ecb892cb2b3268190551d666cda7a60769a02d54fbe6da7a8`  
		Last Modified: Wed, 24 Jun 2026 04:22:12 GMT  
		Size: 18.1 KB (18094 bytes)  
		MIME: application/vnd.in-toto+json
