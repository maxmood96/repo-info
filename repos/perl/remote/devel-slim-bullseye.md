## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:b9bea6383ed7a78f512028d8cfd834f7c42c5a48fdd3cb66797a1ad6c9452728
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
$ docker pull perl@sha256:748323f2ded8d3d9ef71ee1ae52739031543c8a020a2e538e0f27a3e6b1a56b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57550898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985faf4cdc9d071c797c0fc089b0d4b0ff37beca16cf57a56d05895b3cd37658`
-	Default Command: `["perl5.41.4","-de0"]`

```dockerfile
# Fri, 20 Sep 2024 18:57:44 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["bash"]
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.4.tar.gz -o perl-5.41.4.tar.gz     && echo '402b2e10dc1a6249685f0cda5897959bfc079fc324b551a1c4771fe401563896 *perl-5.41.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.4.tar.gz -C /usr/src/perl     && rm perl-5.41.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.41.4" "-de0"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5feb9faac5d6ccdbd15ab30e3dab06e1e6128288744885877a376bbb0a7716`  
		Last Modified: Fri, 27 Sep 2024 06:15:49 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266ee007f827028787a1bb6b90c337c4b5f8bc05b8a0012d3c3713878ab8f63b`  
		Last Modified: Fri, 27 Sep 2024 06:15:50 GMT  
		Size: 26.1 MB (26122033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0cd4f5f934155a3868b396525914d46fa2ff72e748c913cdae572627b76f9`  
		Last Modified: Fri, 27 Sep 2024 06:15:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a914d8e17ab5ecb05aeafce68273542051bed1c4c28ce9bfd7fd7374a1ef61d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5bc2542f218eafb67f92441c8cd4317f93986f5d7127e31e30bf835c0ae1fb`

```dockerfile
```

-	Layers:
	-	`sha256:3db3b320274763931f4d9ccbb157f4d53f4a5a1a3f121d800483e2bc2b0ba2f1`  
		Last Modified: Fri, 27 Sep 2024 06:15:49 GMT  
		Size: 4.0 MB (3989421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e8ef339ddb6ba0d7c8dfcca09c871889753fe74ec0b0fa50b186f4a529a87d3`  
		Last Modified: Fri, 27 Sep 2024 06:15:49 GMT  
		Size: 18.1 KB (18060 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:a3dcbcc31479817ce97fe7c0a5b9970c22cb39e83df8c81e995af66209c93155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49967882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7522082781b752b34ec054fde304c0a4debdb8102be2a0d9d0525b428d8e1cf`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:29 GMT
ADD file:c451ece1244c14bce110ffbe6906867ce12f8e88234988b0edba91009a9dbbf8 in / 
# Wed, 04 Sep 2024 21:58:30 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:f572303598915f7fb61cc4b47f7207c9ee64d52b9db5fc03ee133ec2dd679347`  
		Last Modified: Wed, 04 Sep 2024 22:02:25 GMT  
		Size: 26.6 MB (26589615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53185675d6d94d789791a2a9c8524d19b7bd6c3dc0fd5c303e79392043b9051a`  
		Last Modified: Thu, 05 Sep 2024 04:59:42 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d695835015abd8b848d3b427fd5d2dfdb807994232a57927f4e7e767012ba025`  
		Last Modified: Tue, 10 Sep 2024 04:19:11 GMT  
		Size: 23.4 MB (23378002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1c090c381ebe0149345e7698a697b25b61dd6db2d33a9428c15e4f9c879033`  
		Last Modified: Tue, 10 Sep 2024 04:19:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:6859b660a686f1ac53111b60e6ffd7399a59cb18ab8421e5b93a31c18dbc095a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3981475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e36c38eeb0f4e01e48c93cb0760ca72fca99234b38b5c45c7dbfd2a98fe068`

```dockerfile
```

-	Layers:
	-	`sha256:e36395dc098e4f74cd89d31e458081dc7dca5bdb5835aa7860afbb367b06c54d`  
		Last Modified: Tue, 10 Sep 2024 04:19:11 GMT  
		Size: 4.0 MB (3963359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d81141c7852a0df17b7d28fa84a287e45bc9370a1d2f5862de752d841e3de29e`  
		Last Modified: Tue, 10 Sep 2024 04:19:10 GMT  
		Size: 18.1 KB (18116 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:1fde8c1675ce82d28c6390cb29dc9ce248ef767529e5c859ea12b8ffc94518ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55341457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f0ba5591035ebc0ce38cf845c21adf62343ecae65b61ad6c2c20167fdb2481`
-	Default Command: `["perl5.41.4","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:08 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 04 Sep 2024 21:40:08 GMT
CMD ["bash"]
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.4.tar.gz -o perl-5.41.4.tar.gz     && echo '402b2e10dc1a6249685f0cda5897959bfc079fc324b551a1c4771fe401563896 *perl-5.41.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.4.tar.gz -C /usr/src/perl     && rm perl-5.41.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.41.4" "-de0"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5aca1fd695cda2cfe9bced49ea5e8800a17d025e6f81d305a484c110f13a948`  
		Last Modified: Fri, 20 Sep 2024 20:19:45 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aec576a0268a3650572fa62e549dd6583a8bd5370c44d7aab5933bcd320c42f`  
		Last Modified: Fri, 20 Sep 2024 20:19:47 GMT  
		Size: 25.3 MB (25266826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd80b01fe4a681c36cef5282363fa530fb5034b93b2bf14b651173c447ca4a8a`  
		Last Modified: Fri, 20 Sep 2024 20:19:45 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:7ea61e66032cad2274a39ae9bfa721daa10be6008511b7936853edeb9a9818ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3982126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29dae44326863900b5c8105297aadb7cd20a7631128f0c6765bc2daad23c6b6`

```dockerfile
```

-	Layers:
	-	`sha256:055d6dd9a2356d2d5f98d6b7693fc55cb8fc5f36fe1457d36f353e38f9a2df2f`  
		Last Modified: Fri, 20 Sep 2024 20:19:46 GMT  
		Size: 4.0 MB (3963769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc00418eeaa089325ffdf0d494781eaf48d484bf9d6bc6c61422a297978929c`  
		Last Modified: Fri, 20 Sep 2024 20:19:45 GMT  
		Size: 18.4 KB (18357 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:e20f3f6100a09db9e188f0799a673267e2b6b5a44e32e62ea6c9083f7b2513cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60051310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc023e1395fee5f68aea2cfa547506b538a17c345288e03748c0ccbdcb662264`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:56 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Wed, 04 Sep 2024 22:44:56 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a051e35171a0367231b71b3067edcd8c4518363bfe858715b7f1c2d0b638d25b`  
		Last Modified: Mon, 09 Sep 2024 19:16:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0b3638001055c88db06a4e4c9cd2e3e30225e418377b6aa8aa4db1eb018a66`  
		Last Modified: Mon, 09 Sep 2024 19:16:55 GMT  
		Size: 27.6 MB (27637730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a893ee2760784273d43e92d7f040e4099b66e92c747ec85c1c6781f781563434`  
		Last Modified: Mon, 09 Sep 2024 19:16:54 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:d16aec42db08b93a94e253443ceb527c5b90635f73ac13cd9de98cfef567245f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4011666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f8cef2e9ad21d3eb3e71eb78e21a4ec4a6efac13d3c9377f3a2b51f3814c95`

```dockerfile
```

-	Layers:
	-	`sha256:e98fc1262d21283607bcdb73d1ed5af1e8033f02768a209bc823f957cb16bc61`  
		Last Modified: Mon, 09 Sep 2024 19:16:54 GMT  
		Size: 4.0 MB (3993636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a12c652372af841a0e7551fd20235d5ff27c35e3be603c2f17cee1e1861e7a5`  
		Last Modified: Mon, 09 Sep 2024 19:16:54 GMT  
		Size: 18.0 KB (18030 bytes)  
		MIME: application/vnd.in-toto+json
