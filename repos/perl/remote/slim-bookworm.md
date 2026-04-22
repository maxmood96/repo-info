## `perl:slim-bookworm`

```console
$ docker pull perl@sha256:f50a505ef39c22cfbdd34ddd730d0c315790e73a40e0470740b9d6b6334dd91e
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

### `perl:slim-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:7ad15800e5921403ae77d78d2e2de8b4627852e48fe95369c10ddad1186d5129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58442633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2a3bbac5acb6c60c09a5d122e2413be436e9ab01797a4c28e3a520a1f724ac`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:45:47 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 01:50:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 01:50:25 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 01:50:25 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4207b4aec838588928a1af3c91aa2ce70547140dbed360785cb1423d9e459545`  
		Last Modified: Wed, 22 Apr 2026 01:50:36 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc07565b9ed6ef0f9627e2a06c384363225c70416e88dbb2f31b9fa773a407a2`  
		Last Modified: Wed, 22 Apr 2026 01:50:37 GMT  
		Size: 30.2 MB (30206115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e60fe681598c0b11f0c43f828877a26b075a1f1d8a9bfab19c54eaef16feac`  
		Last Modified: Wed, 22 Apr 2026 01:50:36 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:9cb232098b160fba0f1a706ffefdee35ba980261ac01f52df8e639bdc9163946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f319e79e0bf9f3a366421fec22f560f754789cdf8086f42c733a81f6ddaae0ee`

```dockerfile
```

-	Layers:
	-	`sha256:97fad3ca5418281e20929d6d5443cab11f26902c46bc7552ba3fb318420c6fa1`  
		Last Modified: Wed, 22 Apr 2026 01:50:36 GMT  
		Size: 3.9 MB (3939962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41a916fdfe2728697c18bfe63a3120f40286b079039c2ac27ce21c9bae213b3d`  
		Last Modified: Wed, 22 Apr 2026 01:50:36 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:43dffc447a2e382a4ee55210ded91578f4f689ee532f9ef52cb99984ad1ad46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53061028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9c781e38bd8aa18c714427d006727ee8a5e95bc6b7b0eb9825eeb9e312b53a`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:51:26 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 02:57:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 02:57:07 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 02:57:07 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:4748d6bbb5a5b9e671dcabe2f909bdd7514f760a5cfdcd37d5b04627424120f2`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 25.8 MB (25765667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420eccfc804cdd9a385fc4913d550a41e93f73995d6e293e8c6994c3fe9b2a20`  
		Last Modified: Tue, 07 Apr 2026 02:57:17 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0881be9b800b266616d7c34a8ad0c563f1e1134de0e7a0e10fdbcd0c12c26a4b`  
		Last Modified: Tue, 07 Apr 2026 02:57:18 GMT  
		Size: 27.3 MB (27295095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ffc60962715b06136a39cc5320f24af43544e1a4197c5557ce6c36ea388e80`  
		Last Modified: Tue, 07 Apr 2026 02:57:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a4ebb6c0722e2780c403ff3acea6440143b93a3d180fefc7e2883f6ee975f6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29de10a8b7730a0f2129811f218f5645be07ca57194525425065d380605a6f6`

```dockerfile
```

-	Layers:
	-	`sha256:81db071242a385bb1699447c84d64a5b1da6cf6e0fd40d6565699c8e106f4a98`  
		Last Modified: Tue, 07 Apr 2026 02:57:17 GMT  
		Size: 3.9 MB (3910829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeecd3b70a0aec57bc6cf07a0b6f234299bdb9383ef2b4bf93d8d19a173f6a35`  
		Last Modified: Tue, 07 Apr 2026 02:57:17 GMT  
		Size: 18.9 KB (18878 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:6de903f726d49198ab34f19d80799b0c361bc05605f125fcea7b596dfd690a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50316902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305b895ff0ba876141457f0d33a601ac145a9353c6de8785af5ab5c8a2b9e1e1`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:14:44 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 02:20:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 02:20:19 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 02:20:19 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5530f15eade7edfd41b6a91fe50098894f736ff0217eb1039cb61782292940c1`  
		Last Modified: Tue, 07 Apr 2026 02:20:29 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6065ae27d3639decff2fd12c7e9268365cf9f243567f6ea40acc1eecc3a49fdd`  
		Last Modified: Tue, 07 Apr 2026 02:20:30 GMT  
		Size: 26.4 MB (26375174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cbd46a4d37c63986019a91ef3477cf880441449f861609b80473456ff6623`  
		Last Modified: Tue, 07 Apr 2026 02:20:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2a3216cd84e936e41f9bd4670c1980457283c0c1afaad904f01c623272e91e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e8ee7033fa273f653643921fd223b1a6c4cae82a9f97811bfd0b3a1d827de9`

```dockerfile
```

-	Layers:
	-	`sha256:f84466a062432eb818b1d1e035ac3e892dbdb1f59b27e7332eb153a1edfd96a8`  
		Last Modified: Tue, 07 Apr 2026 02:20:29 GMT  
		Size: 3.9 MB (3910054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaa866913b97ad0a8b2f05ba40479b4c01113dc262390ada12da2d5317fe9f07`  
		Last Modified: Tue, 07 Apr 2026 02:20:29 GMT  
		Size: 18.9 KB (18878 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:60e5abe33040fb15cb184e47919efdb3a6e84e6576e068929751719db5183dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57194654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc80f42f5ebbe6e1296182a680da762c3e6eb186b6f64c246729e479c5b8971`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:05:39 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 02:10:27 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 02:10:27 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 02:10:27 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61344662478f4d7d6443bb32534379fc1b075293420c4022510f9c935695cd5`  
		Last Modified: Tue, 07 Apr 2026 02:10:39 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df14f8dcee12985473a5ab2b2ee8040e3f947b098a42dde0845434e5062a957`  
		Last Modified: Tue, 07 Apr 2026 02:10:40 GMT  
		Size: 29.1 MB (29078219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ec03a07e37949329cb60beb560bf69fad719365b63671d41950fc3f8ba5d8b`  
		Last Modified: Tue, 07 Apr 2026 02:10:39 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:820058f013a8a970086f2193b1664d284d5444ac805ec86e8495a4da63c794f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15118febeeead44449397b368099b8bdbde2ff18d9182030a966e92f3542b4b2`

```dockerfile
```

-	Layers:
	-	`sha256:d9965109a967e780285159b9de96c1e900143564e37cb5159ca9b8c01fcda541`  
		Last Modified: Tue, 07 Apr 2026 02:10:39 GMT  
		Size: 3.9 MB (3911223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd951dd1cf12fddc08c604c9cd9dedd7f53039eafe468f15d49bd92af1eb9f0`  
		Last Modified: Tue, 07 Apr 2026 02:10:39 GMT  
		Size: 18.9 KB (18906 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bookworm` - linux; 386

```console
$ docker pull perl@sha256:a73a2ee946975699cb06e37525c52deaec9f94e5dce33de7d25a6b56e38d4f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58564876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624a94aed413a049608e3935490809eef0a07b9b2adaa115ba1c5533f5301c80`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:48:40 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 01:53:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 01:53:32 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 01:53:32 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:2686573d3309fb5ec86398e0f20a729a351a259d4d793edf6cb41a0ef910fccb`  
		Last Modified: Tue, 07 Apr 2026 00:10:58 GMT  
		Size: 29.2 MB (29221768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bdf96b4bf6e7137cedf440f3244afacf01699dd87631617e002309b8325b11`  
		Last Modified: Tue, 07 Apr 2026 01:53:41 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceaa3ee8c8b757b64814b1006acffa47c63f5f88068585f1841ee21b2187af94`  
		Last Modified: Tue, 07 Apr 2026 01:53:42 GMT  
		Size: 29.3 MB (29342844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac069fc67fa81f3843218b548225f63ec130ad45065fa5faf8e448d41be174a`  
		Last Modified: Tue, 07 Apr 2026 01:53:41 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:6ade256d945d5ec15eece533f003ea0407a9b849336da5fb520b2d1434aa8016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c3d9883d0c450b8338d345feb94f8a72dfe73a8ff0ade4b994bdba404f035e`

```dockerfile
```

-	Layers:
	-	`sha256:eb7d037deca73bfa871a01b81508d8bd1ab5ded0bb9890620b37ddaee4e1ba45`  
		Last Modified: Tue, 07 Apr 2026 01:53:41 GMT  
		Size: 3.9 MB (3933894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0caccb73308efb7f2f967d92210abd930fe73f3f7cdc9dd3b4599f14635bfce7`  
		Last Modified: Tue, 07 Apr 2026 01:53:41 GMT  
		Size: 18.8 KB (18751 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:c3c3d4e2f4792bc2604fa0b28881df0d5561bd45ae897d0093372f736e34c80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56907594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e73baaea8a4bddf7417d25f8af24ec6435a89a36efcc1b3271d656550888ca6`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 15:40:36 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 16:05:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 16:05:58 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 16:05:58 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:7377a524ccdc918cca6272a35a48618805ffa8fb443fe7f687971509cb1f8d53`  
		Last Modified: Tue, 07 Apr 2026 00:10:05 GMT  
		Size: 28.5 MB (28526285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61569bacde7390f6ac6013444e8d7cbdd110175943fd2a8363795805e8b5a91a`  
		Last Modified: Tue, 07 Apr 2026 16:06:41 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbba1a97fc0319826dd92247e29b10774910a950766ad721919222bde26e9e3a`  
		Last Modified: Tue, 07 Apr 2026 16:06:45 GMT  
		Size: 28.4 MB (28381040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d76acf8de227f06c828ebfaf054588f06489cf8d7bf320dacb9aa1da32fe9b5`  
		Last Modified: Tue, 07 Apr 2026 16:06:41 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:60705d50505a7752b908a18774f20fface57780e596aaf79c166a807a8a9a17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2068ce3d31ae7de78981793d34c1fed3b4c5f60925cb282ca378d3145f9862a`

```dockerfile
```

-	Layers:
	-	`sha256:3e9109e4d51193129340fd147aa79aea90c65f78637262e7cb5dde794613dbbc`  
		Last Modified: Tue, 07 Apr 2026 16:06:42 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:30f614c1b42edc22e04d86ae33f8dec0822f0bd36d41d8f44fddacb59985f31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63090064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bd39e0f43069dd7984d00dd7e1ba15a3c7bcf530b6dd97fd55406063689124`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:26:01 GMT
WORKDIR /usr/src/perl
# Tue, 07 Apr 2026 05:34:27 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 07 Apr 2026 05:34:27 GMT
WORKDIR /usr/src/app
# Tue, 07 Apr 2026 05:34:27 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340168cedbbaad69c0a1ed5b35ebf9c57e0e448ebbbfa035fd08f23ff167e4ad`  
		Last Modified: Tue, 07 Apr 2026 05:34:51 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37be9686f0a516450aca7d8a7f3c3e8ad351134ced369abd6ec671afe1f882e`  
		Last Modified: Tue, 07 Apr 2026 05:34:52 GMT  
		Size: 31.0 MB (31011332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbb3d3d68b839d47530f7da1dc10bbed9f9306a4d417335498f7fa4866dba81`  
		Last Modified: Tue, 07 Apr 2026 05:34:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:b6d24bab9ce183210f91ff50d0ffcb95ace26b8ff72884231517ec33c91fdb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534a224ff6139e1d79bfae514e0e1ee89b10f6cb5b24fb226bc2206d5e6630e9`

```dockerfile
```

-	Layers:
	-	`sha256:006661bc890c4373b2ebd76cf9f30cf21f88292966d28c317e38fa75c9467109`  
		Last Modified: Tue, 07 Apr 2026 05:34:51 GMT  
		Size: 3.9 MB (3925902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71de64691a861d33db5702dcf4f6a74228531924440f387462ef1f5ee6d3e085`  
		Last Modified: Tue, 07 Apr 2026 05:34:51 GMT  
		Size: 18.8 KB (18840 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:95825b4280f529eab08ebabf205b2730e18571941370c37025edf80ce5145424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55643291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa305787fea7af092028656296cbed896313db8a6be21e0c44ab1efd7e0d0f58`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:42:00 GMT
WORKDIR /usr/src/perl
# Wed, 22 Apr 2026 02:48:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Apr 2026 02:48:10 GMT
WORKDIR /usr/src/app
# Wed, 22 Apr 2026 02:48:10 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb976f04d2b6fc2ed16c530b6a8e512d087997d1ca06884bf53388c493724a0`  
		Last Modified: Wed, 22 Apr 2026 02:48:29 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034c48c526ad13dd9a693c418f9e79002bee480a0bde2010d1005cb6d732efe2`  
		Last Modified: Wed, 22 Apr 2026 02:48:30 GMT  
		Size: 28.8 MB (28751461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47015274f1ecd3733fe89238f23fd0e7cecdfb8e5481c0d985e87ed03612a3a5`  
		Last Modified: Wed, 22 Apr 2026 02:48:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:81258c24e2b88bd68c68589cf59e4ede4de9369ef5eadbb1db6b6f8da3885ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281b437d3963a0ebfd00f676af7d9e4629e56d0e039a420941df0f64750a2a80`

```dockerfile
```

-	Layers:
	-	`sha256:ff67c3bd84f4d1ca0d9eb60bf68d8377f7e84052b470897992d239026d0beb91`  
		Last Modified: Wed, 22 Apr 2026 02:48:29 GMT  
		Size: 3.9 MB (3925235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b1e34417fa70e449f93b2ae22fea0c09b10456c7bfca9e184d6e85e5d996145`  
		Last Modified: Wed, 22 Apr 2026 02:48:29 GMT  
		Size: 18.8 KB (18790 bytes)  
		MIME: application/vnd.in-toto+json
