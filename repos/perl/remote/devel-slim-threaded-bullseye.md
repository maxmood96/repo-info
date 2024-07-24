## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:da1aa51a594f51961715c5bf1122f743d6a246f2765a22badf2969a8d8d01f9d
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

### `perl:devel-slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:e9064ecbd91da14c4400aabb7466cad1ed8513b8cf231bdc717a0454f1c410c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56219621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5396d4bf0f027bdbca741d6b0ce8a73aacf97104d5fb66dff1ab519246af4b8`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45fa6ad8d16de1712aec7dd0dba52e031e035771fad268769b4d8e60d5a123a`  
		Last Modified: Tue, 23 Jul 2024 07:29:52 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210ff33db130f0da5eb55eb54837375e011e56ec88ea864d78b12790954462e9`  
		Last Modified: Tue, 23 Jul 2024 07:29:53 GMT  
		Size: 24.8 MB (24791025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baaff1444572539234be0d6141c232de3d2cfc80fe366154d2c37ca2203f350`  
		Last Modified: Tue, 23 Jul 2024 07:29:52 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:6984cd70e83b1d86d2d71e65595987859cb47db7e85515013a603acf3c418f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9af8aa663b26b98f4d53d2ae117f8438425ae405f769a12a9eb262daf934ff8`

```dockerfile
```

-	Layers:
	-	`sha256:74a96953f14878232aa41ea11cdbb837fe47caca2af2f9dd257190be0fa346c8`  
		Last Modified: Tue, 23 Jul 2024 07:29:52 GMT  
		Size: 3.9 MB (3933683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ef9f508252541a9a9503d595bce21669e9bde0069c85ec2381469430018bec`  
		Last Modified: Tue, 23 Jul 2024 07:29:52 GMT  
		Size: 17.5 KB (17461 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:090477106490ecc4d6e27859c1a9ac66e406cd6e6dba653924492a391badd7a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51705190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f4d82fe76332c6e63203769dc62f9318a2fd4ec7c1603f8a024edcd5fefb99`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:56b9d2d0e0360f64ade3cbe073b446e10c8e6bd253b761c16b5f319a8103d181 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:5b04226d50f1c00a6c8950192ad70a2038016868ab6ffb162ad447e35e67a3cb`  
		Last Modified: Tue, 23 Jul 2024 00:02:06 GMT  
		Size: 28.9 MB (28930588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66647c1f3ce664aaec353a91e99652d845681b6ca7432e025c53648644e5839`  
		Last Modified: Tue, 23 Jul 2024 08:31:25 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc31c75f16f8594bf0240ef91a9d796ee1a23d72d957c606552411fb2129017b`  
		Last Modified: Tue, 23 Jul 2024 10:15:34 GMT  
		Size: 22.8 MB (22774335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb40816c977f53a8e217f681e41d6b66bf51248faf252eeadede130a38c4e4d`  
		Last Modified: Tue, 23 Jul 2024 10:15:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:02aedaaf79d2dcbf03eb74240c37659a86542195c9135829e2292d8df179ad29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb634eb7bf45fb06d8910c1d07bc5d6bc78ab4513f0972c7e4e2ca979f2be99`

```dockerfile
```

-	Layers:
	-	`sha256:e5fe7252bf7a823cee7203480d15a498dc67c6356500f92fe32d4f8e76b7ff3d`  
		Last Modified: Tue, 23 Jul 2024 10:15:34 GMT  
		Size: 3.9 MB (3904880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a3994216cc79c4f050ae017de3dab550d7884681f0734eaa9a7d2fb216b2ae`  
		Last Modified: Tue, 23 Jul 2024 10:15:33 GMT  
		Size: 17.5 KB (17523 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:1f590e6264464791183d01b25054333cda1c35d94537f0e07e0a6cdcd1a6798d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48760969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9011120635ee512dec403dd85da73d11b0f173e470f146b83a1f0d6c90b932`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a8cc186c41214e293c47fedcd8aca489d4fbaae7b1b4731b3e51cf40bf665`  
		Last Modified: Tue, 23 Jul 2024 23:49:29 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fe35a09b75b669fba8d5988a9119c75647b8e6a5338db3325b12e8a56d5675`  
		Last Modified: Wed, 24 Jul 2024 03:06:54 GMT  
		Size: 22.2 MB (22171571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfaab8d316cbaf827880dd7b6bbee420d25e55e03a8de3338965dca6872f7a5`  
		Last Modified: Wed, 24 Jul 2024 03:06:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:796cc969988c1cb52ad2d288c567994be12b37ffe68959d11ce4d6fb518a111f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ae8f0de416305f2a17dca47e6073912e3f21621fec36e79fcbf7423f7478a4`

```dockerfile
```

-	Layers:
	-	`sha256:779cdbbd72e19c7b2819e121a17541c3e7662b9ba99aa9619bd286e27cb2006c`  
		Last Modified: Wed, 24 Jul 2024 03:06:53 GMT  
		Size: 3.9 MB (3907598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9ed73405ee268fdc668f3b083c230e0524a25891d29131ceec823afa5d1a512`  
		Last Modified: Wed, 24 Jul 2024 03:06:53 GMT  
		Size: 17.5 KB (17523 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:af81f700742f2ede29c32601e5fe81b63de327a1e3d5acd44ffe33a79b18944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53984034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ba8f85f29a370106692010b37f9fe932dbef55eca5868d9f6e2e5807486251`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece3dd88229cb7c04fd86720e827b333669f51a2ee41967294dc743daff00b2a`  
		Last Modified: Tue, 23 Jul 2024 22:32:08 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b91d28bb9fa23e8f268ba465a61bef51c47f6de3d1d648f4b2d3db6b3f4463`  
		Last Modified: Wed, 24 Jul 2024 01:10:59 GMT  
		Size: 23.9 MB (23907682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbeb21adc930fb225d59b4434cce2ec80fc4caa3f5a6d9f9580b42241930663d`  
		Last Modified: Wed, 24 Jul 2024 01:10:58 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:0aa469a460e492a29f05d8cefa4900fc4c5bd9099f5aef4eb4ec41ca30db473a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f513e499905c2297185404a2f28048610aafa595634591c358a83610eba52d5`

```dockerfile
```

-	Layers:
	-	`sha256:84047c662e91637348a80dff8fcb127ab5afd7f26f57ccbb59f0e77a534ef72a`  
		Last Modified: Wed, 24 Jul 2024 01:10:59 GMT  
		Size: 3.9 MB (3908032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1dcefdc02d3694131d603c0946ba59e5f228fb27c2a13510658b56b1de0802b`  
		Last Modified: Wed, 24 Jul 2024 01:10:58 GMT  
		Size: 17.8 KB (17758 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:4f95b491b2360c7ca415dfd927e0ab05aed75192f512f83b3613d84179fde945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58671236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384eafa81317ebe6c58482707bfa26c96f6c4e728764eda04853478cc289fa12`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4d5542630ffadcfbe3b702d596370140c404f7c7ac39c8afc846b88fad0be6`  
		Last Modified: Tue, 23 Jul 2024 06:19:07 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c3abb962868effef93e653da8345b7a323fc40cc4d1f0942308a96b7d8488f`  
		Last Modified: Tue, 23 Jul 2024 06:19:08 GMT  
		Size: 26.3 MB (26257161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd50fb956c3b440c5268113a9a0306b0e9863659ac5e2390d47ed011d4660df`  
		Last Modified: Tue, 23 Jul 2024 06:19:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:fa8981aafdfa09f284df529b0c2c2ea2cf037450c69a8205ac8d21611bdc8e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3955381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c03395e4cddc83576fc943d198fa32b1dc2e2d4025c1b39cf31b0de2ebe7b2`

```dockerfile
```

-	Layers:
	-	`sha256:70f83810279c50afbc7072d23cb8947001198f807ce5908388f9eeaf9fe711b6`  
		Last Modified: Tue, 23 Jul 2024 06:19:08 GMT  
		Size: 3.9 MB (3937944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e3f504d94f20a43310f5fc8c5151b7e1a63b3341d2f05e13d4052491e4010de`  
		Last Modified: Tue, 23 Jul 2024 06:19:07 GMT  
		Size: 17.4 KB (17437 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:3af8747a6945dfc9660fcb7f09d51337612d6d10922f6238ca7c91357625b5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54278249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6df4c98273d1a36b2a9755c330a0f1711d1447e126fe45af69951d6007e5f5`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 01:19:38 GMT
ADD file:791d05eca72cc81080afbb76c7f3f02a74893142203b6aada9e3170404049223 in / 
# Tue, 02 Jul 2024 01:19:42 GMT
CMD ["bash"]
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/perl
# Wed, 03 Jul 2024 14:39:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.1.tar.gz -o perl-5.41.1.tar.gz     && echo '7dee38af601b0ba3f3730cb812cdbc799c921da440cb0ce96dd7a4f508b1a6f8 *perl-5.41.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.1.tar.gz -C /usr/src/perl     && rm perl-5.41.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/app
# Wed, 03 Jul 2024 14:39:46 GMT
CMD ["perl5.41.1" "-de0"]
```

-	Layers:
	-	`sha256:59602b870d8ca1e13dffda9de0c5f866f86ff35c1e595ea481bb1b2c48c18b8e`  
		Last Modified: Tue, 02 Jul 2024 01:30:52 GMT  
		Size: 29.6 MB (29639850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22767307e1d662a70e68a8d4470fdb2bf8671fa16d3427f7210aa1cf0e8296d7`  
		Last Modified: Thu, 04 Jul 2024 12:12:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2b86726f62bee5117f36aa60a37aaa5a83d00f6da6257d035e9ddeacc7e343`  
		Last Modified: Thu, 04 Jul 2024 14:04:25 GMT  
		Size: 24.6 MB (24638132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db185592bf83349f404430cee14fc8efafe36ddaa198904fea3a740a27182f97`  
		Last Modified: Thu, 04 Jul 2024 14:04:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:de7b86d0e0ea62c51d4f8b45635fdf021b48eef1e8ce8e047bdccd4d0d017a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb8632fabb05527f633c1bb64520e9be99644b4cc779dbebf7afc52d694dc35`

```dockerfile
```

-	Layers:
	-	`sha256:16ccedf3487b7a9ae33fb9e510c30592de1bb72ae05a33348214e6af10635406`  
		Last Modified: Thu, 04 Jul 2024 14:04:23 GMT  
		Size: 17.2 KB (17171 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:d78ef042fe7941e9083109f942f3f98732ecbe46e7f29861c7fe1d6fb91cdbec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60380900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ad4bfd86fd9c3b424719c044722e8ce0027ee00f5b08852f467618a2ff1add`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b13390f73cc9a8d336ed123d1e1c59cf672505e174b2098c59de21a7ce91e66`  
		Last Modified: Tue, 23 Jul 2024 20:06:31 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1ace6d875baacc404c9a39f148c8f19f8df95506a3b19dad5a64fd298a178c`  
		Last Modified: Tue, 23 Jul 2024 23:12:00 GMT  
		Size: 25.1 MB (25075428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326aab0c16f47331a2d5b0699e05119ed0590b5db7c25f8337364cf58a31cf8f`  
		Last Modified: Tue, 23 Jul 2024 23:11:59 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:8479722a22f196a0f8c40b78b66b775b6a62ee4b1f12bb8ca331f7a5d6e3d790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a8cd0eedcd4b107433a7935b0ffff344b41e3e431a61b16287f50d06a964f1`

```dockerfile
```

-	Layers:
	-	`sha256:d50677fff092694e0a0cb620bfe19c8739b1f6cf6f2a82ec8d859601fa46034b`  
		Last Modified: Tue, 23 Jul 2024 23:11:59 GMT  
		Size: 3.9 MB (3922438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f5859a587054c23163f1955658800e1e0bcff6de04d190143b56cb5c0662d9`  
		Last Modified: Tue, 23 Jul 2024 23:11:59 GMT  
		Size: 17.5 KB (17493 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:6d097ea93d7cda01b1edab0f508d2f94200c5e4391e660c16f6a6aad2b1aa89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53684020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8951bf628d1e4c22b697f7e627be6ca8c474fc699534ddc04de722b46058caff`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:c9cf6ed72c109eb68384476670cda2086783dc0a2ea6379cb1a662b3c8509591 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:de4a305fc1af45cc7ae97020dfe639e8990f6d00b7e0ef222c4cdd720f0fc373`  
		Last Modified: Tue, 23 Jul 2024 02:33:12 GMT  
		Size: 29.7 MB (29669018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf94d6b35849c4e38dfd9727021755e090ca2dbd3b3ee2d4a3678a8b4ef302d8`  
		Last Modified: Tue, 23 Jul 2024 22:45:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9a9c88ab6864e0b8c04a971f18d45d674fba973aa55177b2472d1076e75cb`  
		Last Modified: Wed, 24 Jul 2024 02:17:44 GMT  
		Size: 24.0 MB (24014734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd62bb8def622d2edf1e837aab5cc00af03b3ed4fd8b41fc1fdd42e4dc7d9c`  
		Last Modified: Wed, 24 Jul 2024 02:17:44 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a2f229bf53515e12d51099c56d9139f3c22159cde38055530d259ff265922b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9297c32b5b5aa19965c7df757937ae137f59aca96956eab6a7cef3c7a97f5b`

```dockerfile
```

-	Layers:
	-	`sha256:f53edb45b4cd2033ff2b08b2579bf19548649f1cbec95f8b2ab3e0aa1baa9db7`  
		Last Modified: Wed, 24 Jul 2024 02:17:44 GMT  
		Size: 3.9 MB (3922385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a19b82865b43172fac1db23b42d0d814a839af340cccd776d0f065daa32a5eb4`  
		Last Modified: Wed, 24 Jul 2024 02:17:44 GMT  
		Size: 17.5 KB (17461 bytes)  
		MIME: application/vnd.in-toto+json
