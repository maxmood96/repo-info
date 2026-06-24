## `perl:slim-threaded-bullseye`

```console
$ docker pull perl@sha256:960e6edd4d89b9e2f0418736cf964942779fcd1a7db15516404d588916dbda2b
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

### `perl:slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:21d59255b792b4299d1204776daaba4b0494239ef00e8f6017c481be1972a2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56516532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000153f219d7ab003d8a8868282589aae354dcb3d90d228680960dcaae9a5e23`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:47:01 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 01:51:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 01:51:48 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 01:51:48 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:0251c4232e4025b51352f0bb7119fd866d4a6a62861f09baea6fe5af4c6eee59`  
		Last Modified: Wed, 24 Jun 2026 00:28:14 GMT  
		Size: 30.3 MB (30259447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e32a1ab283ba982eefe6c6c6ef884f3ecdf49b20e4052ac27db0691655d17f`  
		Last Modified: Wed, 24 Jun 2026 01:51:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93071341d0c8eff27d337bec508a0d62a90439fa1027dfc254e4f238bc661129`  
		Last Modified: Wed, 24 Jun 2026 01:51:59 GMT  
		Size: 26.3 MB (26256818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8362523eed80fd519d8643238d6231f79cfd77298569f2021aab1d4af8afeb`  
		Last Modified: Wed, 24 Jun 2026 01:51:59 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:be359232b8b2e7d76dc389ebe1a3366494e5a6e2d4a4b772cf8aa32d8d5df717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361526356d5253fa77cd7aa27e9e6708bc433f57e3c7f8f80914c72107e78744`

```dockerfile
```

-	Layers:
	-	`sha256:b2fca0625b1f3b18dbac12a8c77a12d74bb7626a11f14556df6c0a195d94799d`  
		Last Modified: Wed, 24 Jun 2026 01:51:59 GMT  
		Size: 4.1 MB (4129779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c310f33987d02c01b8118c4b1509e3a9f48fa5712b56a1d97a528757779f8fad`  
		Last Modified: Wed, 24 Jun 2026 01:51:58 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:a93ad5ce52ad3d2478aebe4359f36af1d46d25cf9b1845efdccb49feb7ae7ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49034900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9033c47ec9f558bcb57821d2429b2c030d0e54405be2dccc86e7e9f3b0fb09e`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:48:11 GMT
WORKDIR /usr/src/perl
# Thu, 11 Jun 2026 01:54:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 11 Jun 2026 01:54:02 GMT
WORKDIR /usr/src/app
# Thu, 11 Jun 2026 01:54:02 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:7ba7c49f3099e93649e55cb3558e8587e0d0458fc435dfc054641c2347c164c3`  
		Last Modified: Wed, 10 Jun 2026 23:41:03 GMT  
		Size: 25.6 MB (25552842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f178899a4533f28df43fa7fce7a97748d36b7b37c8f9b50e32ff356643fb2e`  
		Last Modified: Thu, 11 Jun 2026 01:54:12 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ac562a8e5bafe5ebf14a24d7950d7a014fb1e57a0da54fe27de97b831664c6`  
		Last Modified: Thu, 11 Jun 2026 01:54:13 GMT  
		Size: 23.5 MB (23481793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3651725e3b80251156292a68122f9658d1571834452e3b8436a6575d50e50c`  
		Last Modified: Thu, 11 Jun 2026 01:54:12 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:7b27eb4e29aaca3e58ceaa5a91f2b08907f8193cc940e85994e9066a66aea43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6daafde19acf3f2f938d53ccbc751bc5c844fe339f1dfde8befc03d4935a9dd8`

```dockerfile
```

-	Layers:
	-	`sha256:38090f4a4232c0e98231afe5e55e3b5da2e42b4ea5e2dd394120db5e9e53c5a6`  
		Last Modified: Thu, 11 Jun 2026 01:54:12 GMT  
		Size: 4.1 MB (4103784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fffe29d6557599110417c6aeec790105171a1392d47069668e089a729cd8b34`  
		Last Modified: Thu, 11 Jun 2026 01:54:12 GMT  
		Size: 19.0 KB (19013 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:05a6eb6bbcc30ab7e702cde4d1092ebf6df0a8af72df5f5a1050302eb3d5650b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54107332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96eecb32389e00e73d4707b6fbafe4f0700b6a5597d9550893a9cf1e8e3b8835`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:50:02 GMT
WORKDIR /usr/src/perl
# Thu, 11 Jun 2026 00:54:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 11 Jun 2026 00:54:50 GMT
WORKDIR /usr/src/app
# Thu, 11 Jun 2026 00:54:50 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7c8b63e9fdacba2b9ca76ed60aaf97ab9b9b2407a73e9cd0219ca4f02cd06c`  
		Last Modified: Thu, 11 Jun 2026 00:55:01 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508af5dc036e57c0d41c206cd521ed514ab1225cd1d93b5d3b784ea17f60bbb4`  
		Last Modified: Thu, 11 Jun 2026 00:55:02 GMT  
		Size: 25.4 MB (25360911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b265ea7a1c91af63aff4e09d1bd68dfed7391224ead3da279e70d701e84e609`  
		Last Modified: Thu, 11 Jun 2026 00:55:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:254d2f052ad9bb2ddf864599c7a79919f7bf11c609755d19528c6d4add981e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0b1f841b1719180be294045d460504cd202722c5d11a758d1ef239b2ab0395`

```dockerfile
```

-	Layers:
	-	`sha256:7c1f244917df3c53a98d671f02d2d02721f4f63dc5d0a0ecc77e30144c3af2c2`  
		Last Modified: Thu, 11 Jun 2026 00:55:01 GMT  
		Size: 4.1 MB (4104198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8138b12f721fabf92de3fb53a93939f22a885f3ceba2a2fb8ceec14d23fb896`  
		Last Modified: Thu, 11 Jun 2026 00:55:01 GMT  
		Size: 19.0 KB (19042 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:c29c1880445a53f5499900cb037997001b982bb26e4d8050a019768569cea1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59009045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e9a1edc389deec1a79552d63fbd6e95010697ece0e883d6786c36d4c81932b`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:46:22 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 01:51:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 01:51:58 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 01:51:58 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:edbad50f4a6e85b8608c496472f5f48b2e108ebbad0ca8f7c81784396f0c79d6`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 31.2 MB (31196135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5702809ef710c52c91d18fdae047ffa10fc84b5fb97b711ad843fd94ea50da`  
		Last Modified: Wed, 24 Jun 2026 01:52:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35b2ab896c2b3a319626a8c848d078307a8db186280292bffa8541cd24303b3`  
		Last Modified: Wed, 24 Jun 2026 01:52:09 GMT  
		Size: 27.8 MB (27812643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ddedc768698af294454566e824b9819f5b3cd2aeb06c6d553c5ecf9c853e87`  
		Last Modified: Wed, 24 Jun 2026 01:52:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:5b282191161372f8e1bac787ea6fca588a6253ab9f11b253213902c30d6279d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac8f1699e6938937c1408a470a143e38733d098b85f1bf3f33f2faee2d6325e`

```dockerfile
```

-	Layers:
	-	`sha256:5570a4cd9c67c17b3ad837d53f98adf3c28e36823ba45a69844de761821f1ee3`  
		Last Modified: Wed, 24 Jun 2026 01:52:09 GMT  
		Size: 4.1 MB (4134051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6127aa9f2bb63a1386d4816cc3a464f43dd3b33bdf2ec6a173e645d158bf19b`  
		Last Modified: Wed, 24 Jun 2026 01:52:09 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json
