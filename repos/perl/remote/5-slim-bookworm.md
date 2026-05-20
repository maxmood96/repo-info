## `perl:5-slim-bookworm`

```console
$ docker pull perl@sha256:225227672c078cbc3956c73d58579ca6515c5b6e8a6278178f81fdec7648c12b
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

### `perl:5-slim-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:e6d765d864d5af9edc19412cb978e3377d9f2ec55edb7f713c75e43216149fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58444335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a27ca45b437edbb4f7fe5410f96e0afc312048177fd8064329380fdd2bacc6b`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:28:39 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:32:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:32:54 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:32:54 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a85acbd4d816eac5e3de1b33abfc7db152f17443f4a6e41311b61db3748b4`  
		Last Modified: Tue, 19 May 2026 23:33:04 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafd0d910137a9010474e7dd44054b0d6f007202ddd7243b68c0d6428111d8d9`  
		Last Modified: Tue, 19 May 2026 23:33:05 GMT  
		Size: 30.2 MB (30210523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcc407f14e59a5cdbed14ffc88452e816414d24f1f3f646787f62012346cc3e`  
		Last Modified: Tue, 19 May 2026 23:33:04 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:f6ec54703b15d7fb6335d154e56c68c8950060ef0882ba301042df64c196f8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b6de68ee367530d3e135a6cc584b503f8da0a01ed06790700b9ec41b7c6c7f`

```dockerfile
```

-	Layers:
	-	`sha256:9cdfb83420bbe7b0b236da87d6fa0a2d1d0fae6a2d246ff2d64f7fc2dca8b017`  
		Last Modified: Tue, 19 May 2026 23:33:04 GMT  
		Size: 3.9 MB (3939980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd055e8ca0b3990e066c78a6c38ede30ea5bbc6fca9656b7d76ce4d2241e536`  
		Last Modified: Tue, 19 May 2026 23:33:04 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:936f04457e814db56cc32ad1a067e5e8cea5a02770b3abcd79782ada00f0d688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53033834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3b30f469b7da6c76abaaa20b69ba27baf3dd21f2bbdcf5b2a21ec54ea470f0`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:57:40 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 21:03:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 21:03:28 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 21:03:28 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:0496e5b1fd9475851f8b3578080061a05ea61be300ea5a278a4a08a883855adc`  
		Last Modified: Fri, 08 May 2026 18:33:05 GMT  
		Size: 25.8 MB (25765670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458436663a7966df4056cc44145874f1cb8d513be7e37baf3a7ee232018e45b4`  
		Last Modified: Fri, 08 May 2026 21:03:38 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9421f524fe362deccb0f1eee270704e24559f5dde51d1effd25e8e06bd564e5`  
		Last Modified: Fri, 08 May 2026 21:03:40 GMT  
		Size: 27.3 MB (27267897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce9ac0e6e4af54cef5613c665e27346158bbc641c3ab561a1b33ba4b102f5cd`  
		Last Modified: Fri, 08 May 2026 21:03:39 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:98287a9aaecc66720f7f84f8f72ee2c8a8b57f1e675ec5afbdcd1546bf024351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab96be42fad0dbab8d229018834395aec78548d16028a119f956d568bb5c890e`

```dockerfile
```

-	Layers:
	-	`sha256:ce96da69e87926511f1f8802f094f34c30c158a76de1f9ef9416c7e72a96ce7f`  
		Last Modified: Fri, 08 May 2026 21:03:39 GMT  
		Size: 3.9 MB (3910829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa8bf9b24506f1cf78361ddf60b6bb6d530e2b300ba56af3acae119c68ee1039`  
		Last Modified: Fri, 08 May 2026 21:03:38 GMT  
		Size: 18.9 KB (18876 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:cb840d4f6d91d5c50ee7307237685b1c08a533dada1bc3a3cf1bf407e3ae8ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50309259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6839a5a4394fa7640a6a2f57c557fb4012b42b8b98dc85ca85c3d7c2bc409ba4`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:47:07 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 19:52:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 19:52:40 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 19:52:40 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5e9fe242eaedcc1a7f865393f7c1e89af25994437ffe48446111b6ab40c35e`  
		Last Modified: Fri, 08 May 2026 19:52:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8ea4ddb007ef40736c848f397314907237ea830350c664916cf8b25ce1bd9a`  
		Last Modified: Fri, 08 May 2026 19:52:51 GMT  
		Size: 26.4 MB (26367586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe997b4e56a93fa1b6dabf4aea5a7600cc24d224fa45216d0704c1169c5f2057`  
		Last Modified: Fri, 08 May 2026 19:52:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:15e857789d3dbc8d3a561f9892d5862e04a562e0c17ad4522ad671ee973c73bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffa5a3617a4fd6bc820594448046c4e2514403698ff6e9b741878a75dcd0c24`

```dockerfile
```

-	Layers:
	-	`sha256:a1e245c3a978507407abda70ca042f9b4e38eabb295ef779f385cc6a92c4c21c`  
		Last Modified: Fri, 08 May 2026 19:52:50 GMT  
		Size: 3.9 MB (3910054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed712e0036099eee1da6dbd0ba1afaa1c7a86209bea349d03f52569bd679e3f7`  
		Last Modified: Fri, 08 May 2026 19:52:50 GMT  
		Size: 18.9 KB (18877 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:e2bff27f40357f299b1b4510ef606e85ea5e9314077d54e0146dd824c6877ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57184468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5426b6d3eca8216b72e639d0ccbe9238008701970692acd7e0c316a2040c158`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:32:21 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:37:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:37:02 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:37:02 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5d16f7837c67f8b6bf4124d2eac0dfaa965b820f3cb77f0f32bb1a5b67b9d6`  
		Last Modified: Tue, 19 May 2026 23:37:14 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bc95c292a5d47af06060856c7302910f7bc38b506cbfd939a404ce2a2cab66`  
		Last Modified: Tue, 19 May 2026 23:37:15 GMT  
		Size: 29.1 MB (29069157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12b55310a1af342b5a84c14c2ab4b2f9d994e3d7d085ec8dcc4a5782bb3b50c`  
		Last Modified: Tue, 19 May 2026 23:37:14 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:f64583578bc9ac15a21cb1b7191d3335172ea776f50f28d7b07e87e8f44e2afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b204984e245b717b194a7eccf9ea630fbd909fa931cdb11d1f3494316ef99550`

```dockerfile
```

-	Layers:
	-	`sha256:0a75e69c4e60ce86bec6ed217089fc811d55caabf261954b0d2ac2277e436b79`  
		Last Modified: Tue, 19 May 2026 23:37:14 GMT  
		Size: 3.9 MB (3911241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a0bc22c7246e965e83fd1aea8caaa962a8c09b17ca7e6406dbb8134aacf974b`  
		Last Modified: Tue, 19 May 2026 23:37:14 GMT  
		Size: 18.9 KB (18906 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; 386

```console
$ docker pull perl@sha256:5104b97e8af0891ae776fd5f263c3d31f855a189ace0a11981fe36d444b670c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58550274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df51bcbd6083c7a73e48846cf56333daee53511e97c0178bd6d7fbeab011dbdd`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:01 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:32:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:32:18 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:32:18 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb0bbf97529068c9be5fd91b47b9953dd4db348b095b4e4d963f65d8e1034db`  
		Last Modified: Tue, 19 May 2026 23:32:28 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc82ecb3bcc208d31f086b5a9004ac06b45ef649131b18381d6f6d60632f320`  
		Last Modified: Tue, 19 May 2026 23:32:29 GMT  
		Size: 29.3 MB (29331406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677708c735203b3003effd25258853821bfa86f6ca0a349e0bdc294e94c11d76`  
		Last Modified: Tue, 19 May 2026 23:32:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:48a3c07fc5c5265306822911314172e00720f4556abcfa3a3e9536ccc91a0d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5d79d4bbbe4cacbc2e64ba17dbb91d3e683de367c491d2c994634cd9605afb`

```dockerfile
```

-	Layers:
	-	`sha256:d0bf0bf3a0817f25b5edc33aa9bdeb7dfa3db254dbfb628b279ed472e9d7a00d`  
		Last Modified: Tue, 19 May 2026 23:32:28 GMT  
		Size: 3.9 MB (3933912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2511bacf0dad88ab77fb24ad9d31d8028bef1b6436edc93581320811c0ed88b9`  
		Last Modified: Tue, 19 May 2026 23:32:28 GMT  
		Size: 18.8 KB (18753 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:26f2d2b02be43541896ca3b3e3edca401f5a300e8a46d110cb2fdf57b3200ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56895747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8aab0569bb98985fcf81d480da5ff5bff60234f85b4607a3e93f66843114b5`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 07:08:16 GMT
WORKDIR /usr/src/perl
# Sat, 09 May 2026 07:33:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 09 May 2026 07:33:18 GMT
WORKDIR /usr/src/app
# Sat, 09 May 2026 07:33:18 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:8e1a6f4f5a9e9628f902e3c8df639d1691d7f1000dc904f820155d1b9b2fa2ff`  
		Last Modified: Fri, 08 May 2026 18:20:04 GMT  
		Size: 28.5 MB (28526280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d14ddd3bed515cfc752781c3991360ceb5cf7a65ec98dc867fe1a1ae48e6ab`  
		Last Modified: Sat, 09 May 2026 07:34:02 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cbfb645578ea78ffe4e5250313a5c83b2ba97ec22392bcc69594ebbabf517d`  
		Last Modified: Sat, 09 May 2026 07:34:05 GMT  
		Size: 28.4 MB (28369199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a6b547f55980c6e3f85352939486276108dc327de3e32ad4600178ad8933c9`  
		Last Modified: Sat, 09 May 2026 07:34:02 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:e2a21385ed66daa0a070cf037286473cce5a1e3155991596d3baf44081ed305b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787b48f84aef32bc27c9e99c97274da18aa138ffc86eec6cac41eb6bb47f384b`

```dockerfile
```

-	Layers:
	-	`sha256:7827052966f5f7a5117f0d203b0c75f22400a29bd43d834bc429c5e800c278f9`  
		Last Modified: Sat, 09 May 2026 07:34:02 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:52258b01eaf8cb836fc7de0941af615992799168877d3489fef2588b66852bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63082347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d93382cc22b1def242bd9c5e08536fad64185a4bf7c54ea3c6159e60edef183`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:50:43 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 22:59:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 22:59:50 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 22:59:50 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6e6f1c77c9955dfc698489a3c4d78858bb1799b5a5f328728717274537eb4f`  
		Last Modified: Fri, 08 May 2026 23:00:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e389b0901c593ecbe690c02ade63caa0cd9c8fcbc58403910872026f8d642edc`  
		Last Modified: Fri, 08 May 2026 23:00:13 GMT  
		Size: 31.0 MB (31003626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518eb455e233252755ac5452a2c1624fd8070301e205a39e55749b790efb651d`  
		Last Modified: Fri, 08 May 2026 23:00:12 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:46d43e7d391fca565480568a372be2104140a243c5f85987f57b115ec72e22f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e259aeb68c3b9aeb026b7afc0025538eb3caa49a9207a2cca2d6c0c63b8bec`

```dockerfile
```

-	Layers:
	-	`sha256:8e01af772ded3906b6263c43d6242999a5e3ea30e4599369f9fca75a3f5a4842`  
		Last Modified: Fri, 08 May 2026 23:00:11 GMT  
		Size: 3.9 MB (3925902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7a7f29d7b1c600c42cd6a86a44346b5a3c4761d4d5d6a9021705d997aa234c`  
		Last Modified: Fri, 08 May 2026 23:00:11 GMT  
		Size: 18.8 KB (18840 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:4c1f5ddb26deacdea071eb26806bd8d63c513340daf933076be20f65485c496c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55644456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1fdff244636f6261ff3e1edc284f7e300a7a5fe45ddc8cd97779c5e4bf6761`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:26:50 GMT
WORKDIR /usr/src/perl
# Wed, 20 May 2026 00:33:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 20 May 2026 00:33:53 GMT
WORKDIR /usr/src/app
# Wed, 20 May 2026 00:33:53 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549afd7eb519783babd541608da96d56aa89ce991bb74cedd15217d2209e811a`  
		Last Modified: Wed, 20 May 2026 00:34:09 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f7bfe435a7f930e94986327a2f9856e75405edf52a04f14edfe8b8f3f0c388`  
		Last Modified: Wed, 20 May 2026 00:34:09 GMT  
		Size: 28.8 MB (28755593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fd34e2489a7cf271bc4471484be2715b62f1ef1123591afb34d822d85f0519`  
		Last Modified: Wed, 20 May 2026 00:34:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:69e7642ac6cbd07b83fead81b2df58c1c12862de33950c805f13b251debc0d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb20f8686d857f6561fb7793b56342c06cbef9428de1f9c60554e94bd8bf24eb`

```dockerfile
```

-	Layers:
	-	`sha256:e336e6c42a1b98f0ddda1656da2ebb9662371d560f999fb99dfcfe14587803bc`  
		Last Modified: Wed, 20 May 2026 00:34:09 GMT  
		Size: 3.9 MB (3925253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b4c12068b22e7ecaf17aab1115a07d27c609e096ee4534fe351734782708a31`  
		Last Modified: Wed, 20 May 2026 00:34:09 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json
