## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:1b1b51f040c9c8386afc63515f86c9033bcaf0c14893c9d582d23cd442f9c203
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

### `perl:devel-slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:a2c028c2d432c5485b3fd0dbf0221938d3a7b780280f16dc5ce3c1e9f3a8d67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56457725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4203dd598dcaaf3b37c7fc2bcb486c1f8c477a864bb6ce15673eb3840ee8977`
-	Default Command: `["perl5.41.12","-de0"]`

```dockerfile
# Tue, 06 May 2025 02:04:37 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/perl
# Tue, 06 May 2025 02:04:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.12.tar.gz -o perl-5.41.12.tar.gz     && echo 'bf10191d1206a41e5a7b57fa072d80e2f9ba391a1331835f20a299cd797660bc *perl-5.41.12.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.12.tar.gz -C /usr/src/perl     && rm perl-5.41.12.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/app
# Tue, 06 May 2025 02:04:37 GMT
CMD ["perl5.41.12" "-de0"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425efbb4d4d28449929ed25a925e0811040e220c5b1574518e9325fe045c4c40`  
		Last Modified: Wed, 21 May 2025 23:32:51 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e8928300056f1254dcce5bbb659291db2c14600cd1b8b6d4d3ef9eaa5bcf50`  
		Last Modified: Wed, 21 May 2025 23:32:52 GMT  
		Size: 26.2 MB (26201519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992e47b9c68c3ade609c85792058015125baad3bff7c09ee854d61be3b42a00e`  
		Last Modified: Wed, 21 May 2025 23:32:51 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:75084fea07e32d3c372903010dbc0b092a9446007b1947a32c026ab462515f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d00cc3a393d45db20035b333ea756a768f1a8c03bc3db776ac672e66c03f18`

```dockerfile
```

-	Layers:
	-	`sha256:d2b6a2f18193d60e033e1120dcdbfbd00691939215fb1e1fa83d567f2eede3d0`  
		Last Modified: Wed, 21 May 2025 23:32:51 GMT  
		Size: 4.0 MB (4024718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496a102fe1d68385085837d21aff9cc790bcc717be51a1664b4935df2f22eb9f`  
		Last Modified: Wed, 21 May 2025 23:32:51 GMT  
		Size: 18.4 KB (18381 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:008d63e39f97b33fa3fa7361c24c7d40cca1a192182a23fe14ada78832fc9d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52780466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4d6b164323000ea44d5e23b008c34c025d98988128ffbb9355ba1cece2e708`
-	Default Command: `["perl5.41.12","-de0"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/perl
# Tue, 06 May 2025 02:04:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.12.tar.gz -o perl-5.41.12.tar.gz     && echo 'bf10191d1206a41e5a7b57fa072d80e2f9ba391a1331835f20a299cd797660bc *perl-5.41.12.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.12.tar.gz -C /usr/src/perl     && rm perl-5.41.12.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/app
# Tue, 06 May 2025 02:04:37 GMT
CMD ["perl5.41.12" "-de0"]
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec1a2611b151e1ec1cf0ef40e5fd497c5c9b8695f6903b37001848a87064be2`  
		Last Modified: Tue, 29 Apr 2025 04:24:30 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38e79452cfeecc486b67222e5a07ea30272d187ba32b0e3b404242af7518aab`  
		Last Modified: Tue, 06 May 2025 18:05:48 GMT  
		Size: 27.2 MB (27237773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bfb44f5e12f7a5e8f417d8a5d2ebf51e138234319151203a52b5fc893ced18`  
		Last Modified: Tue, 06 May 2025 18:05:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:3dbc120529a05dc8c57e9d03c78dad08f9fabf77ded4a911454f32dfb2a94ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa330a5bf52a3b7e7c30a9c053211734b5e35d3da2b66e576b23d0afd0d01816`

```dockerfile
```

-	Layers:
	-	`sha256:0d5eef5677963da71b4a971f28b473786628ab6c94b7241c1312e84655e37268`  
		Last Modified: Tue, 06 May 2025 18:05:48 GMT  
		Size: 4.0 MB (3975714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37bcbbccd65ab256a8f644cee9fd27a1fba7a642f924507e2f1d00ad09ce1e99`  
		Last Modified: Tue, 06 May 2025 18:05:47 GMT  
		Size: 18.4 KB (18448 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:20ce929b346118906e53ca14b78c1d8c5fbae7c77753ffa7a17abea237217961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58211769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0fafa7910c52fd59bbc7f0f41ca00160034da71b394312fb89c7c2421e5797`
-	Default Command: `["perl5.41.12","-de0"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/perl
# Tue, 06 May 2025 02:04:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.12.tar.gz -o perl-5.41.12.tar.gz     && echo 'bf10191d1206a41e5a7b57fa072d80e2f9ba391a1331835f20a299cd797660bc *perl-5.41.12.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.12.tar.gz -C /usr/src/perl     && rm perl-5.41.12.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/app
# Tue, 06 May 2025 02:04:37 GMT
CMD ["perl5.41.12" "-de0"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895ac38237bbe6af7dd8a0c28fc45e1ad5371403a3f63c77a574b8a5edd3704b`  
		Last Modified: Tue, 29 Apr 2025 20:41:03 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dfb33cbd3228bad3eca19bf082dafa75044d53fe9f47bed301b16472bed7e4`  
		Last Modified: Tue, 06 May 2025 17:56:43 GMT  
		Size: 29.5 MB (29466857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad1596840bec69ceb63090e21f231b6c658a3c084fed6e7749f6df14ae4b204`  
		Last Modified: Tue, 06 May 2025 17:56:41 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:6aed179cc592f6c4b029ce44f02ee5f7aad66cf0e2550c9a729eed16bbb187de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ad6df3d84d2cf6ff10024a8cbb8a1d6bb092a4eeae66f070bfb15d22137fcd`

```dockerfile
```

-	Layers:
	-	`sha256:8e370d9bae107ab898a357fe1eb09d3e7eb2cbb8039aac84409584c103d70192`  
		Last Modified: Tue, 06 May 2025 17:56:42 GMT  
		Size: 4.0 MB (3976120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f9add12f0f00c29ecc03e7731ec54e580fa1ecf4c27a886ca01559aa8b415ec`  
		Last Modified: Tue, 06 May 2025 17:56:41 GMT  
		Size: 18.5 KB (18472 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:10feddef8fc650c7800558953098735f6c4d5527c3bc7cf0d96e8da50b7d19d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58948803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878d2c441b51d8d342b7a9d9a739a34679b7f532bcecce33158d8ba4f29839ca`
-	Default Command: `["perl5.41.12","-de0"]`

```dockerfile
# Tue, 06 May 2025 02:04:37 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/perl
# Tue, 06 May 2025 02:04:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.12.tar.gz -o perl-5.41.12.tar.gz     && echo 'bf10191d1206a41e5a7b57fa072d80e2f9ba391a1331835f20a299cd797660bc *perl-5.41.12.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.12.tar.gz -C /usr/src/perl     && rm perl-5.41.12.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/app
# Tue, 06 May 2025 02:04:37 GMT
CMD ["perl5.41.12" "-de0"]
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dd9e94c1b17af08da2474f0cad4f714be3cea7de270113e42207accc7440dd`  
		Last Modified: Wed, 21 May 2025 23:44:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574f754e6ca0e9afa297bb6a988072fffd2c6c9f2078d90a4b82e2de245a2639`  
		Last Modified: Wed, 21 May 2025 23:44:57 GMT  
		Size: 27.8 MB (27759335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92e5de861e624722b7a0e9d7adb368691c532b137d4cbda016f41df3af9268a`  
		Last Modified: Wed, 21 May 2025 23:44:56 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:0cc0aa4c61b7755b0e4d9ed7bdf5640707d0aecc3f278c852b0d1036374fb47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4047354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c048b9f593497c2a6fb9d931d61ba0cc8a6b58dcac6ccad5441b9b3a76c7f30`

```dockerfile
```

-	Layers:
	-	`sha256:740195107286ab6065cc1a0fc7ba107de166396f4cc4ba9b0a26b9f44ebf2885`  
		Last Modified: Wed, 21 May 2025 23:44:56 GMT  
		Size: 4.0 MB (4029000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60089f62dfe2a18d6bcd54f07d8a27e4f16c14c719cd3cc0897751948d8225a1`  
		Last Modified: Wed, 21 May 2025 23:44:56 GMT  
		Size: 18.4 KB (18354 bytes)  
		MIME: application/vnd.in-toto+json
