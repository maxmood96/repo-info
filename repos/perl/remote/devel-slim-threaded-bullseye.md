## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:10467ceb365411567c0630020c738bd2c0ffd9a253f9cead15826e2a3037166b
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
$ docker pull perl@sha256:d0a1fb49954e5651151891e41a39172b29816077512d7d51d48fc1eba2537b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56281845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58149abb8a306a17564ae714cce7cfc7aca57371f39f8975d78ca052f65a3a9c`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cbc07f04c6bdca4ba1d1146dab7fe734a7f326b318be4a9a13e2e076e7373a`  
		Last Modified: Tue, 12 Mar 2024 02:07:58 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92472ee939c8e4deca7175c403a087aa9bf57dd8ae4ff8459ab71d3f5cd9f65`  
		Last Modified: Tue, 12 Mar 2024 02:07:59 GMT  
		Size: 24.9 MB (24859093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c719a499383142b2e26a13cd82ba865e1b168e1108c84dbbef79e64c247ea7ed`  
		Last Modified: Tue, 12 Mar 2024 02:07:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:5f06de488df7ab0d1cd2d7f34c33661a0da711b642bc9aedefcd2d196ee17c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8ce53caa53649e623be631f5bcc26365938a8dc1959b77686f89123a81cfcc`

```dockerfile
```

-	Layers:
	-	`sha256:f202d01e9306898ada2e50d184412b0b6723f26835346a2e89d7718a7693efa6`  
		Last Modified: Tue, 12 Mar 2024 02:07:58 GMT  
		Size: 3.9 MB (3912189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40f46daa7438800a1ad09a6b6f462a303b92347f222a01f42496a77b7ed002f`  
		Last Modified: Tue, 12 Mar 2024 02:07:58 GMT  
		Size: 15.9 KB (15922 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:926737e64ed541db2fdae4d1ad4bb0b43e1ef9c8034a7e67533815a138702af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51760399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edd353b82c9030d2baf71474e7de44ad00e7fe1456f3647e458da13d5d9e8b4`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:90e7b77db704f73ce102dcbc0f6cbe5d778409a08ca0d29224ab736a76537669 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:5f50de7913c8d45142222ead3575799095853dd5af08b7c42fe0f070c5947afc`  
		Last Modified: Tue, 12 Mar 2024 00:52:28 GMT  
		Size: 28.9 MB (28924563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b670589f0af3f19325dffd077f65c60d3960566a2b323cde63e6991d391a149`  
		Last Modified: Tue, 12 Mar 2024 15:35:45 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e333d46b156cbf87cf465cd5b8b38b57a6ace4df387feaf227a8ded189c0f342`  
		Last Modified: Tue, 12 Mar 2024 18:23:19 GMT  
		Size: 22.8 MB (22835568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69fb61ca12341bf67adf2b9336e711af2d3475d8f59ef938f53419d56daa78d`  
		Last Modified: Tue, 12 Mar 2024 18:23:18 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:04a6146c322809ae930881bd43b2a1978ca2230a751fc60ee061085c0b0be607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3899205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f2959467da7bfd5e3d03298e57a49db703945f58f22b7e4c16edd1da64cb19`

```dockerfile
```

-	Layers:
	-	`sha256:ed900996363cb54f42d7d3ebdd2d5c5417362969e4bdffd10805ce989490f2e0`  
		Last Modified: Tue, 12 Mar 2024 18:23:19 GMT  
		Size: 3.9 MB (3883388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45229dac8eba6c14469fcbf9dd9397e1c59c078ab05dd7e5d72007f40510f9e`  
		Last Modified: Tue, 12 Mar 2024 18:23:18 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:1a2bed8f827ca47e220f03219786461b7f325abb498aada96e1e4c2273c6b2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48818478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8a78ca38e509aff328bb9a73ec2d6a0d1e9006275cdcdc8b1a06d0c25d94c1`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:f0436b046c7a5f796efae4d2d2be5a99ad212807e4aa49fc8cc372a4c4c8c4b0 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:5b16029f28c496dabb357a7310d24f957046a925411ccd44eca962c03f85e38e`  
		Last Modified: Tue, 12 Mar 2024 01:04:23 GMT  
		Size: 26.6 MB (26582714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475c25e9dac719893224a1cd5c8dc1762f32d0d860b64613e5a47f29710b6baf`  
		Last Modified: Wed, 13 Mar 2024 01:25:53 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716251fa8b521657cb0d255b61cd5cfd977b801a6816e73b91f863271f299673`  
		Last Modified: Wed, 13 Mar 2024 05:31:41 GMT  
		Size: 22.2 MB (22235496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dc7ece0f797a771329382eea0490251c1e1ef90be2c3b6bb18fac2dbb74d28`  
		Last Modified: Wed, 13 Mar 2024 05:31:40 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c497898b1d5e50f96c40d36227e2bddcde0767312021fd25fcdb70a642d595b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3901922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e07db37c62ae93898fa04db510fa274eaf10dfde5a6e0cf9bab41087f4f944`

```dockerfile
```

-	Layers:
	-	`sha256:d85fb942136d571728304ad2378c4935fdc61ec9a23ccbebe6caf2b4f1628227`  
		Last Modified: Wed, 13 Mar 2024 05:31:40 GMT  
		Size: 3.9 MB (3886106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e2deaf93dc0c150f209ee338136fe9320133a81d8fed6396e3a38c867daf4a7`  
		Last Modified: Wed, 13 Mar 2024 05:31:40 GMT  
		Size: 15.8 KB (15816 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:736f8eb53522ac79878992a5a925e257be8f426c0fc1424ab9b9c38542b017f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54043078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e422c065c64e0d0a1c1ae31fb7b3116f7c9fb8554c441d5b79460bcfd166865b`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96543ff7344cb637d3f3562c307cf897cbc222515d013ea586c43ea451f17a55`  
		Last Modified: Tue, 12 Mar 2024 23:07:19 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecf706f011479ca59e308afbb2b09027a6a2fb48c9d7870c52e88a297f319f4`  
		Last Modified: Wed, 13 Mar 2024 03:51:38 GMT  
		Size: 24.0 MB (23971693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea0a1882ffe156edb9cffd03468361cdbe25335723febf711872e2aa8849e40`  
		Last Modified: Wed, 13 Mar 2024 03:51:37 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:aba697f6f2a2e0912e6e0972b5700b0c2d2fa079a19b92c76bbe268be22d6bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3902267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb5b3b206cf67d02d15cdfbbcbcf0036aab0e9b653bc14c0519c2a340da0d95`

```dockerfile
```

-	Layers:
	-	`sha256:e52622bb01b96afee6610d32e6ffeede0993f52a58523425c46e96c443e424f0`  
		Last Modified: Wed, 13 Mar 2024 03:51:37 GMT  
		Size: 3.9 MB (3886505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29a835d1bfa1356a452ab4a9a9164cf5d5754a6d436e0935eadfb7c0e4cec324`  
		Last Modified: Wed, 13 Mar 2024 03:51:37 GMT  
		Size: 15.8 KB (15762 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:2c721f076c7d1e2708ee58f45499109008fa995dd296570270e89eda413ce2a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58734088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af8799898cb8fcacf71bff24e103adf97d65b67df8913b5f24d3fd39c544c10`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:515cf6a96eea91239bc61e64b973eb555a9299d1053e3c6cb694d8bafa627086 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:4276507bfa4980b432cd9334306e3335cf1bbc8e6dea45aad2ae9ec091223f03`  
		Last Modified: Tue, 12 Mar 2024 01:03:30 GMT  
		Size: 32.4 MB (32407589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06336cc119c14380b2a741bf21dc3f3fa25d36779e6d95e93161f33178323fc5`  
		Last Modified: Tue, 12 Mar 2024 02:08:51 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63a1d440c426da459dd10418af639685abcbc2f89ab75f804afd13d1fabd59e`  
		Last Modified: Tue, 12 Mar 2024 02:08:52 GMT  
		Size: 26.3 MB (26326235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5949b2168a5e763f3242a681f8e791952d5da3693b1fcfc4a901be37d960a0b3`  
		Last Modified: Tue, 12 Mar 2024 02:08:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:75442b8e775c5693ba56bc673c398c0f3e94557ce0f09b89f60e813310cdcd4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9978c45c564d7d91a66a93866f59db035aefb60c2f9facdf08538b0104f2ca68`

```dockerfile
```

-	Layers:
	-	`sha256:35a735848a306e46dea9d79dadc19b3e8e4fa9e225bf3b24dee2377a5bc22ed9`  
		Last Modified: Tue, 12 Mar 2024 02:08:51 GMT  
		Size: 3.9 MB (3916452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec3a84f382d3129dccc05859831f49a26c4aa5d86e3e09472bd6fda2a34f8e1e`  
		Last Modified: Tue, 12 Mar 2024 02:08:51 GMT  
		Size: 15.9 KB (15898 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:f8d406e9780f0a789c6864bc2cf946c3cb217ab42ee9a75c92994e46f0743f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53410510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0f99c1f8f780f9afcd1db4e820ed25708a80bc086ce2010c0439012fa47dba`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:a42bb6c1ce6dd3579b82e6f04b91787c20ac276a10c0bc36d42b2b260789343b in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:ade123ee9f81df730fd8edfcb3e77a2032d0f4380f0cb466cccda650f64f9560`  
		Last Modified: Tue, 12 Mar 2024 01:18:36 GMT  
		Size: 29.6 MB (29640502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f6117b377a412f78d6343911ec533a23e82b770b04947782a3da9f6175317d`  
		Last Modified: Wed, 13 Mar 2024 05:05:10 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9aeecdb4a5be470331c74992985a5c58fc9bf8cdfe4e45b318b738e8332bb6d`  
		Last Modified: Wed, 13 Mar 2024 15:54:54 GMT  
		Size: 23.8 MB (23769740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12e3b1ab4bafb72f55a8408e393a30b517a2fffe01c089375fd7bb79617129a`  
		Last Modified: Wed, 13 Mar 2024 15:54:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f217246e79c24954022d4fc494972cc5646be4eae4edc61168a65088a38aa6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52122b32a4da08d1a47f1689e6bb83fb59404c83a51e132e4c19160e2596fe88`

```dockerfile
```

-	Layers:
	-	`sha256:04c66f65415811fde2d4f0ca065ff8235d8e8c476379ee8db2b961fc1a90873a`  
		Last Modified: Wed, 13 Mar 2024 15:54:51 GMT  
		Size: 15.6 KB (15588 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:6a192e043452d02e69fe704a008b643552c6894aa80e32bf0ba991503874b916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60436331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0918005b633953a71a9c6d99058c2880c1bb17fdb5172143f4b432ce3d5d0339`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a7e7152ecf714cde62c8fd8e3ba92f1a840753d61e7dfc0d5e581ebdc5174b`  
		Last Modified: Wed, 13 Mar 2024 03:06:31 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89dc91c56a5f10066a94181160f28ecef44a74148897d93857e2c51154fa3e6`  
		Last Modified: Wed, 13 Mar 2024 06:13:16 GMT  
		Size: 25.1 MB (25138055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8d52d28ea1abe6aaf07b43215edda130f292a79f3a79289da31031a7fcb5f5`  
		Last Modified: Wed, 13 Mar 2024 06:13:14 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ac524a5ec68d341dab88ba32b7fd2a6080eeb0ef31c2088d54dbac88f8bbfa38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91f782ad2cb85b08e4153f581ad1a41218f33f0ca7287234205d69fd2b43e34`

```dockerfile
```

-	Layers:
	-	`sha256:18d4e2887756f9ae2443c65fca55a16cc0b5a2c673dc8480f72833dd1bb9db53`  
		Last Modified: Wed, 13 Mar 2024 06:13:15 GMT  
		Size: 3.9 MB (3900946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0a1bc8674fb6a948ff275a340e3073c31600b29996d4aed354e5a1e59a33c99`  
		Last Modified: Wed, 13 Mar 2024 06:13:15 GMT  
		Size: 15.8 KB (15787 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:a072550b327d7b868ae4d57a080e974e4fe90c7da6e986ad98ff1c7b6511359f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53738824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d2886f29cabb8a050aa8e5e62e221158c01e0f2d5be802e45249601bc9db16`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:e121f5164f2335792d17befe564e4a4caf1dec33d5039c8245ce418144782215 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:840335d52e6c781c13aaaed8df36659831a5cb0747048da9bf578dd19a02b30e`  
		Last Modified: Tue, 12 Mar 2024 01:21:45 GMT  
		Size: 29.7 MB (29660245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d59044bd93597378fab38b4497e1310cc4b774711d2793ce0dfd9ab2a08fda`  
		Last Modified: Wed, 13 Mar 2024 18:10:06 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bf54a538e3ab1b70724a6cfd6ce9161031c91d664f433e1663d86cff8f3662`  
		Last Modified: Thu, 14 Mar 2024 04:01:33 GMT  
		Size: 24.1 MB (24078310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d5efc947e43f4bfd3ed9cc071f11e955098585dc2a855431c21cd707288889`  
		Last Modified: Thu, 14 Mar 2024 04:01:33 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:35d65c2d7facc20e420064d520c529ddee78d5641e912cd4c09a0d6b22e848a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998c0d18b5345f85a77f7dd0627cebddeeabdc46a371d83dc63037cb3e371c1b`

```dockerfile
```

-	Layers:
	-	`sha256:a34b4f61d19869ceeddf2d7af84d85801a8fc8f4224e0888211d0d662d027655`  
		Last Modified: Thu, 14 Mar 2024 04:01:33 GMT  
		Size: 3.9 MB (3900893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8850d9bcdabe25cab5d61475f9f391e5c89d2816cf75f8a8ece8573674a460d`  
		Last Modified: Thu, 14 Mar 2024 04:01:32 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json
