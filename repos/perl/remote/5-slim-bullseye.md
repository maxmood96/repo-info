## `perl:5-slim-bullseye`

```console
$ docker pull perl@sha256:5bb44a2c1d634e586abe0ca2e654d98879d47b7c38a244fa9fab9db6cf6d6c0f
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

### `perl:5-slim-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:47304fc078a1db2aecf45a9af88753af304ae996edcce72b9321d186db084a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56456632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5964226f5208dc0e3dd0b9cbff0a8d20ffd5aa7117ec5fab8543b95e7ac4ce3d`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:46:09 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 01:50:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 01:50:07 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 01:50:07 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe59b3b0e5f4c4515b59735b73d1bdcdff82cf6a1567d69fe6b35526aaee561`  
		Last Modified: Wed, 22 Apr 2026 01:50:17 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8bc265506cf172798570bd385918d9590673088474b5bcf364cbce29ddacce`  
		Last Modified: Wed, 22 Apr 2026 01:50:18 GMT  
		Size: 26.2 MB (26198431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c410b75ea831427bb2b7927612562dfecad693b82dbc9a2e65e6d74180b4e144`  
		Last Modified: Wed, 22 Apr 2026 01:50:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:3b418cc1f512e0ded8bb1580717241f1ea4a58efdd2c8ad9ad6e55701e008317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a768097571851bee4baad8a769cae4282a0ecfcad16a97951c5d3bd5b2371008`

```dockerfile
```

-	Layers:
	-	`sha256:13e769195bf6bfd2a4e694630db8796b2004729f783183e8cfb37ef25465972c`  
		Last Modified: Wed, 22 Apr 2026 01:50:18 GMT  
		Size: 4.1 MB (4129685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d929cde176bf105a7068f2fc06a5a31f4df2b747b29fabaffa45e97866f33a`  
		Last Modified: Wed, 22 Apr 2026 01:50:18 GMT  
		Size: 18.8 KB (18790 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:11f9d81779d7b0b318666e8a5d440d274913cce5e11daa1cfbcb6d85c9a4a0b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49001964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751b9811be1c8cf556f99817bc2cf7d37b4ba8d4520fdaf4e89a916ee2467b02`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:15:06 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 02:20:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 02:20:37 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 02:20:37 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:0e68d06981293adfea04925ae38b70c2f51ed1a5e0d6b2de60d6bdd09f147afe`  
		Last Modified: Tue, 07 Apr 2026 00:59:07 GMT  
		Size: 25.6 MB (25551488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfa9243710df9da9019f67fb451ea9a7c9588ff0455bfe09467f28e8791e1ae`  
		Last Modified: Tue, 07 Apr 2026 02:20:46 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b8887cce51966124ba20282bf8c9c994334cb23ae3c62b0acaf283b4be1668`  
		Last Modified: Tue, 07 Apr 2026 02:20:47 GMT  
		Size: 23.5 MB (23450210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e6f61c055b96f5daf07fbfed0f445110c6b8145a5d7fe5fb04837f3a504907`  
		Last Modified: Tue, 07 Apr 2026 02:20:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:9a707bb9c302aa5f1d34a3ea972d2ce3271754d818504e0c7d7b46bfad1a7184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e2e55e85acbeb8b742c5a50c22a0b7820017bb1e55cfe9ed4779604911e9b8`

```dockerfile
```

-	Layers:
	-	`sha256:9b71fa3bb2fbe071f234098f90c36a40b1a502387ebb369013157ed640b1e5e4`  
		Last Modified: Tue, 07 Apr 2026 02:20:47 GMT  
		Size: 4.1 MB (4103690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903484933579c198e177a33ee152a58a8b6b00a7a70d064817bc9b39ccb4ffef`  
		Last Modified: Tue, 07 Apr 2026 02:20:46 GMT  
		Size: 18.9 KB (18877 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:4e2a51ff16cd5ee476b265d1e2f16486b1d69e1705c257fe7dbe5ceeef1edb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54070366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34aefca3fdf672bb4dd8632de1c6a76a1e82cad57d9e1ae4d815a1390652bde`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:05:45 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 02:10:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 02:10:13 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 02:10:13 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263117b39adc44ab9132a00ac5afc92757d882ac5860634d2e1d1f0d4d95acfe`  
		Last Modified: Tue, 07 Apr 2026 02:10:24 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccef52dce15ca2e4956de5df1b6f4773dbf1ff259b3da6fa8aab2f348268422`  
		Last Modified: Tue, 07 Apr 2026 02:10:25 GMT  
		Size: 25.3 MB (25325411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f90d6fc0f1c2262758f77a83555d936093248ef471f15eb6b283aa69618843`  
		Last Modified: Tue, 07 Apr 2026 02:10:24 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:afbaa59480bd22043424e8ca9cffd92793dd102912da8308619cc823af54da76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f9f34994302f7c131017de454e7612d656d9453a8014e95f4370533af678ad`

```dockerfile
```

-	Layers:
	-	`sha256:5e1fa1b290f275ee2d7149852ebdef1f3b031c5125580dad441a1ab4770e635f`  
		Last Modified: Tue, 07 Apr 2026 02:10:24 GMT  
		Size: 4.1 MB (4104104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af09c3d4257052b4e681e1f8bf4e2f34a57e40dd852bac5626675282cf4229ac`  
		Last Modified: Tue, 07 Apr 2026 02:10:25 GMT  
		Size: 18.9 KB (18906 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:1424a492489f55ac6a4d82d9ce93fae358fe64466cfbbe1662809e10ff568270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58897763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395ea3059bea531eb6bc2cdab883c7b1cf37ff4a2bec12cdf742bcdf7681d8f5`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:48:56 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 01:53:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 01:53:53 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 01:53:53 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:829e928df5d3a0d826eebb9db2afcfac51736338a5db0631a2852b75006909fb`  
		Last Modified: Tue, 07 Apr 2026 00:11:00 GMT  
		Size: 31.2 MB (31191810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f63a03d8d5567d2176c64e2737fbf25ad6ad2abe0c0aeb5c2de023559da821c`  
		Last Modified: Tue, 07 Apr 2026 01:54:03 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6c7872e28f4a9f70f58c698db6127e616c74d421168e99d3b1259e23753139`  
		Last Modified: Tue, 07 Apr 2026 01:54:04 GMT  
		Size: 27.7 MB (27705688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d1427b34e2e01c4d2b2e1735e028d4ece10de59b60baa1e12f6549c6f35728`  
		Last Modified: Tue, 07 Apr 2026 01:54:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e4eaa8ade450d21323ea2022d3029950a5b5f7c22cd41e20301f9c8388949b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8e009eef3ae92f410a21d153e42d55f355fcf93ad7a9d0172234571dd9fc90`

```dockerfile
```

-	Layers:
	-	`sha256:40f31f920077780cff783de1b3d349480a5bb1b82b57c91445182cd2ed336d0b`  
		Last Modified: Tue, 07 Apr 2026 01:54:03 GMT  
		Size: 4.1 MB (4133957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870c2bfe0579c1ba660dc0d81e952a6a49bdd750be3675fc8c8ba86ce210528c`  
		Last Modified: Tue, 07 Apr 2026 01:54:03 GMT  
		Size: 18.8 KB (18753 bytes)  
		MIME: application/vnd.in-toto+json
