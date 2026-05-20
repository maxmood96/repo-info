## `perl:5-slim-bullseye`

```console
$ docker pull perl@sha256:7cd6dd2fba09ee568dd972219a526783c5018ba533a1461cfd9ce2fbcfe12493
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
$ docker pull perl@sha256:6e03620475e59c66061f239b63f31117b0974986008dfae2e62f27cc2be08ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56456401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78168f9d685f72984a631d6f8741b307e0405470aa01c5c50754e70479502087`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:28:43 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:33:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:33:02 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:33:02 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4238e2884ddf3ca7b394a909dac880515de0bee4350c84d3475445d854523959`  
		Last Modified: Tue, 19 May 2026 23:33:15 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5f049cef7aa7e6d3e5907548317edf0da79a114a3586b57b19e6c5e059985d`  
		Last Modified: Tue, 19 May 2026 23:33:16 GMT  
		Size: 26.2 MB (26198534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a330b3b6564aac1f02c2b471e8407c7c9920b8fed4e433321607a0f8dc10cae`  
		Last Modified: Tue, 19 May 2026 23:33:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:43a11f54b144c0c42d091da60d18002d8e0407ae1e711f469244e6565be5d735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fd34e7de4cf3513195e274a35400daac8207ca53f31aedfdd8b39dd0152158`

```dockerfile
```

-	Layers:
	-	`sha256:48ce63c38e50524eecc2e23c30f0224f08e13e2c2b881c03cc865701f53f6587`  
		Last Modified: Tue, 19 May 2026 23:33:15 GMT  
		Size: 4.1 MB (4129685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b07277c51c30e1963635f49ffa12d5a3c35464f6da7b41243e55a4ea9e8280e3`  
		Last Modified: Tue, 19 May 2026 23:33:15 GMT  
		Size: 18.8 KB (18790 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:dd50283af9595b1c1847d1d818db9baa58a010ef80a5c8b63a46b70e5199a5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49001675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c997ab06ab5285cab5f21dc236f0de2ce8a2e06d89723d2720a2126de2a23e`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:47:26 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 19:52:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 19:52:48 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 19:52:48 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:976dfa794c59ebfed71602151daddefd6dc6a747d5d0ff3934bce4d42d3677c5`  
		Last Modified: Fri, 08 May 2026 18:37:07 GMT  
		Size: 25.6 MB (25551243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8b3d5dee4ab9c9fa5670c5b4b95ab5fdcd2729b58d2f7eecd1c6691af6b823`  
		Last Modified: Fri, 08 May 2026 19:52:57 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb61e1e47de687dc2943a385743955459cd974b267f47b672fa098e9a0a0ff0c`  
		Last Modified: Fri, 08 May 2026 19:52:58 GMT  
		Size: 23.5 MB (23450164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f9a25dd019eb192ff06055be3b9e2283b6c98674f895fbfcbb3570c65eea5`  
		Last Modified: Fri, 08 May 2026 19:52:57 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:92f0f47714122083dc1e0510f620a89721ca6f584d464d99ef55c17947bfbee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df666d95456efc2b4dd7d48b9b7b241b9c3067faa745871f5e5d03cd7061f790`

```dockerfile
```

-	Layers:
	-	`sha256:46465dce6c8fa776d524cc2ed05b03546fccc03a6109fdf27bb2f58bf0b38b66`  
		Last Modified: Fri, 08 May 2026 19:52:58 GMT  
		Size: 4.1 MB (4103690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd1fc29ea6735afcd8a910c696a85a353e0417fda2cd3631243bcdb30374921b`  
		Last Modified: Fri, 08 May 2026 19:52:57 GMT  
		Size: 18.9 KB (18878 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:57ff3ef1f22cf7158426ac3528ad3b2be1f6627302b0eab7983d902682215a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54068781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a7c8597fc02b57b16f3908441fe006cd843c2ae1733a524ccdeff05deee264`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:32:16 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:36:49 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:36:50 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:36:50 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cdb4c7d9b6c00b55c6ee7970869b0306a3c9e7e12df4989c013baddf929af0`  
		Last Modified: Tue, 19 May 2026 23:37:00 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897831f42115d65861367e03dca40b7d0626ec2f93c3c0e28293f44fe4ec58cb`  
		Last Modified: Tue, 19 May 2026 23:37:02 GMT  
		Size: 25.3 MB (25325541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fc8ed02dd36f1a97b4828d2832f75169e9c84123812371bb4114e088e73c3d`  
		Last Modified: Tue, 19 May 2026 23:37:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:bfe7469d548dfbd7939c1cfd4222d254c7eebe1da26e144414256c404dca81d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a389c05bf0753c86cc79335e4a6b474665cebeeddd30ae705f930713777e946`

```dockerfile
```

-	Layers:
	-	`sha256:27162df0abf11273f647727a124697637e958890db1b3befae33960b9a7c3d73`  
		Last Modified: Tue, 19 May 2026 23:37:01 GMT  
		Size: 4.1 MB (4104104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f162d25f2e6b9fa847098c1a950467a77f7a5d5c794190e9822598450c60f953`  
		Last Modified: Tue, 19 May 2026 23:37:01 GMT  
		Size: 18.9 KB (18906 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:54903cec3ac883c563774e978e566aa315c61a6e3d8083726171f27293f86ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58897947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5637af4e3e05ecfac6f61f55d0166d9cfb1316d3a5258354a4352f23b9d9dac2`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:27:20 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:32:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:32:17 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:32:17 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:2f6471dabb4ec95bed651099aaba5ff48a4c6332742cc6af6c957b880b8a6aff`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 31.2 MB (31192759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a15636740485874e82a30268d3b34bf07c7d6c0666c9089e7807c7aa9d367d`  
		Last Modified: Tue, 19 May 2026 23:32:27 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9defb23869ac4f2e64e61800f2f98710c9d30bf496f1bf6d44df27c599127a0f`  
		Last Modified: Tue, 19 May 2026 23:32:28 GMT  
		Size: 27.7 MB (27704920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463fdec3673cf3eaa8db92fd21d8ace2a06adea0e6e0b2b4c9237cbb76e91b34`  
		Last Modified: Tue, 19 May 2026 23:32:27 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:0a117f5617a99a4e0fb617005b85e022a215358311d94ffa9d40029e774b5302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8529a2eee080246d4a64ae84573a02bfc66f5d168f35a50a54c9580cf9bcfb37`

```dockerfile
```

-	Layers:
	-	`sha256:b034a48ef062fca8b75ee8faefba44d58c0d2da302fc013f416b60a6728b438a`  
		Last Modified: Tue, 19 May 2026 23:32:27 GMT  
		Size: 4.1 MB (4133957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d69a91d77233c18966f5d743028cae50fbb39101b14bd62049b6522bc8743ef9`  
		Last Modified: Tue, 19 May 2026 23:32:27 GMT  
		Size: 18.8 KB (18753 bytes)  
		MIME: application/vnd.in-toto+json
