## `perl:devel-threaded`

```console
$ docker pull perl@sha256:7b2e5a60d2b9aeafb773f963086e9857fa6b05b04e9eea1942b7c01417ff05ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `perl:devel-threaded` - linux; amd64

```console
$ docker pull perl@sha256:9be7aa354c9c376d76e556c2819534c2687e2d45273a5dd6ed9f42b17f586bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.8 MB (394842939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd3b2b2186c4178335d030a7cb7b5c117d66b8dccecceedc9c3f428901abccd`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:50:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:33:53 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 05:52:57 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 05:52:57 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 05:52:57 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:48 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d823e3848f3d74363d9b5b44f39f2d2f81a99a37d8c7fb54831a489a32e999`  
		Last Modified: Tue, 13 Jan 2026 04:50:59 GMT  
		Size: 236.0 MB (236001828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d09603b2948786765909364921e1204b856160748af0f3f6906eaca7457230`  
		Last Modified: Tue, 13 Jan 2026 05:38:51 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc620fbe2ee7e44f6e4684b3991483e81f6f2ac55e5a4a3e261224699a1192ee`  
		Last Modified: Tue, 13 Jan 2026 05:53:23 GMT  
		Size: 16.2 MB (16155039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0833df42c5f8a9924512ef9eaed15ab79f495440a0c2f6bbaef85a93b6741a`  
		Last Modified: Tue, 13 Jan 2026 05:53:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:51c0083f8b6c377a8a63cf2efb418a72ab0d78138e67b31a1b3bead807396baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17229276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b31b8959ff8137c60a1302471ff83729b4968a636a45871f25932481b8d7611`

```dockerfile
```

-	Layers:
	-	`sha256:811666b19a10a5c9430260e631c3881f95ad67e7b4ebb706877927bedb196bbf`  
		Last Modified: Tue, 13 Jan 2026 05:53:15 GMT  
		Size: 17.2 MB (17210664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe81f631644d47c97d85f677268ec502b8e1dbf8d240c02103cfdee5887695f`  
		Last Modified: Tue, 13 Jan 2026 05:53:15 GMT  
		Size: 18.6 KB (18612 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:724211b3d06e62b5a49cb7c5ef56ff4bc2d47cef79640a0480d17a5934af1e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.3 MB (358296729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cba7de6abf4bd7e42982790f3d8e922a168ec98085b0e19e859f544986b112d`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:29:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:08:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:13:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 06:29:23 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 06:53:57 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 06:53:57 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 06:53:57 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:16d4329ceaa8dc305221873389c356e4c5bf3cdb5b245a79ff75a1b1806f3778`  
		Last Modified: Tue, 13 Jan 2026 00:42:16 GMT  
		Size: 47.4 MB (47448362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ac90147d1f1c4bc0ab2c1c245fb4105c9ad56d7e5e75726e8ec474c79f05f`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 24.4 MB (24353866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0fe9087175027e9a76a41e2c394603c9345a19f6296b58e7044e930aafb08`  
		Last Modified: Tue, 13 Jan 2026 04:08:29 GMT  
		Size: 65.3 MB (65318536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a03a66aae139adaadd8a808ca96b9e5d75cefae43a5eca814727bc64c805f6`  
		Last Modified: Tue, 13 Jan 2026 05:14:31 GMT  
		Size: 205.7 MB (205729923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058884aaeb03f8e60695d0202990780ec44ed511ea301391f6b534c0e899acac`  
		Last Modified: Tue, 13 Jan 2026 06:35:26 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b545138333bdab2f57fb2441467f5895745c1a27206030791f0259a286561a64`  
		Last Modified: Tue, 13 Jan 2026 06:54:17 GMT  
		Size: 15.4 MB (15445776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89217d0b0ac62c8f3afd0abfd4491a5276f5df630a6ba231df6a77bcb3a8ef3`  
		Last Modified: Tue, 13 Jan 2026 06:54:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:2bc7f503d5d26f55b7513565f572aef673f9d0d25c94ef205328c636382c89ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16991593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc575840ab3b3ec104633b1b9cbd245f46af9f40539f978b906250cd4bf76e00`

```dockerfile
```

-	Layers:
	-	`sha256:5877cd357871a8df8b21766d31f650976a030e5d18a9c9971bac093e58184fbb`  
		Last Modified: Tue, 13 Jan 2026 08:47:45 GMT  
		Size: 17.0 MB (16972886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0136670e5a0771306c81d5d929e61ef183cf58b799de22958004f957fb6872d`  
		Last Modified: Tue, 13 Jan 2026 08:47:46 GMT  
		Size: 18.7 KB (18707 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:2b9f741f7bde27af89e3307d25866947c62f8f63114011832d604c98a0350f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340621230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b1b7597ea030713ff17d8524421a87736f015ce548e632966b98d3b265cafc`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:25:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:19:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 06:37:51 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 07:31:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 07:31:52 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 07:31:52 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:0f4296a8ece8abd5a409e5fbdb0cf93258815e4fec9dc768c39a63faf3c16052`  
		Last Modified: Tue, 13 Jan 2026 01:18:45 GMT  
		Size: 45.7 MB (45717820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8e700e2f18987ab9f97abcd0497d5dfc1706a8c057e685438ce3b71d8067c0`  
		Last Modified: Tue, 13 Jan 2026 02:59:15 GMT  
		Size: 23.6 MB (23626665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf6f5dfbcc297b2e354e856be84c591ec9f96e89fd8401a4d485596c43b8ed8`  
		Last Modified: Tue, 13 Jan 2026 04:26:15 GMT  
		Size: 62.7 MB (62713384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc2c3dfa2d6df259da14558beefb7cee69246c0da0fdc440a04d5af7c8fb7dd`  
		Last Modified: Tue, 13 Jan 2026 05:20:01 GMT  
		Size: 193.3 MB (193306851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f016ddb867ea0367ad3fe4f01041ba08d579f7645ca33bad41cd0c1072a413`  
		Last Modified: Tue, 13 Jan 2026 06:43:40 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ad6d970e6a8c20b464ee0c9c41622bb190a9bc4d7979bfe78e9cc142077611`  
		Last Modified: Tue, 13 Jan 2026 07:32:12 GMT  
		Size: 15.3 MB (15256244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035cd1ab0c99e6ec7b7651af4b5a935336a96143c3dcf35bcd7b3c8782b9929`  
		Last Modified: Tue, 13 Jan 2026 07:32:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:f8706382331daae5c98d724631b9516a4b26a5c2c77045a878f976bb1f22ff23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16997384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00e533dfd2e0f8a3418f1a75bc19242008aab7fdaa16482c2dbf5e96e4d6b4b`

```dockerfile
```

-	Layers:
	-	`sha256:e17c85c37a64690fded3b476197c0554c648a37d41ce2269b29d1ed8f43d9fa2`  
		Last Modified: Tue, 13 Jan 2026 08:48:06 GMT  
		Size: 17.0 MB (16978676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:227bd13e5f7f793ee94b882d482c63385575e545df6d5b6afb0426a1af2dd5ff`  
		Last Modified: Tue, 13 Jan 2026 08:48:07 GMT  
		Size: 18.7 KB (18708 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:8b325cb8ac8405308faa081d82292b104c7824c08a52210688f8c1f661b50244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384504417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cde08736fccc5661edaa0a3e61b0dfeae11c7f7662d68b0d8c945b46cee3a2`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:52:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:31:37 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 05:52:38 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 05:52:38 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 05:52:38 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:57 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:49 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fffeb567ed4215b503f814aeaab9fa5a2e701d3efa35d4c285b3cf111e9cb4a`  
		Last Modified: Tue, 13 Jan 2026 05:16:01 GMT  
		Size: 226.1 MB (226143857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aed25628dbc28e7f46f4dcebe2739a13202d385a8f543531cbfa592e030125`  
		Last Modified: Tue, 13 Jan 2026 05:36:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eaf71005861ed41bf249b02666b8261ea405ef4707cc2882a4af7e151e0c14`  
		Last Modified: Tue, 13 Jan 2026 05:52:59 GMT  
		Size: 16.1 MB (16098062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4958c4fbf38095166693ff9a387080968a3093ebfd9a278ddd538a510b22f196`  
		Last Modified: Tue, 13 Jan 2026 05:53:04 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:28a46c7fec9c447f55c7d86fc0aeab44e9dcc78367d80f01c3eee9bb7844a9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17313734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d03c19b3d06bdea3bbc123157ed2d9f542528c0109295f06c8fc0e4c900512`

```dockerfile
```

-	Layers:
	-	`sha256:0ec16ec3aa35d049f93d22c2d651ff051878593343c21ce18341d79e24598ef8`  
		Last Modified: Tue, 13 Jan 2026 08:48:27 GMT  
		Size: 17.3 MB (17294994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:485021f028539ef52ce1e213d7a803b4f80d46a89a68adef5f0f2d1fc3f2d804`  
		Last Modified: Tue, 13 Jan 2026 08:48:28 GMT  
		Size: 18.7 KB (18740 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:11ed5e4452e55290be7a9dc4f170db3b45492972803691ea9688e691e0b03bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.5 MB (400466831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3265f58f057f3d30cbf963976a8d5fab242b138bb4489b4203ee3e02f50d6c85`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 09:15:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 15:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 16:13:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 18:36:00 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 19:06:18 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 19:06:19 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 19:06:19 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21554c0ffe7aa9121703873815aca94dbbdf6352a46266dc923fc9e36d0d58a`  
		Last Modified: Tue, 13 Jan 2026 09:18:09 GMT  
		Size: 27.0 MB (26998052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb58d20828d54df35a08218c574236606c9e3ab14d0f2ddf036e12abcf8c85d6`  
		Last Modified: Tue, 13 Jan 2026 15:20:19 GMT  
		Size: 73.0 MB (73037608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e13e772271d599b914654801e760b6e090a2d2a51765f2bd85981f821d1eb0`  
		Last Modified: Tue, 13 Jan 2026 16:14:51 GMT  
		Size: 231.1 MB (231145655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7620e836e6fe63c19ace32872be567468aa5e39f6221c796982d10ab4f82e30`  
		Last Modified: Tue, 13 Jan 2026 18:43:28 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db0e9af3926fbdb28faa3097d52e79d096266fae015762a2e32f4961236cd94`  
		Last Modified: Tue, 13 Jan 2026 19:07:34 GMT  
		Size: 16.2 MB (16178288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f8d237b3ca529d7a897d490791ee5d5a00816ed9e78d7f0b1a8e763e03a861`  
		Last Modified: Tue, 13 Jan 2026 19:07:15 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:eb2a263ce9344ef681f9a50de5bbbcd2920914d09e803586bc795c987f6d3ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17214900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa366d95f1edbbd83b43becdcbfc5df3201c097cf1b375f3d807de96d4c0b7c`

```dockerfile
```

-	Layers:
	-	`sha256:5d321dd60114dab8d75ae56cad327e815ff24723ef6b6dafc76ae79c974422f0`  
		Last Modified: Tue, 13 Jan 2026 19:07:16 GMT  
		Size: 17.2 MB (17196233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b7b3a2dc892042d9e1a1a43e2d7adb8c94a712aef2bed0bfcf87a6fc009334b`  
		Last Modified: Tue, 13 Jan 2026 19:07:15 GMT  
		Size: 18.7 KB (18667 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; riscv64

```console
$ docker pull perl@sha256:115d01a8e3c1118b6e4cd60ce357d076b330b830c6a43e7d363b1e37b945c47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.9 MB (477879002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde6ea4d22b59ad0378dfeca4c2c300916ae00e9b06715bdffc8974131eff3a7`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:16:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 12:43:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 20:04:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Sat, 03 Jan 2026 01:35:40 GMT
WORKDIR /usr/src/perl
# Sat, 03 Jan 2026 11:41:12 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 03 Jan 2026 11:41:12 GMT
WORKDIR /usr/src/app
# Sat, 03 Jan 2026 11:41:12 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f7933c6ef71f06a1f0f33145f157cbfe6df70a0a3efc496c514e6bf0f3c52`  
		Last Modified: Wed, 31 Dec 2025 10:17:37 GMT  
		Size: 25.0 MB (24953863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e727fba04feac92f30181733d92a9aab095f91af402efca58918b26fc389037e`  
		Last Modified: Thu, 01 Jan 2026 12:46:45 GMT  
		Size: 66.7 MB (66660576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5842d1b9c503108d0c11e7fac9c78cd2e8430f5b938c14278c02d62d5dcbea`  
		Last Modified: Fri, 02 Jan 2026 20:21:44 GMT  
		Size: 322.9 MB (322886588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89744d281ae7043a6d08686f11a85482d714b043baa7087bf99fb9b551b5cd58`  
		Last Modified: Sat, 03 Jan 2026 02:48:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e9a1267b2e233267bbe6660f88da2d6ed5c5e970186742287bf7db09d788b`  
		Last Modified: Sat, 03 Jan 2026 11:49:18 GMT  
		Size: 15.6 MB (15606555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab74caae6bdbc271f7e45f68dcacd307e514d86c4cd25464cdc0d9971a3e0f1c`  
		Last Modified: Sat, 03 Jan 2026 11:49:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:113e0dcdf166ad726498465c68d3c08da90e6dbb7d113b7187527e0a5b5ca509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17284359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a5f22af3cf1ceb6ff2c01aec5903d87d1106277057c5fb78e50c18c8e5067f`

```dockerfile
```

-	Layers:
	-	`sha256:60c2f499870655d2e0903ad777b1059a10d85a82843e1eb184fcd0b599ced93a`  
		Last Modified: Sat, 03 Jan 2026 11:49:10 GMT  
		Size: 17.3 MB (17265691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd93b30b70c5c0b4c9213d6da542ba7c37797991d18bed965a602490ece768a0`  
		Last Modified: Sat, 03 Jan 2026 14:41:04 GMT  
		Size: 18.7 KB (18668 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; s390x

```console
$ docker pull perl@sha256:6cdab2a4a02bb15574580ac4919a7f0406d89c57d0970e8dbdc830618ae5cd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.0 MB (368045344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224170a6d616fc68d9fb032eeb33c56c569d155e7b951aec7fb25258b7d88753`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:18:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 07:05:25 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 08:42:04 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 08:42:04 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 08:42:04 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a9411869af8d59bfb1073c3573138af1f96d808896b3f2fd14cf62fca6dba`  
		Last Modified: Tue, 13 Jan 2026 02:11:26 GMT  
		Size: 26.8 MB (26792892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff54b33211ee85001fc045dcc86b026876894b17d1d6f873a415014f68cb0c9f`  
		Last Modified: Tue, 13 Jan 2026 03:16:21 GMT  
		Size: 68.6 MB (68632678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fc8348b5ddb8c2acabb8e9ca2d1b4b97457b5a1f89dd3ca04047f15644b88c`  
		Last Modified: Tue, 13 Jan 2026 05:17:23 GMT  
		Size: 206.5 MB (206530469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242d2c95c50ac1bae020573f8e6ce3b707f5e2ee7c69bb6fca594eb686465013`  
		Last Modified: Tue, 13 Jan 2026 07:11:51 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af25eef97c4505c079aaa3d4fddb56d7a5a0d3f6a61906441b62d7d614f6ab5`  
		Last Modified: Tue, 13 Jan 2026 08:42:39 GMT  
		Size: 16.7 MB (16740334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c2d06e80cb058f59f3bb795c126e7fb0ef41c9b7bd84301e19cb18c03f1f0c`  
		Last Modified: Tue, 13 Jan 2026 08:42:45 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:477018b4dbabeb6d3f37612654cbc5137dd41c465944b3f306103b6c92cfa5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17006509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecd18b49089ea9955a3f5b259135eb515e4a887199ee18f2c41e6f6d0f07e47`

```dockerfile
```

-	Layers:
	-	`sha256:7147e86c2e64f630c090f5b07777ba431f9f837b44b493b02a02e3aa1577dcfe`  
		Last Modified: Tue, 13 Jan 2026 08:42:39 GMT  
		Size: 17.0 MB (16987897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70a58a2d4131cc5330814fcca6855431418d7a397fa18c72f674c529c714c0e2`  
		Last Modified: Tue, 13 Jan 2026 11:42:15 GMT  
		Size: 18.6 KB (18612 bytes)  
		MIME: application/vnd.in-toto+json
