## `perl:slim`

```console
$ docker pull perl@sha256:1e9bfeaa4cf9676351850975a2fcd29d4da08d65e48541b429f0539f7b7a48d6
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

### `perl:slim` - linux; amd64

```console
$ docker pull perl@sha256:f5fba30b2d2946e30f0c23dab5874690d98dafc03ba5f635371d6cf7393ad1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61730624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbceccecda2b01b99dabfd2159d9d79f71336d52b34646f5220b789a86062974`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:45:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 01:50:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 01:50:00 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 01:50:00 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1a4a29c0d629b96155da1b991c830d5b16af1523c7e1e4abcd168f94879651`  
		Last Modified: Wed, 22 Apr 2026 01:50:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f4ec7b837987c6545fab34d7ffe73855094da3fb974d6c8a31f7693458265a`  
		Last Modified: Wed, 22 Apr 2026 01:50:11 GMT  
		Size: 32.0 MB (31950185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced49508526c39a319858622189d5ec3b595c777cb6046ac3052d2702447c165`  
		Last Modified: Wed, 22 Apr 2026 01:50:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:a46d439e283f4617d8623dce9e4ce8d0e6afbf165e38495e12dca2c7ef3a24fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4030902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208a8fbd5eca57375a7e9b235c751865c6a500a4d1680d4ce511305f266bc74d`

```dockerfile
```

-	Layers:
	-	`sha256:393ac8938b2ecc554362acafeb5cf50c707e3405b203522278409d4fe48a123c`  
		Last Modified: Wed, 22 Apr 2026 01:50:11 GMT  
		Size: 4.0 MB (4010650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b745551d18127514f0033441e184ad76d4fa975eaacba73174a46a4004b2b0`  
		Last Modified: Wed, 22 Apr 2026 01:50:11 GMT  
		Size: 20.3 KB (20252 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:6cf6875e8c77c0d510250d87be94037fb8b1cfb655ffde60ac838b6f2dc7382c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57134017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2074884bad5f8c6ba9c457d42cb76436cdd5bdc2a25f084c514aaa8319276de`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:50:40 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 02:56:29 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 02:56:29 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 02:56:29 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0794cb903a10ed3f1077a37fa372d3c24fd62e393cd0288d42835998b5c8abbe`  
		Last Modified: Tue, 07 Apr 2026 02:56:39 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d693ba05ab6eec80db66f69581fb217af91263c74bae676653549fdbd4522da9`  
		Last Modified: Tue, 07 Apr 2026 02:56:41 GMT  
		Size: 29.2 MB (29189942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111360c590f027fc5625ec046717f0d2c0988c32098d65fc14f6a5ab21717a26`  
		Last Modified: Tue, 07 Apr 2026 02:56:39 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:b183fb4fd8fb0d9352f90d97c5b783af6f767409dc6b5b4bd29853303a89d55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e359736d127ec3d8eab1d5527d658864d532191b2936a30c12d968df66318c53`

```dockerfile
```

-	Layers:
	-	`sha256:083823c25af84f99bd039cc127e8c79246b77049e76a93140c78d011c4f0889f`  
		Last Modified: Tue, 07 Apr 2026 02:56:40 GMT  
		Size: 4.0 MB (4003727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e04a92a422abbb3c7bc11842a2c2485b6f9a4d4f1b90b3e1960b8c494922fbf`  
		Last Modified: Tue, 07 Apr 2026 02:56:39 GMT  
		Size: 20.4 KB (20380 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:2519c346d168ae6ae802b3a7d3ce508d94e7c8257da28d1681cf1b8bc630b8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54472963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2316686f0de2b6deb924bc82a1b29df901da98f3596e3d30e2cdb0037c1c660`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:14:30 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 02:20:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 02:20:02 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 02:20:02 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3619dc9a3d6c71b2ccc6f4f63991344077caead2ca9bd1e0f5335e5a8ba416e6`  
		Last Modified: Tue, 07 Apr 2026 02:20:12 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bce31cfa9b269142dbfceba12490b644dc50ffbb0bb515433a49d3c4444fbe`  
		Last Modified: Tue, 07 Apr 2026 02:20:13 GMT  
		Size: 28.3 MB (28263043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d044b61e3a731c680cb9c52334eb7392ce81b269b91391ec22e6fef610007c`  
		Last Modified: Tue, 07 Apr 2026 02:20:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:a8badf9bf97404505dbadac0a38b4e09ea48f370c878da402e4fcf6ab643d7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d3d67eb87d31078555ea5835c7fa8b7fe9ba2e67ff2f7b5dc9ba39fff897f4`

```dockerfile
```

-	Layers:
	-	`sha256:884f42484d5634570aa70cd97b81fe6ce1af2abce04e7ea2a55a42710513ed12`  
		Last Modified: Tue, 07 Apr 2026 02:20:13 GMT  
		Size: 4.0 MB (4002918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796d8de7b32b3eae8b9cbcf80488460e739d525251b5b5aaa14f45f641e73563`  
		Last Modified: Tue, 07 Apr 2026 02:20:12 GMT  
		Size: 20.4 KB (20380 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:ad072390a0a003c6667317a26a3553c5eb30c8e50bfb6fe22518ca215ba2cd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61760999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b6a8b5f99f76ac08f7eb5ef87df1d5d42ca6ec8790079cb1e61f24d6a7f1ed`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:43:14 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 02:48:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 02:48:01 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 02:48:01 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971d5ca704d1ea6530da9ecb688bb3f25a894b6b83a0a21f4fc91e6768b6e2a0`  
		Last Modified: Tue, 07 Apr 2026 02:48:14 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e112d14ea90d97f3751ff385f969b9879011d5c154e493c8b3d2f623109bf5d4`  
		Last Modified: Tue, 07 Apr 2026 02:48:14 GMT  
		Size: 31.6 MB (31622181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00e93066785c6e49c87e9a8b6e97804fcdc010f935705f5fba8113ed6e2008f`  
		Last Modified: Tue, 07 Apr 2026 02:48:13 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:b6dbb9b382edf00a11b5e5b7d69f34d0df931dbff3d0c53f1be4bd446daf1fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d0f80a5eb25b8427d5cb919bddeec5c1dd5140b7a2b9569c1855d53e130998`

```dockerfile
```

-	Layers:
	-	`sha256:a785326174b5a681fc54fd4c2fc102c7c4cc8bfde2d73d946a9686e1cbf1ada2`  
		Last Modified: Tue, 07 Apr 2026 02:48:14 GMT  
		Size: 4.0 MB (4005793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:221a570bc1ff0de6214475de89f11e8481ca51a5df9d0f3df24b1507c239127c`  
		Last Modified: Tue, 07 Apr 2026 02:48:13 GMT  
		Size: 20.4 KB (20428 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; ppc64le

```console
$ docker pull perl@sha256:5eb5713067e67b59634d41c0beb66a4a8e448fe251e94cba269b7453d39a576a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66270046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b34b3d1000bbc97db53a27df2b527dda3c4a2b61df10ccdf68849c0edc47d8e`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:24:31 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 05:32:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 05:32:56 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 05:32:56 GMT
CMD ["perl5.42.2" "-de0"]
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
	-	`sha256:e67b0fa5b3d6eab2ea677e08a928a99d3bf28364732c791176cc1b4dd836aade`  
		Last Modified: Tue, 07 Apr 2026 05:33:18 GMT  
		Size: 32.7 MB (32676763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d319157decd14504c28266d80c5a5e8424f2bcded864affdbb8aee1132171d2b`  
		Last Modified: Tue, 07 Apr 2026 05:33:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:8529648d1b38597acc16bd0b6356a43e4079258820490d3080c3629f0169df59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4027018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf264e6fe6731e3effcbb9025a37685e3ac41beeaebc503230930d083ca7c8b7`

```dockerfile
```

-	Layers:
	-	`sha256:f1f670d20791ab163c641e5608d7c52d8e3ab3b1bf90d9375c1437838fdc5e93`  
		Last Modified: Tue, 07 Apr 2026 05:33:17 GMT  
		Size: 4.0 MB (4006686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69244e2f511fc471f9ec1dd7b9000c6da4d85f076b9777a4d33e3fbd4c79d1b1`  
		Last Modified: Tue, 07 Apr 2026 05:33:16 GMT  
		Size: 20.3 KB (20332 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; riscv64

```console
$ docker pull perl@sha256:f7e82cadc1b79f2fabf4ad28e515fe847256a543bcf774d52914126207919afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70670673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87fb523d5492b73a2426c62c7213380fb77064959dfd0f79ad7f8d33386379f`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 02:39:11 GMT
WORKDIR /usr/src/perl
# Thu, 09 Apr 2026 03:45:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 09 Apr 2026 03:45:54 GMT
WORKDIR /usr/src/app
# Thu, 09 Apr 2026 03:45:54 GMT
CMD ["perl5.42.2" "-de0"]
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
	-	`sha256:459bee2f52e879969fa6e48ed2719cd42a73fc1e3a54592c6051520bf52b815e`  
		Last Modified: Thu, 09 Apr 2026 03:48:25 GMT  
		Size: 42.4 MB (42394628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be075ae7f09eaf0bf0171792e6008de812ebb8a0160d21224bda85576bdd0ac9`  
		Last Modified: Thu, 09 Apr 2026 03:48:17 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:b7aa653160e7246c2168403fcd1293afb02ea6d48d4b5d6b99e41e488f13b7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4018284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42e0048ffd9e153050f3a7987429331ef9e8cd2f73c10f2d4c990a3c753d475`

```dockerfile
```

-	Layers:
	-	`sha256:22add0d1b608ec243458939818105444ca4405dfa746c6d8b282f7b689784978`  
		Last Modified: Thu, 09 Apr 2026 03:48:18 GMT  
		Size: 4.0 MB (3997952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc37b808c2b1c624346f0b704c385e7c78a58d3b8db38eb591d2bbd9829558f`  
		Last Modified: Thu, 09 Apr 2026 03:48:18 GMT  
		Size: 20.3 KB (20332 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; s390x

```console
$ docker pull perl@sha256:23f0ce4b9cfc2ffab0109d83d0c3de9776e3bb669ea53ddb1f4b8a45ba2a40da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61132834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289fdcb4970ae89c9742072ca323b6fab6ac0f01230564534e2fa815e83b867c`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:41:53 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 02:47:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 02:47:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 02:47:54 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d377e4b58ef9ee117d18874ebdfe374731aecf5b6856a43e17cf99c320a1c1f`  
		Last Modified: Wed, 22 Apr 2026 02:48:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030e2349a48ece7cbf998d2b84e8f594c662925c6c1d759556ac4070a212f383`  
		Last Modified: Wed, 22 Apr 2026 02:48:12 GMT  
		Size: 31.3 MB (31292269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a11c89b8693bf93c289114c827546df30877989f5f93ea1592a2498d37a2c0d`  
		Last Modified: Wed, 22 Apr 2026 02:48:11 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:335b06d932a6de0ba035604848db3c1017e1f5b28da0fef90865449f172eead2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776d352e8cd0ebd00bed502a0d5c249a92e8bb8d75fb33d52f50ea7211891632`

```dockerfile
```

-	Layers:
	-	`sha256:dd7202bab00170c9688d21b43b3bde8265feaa653698ecec7da40c5d16f6a3dc`  
		Last Modified: Wed, 22 Apr 2026 02:48:11 GMT  
		Size: 4.0 MB (4002978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8eb0c53eccc6d4d75488dd898b382d49172a9135ddfd8dc67a5af94b8c763f2`  
		Last Modified: Wed, 22 Apr 2026 02:48:11 GMT  
		Size: 20.3 KB (20251 bytes)  
		MIME: application/vnd.in-toto+json
