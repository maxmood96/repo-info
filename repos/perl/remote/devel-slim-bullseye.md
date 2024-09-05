## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:b116c4baf998918ec418e918b2f693093dceef855205449df15c56b63504e423
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

### `perl:devel-slim-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:abb8af557ad9e2543333b055f8d351ccdb38ef35d297f2194fc70ce56bdf7896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56190560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6738bb88044f73052e9d32bba9130a303e6b0801f2e1a3ecfa2cc494a6222060`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca9dc81ce36fcb1bcba449382fea27038d9da16d5fd37f7abcf1ebbbdeb7ebd`  
		Last Modified: Wed, 04 Sep 2024 23:15:34 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451810ca14aa7077436bb273698f9ed95efd29bdeef12752798f750cfd363ee6`  
		Last Modified: Wed, 04 Sep 2024 23:15:35 GMT  
		Size: 24.8 MB (24761616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2366b66469974e1ca5f939a56ffbf3b4eeab0d10e7f69a62f0bbfff18e525b0`  
		Last Modified: Wed, 04 Sep 2024 23:15:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:0fd13d35160abbefb647cd0091323720571804eb721efc2ac2858910318b42ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33610610d348d5bb4fe6e6ec072addf08941513604a8495b15047581a433df30`

```dockerfile
```

-	Layers:
	-	`sha256:9c6275de0fa408ddd541b4b3e76283477c06d6be5cf3bc8242b188d88fb8b138`  
		Last Modified: Wed, 04 Sep 2024 23:15:34 GMT  
		Size: 3.9 MB (3933629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb97e4a9333c31901a8d7e075c263d287f32232390aad5768cd35e4164e96e5b`  
		Last Modified: Wed, 04 Sep 2024 23:15:34 GMT  
		Size: 17.8 KB (17842 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:d49eeb41fb9f121628032540987caa2efe6f8b2c6efad8c2604e8a4f08eefe64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51709311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f1e2e6194e4c1b0d8ed7c77f2604950768a8d621187ab04e703feb1bf594c5`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:b6f3f19f4bd2bf78068380b3cd10d72519ced99a2b5abe830b4729df341dcfdf in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:c8ed7888c72e20491bc1a05ae8b473757ca4d400de33029eab69bacfb9dd933b`  
		Last Modified: Wed, 04 Sep 2024 21:52:15 GMT  
		Size: 28.9 MB (28924911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c583beb80e6f7ecfb8f1db6d2235cecf4965d351990190717b574ea357b1f0a2`  
		Last Modified: Thu, 05 Sep 2024 03:47:59 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b4dd7cf80f37e61bf4f54dcc8ebab7c86b3e197d514720badb2b02cda41c57`  
		Last Modified: Thu, 05 Sep 2024 05:15:17 GMT  
		Size: 22.8 MB (22784136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202deb9d40b9fc211697e3aed0f2f9aa218dc4e210f78db936769aa4554381f5`  
		Last Modified: Thu, 05 Sep 2024 05:15:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:44a313a3d3821ff446951e92105954529643644f25560ca0e58cc3e1520de854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30016eb491644935ba012a879d9557d76ec6cc6b051b0d05e1d288e477affb8`

```dockerfile
```

-	Layers:
	-	`sha256:394bc7a38e00e097f8cc4d7c60c73280ddc339c6fbd836a1859e674958c3e3b2`  
		Last Modified: Thu, 05 Sep 2024 05:15:16 GMT  
		Size: 3.9 MB (3904826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e0df76a6d5fbcd7ab9a0e5fcae13381fd7bd45c97430b1cdded3faa0768eed0`  
		Last Modified: Thu, 05 Sep 2024 05:15:16 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:bb80efec987ed7b6a0f42db62fd1de4c9591bd7d90d53445f633569e8471a26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48772966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd28511072927024ce987923e654bb2c1fc663ebee2f26845d2ce628c4bdd26`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:55 GMT
ADD file:9f6a2e97ea42608bfeab22c77e01d6614f64a00a2be04ed1cff9909375d517a8 in / 
# Tue, 13 Aug 2024 00:57:55 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:1a1ab1e12ebdbe1b5383067049fc746bcb9b882bd309b8befaa11c47eed5d4dd`  
		Last Modified: Tue, 13 Aug 2024 01:01:38 GMT  
		Size: 26.6 MB (26589215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1705edffcf0f99170984d5e897d8f2209d3d07e9917f9bb477107523ab0fa2d`  
		Last Modified: Tue, 13 Aug 2024 12:53:01 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d13098377776051a064157d992b71cd6c2772ea344878fcd8de5b53637cd351`  
		Last Modified: Sat, 31 Aug 2024 01:54:08 GMT  
		Size: 22.2 MB (22183487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fcf3036860393fd33bff9fcc1f361cbc9a961954b177c8297aad3167b4a12e`  
		Last Modified: Sat, 31 Aug 2024 01:54:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:50a15771583343569a1aa3b368a728053e65e5a591fe350501e0a60028c3e50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01265ef4a894f892b3051fbcbd368c5b072aae0b897d506423bb2a391c4ad645`

```dockerfile
```

-	Layers:
	-	`sha256:adc5c28d5c59c57f22289195f38c350732b8d695c7b42ea25a95985e00a520a8`  
		Last Modified: Sat, 31 Aug 2024 01:54:07 GMT  
		Size: 3.9 MB (3907544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85861ef69e1debb6b06760101a399fbbedb5679145289b2cababbb6d473983f4`  
		Last Modified: Sat, 31 Aug 2024 01:54:07 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:f9313690b3b681e086e76fb522583ddff17ccdb60fc5fde6ea4263bc8b3bd418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53976269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c9fcd178f6c040efd47888cf43a84973ee51934334dc947f48c2d2d781b321`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:06 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 13 Aug 2024 00:40:06 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6768f1223e6d26a4bbcdca7648240e8023a2dc4f4871f0ccf3daf94475a188`  
		Last Modified: Fri, 30 Aug 2024 18:19:24 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9674725ffa9f1aff265664585f3b4706c47cec2777d2a60be572a154ea204154`  
		Last Modified: Sat, 31 Aug 2024 01:09:04 GMT  
		Size: 23.9 MB (23899917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d607d8dabebd3d9defb8bf9e9a3e3e7042de1f9f2f8d245de49dccc4d2525e8e`  
		Last Modified: Sat, 31 Aug 2024 01:09:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:cab1a558779f84c0c39a58fdcc905464fbf3a295d742479456f51ffdadeba110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3926118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2942f8604442cded0323764483bdc25632c044bb920bbcbafb344737bba1f3cf`

```dockerfile
```

-	Layers:
	-	`sha256:2221eff55152388554c57b3e12a931ec17b79ad059f5e78aa779467b77fb27e2`  
		Last Modified: Sat, 31 Aug 2024 01:09:04 GMT  
		Size: 3.9 MB (3907978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a8bb7049c33a19cf8f03fddd776878695999c0ccb6ef8412e70d99a0cb4851`  
		Last Modified: Sat, 31 Aug 2024 01:09:03 GMT  
		Size: 18.1 KB (18140 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:52d01fdc5cd2dc8cc139d6ea9ebdc72c92edb4d5984720049a69382acbefe164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58604785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e487e4e5fb0c296c73c09451dd7c4c4b830aca75507f7027cc83d033e79b7b`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66f9a962c502b92b37ac9314e954e8872fcaa4f06dda16f317f2edfae1b138a`  
		Last Modified: Thu, 05 Sep 2024 00:16:09 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466db95d803bd4995534ffc4fdc04d823ce554c078a754d528dd65a92c68ef2c`  
		Last Modified: Thu, 05 Sep 2024 00:16:10 GMT  
		Size: 26.2 MB (26191206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f025a23d3bb4724a6ae2e0dd772f35716e0d5aaf35feb448c4913d359cf0ead`  
		Last Modified: Thu, 05 Sep 2024 00:16:09 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:eef3a2fce8049e3a43ecf8864563427633cbec8982340c4fa2ccc9f5c80d73c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3955709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bb0e9262ca6a195ddc21889c011154c3e82bb2416e38bddd8aab88384b7c4c`

```dockerfile
```

-	Layers:
	-	`sha256:13ef5158d476c86ffdfe6de063648b8ef30329688c0e5306abb154c02aff6c32`  
		Last Modified: Thu, 05 Sep 2024 00:16:10 GMT  
		Size: 3.9 MB (3937890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f794315240e0b5bf524d59dc169cce6f50e12476ce1273234cda583883f34e0a`  
		Last Modified: Thu, 05 Sep 2024 00:16:09 GMT  
		Size: 17.8 KB (17819 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:fd0efd0b58f21c35a7aa9fde052e4d46e0cef85fbdda7b0b99797717cf8bb4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57605876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96381cc7cc2fc9dfd638b17952abab14e41d0ed1aa3f329bfc0c35300979194b`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:12:29 GMT
ADD file:d4b92daa2701c7af077c4c89b2b1f5a97cfc6389c09e049b3bdaa36454653bbd in / 
# Tue, 13 Aug 2024 00:12:34 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:15b8bd5d9ec350cbe23bbccddd5284b3cc9139e037500a63a02025354518d5c8`  
		Last Modified: Tue, 13 Aug 2024 00:23:52 GMT  
		Size: 29.6 MB (29646095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa7099e1bedef4abac5565314aa663115d1958638c57948643a95b56b2a7c31`  
		Last Modified: Tue, 13 Aug 2024 21:21:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3711c8c7eefc18ebe96d4331249a5fa934ad56810298572cebbbb1940048ed`  
		Last Modified: Sat, 31 Aug 2024 17:32:33 GMT  
		Size: 28.0 MB (27959514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd964ba47f73e6dfdb1d547e5398ab3cb014814dde28a27bac1ee9daa3c9fe2`  
		Last Modified: Sat, 31 Aug 2024 17:32:30 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a5475af0e2ebe1358059395a09dc7307b2c73c1bbfda846898730ee1485cd8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 KB (17672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471d1e5264fefa54eae05caf2963ae107d7e7d96fc5dcf709691e99b3ddd6953`

```dockerfile
```

-	Layers:
	-	`sha256:811a7aebabd746451dcba48297c9f3944012771b517b1f06dbb1c13903375c88`  
		Last Modified: Sat, 31 Aug 2024 17:32:30 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:26c92b325412dfa5f6baf5da7a2beaf632a5948d1ea659517e6fb674fc30827c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60313006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f227486caea7f22b5fee89757db7c5644c20bdd6bd7c70c666c65d2ab504ba9b`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05a4dfe7b57aa553ae464260d6d528d00a65a9704395de98bb0c889034560a8`  
		Last Modified: Thu, 05 Sep 2024 01:29:06 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1c87a9270e95b6bca006ae92607051b5af69a9a17ba3e87340604c7e086997`  
		Last Modified: Thu, 05 Sep 2024 02:52:32 GMT  
		Size: 25.0 MB (25013469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9379a85c3f87389fcfe95e3d07b610ff2c57069898b1d1a919d6d3c3e3754ac4`  
		Last Modified: Thu, 05 Sep 2024 02:52:31 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:fd5476ff47235f1b6c1b0f0ef19fc5b82ee85a2b88e306eec160c68454a65a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6592ee7642e02fead8e0bf5a40a231993a259daf50a08657f4cf55065b6296`

```dockerfile
```

-	Layers:
	-	`sha256:62ab6b574e85831ab5dd6904eca066fb71fb48e821e2fb708eded960ea0765ce`  
		Last Modified: Thu, 05 Sep 2024 02:52:31 GMT  
		Size: 3.9 MB (3922384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed69a40fe4a8fc0c3ac72d2de1b7fdfc10fdcfac3d73183c591543183397b3b`  
		Last Modified: Thu, 05 Sep 2024 02:52:30 GMT  
		Size: 17.9 KB (17875 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:e1fe4534e696bdc94f585bee99141e5be931b91c87c7af46b69e3e0a2a3c0e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53649516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c121c174a65e60cb3010c9b551224c17ed45a4287cfe31dd9f94acbb8b9720`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:43:12 GMT
ADD file:a473fc09ddb0d1045f7f330f3a48b9cfe65ff9ea65cfa5c8262a8a5be9d4db75 in / 
# Tue, 13 Aug 2024 00:43:13 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:83ea1b2f9d26c88827c9a658387c782a21fca528fbf7418f1a4eaea9a9818bdf`  
		Last Modified: Tue, 13 Aug 2024 00:47:58 GMT  
		Size: 29.7 MB (29668965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85346e731181cfe57afab816b68be63cc66bbd40a65b978876abf641e4e764a0`  
		Last Modified: Fri, 30 Aug 2024 18:25:34 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fba2c01081660f617d378f12e7ecaf67fbd59069996628354f3377766fbfa4`  
		Last Modified: Sat, 31 Aug 2024 01:19:50 GMT  
		Size: 24.0 MB (23980284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bc766ba56609cceca13b1e5d9ac7ae1b691cece5fa7a0d8d731c69d6b97fab`  
		Last Modified: Sat, 31 Aug 2024 01:19:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:360ac15379797221f39777c70e309e2d7ea4e6cd9875a6c3a76a1e52562d3671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bbad5e89cc9c2bf70b5c249bab56c9f36063fdc18d591a345122d15a4b62b5`

```dockerfile
```

-	Layers:
	-	`sha256:2e3f8a3f25d6bc2f0b8b28b0a6efc2894128ada594181c4a52dd28bd68a884b2`  
		Last Modified: Sat, 31 Aug 2024 01:19:50 GMT  
		Size: 3.9 MB (3922331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:004775e902677fc4a0641a75096b9e82f27f33fa02b4d4756ca528b6f9d79892`  
		Last Modified: Sat, 31 Aug 2024 01:19:50 GMT  
		Size: 17.8 KB (17843 bytes)  
		MIME: application/vnd.in-toto+json
