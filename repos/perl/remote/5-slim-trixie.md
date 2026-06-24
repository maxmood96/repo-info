## `perl:5-slim-trixie`

```console
$ docker pull perl@sha256:f9f7a1c0cfb20a6e08ae94afe4037c14dbe85ef3b9d0b65d787058546f34642d
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

### `perl:5-slim-trixie` - linux; amd64

```console
$ docker pull perl@sha256:28d282bdac351ee71957c789557284996d40520a77c4f7863ba63504f2906f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61741097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2804770f8122a7bfb5dc1f5c437b8c9d448c790c17b2d0a86463f762045a0174`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:46:37 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 01:51:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 01:51:12 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 01:51:12 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3253d7a4f864abae02acfa4fb25f6f4827866c7bbb808b48c0abdb4e6c036f1a`  
		Last Modified: Wed, 24 Jun 2026 01:51:24 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2925b306af198dfdaffdb1bd1544a63f6b95fb6c4973350e59cf40185a2441`  
		Last Modified: Wed, 24 Jun 2026 01:51:25 GMT  
		Size: 32.0 MB (31955411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c629e7f93a32a4da6adf66d0f8352db40ddbd3284137be1406dc759f6a5d710`  
		Last Modified: Wed, 24 Jun 2026 01:51:24 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:4f24b72b6dd989e7dd0ff792ff6c595c0327eccd0ddd862424d6614cb80e9dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cadaaa4de23fba818d2fb2ce3448451e19fec175656900deecc3b38ea262a66`

```dockerfile
```

-	Layers:
	-	`sha256:9f13156f76816191672584ebaafd07aa53768418626a7ee28995ead4dd330ed4`  
		Last Modified: Wed, 24 Jun 2026 01:51:24 GMT  
		Size: 4.0 MB (4010818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:086c9b6c7ac0c965b22e3a7aa7870f158ab3253926255d46fb5d0eaea0c0faf1`  
		Last Modified: Wed, 24 Jun 2026 01:51:24 GMT  
		Size: 20.3 KB (20252 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-trixie` - linux; arm variant v5

```console
$ docker pull perl@sha256:07c8a286ac82cc52ab16e7c9c0170db68229152e5dfaf4172fed561aec4502d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57160327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03e8df7566297580f11be6f5afd2a7784599d7a33886425518c6c84a0ded09e`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:22:30 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 02:28:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 02:28:13 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 02:28:13 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6f7335b351bc7d34a3c7c09245dd4d3a517f91284a5b3591f26fb6edab9dd2`  
		Last Modified: Wed, 24 Jun 2026 02:28:23 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a92b8bc759705f3decdf17025a1b7e587f2838cc6bbb8cd01d90779a48508c0`  
		Last Modified: Wed, 24 Jun 2026 02:28:24 GMT  
		Size: 29.2 MB (29200839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526fb0a6c0aa2d3a6a66b997147557eede61a990f43fb711a40c84c2b97c2903`  
		Last Modified: Wed, 24 Jun 2026 02:28:23 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:8ccc0fcb277be8e850daebe3715ae8b4a025a392d061e8c549ca47cc30ed7b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d96861ff04eb099b8407ac0a03f6f1c53a4e058f4da58090020fe5a9bf3ee67`

```dockerfile
```

-	Layers:
	-	`sha256:e19e5baa511d4b15233dad927e08ec1a1874161692a93f94d9c60e31ed7a25b2`  
		Last Modified: Wed, 24 Jun 2026 02:28:24 GMT  
		Size: 4.0 MB (4003895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c3ddbbbecc085468dd7f244b72b4779845cb7de99c36863d3687b84db377a57`  
		Last Modified: Wed, 24 Jun 2026 02:28:23 GMT  
		Size: 20.4 KB (20379 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-trixie` - linux; arm variant v7

```console
$ docker pull perl@sha256:dfd64a5dd0dd37b061a5eec7d9044c32f4baf332bed860734ae12813e4def20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54480197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20bc2651de87325c1ca3c7a0ed58bc2e71f7e0c2e1baf77df3de3f8ff63eb30`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:37:36 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 02:43:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 02:43:00 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 02:43:00 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d71398045a8b69cd57e98801391b79a4eb7a810c6896298d6ed94f683c3ea7e`  
		Last Modified: Wed, 24 Jun 2026 02:43:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a475053adff28cc18fc7bf14ac9e9b96b91b6984ee2dd6193daa2646507833d9`  
		Last Modified: Wed, 24 Jun 2026 02:43:11 GMT  
		Size: 28.3 MB (28268880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fceb7a4bab923bcc72fb71b6ccf54de8155848a81567d37e410ce1021fd1b64`  
		Last Modified: Wed, 24 Jun 2026 02:43:10 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:2e819c65f6e2cd8316c9018e10d182b534038a1ef5bb7134763557c4fd7d1e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59df9b5b36ccf4adada1acb3bf8ac86f5e4c558b52575f9cced7bfd76550d44`

```dockerfile
```

-	Layers:
	-	`sha256:ff7ef84051f2e36ee9de974bced2923cd943a8364d9dbe0fc54034c85e702a64`  
		Last Modified: Wed, 24 Jun 2026 02:43:10 GMT  
		Size: 4.0 MB (4003086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64f6cbeb487a344acf6bcf2180a9345f53ca87d5850afd7147690022aa5c3173`  
		Last Modified: Wed, 24 Jun 2026 02:43:10 GMT  
		Size: 20.4 KB (20380 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:df115390560b6549b1473eeb93d8f47116e12ab2837fcf6f79eee19696f49fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61781382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8ae836b4da0055878f9e92eb0e44413c55d0d139eba2f9c9c2a5f4f53772dd`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:50:01 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 01:54:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 01:54:42 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 01:54:42 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3190e20d9dbf5467c9df61c963959f0ba1a2ecef9f5c411c6bd55b285d3d5fc`  
		Last Modified: Wed, 24 Jun 2026 01:54:54 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51114027e98c92a9ef54175c88358ca25d3507767a7282d604689539fb2b83fd`  
		Last Modified: Wed, 24 Jun 2026 01:54:55 GMT  
		Size: 31.6 MB (31632563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6efce50d752ceaf698ea1e766070bb8e421cfb81cbe3b42e8c3f1d2b80f8fc`  
		Last Modified: Wed, 24 Jun 2026 01:54:54 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:8bc36083fcf14f8835b714415702c13ca5a82f4b9952d792d9ff4407407cddb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5cddb1f385b9f2dff2a50259254fe0bdd73ae57750594c63d986988cac1279`

```dockerfile
```

-	Layers:
	-	`sha256:ce4267e5dab89eff49694e7faf29eaf79a7e74b10c72768e81dc580fed872b04`  
		Last Modified: Wed, 24 Jun 2026 01:54:54 GMT  
		Size: 4.0 MB (4005953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1ee9339385c6e829056b584fcf1f97a45133948685c0d1ad0e32a6a8615c95b`  
		Last Modified: Wed, 24 Jun 2026 01:54:54 GMT  
		Size: 20.4 KB (20428 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-trixie` - linux; ppc64le

```console
$ docker pull perl@sha256:f3c07cfeb8d161cd527d47e774166ea8cb90ca327515feb5197e3a459771253e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66284321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e287f6fbaa6c6091ce869e602fa11953fcbd43867d6d0e606f02891e39b17475`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 03:45:42 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 03:55:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 03:55:02 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 03:55:02 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d88ec8979ad339cede60b60bbb5ef8f9cd5391d805932f3269e95c797158c3b`  
		Last Modified: Wed, 24 Jun 2026 03:55:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff53683019e19a2b526c4a8f2f4f6fcb3f48b1afbeb9d4a3582b04b4729dcbd5`  
		Last Modified: Wed, 24 Jun 2026 03:55:27 GMT  
		Size: 32.7 MB (32677665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033de3322eabafb3349f86581c9ca0320878716390ff85bb3eb59cba69061688`  
		Last Modified: Wed, 24 Jun 2026 03:55:26 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:7458d65b1308c6645cda11c723fca7999863bde28f23a4bef8bf2a022dd65faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4027186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff5700f139db05d5715fec4adf5de1c264e88a65b6dcd05d00dbfe0ff585024`

```dockerfile
```

-	Layers:
	-	`sha256:a4cd7c2a8a2bb89dd3dc6f9b28ac8babae3dafc86b082ea8b0a0a18205a7316a`  
		Last Modified: Wed, 24 Jun 2026 03:55:27 GMT  
		Size: 4.0 MB (4006854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5bf3aa160ee4eb0ed83522af4775542f7c4e85274b31542ec0ad3e0848c90dc`  
		Last Modified: Wed, 24 Jun 2026 03:55:26 GMT  
		Size: 20.3 KB (20332 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-trixie` - linux; riscv64

```console
$ docker pull perl@sha256:455c20ecd61af15452edf6277ca73fb5a5810386f19e5b99a40460004d8e1f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68080288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88f4e5c52ddb242442bee6381a0e11ce197353fbff4434475d6d39fe4d77e46`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Sat, 13 Jun 2026 07:54:37 GMT
WORKDIR /usr/src/perl
# Sat, 13 Jun 2026 09:01:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 13 Jun 2026 09:01:34 GMT
WORKDIR /usr/src/app
# Sat, 13 Jun 2026 09:01:34 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720d132b19a69ace7403afa261c7ea8744650e553ed6437bfea4aee8bb522f97`  
		Last Modified: Sat, 13 Jun 2026 09:03:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dbe63f5c4442d2f0a6521992a66295dc8107c6ab8b9968c044afe01d69d619`  
		Last Modified: Sat, 13 Jun 2026 09:04:01 GMT  
		Size: 39.8 MB (39797714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fc550d9a67f6583df5c61028455f084c8d235f8546c2497b35ae891143fc91`  
		Last Modified: Sat, 13 Jun 2026 09:03:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:96f8ea47257a5ac0527220ab9b3995b810b6fbc42895a6806ff0e320ab143fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4018452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a008db40a61d93c377d46de0dfbb919c196c2beb59e8f38fe492b52ac7c310b0`

```dockerfile
```

-	Layers:
	-	`sha256:6a1dc968a832fcecf0d6cee34df99e42393c3114b9ce62a0f6324aee07741f86`  
		Last Modified: Sat, 13 Jun 2026 09:03:56 GMT  
		Size: 4.0 MB (3998120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b941ba5da4af1db50dfe00a6d8606bb1ba3cb037bb17075684d240dfa723eb`  
		Last Modified: Sat, 13 Jun 2026 09:03:55 GMT  
		Size: 20.3 KB (20332 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-trixie` - linux; s390x

```console
$ docker pull perl@sha256:eaab6d2a2bceb0caffa1ec20ee2c538a4cbf8a818e7307ba59d2d71f62064d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61155722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a25c6cc7dc7875994bbfd8e7bc2d944aa37126e55cc69e4a18ebbe9b64d0c8`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:52:50 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 02:59:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 02:59:24 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 02:59:24 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4c2513a39cfeddd6f5ed965670fe5e92920d68651d1d840e79b3ce0f56c41`  
		Last Modified: Wed, 24 Jun 2026 02:59:43 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422a1a33ed6f48cb48e382614ab9423b2e347007475fba131e74a1d4bfd6388`  
		Last Modified: Wed, 24 Jun 2026 02:59:43 GMT  
		Size: 31.3 MB (31304074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1a7f9254a111a76ae16dece8b29cb244d8070f2db98474a6c41534ed3ca69e`  
		Last Modified: Wed, 24 Jun 2026 02:59:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:c4e93e62bf252fa777ed76164686623c5428f09a1c5a538f26b97eb7e1450e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b85895c92d25d9335aa2d9de363fea108d1726fa85af796824ed8eda939ee9`

```dockerfile
```

-	Layers:
	-	`sha256:9e7a129b08a39a6b942ae6e659054f51a37809148f545734d1f5a48bc31c9aac`  
		Last Modified: Wed, 24 Jun 2026 02:59:43 GMT  
		Size: 4.0 MB (4003146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc00e2cee5882847b80227b2b20501e0a82de445812f1e0f184db98421551628`  
		Last Modified: Wed, 24 Jun 2026 02:59:43 GMT  
		Size: 20.3 KB (20252 bytes)  
		MIME: application/vnd.in-toto+json
