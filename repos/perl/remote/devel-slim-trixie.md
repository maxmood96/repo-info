## `perl:devel-slim-trixie`

```console
$ docker pull perl@sha256:0c5dcdfb27aefad2af02ae5b41870fdf570ddb23f6550599fc838dcdf30a25a0
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

### `perl:devel-slim-trixie` - linux; amd64

```console
$ docker pull perl@sha256:66687573f88cc144f574ab1c3c2c352df473d3ef9d711d0d836f1d4c205eaba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62002341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a210bca45896ce0c9cf63087ff785d84f40b76c5782a7c83b46bd9deb2273ca`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:34:30 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:38:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:38:47 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:38:47 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf3edde4e9b6efd5b5819f0f08c64219987aa1655eba320adf5d246b05c65a2`  
		Last Modified: Tue, 19 May 2026 23:38:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb609e8bf065314271c230d94a373774393015ddf96d84086bc70a1136c6c4b5`  
		Last Modified: Tue, 19 May 2026 23:38:59 GMT  
		Size: 32.2 MB (32222147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed48490d7abaaf9c38fad30783ec9b4b5ab72e4ef9b14676917e1e5d9bda311`  
		Last Modified: Tue, 19 May 2026 23:38:58 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:f18e8ccc68e8a72cde6388b316016504988cf0a88fb4e0b1e7cf444e08f563ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7649ed6b64788c019ddd58f0c0bf4d64171c1c27cb6ce157487b347b99a64f`

```dockerfile
```

-	Layers:
	-	`sha256:b439f58d1b79853fd5d987a81291ef37b90f85e39cde3977f4ce27d5c415514a`  
		Last Modified: Tue, 19 May 2026 23:38:59 GMT  
		Size: 4.0 MB (4009528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d84fd52a93d1f76c6781187fcfe7ee03ff17a390e1a9c3535326100aa518c6f`  
		Last Modified: Tue, 19 May 2026 23:38:58 GMT  
		Size: 19.1 KB (19129 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; arm variant v5

```console
$ docker pull perl@sha256:109c1cf04f0b337d8c0671f40bb8bc676cf1d89fef06b3e590c339d0156fc6ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57418165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9acf7e5942dfbfb9d7da5574fab85483b80ac8288bb09db00c2e48643afacd`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 21:04:24 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 21:10:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 21:10:13 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 21:10:13 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f33396df2855a6262425010e12ea02405e9fe2e3ed1ede80fe9d605afbd203`  
		Last Modified: Fri, 08 May 2026 21:10:23 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62112c4009a06a8ed55ad017d45cc0e5c76921d133fb5308496528d0639c3b1f`  
		Last Modified: Fri, 08 May 2026 21:10:24 GMT  
		Size: 29.5 MB (29469697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50058c87aeaaed7cdf43352592fc97b33c6d43882bb2f643a8371d002f53967`  
		Last Modified: Fri, 08 May 2026 21:10:23 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:808665f5bf9ee8c5ecbe1420bd182b0c41a921b11df0700e6828200a8affae0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4021720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3779f6f56ffa2ed4a2caa9c23ec79de5dfc7521e2abc3b30f6ea1aeeefd609f6`

```dockerfile
```

-	Layers:
	-	`sha256:03b087f3b40e42ddcc52e12c65d24dcd81475eebe7ed6e86c4c92c78102b8446`  
		Last Modified: Fri, 08 May 2026 21:10:24 GMT  
		Size: 4.0 MB (4002495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e411de65c4fe43150d68deee4ae97c8167027c11808b3a5c07a129fe3879a4fc`  
		Last Modified: Fri, 08 May 2026 21:10:23 GMT  
		Size: 19.2 KB (19225 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; arm variant v7

```console
$ docker pull perl@sha256:eddc81e6d8b8111c06a758dca948e3dae36539ed99f5902a2204aa0d7114ab07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54746455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f6f41fdfb365c1f7a835813e62670f1e4ec110aef92d50ac6159d281e0da19`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:45:18 GMT
WORKDIR /usr/src/perl
# Wed, 20 May 2026 00:50:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 20 May 2026 00:50:51 GMT
WORKDIR /usr/src/app
# Wed, 20 May 2026 00:50:51 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727e64a72f528b9b8898f6195c1884811ad626d17051bbbedec0de9afebed203`  
		Last Modified: Wed, 20 May 2026 00:51:02 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b0e75a3b95e77a4b8b9cf7629528706415e3775a594c33f234471e88197947`  
		Last Modified: Wed, 20 May 2026 00:51:03 GMT  
		Size: 28.5 MB (28540355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffc447c60820205477957cd5713ec3bdba7ef2caf28146ccee9936069e11094`  
		Last Modified: Wed, 20 May 2026 00:51:02 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:e1889b786e13c909c4a731a4aa442a99f326fdcbdf5c56d8ce1c62cf96b8c3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ca1c84dd198d59e6fc79aafe44a9c12d8ae8cfaf96c182aa5e09ba90f50c89`

```dockerfile
```

-	Layers:
	-	`sha256:28f4a26ca38bee8c36a6dac84de6bc91ea3d826b8e934904fddf4567128b0a99`  
		Last Modified: Wed, 20 May 2026 00:51:02 GMT  
		Size: 4.0 MB (4001764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854d6bb9d7a74922631985e2cff10b9b7eb1ea7158e03d004103ce6989ee9156`  
		Last Modified: Wed, 20 May 2026 00:51:02 GMT  
		Size: 19.2 KB (19225 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:cacd9fc454bc9af75c2f5c8a44c36f441ee5a943459f0d61b2a1ec594dabf0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62027384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8313ce64ac7cb4d37fd7f20fe2965d0b019da96a79cda420eb69e5b8e3015fd`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:38:13 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:43:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:43:10 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:43:10 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e043188b1ba69fda9da039998bf385ad8646569be5b2d363593b471af29c01a8`  
		Last Modified: Tue, 19 May 2026 23:43:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b05454f8fb9c7b1d97d6dfa4a6750f180a383a0e0b34a4a2ee6f44d20479b9`  
		Last Modified: Tue, 19 May 2026 23:43:23 GMT  
		Size: 31.9 MB (31885197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cd5e1d1f1c43fde024757de1914ebdf396f97c7ce2aef3b1c499ed1cfc002d`  
		Last Modified: Tue, 19 May 2026 23:43:22 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:836b5a960b4cd51682e21a085ce3480c313aa83032a264d348918f6628941d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e0859072d2202a2bf6a879287a47f9ab2885e004cd7551bbe4b77ae6b7bf18`

```dockerfile
```

-	Layers:
	-	`sha256:273ca7e84dc651787ab20a5cd6bfddbd7879af04a0e897bc45f1a8155aeaee21`  
		Last Modified: Tue, 19 May 2026 23:43:23 GMT  
		Size: 4.0 MB (4004615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1e6a901a21ccd309e00bcb399506a659b48d46139f723990c15748c37b59d27`  
		Last Modified: Tue, 19 May 2026 23:43:22 GMT  
		Size: 19.3 KB (19257 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; ppc64le

```console
$ docker pull perl@sha256:ec3ea69a4e8470900cead122339976c11771f6352afe833c29a5f4a854e4fa83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66543246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5d3f873baf06f64ff14b1831d3e88ede4cb0d1626f9aa3a3fe8df9af494790`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:49:21 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 23:49:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 23:49:26 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 23:49:26 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24acde6d1e4e16cbadc8f232a1dd36eeaecbfbd4bb1dfb725e5c40355d61459f`  
		Last Modified: Fri, 08 May 2026 22:58:33 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da75696aa7019f212a9a8440d179f923bc6f7cde3dae3c758d639a6b048e0df`  
		Last Modified: Fri, 08 May 2026 23:49:47 GMT  
		Size: 32.9 MB (32944890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87221cec2eab725e312a4e40aa4f8d3d7f621d086801f56c9893decd081747f`  
		Last Modified: Fri, 08 May 2026 23:49:46 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:d727766cf16fcfd8198bf58361b1a199c057572b54070414da78e2420fd1906b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a349403c64d8ee5f313695d23f087b8f9ba8cf514100ae59096a106c2c53ce`

```dockerfile
```

-	Layers:
	-	`sha256:c3126fa7cf2d27d4466e2066b5cfecb45e596b87b14a3b93101164486a3dd165`  
		Last Modified: Fri, 08 May 2026 23:49:47 GMT  
		Size: 4.0 MB (4005462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ce492193f9b67670851c98070200fdd3451c9967785eecded4155a5a30292d6`  
		Last Modified: Fri, 08 May 2026 23:49:46 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; riscv64

```console
$ docker pull perl@sha256:4ef61304b6fd6997ec1552e1442d383d37070869d0b31a652cf27d2253607794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68329042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e13f93250dc2d54f1b87afdc115d0a4612c1a3860aacd9545a5a6ad73377b3`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 02:26:28 GMT
WORKDIR /usr/src/perl
# Tue, 12 May 2026 23:43:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 12 May 2026 23:43:44 GMT
WORKDIR /usr/src/app
# Tue, 12 May 2026 23:43:44 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2481e2aa640643fcb248bb32f0916ccf5ac884b5babbbcadbe4c92423293f085`  
		Last Modified: Mon, 11 May 2026 04:27:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a613458b09a44ad9b312761460848a202e14ee61ac5e5a59711bdab8db9cdd10`  
		Last Modified: Tue, 12 May 2026 23:46:11 GMT  
		Size: 40.0 MB (40048541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a5d992f07b076e9e0222232f72b4bf23dd21d93178df2138d363e66bd7ba2e`  
		Last Modified: Tue, 12 May 2026 23:46:04 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:bfe21003396a320a485f8f20d85388cb0286dadb4a088208a6ffb5e354d357f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabd832e1032fac5810aa03e1e1ebf764ac3873d588238542910917bf895e98b`

```dockerfile
```

-	Layers:
	-	`sha256:3205fbc4875b45b9ec75f75a8e09d5a1259f9c1a3c5894014943c6a253a3574d`  
		Last Modified: Tue, 12 May 2026 23:46:05 GMT  
		Size: 4.0 MB (3996728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f1a2974b2b6cfa7564d63e141b6156f8169396c14bd8e6d537900a1deb7f8a1`  
		Last Modified: Tue, 12 May 2026 23:46:04 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; s390x

```console
$ docker pull perl@sha256:f8ac575d5880929bdd8149bca8f1cef35c96429fe50cc644eefd1844ad36d225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61427451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afa6a80d2b715fbfbd2dccdbca5f5413acb59d2e593d82be48ba1ff9257391a`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:26:43 GMT
WORKDIR /usr/src/perl
# Wed, 20 May 2026 00:53:29 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 20 May 2026 00:53:29 GMT
WORKDIR /usr/src/app
# Wed, 20 May 2026 00:53:29 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb287c4796461f54197c3266d957c5f95ecb519ec9905fd12cdf133d77ec8050`  
		Last Modified: Wed, 20 May 2026 00:33:40 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3423675d47b869d531db37c1d45542e862ec5a2f1d12dbf9cd987b5e23a9b2`  
		Last Modified: Wed, 20 May 2026 00:53:47 GMT  
		Size: 31.6 MB (31581260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b449e37886a647ba711bcdd67460517e73226657d1b105a3d2746afb3ea1474`  
		Last Modified: Wed, 20 May 2026 00:53:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:2eaa0ef94b7248d331b4c3035bc7fcbe28f70bfe88e005dc37400206a8743243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6e722d074935d78436ff8f8f810ae503e5d87944dda88d131849cd54764ab7`

```dockerfile
```

-	Layers:
	-	`sha256:943560e4fee1372b97b0282d4c391aa8a0c26fa511d7f5f9fe326d9cc022eaae`  
		Last Modified: Wed, 20 May 2026 00:53:46 GMT  
		Size: 4.0 MB (4001856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7cd39a475bde2c36c4abf1bf89efda417fde4fa3c29aec47da0a241cad9b0bf`  
		Last Modified: Wed, 20 May 2026 00:53:46 GMT  
		Size: 19.1 KB (19129 bytes)  
		MIME: application/vnd.in-toto+json
