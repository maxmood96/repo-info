## `perl:stable-slim-bullseye`

```console
$ docker pull perl@sha256:3c997e89774e29922bbb75b5c0f5914ca5504138332b66594c7cd5f85226ab06
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

### `perl:stable-slim-bullseye` - linux; amd64

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

### `perl:stable-slim-bullseye` - unknown; unknown

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

### `perl:stable-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:921bb12c035c6ab6ebb0aac884cfe1bee86a3989ec68124df9872ffe097000ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49002149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0900433aa86547c075850bea5a787f110f77385537a3ed2381496c7b11f61a25`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:34:57 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 02:40:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 02:40:24 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 02:40:24 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:50e0a76bf8c998cc60af8a2a79ba2b2fade75366a3cf5b118733534c51339aab`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 25.6 MB (25551211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25efbbb9f752125a5a0effff76f575baa81abfc686cc2569140c44d0b93c8d4a`  
		Last Modified: Wed, 22 Apr 2026 02:40:34 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fe2c709269561001de46e354a06f38576a9da3259230395a0db96e72ee2ff8`  
		Last Modified: Wed, 22 Apr 2026 02:40:35 GMT  
		Size: 23.5 MB (23450673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312f066697640f59862192d0bf0d30427f929fa0b5c9f9f622add4e84450bfd8`  
		Last Modified: Wed, 22 Apr 2026 02:40:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f1f2da789d538ab01c1e18abf23afd9c17515b976691426ba722548cdcc9dca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e2cfb2646e0a62bc8252d9ba9a4090698213b2df468e1ab201c76d70a6c710`

```dockerfile
```

-	Layers:
	-	`sha256:729d32b63f18f20829c8c8a54386a7677a51647a15f73e258305035831a94b76`  
		Last Modified: Wed, 22 Apr 2026 02:40:34 GMT  
		Size: 4.1 MB (4103690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57259101fc794e6a95101d630cd705515bf133bda3723a431bc99d2afad59a4`  
		Last Modified: Wed, 22 Apr 2026 02:40:34 GMT  
		Size: 18.9 KB (18878 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:166f6b29d408b4ebbc7992356c003684441ac69bb68928971a53671b2860b8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54068348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9970a140e832456a1d5e84734a82b63440630b93a631f301b61f9138648c1b0a`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:48:36 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 01:53:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 01:53:09 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 01:53:09 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4417b4e66147fddb12ff92a8242bc2ed80be76dacdcd3fb8d35c1e0669d52aa7`  
		Last Modified: Wed, 22 Apr 2026 01:53:21 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550148e4de56c673c22dff76054e1be5e57fc79cc8ccbd27e6d499f160590e49`  
		Last Modified: Wed, 22 Apr 2026 01:53:22 GMT  
		Size: 25.3 MB (25325571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d183403a47833cfe8349c42869ac985fb5c9549faadc16f9c235f7f34b3a7504`  
		Last Modified: Wed, 22 Apr 2026 01:53:21 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:1583583cda9bba3f2befb834b91684e16af8b4370e351aa6a163767496d9ae2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607cd26f6d4fc72ed7918d472c2f81d43b93b96e8d664cd00355e9caaf3fdd6f`

```dockerfile
```

-	Layers:
	-	`sha256:f08c102fbdf09866d3f56bb7f477f1063a1463f67517bd729172f726c369b74f`  
		Last Modified: Wed, 22 Apr 2026 01:53:21 GMT  
		Size: 4.1 MB (4104104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf816cc3c4f22e05d1d2d2927214a8e683d798d2fb38c68104e5aebbf37ea940`  
		Last Modified: Wed, 22 Apr 2026 01:53:21 GMT  
		Size: 18.9 KB (18906 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:e09a68d229b3d06fe64db7003afa6ebb34035c04de7c80ad37fd503d0c762ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58898760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2c99037519ea90491250d3276192ed6e87862582d4fd513b5356bdf22aabbe`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:44:42 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 01:49:29 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 01:49:29 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 01:49:29 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:47e384a5452a4d00e629d1a0b87cc7a9d5181fba1c9a08d06b63e76375ad248c`  
		Last Modified: Wed, 22 Apr 2026 00:16:44 GMT  
		Size: 31.2 MB (31193070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3dc462fabc39e1e908f85979d0c1748059b59ae5f3f34feb8a10144e1316a2`  
		Last Modified: Wed, 22 Apr 2026 01:49:39 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d072104cb264815a167d328164a7453226a6151181641f7a65581c7ea7d0853d`  
		Last Modified: Wed, 22 Apr 2026 01:49:40 GMT  
		Size: 27.7 MB (27705424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2c6533ffce37d48edab90d359fd87136d4f236f8e44bb379b3c5ca09a15ab0`  
		Last Modified: Wed, 22 Apr 2026 01:49:39 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ddc9e536d84c8e2b1093562d542e108940c32fa25b83d2bf6dae16b83442dd89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b948bc7155bc764e096785c2a7bd2a6a3756419b2b3eddc37dec040df042888`

```dockerfile
```

-	Layers:
	-	`sha256:8200db6c8217a734aa08a889e271c04f282583e519c71d69a1104b1569d19c24`  
		Last Modified: Wed, 22 Apr 2026 01:49:39 GMT  
		Size: 4.1 MB (4133957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85374111d4ee0f1400ff74313f0283fc58dee1a8fdac19ead3f05faa13a57a69`  
		Last Modified: Wed, 22 Apr 2026 01:49:39 GMT  
		Size: 18.8 KB (18753 bytes)  
		MIME: application/vnd.in-toto+json
