## `perl:devel-slim`

```console
$ docker pull perl@sha256:2ac4c04527bacc26425ce6ff79482ee46e6cd2a1c73e00c5cf757b4331155c9f
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

### `perl:devel-slim` - linux; amd64

```console
$ docker pull perl@sha256:c5181028468aa58c640a16da552651823687a2d456ca80a6b499813fcd0a6953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61993440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d815c70e8c174df4103593fbb3588c0a0cba1d33121f7a6a3c936e2ffd0e4e9e`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:11:58 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 02:16:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 02:16:21 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 02:16:21 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1801631c3c7b78b102265be328dc12cbcb36937db7237d90d5a52e3a223b9d`  
		Last Modified: Tue, 07 Apr 2026 02:16:32 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae45fce3ed14f905d55197376b34166893d2c8204231e61366a31b0729966396`  
		Last Modified: Tue, 07 Apr 2026 02:16:33 GMT  
		Size: 32.2 MB (32217532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01a27be416e02daaf645ab420fc1b55ad4344847e919fca6dc1d10302298890`  
		Last Modified: Tue, 07 Apr 2026 02:16:32 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:4fd9004da50d47b4e38e6b35415e022d21a81a81df3a0a28055463fd377b52d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bdf1366fb35283e82cdc64f68382ca42cc86e9cf2f0fa01373066163ffff3c`

```dockerfile
```

-	Layers:
	-	`sha256:ccf0be1bfb9dc3e5477df01dcd4303dc8c087191ada36142db912edf54dadb7f`  
		Last Modified: Tue, 07 Apr 2026 02:16:32 GMT  
		Size: 4.0 MB (4009450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e558e1ad95a5bbd6a8c2a599b065de014356b69a12ec4b1e83a2b34570ee8915`  
		Last Modified: Tue, 07 Apr 2026 02:16:32 GMT  
		Size: 19.1 KB (19129 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:6f6797bcdcea50b9a36a8f77ff4b0b61249f07a373d82ba2e2df632588a9db8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57413042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed8f92fa256a4138c3e755bfce584e09a7c3757460294963de0958af196a232`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:14:28 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 03:20:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 03:20:11 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 03:20:11 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e724ad932bd84fa4f43c4acff8dc5fd0fe442c589ffb7c03d1f61a492cf9861`  
		Last Modified: Tue, 07 Apr 2026 03:20:21 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cb1bbeccbce95a2c07c49497e2bfca3c546b0dd08a58fdc995727afbeafe5d`  
		Last Modified: Tue, 07 Apr 2026 03:20:22 GMT  
		Size: 29.5 MB (29468966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53366d38cba883bbbaede4a41626c3bcea886fc45da175f41cf3a91e09c5c30b`  
		Last Modified: Tue, 07 Apr 2026 03:20:21 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:86766b7dfd195e4281a511647f2e30b7cd2678a684e8b32c4e95b57e2243e187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4021720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cb14f705844ccf99a35cb2f900ba03b0c5d9ba2feed4bf3b866184c488a569`

```dockerfile
```

-	Layers:
	-	`sha256:43c35e8cc7faac99c4ba3acc65dab42f212cb8e96c161b686ef5caf6da3af53c`  
		Last Modified: Tue, 07 Apr 2026 03:20:22 GMT  
		Size: 4.0 MB (4002495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:979c413b6b6bfeec6d820e46705087c6cc0e9856e30c8523c51e96fb33ce0716`  
		Last Modified: Tue, 07 Apr 2026 03:20:21 GMT  
		Size: 19.2 KB (19225 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:67816973a96ddc0586a65cfd555736b5fd9695c7f5d46bde6de1c32a597bd967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54747764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34816a027c6481265c97b32d8fc12fa7111905a848e18f3983c05893c6f29939`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:41:43 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 02:47:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 02:47:22 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 02:47:22 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da6c7533709aa91c9a6d637e3a3e9b80b4fa13f814acb7fd15cfd4fad8a0444`  
		Last Modified: Tue, 07 Apr 2026 02:47:32 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20989b244cad7c64d08e7d80fac8ab8aa03379a5cd265010769f67b747df3508`  
		Last Modified: Tue, 07 Apr 2026 02:47:33 GMT  
		Size: 28.5 MB (28537844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fa4c2734285cfc28d77fe002b22cebb442b913f1d80e08ff7e033c229042ae`  
		Last Modified: Tue, 07 Apr 2026 02:47:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:6fb166b2904649992606a64247827e3c92ee5fdcf9e589835f837845990bd0ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e828333287fb0dad2bf8ad03f217133f29a6c5735f58ef79299e1361c6951ecc`

```dockerfile
```

-	Layers:
	-	`sha256:09fc4d438a48743a71e1c901a592216eb241a21b54155cc7d793dea0f69391ec`  
		Last Modified: Tue, 07 Apr 2026 02:47:33 GMT  
		Size: 4.0 MB (4001686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1421add428762963feed5214e8c08ca5cf68cda422e4f3bf667bd7ec51ad98eb`  
		Last Modified: Tue, 07 Apr 2026 02:47:32 GMT  
		Size: 19.2 KB (19225 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:2df94276e69bab731de8106c653e141393ed86c410db1cf703c65e67b6333016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62023858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756e650f3b49e02ce0f142ccada44be29d72bea7c22b546c25f318a7821a2f4f`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:11:57 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 02:16:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 02:16:42 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 02:16:42 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9eca3b7ef1e27a3a52ede51a4c21ea4741e05aadd3a03d2c2f1bfdb4d87107a`  
		Last Modified: Tue, 07 Apr 2026 02:16:54 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5620ccc3913ae8fb5c961f3f0ea344e73019f28dd36177a7f8ce72712a5049b8`  
		Last Modified: Tue, 07 Apr 2026 02:16:55 GMT  
		Size: 31.9 MB (31885041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6615ab102e684434147125091581f46de563956e4c94a0e7503e7e3ca3ae2648`  
		Last Modified: Tue, 07 Apr 2026 02:16:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:29e9eb93a7e12649530291dfec0ab48cac47055149ce0ab1d490dfab06d449d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3333bc8a2c95c3c372348a8ce9d6e0ecc18ff79fbddf993dbe6b180baef7393a`

```dockerfile
```

-	Layers:
	-	`sha256:c0d9ecf04e4d2c15595060cef4a00b8bf520e772774f5b1903ebd4d33b34d412`  
		Last Modified: Tue, 07 Apr 2026 02:16:54 GMT  
		Size: 4.0 MB (4004545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53f5f23618cf504389b124dec5359371bad194a8fe4f5ab3a9a7895c0e61c5c9`  
		Last Modified: Tue, 07 Apr 2026 02:16:54 GMT  
		Size: 19.3 KB (19257 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; ppc64le

```console
$ docker pull perl@sha256:8b2c5397c5a24f559f82286fa83fef191407e506f686d5445a4a61eb84a3ad77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66537692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2a37d6f1f7e3e91fd207127c73d5ed54396f9fcd793b8f41bc4ef986f24fed`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:24:31 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 06:23:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 06:23:04 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 06:23:04 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcff421d6e5e4cd340f042ff2d092323cbef81aaf4fb5951f20f3ef8c800ab10`  
		Last Modified: Tue, 07 Apr 2026 05:33:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccb1fc180d3ab6bd067f71cf1fcc814e7fc05cb4612dbcc63422dadfb034556`  
		Last Modified: Tue, 07 Apr 2026 06:23:27 GMT  
		Size: 32.9 MB (32944409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff454dc7a2e88787b10821256f232c003b61c3753f67bb2962df6c0599101d3`  
		Last Modified: Tue, 07 Apr 2026 06:23:26 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:a696f5e802f9e97c2fd377b0895bc1b7f06c6f99738ab5d3dbea19a1ca4639e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7879874c13d6465e33ef12fc118d2b52b0b24aa0f219b998f5b8a7c3e5ec0359`

```dockerfile
```

-	Layers:
	-	`sha256:7ff11a04a152ceedbc004346c312126986ae9d376615992628259b211e8db420`  
		Last Modified: Tue, 07 Apr 2026 06:23:26 GMT  
		Size: 4.0 MB (4005462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e586b697306b5822f7a88fc6d5ea08ede330bac4f4686379edd8bc8a3dadccad`  
		Last Modified: Tue, 07 Apr 2026 06:23:26 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; riscv64

```console
$ docker pull perl@sha256:a3177925a42c34575e129ea5d5a8b46d9e5af87ac36c64b1593e917d503e9a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70934836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8172fdcabc1ae6770b92a7ceb0fe2bc68f5340b420456a8b9d380b0cdc49c41`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 02:39:11 GMT
WORKDIR /usr/src/perl
# Thu, 09 Apr 2026 11:01:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 09 Apr 2026 11:01:36 GMT
WORKDIR /usr/src/app
# Thu, 09 Apr 2026 11:01:36 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2376cb620c6baaa11bef2eead5c70550641dfef0285bab0aad2ffc6e1072b45`  
		Last Modified: Thu, 09 Apr 2026 03:48:18 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767ce43c375504211e9020692b15589e47c5f30b26c7f627a60516f0bc2b4f0`  
		Last Modified: Thu, 09 Apr 2026 11:04:06 GMT  
		Size: 42.7 MB (42658792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3551001d3f6807653fe36d65fa499ad7e983b273d523a9ed152b3312a11729fa`  
		Last Modified: Thu, 09 Apr 2026 11:03:59 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:122b1f0192d75ba3b3c90d52f3a9a5f28f8e2f335ae2b4bae06dfe9304d50814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17f8960d54ce56fdd10204323271fd90ef18e02840b1dfb6178df24bd070de1`

```dockerfile
```

-	Layers:
	-	`sha256:40eb13e6400e773a07deb8c25deefe8c366fb0ad75ecef6c2ae9f9d2b1377093`  
		Last Modified: Thu, 09 Apr 2026 11:04:01 GMT  
		Size: 4.0 MB (3996728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4dc2b26788c13c1a366ba35d18a63f7cb24f1ac2dd4b446025e91147d9e85ca`  
		Last Modified: Thu, 09 Apr 2026 11:03:59 GMT  
		Size: 19.2 KB (19184 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; s390x

```console
$ docker pull perl@sha256:f5046a852eda311671f267d287e2937a232f9ca0550074fa79b8bfa16cbc7173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61409603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48020c8918df891b3c2f5f34e419f8457877b4228b0ee84e6e80df6ab8740c18`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:23:08 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 03:48:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 03:48:48 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 03:48:48 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2fcf0fdf05a252211e5236b86fed50226dee7b176a9a77290b324c10132616`  
		Last Modified: Tue, 07 Apr 2026 03:29:34 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975f6545d90160a1804dc5dd9ade35a6ce99075e09c6acaa5b680af3a9dbd8b8`  
		Last Modified: Tue, 07 Apr 2026 03:49:06 GMT  
		Size: 31.6 MB (31573918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbcadab2cd6cf5d1b22c5ec3ca61b33e1b83d2fd4b5fdc1731f52d22515aa1b`  
		Last Modified: Tue, 07 Apr 2026 03:49:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:ceeaaff44f2f50ee2be5f6bbb96e0e48f13c16e02edfd677420e5c18d5e93fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb77b1d0bf7abd1104919af10371334bc9d109399cd22d6cc4243ce42d8d8528`

```dockerfile
```

-	Layers:
	-	`sha256:804dc13309cc73dc33c6735d7315952df67c966e6dc2a1acd142e9b75f4ce17c`  
		Last Modified: Tue, 07 Apr 2026 03:49:05 GMT  
		Size: 4.0 MB (4001778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28df77acd2910845fd97b2c02fb525ce779bc4e13d932d00b206949c5d2ea449`  
		Last Modified: Tue, 07 Apr 2026 03:49:05 GMT  
		Size: 19.1 KB (19129 bytes)  
		MIME: application/vnd.in-toto+json
