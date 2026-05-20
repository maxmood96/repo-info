## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:65218185ff6a29d17eaa7fd088fa3b71d8e1daf6690c3aa0b99b871c09eb664e
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

### `perl:devel-slim-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:d5bfa06330a27fc8e2c07a4bf6c0f550a4b9a39330cef85d5b30ccfb68751630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56718436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33eab066ef016b2fc259b1a662b2c10320c892e78c30b6c99c8e6328a75320d`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:38:09 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:42:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:42:12 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:42:12 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21c7a7dd1273140bff0e5de2c7dace42d860f7ef3fdc5e0ab0723b95b263fcd`  
		Last Modified: Tue, 19 May 2026 23:42:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ccc09b629a1bfd5b2ca9b0d064aeb0aaf72bee48cc1ca01a707bc13f6abb8`  
		Last Modified: Tue, 19 May 2026 23:42:23 GMT  
		Size: 26.5 MB (26460571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f986edfdef77edddb56889a2f525791c80c25b5de6d539e716f5ce48b9e755`  
		Last Modified: Tue, 19 May 2026 23:42:22 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f878b5911451550cbec1fad0bebbf398ee3e949e18de62f77be714f9de44b8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4147308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233cd270c01a9ad1908b39500eee0ea4a1b761add53befdae7defe960adf1350`

```dockerfile
```

-	Layers:
	-	`sha256:537a67f3d59ac6a213bb9d66217efcd18abab45c5d25728b4de72bece5f02ff0`  
		Last Modified: Tue, 19 May 2026 23:42:22 GMT  
		Size: 4.1 MB (4129063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3926e7885927274bdae1016ac9a522788e837ef7afd8f65e2279e255c333eb33`  
		Last Modified: Tue, 19 May 2026 23:42:22 GMT  
		Size: 18.2 KB (18245 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:a40fa656f4df316d77b0cdab7c8f4329932712d9de9dc3421fb5e4db86808ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49270566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81926db71371cac95d4f092a19758f93b0927459e4a00ddce300212a1fe4413b`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 01:12:24 GMT
WORKDIR /usr/src/perl
# Wed, 20 May 2026 01:17:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 20 May 2026 01:17:51 GMT
WORKDIR /usr/src/app
# Wed, 20 May 2026 01:17:51 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:03d011f22c8996d930f4cd66e165f41f901636aacd59f9f3a74c6b0df7ffa952`  
		Last Modified: Tue, 19 May 2026 22:36:39 GMT  
		Size: 25.6 MB (25550938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c1a3994d0b0435bce6eebb4275b7b12803ad02f3035aaf6be731e0ce1f4c84`  
		Last Modified: Wed, 20 May 2026 01:18:00 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f8a0b7bb048cdf3db1a69392ecaf09feec0fdd743301ae7795a503a27ffb17`  
		Last Modified: Wed, 20 May 2026 01:18:02 GMT  
		Size: 23.7 MB (23719360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8843e1a41475e1d3abaad6feab2dcf202ca9d45db79b02e2abf011b68f946d`  
		Last Modified: Wed, 20 May 2026 01:18:00 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e5c34e7e2496e5cfc12657b6b615bc5d9b70043a99a523f050e83c2745c34bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddd67285866a99267d640f882061b3ce2e24785f03ce01d5548d9df229a7487`

```dockerfile
```

-	Layers:
	-	`sha256:fa4ad1a844bd1fd7ae70581e01c708b7a9833c75d9d7cbc111b82a951b898210`  
		Last Modified: Wed, 20 May 2026 01:18:01 GMT  
		Size: 4.1 MB (4103052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f256d0caa696181bee61175b89623dc48d5a59e093a69731a3473fbd3eb78dea`  
		Last Modified: Wed, 20 May 2026 01:18:00 GMT  
		Size: 18.3 KB (18317 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:8457a0b8afe95ff506cc6f66d318273aef3c04add8baf64fbebf0c6306b3e6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54329327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79919ada48175124ae0dd816929acb0d162634153c2305ac4caececec33d3e7a`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:42:11 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:46:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:46:45 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:46:45 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d23398e72d44743f41d8087a06cafc7d6035ada23ffb6b9bdd4a165be132fb4`  
		Last Modified: Tue, 19 May 2026 23:46:55 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60158cbe3daeeea2c184a9f5cffda4c24c325804862d4d9369c3bff292292a2`  
		Last Modified: Tue, 19 May 2026 23:46:56 GMT  
		Size: 25.6 MB (25586088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68f85aff53f2da3818d576c1ae4d19e4166b10f49e2cfa9da72e7439a9d629a`  
		Last Modified: Tue, 19 May 2026 23:46:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:47c748eb668faed6f6206d49d0940b239c511d8e5fc392892f203a77753ec277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880df40e8ab65a386b518d26751d8643218ff89165a16ccecffd7552d8281f1e`

```dockerfile
```

-	Layers:
	-	`sha256:d1a5689d55d43bd9f7985a22a50e4d6370f6d4f6371028f20a1ecc077b025549`  
		Last Modified: Tue, 19 May 2026 23:46:55 GMT  
		Size: 4.1 MB (4103458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f2fbaf28886724d31133a1b1bccff79735b829bc56ef25ccfc78521c383713`  
		Last Modified: Tue, 19 May 2026 23:46:55 GMT  
		Size: 18.3 KB (18337 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:f4363282c661030a32a916116eef92e76d68e594479f19f7513601c0d09d3ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59164967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2087069330f506968a0dfe611384f3d2276417d2889b952a37964705aa78cf28`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:32:37 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:37:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:37:32 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:37:32 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:2f6471dabb4ec95bed651099aaba5ff48a4c6332742cc6af6c957b880b8a6aff`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 31.2 MB (31192759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bbf795da2486a6c663e9eb89da1a0a77e1442ebbdc7f370bf15e40d685f50e`  
		Last Modified: Tue, 19 May 2026 23:37:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f551c6c70c22a7c04452b0d1088527d02af6c1c1a80c4a741557f63b41b5e87`  
		Last Modified: Tue, 19 May 2026 23:37:42 GMT  
		Size: 28.0 MB (27971941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b500de843bbcd6464dc9bcdcd16299eed5fd3d9450fcacd2450af18181e4d46b`  
		Last Modified: Tue, 19 May 2026 23:37:41 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:d3391ffbdb6a30b64592dfa35c5179e76db25145b9c7707c382acbc44cc360de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10870f474fd118e71f3e68fba869495c1e5ea7563345db2ca1b92ff29b47285`

```dockerfile
```

-	Layers:
	-	`sha256:45902c8a966507c453075c11275d0551cc09f73397851911e697eaa6e2a7ae27`  
		Last Modified: Tue, 19 May 2026 23:37:41 GMT  
		Size: 4.1 MB (4133345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d37c5ad240e6d1ca684ccab17ba9ad843b9ded3cf76136121328b8a86959a25d`  
		Last Modified: Tue, 19 May 2026 23:37:41 GMT  
		Size: 18.2 KB (18217 bytes)  
		MIME: application/vnd.in-toto+json
