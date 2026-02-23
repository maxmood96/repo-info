## `perl:devel-bullseye`

```console
$ docker pull perl@sha256:a43271e206c41d7329c0613506314fabb64bb82a06bf2a8b4c933ea8d048546b
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

### `perl:devel-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:3878e3c7ee6a95422d4578e7303e8bc017f14e288d83fb8c7b3692d5ff4b3ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337631211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5311de59b9f664df9031f4184eca292ee68bb874ebc0ea826106ae4907f9e5a`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:42:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:17:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 18:50:23 GMT
WORKDIR /usr/src/perl
# Mon, 23 Feb 2026 18:54:32 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Feb 2026 18:54:32 GMT
WORKDIR /usr/src/app
# Mon, 23 Feb 2026 18:54:32 GMT
CMD ["perl5.43.8" "-de0"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee799e8390add15bd75ca0b567540a98a55aa9abc40d4c0985dca18f87c25044`  
		Last Modified: Tue, 03 Feb 2026 02:42:11 GMT  
		Size: 15.8 MB (15765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fdfb3ae60fd4b8638b772eb2ef287a4577644db16ea91d523e4c096965618c`  
		Last Modified: Tue, 03 Feb 2026 03:28:38 GMT  
		Size: 54.8 MB (54760555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6579754635b29789797f6e942ef5b5660b9102f1f697320c35499bee41c9c9`  
		Last Modified: Tue, 03 Feb 2026 04:18:01 GMT  
		Size: 197.2 MB (197224906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99cd22e080f1696ff8313405dbc0119439c3610a3a66baf619a01ad82dec2b7`  
		Last Modified: Mon, 23 Feb 2026 18:54:53 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ea03fa43bd9e5ab90e7f64f422843dfd43dc068299c08b9327f93c7827871e`  
		Last Modified: Mon, 23 Feb 2026 18:54:54 GMT  
		Size: 16.1 MB (16123625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a28d5c04e31c768cfc4fe7433e39cd6bd11adb3075e2657355356552358aed1`  
		Last Modified: Mon, 23 Feb 2026 18:54:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:59e4d89768f2654c01e654d28bb4bb1deb26ef604920ce9c51b5e6a1614381d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15482108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ff2cff6d4886bfd35f94136d76f08b41f642732c3df607affa3b2c11150a89`

```dockerfile
```

-	Layers:
	-	`sha256:6a8130325d80a5c50716d9fe1e37a4e918686fa42abc470fabcd098fe30be293`  
		Last Modified: Mon, 23 Feb 2026 18:54:54 GMT  
		Size: 15.5 MB (15464503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8af20713c2f5f04d821b8baff3bb4ba0d3ba56ac9b654d6a593c07a091a3fcb`  
		Last Modified: Mon, 23 Feb 2026 18:54:53 GMT  
		Size: 17.6 KB (17605 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:d13092951ff84d9f3fa025b35a5e2f30d2092596ad5413d8c6febf15cfd15d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297423028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d279bcea04d736d9b9a7303580cf3735a1c4f5d5dfcdb9f2ba0a3f1dbe96009`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:30:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:59:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:21:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 18:50:03 GMT
WORKDIR /usr/src/perl
# Mon, 23 Feb 2026 18:55:11 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Feb 2026 18:55:11 GMT
WORKDIR /usr/src/app
# Mon, 23 Feb 2026 18:55:11 GMT
CMD ["perl5.43.8" "-de0"]
```

-	Layers:
	-	`sha256:6ca5f53d580fbc72887807a74d2d1c2f8900fc3f535a8082d3df4fc3f9e84caa`  
		Last Modified: Tue, 03 Feb 2026 01:13:42 GMT  
		Size: 49.0 MB (49047418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b496e431ca97183650bec266004dde0fc1c85e5f1c690d4146afd2ea94035dc`  
		Last Modified: Tue, 03 Feb 2026 03:30:31 GMT  
		Size: 14.9 MB (14881625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466cdd399272acbb9a1e85ac72634d24be95fda0a3f55eab1a8ce1da5fc02bb0`  
		Last Modified: Tue, 03 Feb 2026 05:00:10 GMT  
		Size: 50.6 MB (50640186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba49f5c360bcba7b6578f214e17256eea46d67b7e8abcf8e38cf1ecf5201962`  
		Last Modified: Tue, 03 Feb 2026 05:22:13 GMT  
		Size: 167.6 MB (167645628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57076f14091d4c19ddd08d87eb6f31a0d25c16550f48d9edb6ec99efcb9823b`  
		Last Modified: Mon, 23 Feb 2026 18:54:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ad2a15e0d19cfdd50273b4acb3278947b128eae65f21026e693a969a2a4466`  
		Last Modified: Mon, 23 Feb 2026 18:55:31 GMT  
		Size: 15.2 MB (15207903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5ca10302de0bb95083bf07bc082e4b602255c50238aadf306e8b9607ac3d9`  
		Last Modified: Mon, 23 Feb 2026 18:55:30 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:3f55ab66c6cb70edf53f6f0a537dd5dfaeaec3141b3c6fcd200ea4d09fab3aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d8cde0fc51c9157f490a3f33e59a8728e49975eea511500bfd90f2f5d7b5f3`

```dockerfile
```

-	Layers:
	-	`sha256:daa35e0456e353de0800a811fe07280e450f8be0b61f1f1a32a17098cf856870`  
		Last Modified: Mon, 23 Feb 2026 18:55:31 GMT  
		Size: 15.3 MB (15263829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe74cceb9de2a8be1e4ac1d5c2dc96142f3064056ea59b0977989770d1f3f1f6`  
		Last Modified: Mon, 23 Feb 2026 18:55:30 GMT  
		Size: 17.7 KB (17675 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:5da175fb15414edaa429885a311cf1b51b1621826211dbf2255cd2044038f567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.1 MB (329063496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a1b1417d129f8f6fad1b5bb294d1cdd9bbf0bfb99a922dcecc677e15a6b8da`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:45:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:18:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 18:50:04 GMT
WORKDIR /usr/src/perl
# Mon, 23 Feb 2026 18:54:20 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Feb 2026 18:54:20 GMT
WORKDIR /usr/src/app
# Mon, 23 Feb 2026 18:54:20 GMT
CMD ["perl5.43.8" "-de0"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8786fbba60dc8d61eaf8fb6b0cf5291a807641e61a5c761e1cba765ef879da43`  
		Last Modified: Tue, 03 Feb 2026 02:45:17 GMT  
		Size: 15.8 MB (15751646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d1a0324220213f9a9398a3adcfcebda6418d2bd83212c762c2bb386f570200`  
		Last Modified: Tue, 03 Feb 2026 03:46:49 GMT  
		Size: 54.9 MB (54875010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542cddbf58e2123886de78abce1dd6b3331f337fa011529952f26928803a5ed2`  
		Last Modified: Tue, 03 Feb 2026 04:19:07 GMT  
		Size: 190.1 MB (190134940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57076f14091d4c19ddd08d87eb6f31a0d25c16550f48d9edb6ec99efcb9823b`  
		Last Modified: Mon, 23 Feb 2026 18:54:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc560a41be88806b7e8916453b2ce2b4cd06cd61efd5d156d250a17aa2a829`  
		Last Modified: Mon, 23 Feb 2026 18:54:41 GMT  
		Size: 16.0 MB (16043312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf59169bd5b65befab76b304601a63b5960b6e89bf24a4ce1124bd96335009c2`  
		Last Modified: Mon, 23 Feb 2026 18:54:41 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:562a0c1d483198d3f51062f362870a21ef133845dd64b899351ab75e905e87d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37325c70a7d9c77d4df82e479e226568e0ec91d97902f07b449e707cc15a684f`

```dockerfile
```

-	Layers:
	-	`sha256:61263188794b084bc2258c40e5c1f1416af8f32d575447a4ce5d0a3127247c25`  
		Last Modified: Mon, 23 Feb 2026 18:54:41 GMT  
		Size: 15.5 MB (15466460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c336cd11c2cc0b21b4e047bb05f966ba173d1ae59d03026955066cd80044df0`  
		Last Modified: Mon, 23 Feb 2026 18:54:40 GMT  
		Size: 17.7 KB (17696 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; 386

```console
$ docker pull perl@sha256:6b433077d8b7e8f20f7ae889dda682a4f97a6cb2b1d467ea85cefad6a295df1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342768815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee3dc7e3accb2f17cd7a52ab43384a27341201ec0021e90f4235e6425ea5ad4`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:49:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:17:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 18:49:58 GMT
WORKDIR /usr/src/perl
# Mon, 23 Feb 2026 18:54:18 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Feb 2026 18:54:18 GMT
WORKDIR /usr/src/app
# Mon, 23 Feb 2026 18:54:18 GMT
CMD ["perl5.43.8" "-de0"]
```

-	Layers:
	-	`sha256:f6d70808fcfec5fc2c45e150a669aa79950bfd30968e7ba0de2c962cff56fc33`  
		Last Modified: Tue, 03 Feb 2026 01:13:58 GMT  
		Size: 54.7 MB (54699582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83b8227b1b97d84c4a7d4b36dd8fcd700f5f0189b543ddd06f7510ecfd20ed9`  
		Last Modified: Tue, 03 Feb 2026 02:49:37 GMT  
		Size: 16.3 MB (16270742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d99aacaea33162882dda20c6dbc4d93f0c42dec71017c78e00c9f875c6c97fe`  
		Last Modified: Tue, 03 Feb 2026 03:25:04 GMT  
		Size: 56.1 MB (56058620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6722f84a515db9aeaa583668d730b4cbe1807d3c00fade8b0de10a3b8c0dfa9`  
		Last Modified: Tue, 03 Feb 2026 04:18:17 GMT  
		Size: 200.1 MB (200125441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89ab5f9f80e532fa380c172b444af30fae17802fb9733b0f7a4d90b449f8e01`  
		Last Modified: Mon, 23 Feb 2026 18:54:38 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c05c21a3d074d64a638c1e33ca79fc9811262927f8c7c2d77668d273df2f9e0`  
		Last Modified: Mon, 23 Feb 2026 18:54:39 GMT  
		Size: 15.6 MB (15614160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae1aaaad37598a80477903dceaa3d1419ae26285f5df36622e5e6ce79499e7f`  
		Last Modified: Mon, 23 Feb 2026 18:54:38 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e3e2c88a9b1dee007d26be7195bcb1efcf9147ad3fc5e385f00f06a25b543b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15470091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb934e106de6e4df9e4163e1019dab1851bc0fb03625bd3436df0a879822f99`

```dockerfile
```

-	Layers:
	-	`sha256:5907d079919285973d8334276fbec98d95366d2e2e070168cce91205c276036f`  
		Last Modified: Mon, 23 Feb 2026 18:54:39 GMT  
		Size: 15.5 MB (15452513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea87937c1bf3a3edd184c7f70c23a6bfffb68afcec5c69e06def89062791e09a`  
		Last Modified: Mon, 23 Feb 2026 18:54:38 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json
