## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:ab27630fd984dd2352d40a02e613f70f40425aca639e453cd68e66f8adc0cf3c
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
$ docker pull perl@sha256:a009fbc4d2b533f412a0614dae64d0c5006a41480fe63156eb761854fbc80f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56268765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae44fae1457b0b7ef1b95ad0bf9797d45e03f86d3a00b5ecb566d9cbcb3b134f`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceef40ee441c4f755f406565ae248c87ee9cc2e87270a8d7263a9b8a613b4951`  
		Last Modified: Tue, 02 Jul 2024 03:12:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efceae6fe2b592f9bebb5f7aafcc21f65f42a2bddf0a5469c1d84d2476429f0e`  
		Last Modified: Tue, 02 Jul 2024 03:12:22 GMT  
		Size: 24.8 MB (24846214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aa6501b09bc54bf25dea004c6257d51d94f6a9cda3d341b5ef4369a1a7e76e`  
		Last Modified: Tue, 02 Jul 2024 03:12:22 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:4110661ef4c65a4cbe7b581085e1700ed877eeaae410a885eabc47b65f47023d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfd7cbf01b4028ec305124a70e53790117dc197606d34fad9ff96b4819a006c`

```dockerfile
```

-	Layers:
	-	`sha256:40614a4805fa9aa9bb87756698c11a2a232b7bded53ae5314d1dd594978f977b`  
		Last Modified: Tue, 02 Jul 2024 03:12:22 GMT  
		Size: 3.9 MB (3912311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6cb0200763f354eca1e9ae533d0dac934bc6fd3b0023d138b4b6924df04c6ee`  
		Last Modified: Tue, 02 Jul 2024 03:12:22 GMT  
		Size: 15.7 KB (15722 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:fe7629a9e7462acc7e7b853a5174e29eba5b1eeb8484508e9e77648ee682468c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51782177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03477d55cd4623dae826edb8f10cfeb69ec7d7cab934d7be46b519b3c4b67482`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:7b150e5fe9a4f014196e0bfb8275f3406ad543dff58b049264b54e2e00f392b5 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:63678471745dce46512f823fc94716da7f08aa84c931dde61ae18c67b55c3085`  
		Last Modified: Tue, 02 Jul 2024 00:52:13 GMT  
		Size: 28.9 MB (28924714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6249820aaf5cf5a046193345d86b89a60b857d4639ac3c4dc68ecf3bea8403a`  
		Last Modified: Tue, 02 Jul 2024 13:06:32 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84af4747ece3529bdb8309c57374d644dd8cdd2620eeec3f62236db59a3b030c`  
		Last Modified: Tue, 02 Jul 2024 15:52:18 GMT  
		Size: 22.9 MB (22857198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8001daadcba4ca9ed9774bedca73f9d9ecf3fb58783679b7c8908c610b5db`  
		Last Modified: Tue, 02 Jul 2024 15:52:17 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e924d65e5a6a0a24cc3815c1e2c900b890d4d9dcecfde451293224cd20d798c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3899292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59483e9ba1ab4ee2f63b6599c59ae8f324cf3de125831f854fb599f3a8d071ac`

```dockerfile
```

-	Layers:
	-	`sha256:58e9ddfb81795ff682013470ebc86d2a904dab0b8f2a239ef4fa94d5316569ed`  
		Last Modified: Tue, 02 Jul 2024 15:52:17 GMT  
		Size: 3.9 MB (3883508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5859d6180f92c17b971b7dfdd0ac4e3de597a53c23b688f74ef72a4eb1b7248d`  
		Last Modified: Tue, 02 Jul 2024 15:52:17 GMT  
		Size: 15.8 KB (15784 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:1f0eccee9676d77f017df9b1cede02cd30d721a081483ef1fd64f58f4b294bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48836121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec990131af6c298edfb2176a32ecf5445e9efb911a3072261935a9354cc4d40`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaa4e63812b42f79340110dd1d76be50aa50dd1506ad2bbe3a4d7de62aa2c8d`  
		Last Modified: Tue, 02 Jul 2024 14:15:26 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db76d1993ff3efc9d9ed525c0edcbd7bca24e707c3766855810b41c78affa5a`  
		Last Modified: Tue, 02 Jul 2024 16:54:16 GMT  
		Size: 22.3 MB (22253150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c9adb80df0961b8ebc7249b7b6d4d56d90f18017159d2319463888d01d1e9f`  
		Last Modified: Tue, 02 Jul 2024 16:54:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:56b81c3b4923902513c2212857310f9067118c2057a42ebc30272b7446ede730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3902010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4032ce0eb7afc344bbdccb9dae4ae0ee0cbac802799909509b7d193723537da`

```dockerfile
```

-	Layers:
	-	`sha256:80bf5a6442095f8b7d3764f65dcd1dcec203089c5dcf5b4d3a089096df839962`  
		Last Modified: Tue, 02 Jul 2024 16:54:15 GMT  
		Size: 3.9 MB (3886226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:115cbb574b2224141914751b3f7a5b0028e4c581dbd8d53044706379488640f5`  
		Last Modified: Tue, 02 Jul 2024 16:54:15 GMT  
		Size: 15.8 KB (15784 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:f7c1b90c6b54fa461af19d82419ce926a5321d1858194d941e12d3be4366f684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54051673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1af6c5804552a82d22369f9db4f83ca9cb35f2687f1b2fef00c68f3e59fe85`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89704e0bd161cc385ea2d359a2d5a74a86d07488f522a94706b4f744779ec94`  
		Last Modified: Tue, 02 Jul 2024 17:00:57 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cc65911ff530dea7460e6d1752833b70ddfa3efadb2e48e142e700a3d153e9`  
		Last Modified: Tue, 02 Jul 2024 19:07:58 GMT  
		Size: 24.0 MB (23981793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549fde5bae4d2b431711e2829d96ec1aa601bbbab0199841aeb06cf310d066bc`  
		Last Modified: Tue, 02 Jul 2024 19:07:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:61109ba5eebf89fa7b448415fb77b59573c91797352f017fe38405a4b248267e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3902679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92fb515c1833b2d3ef2e7a10448607a7d2218be3815f484c29cb932d051e85c5`

```dockerfile
```

-	Layers:
	-	`sha256:55828ee259f8f2f6664fbe63a20e2643fb38cbf69d09de9f1bde1864ceab7383`  
		Last Modified: Tue, 02 Jul 2024 19:07:58 GMT  
		Size: 3.9 MB (3886660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588c641489358726ed7a6af174ce8347d9f76a26c2c7e24f7729f7e024978623`  
		Last Modified: Tue, 02 Jul 2024 19:07:57 GMT  
		Size: 16.0 KB (16019 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:b24b7b46bf7b031c7c2974ee80ae636427ebe4544e41daed637f3da81ae523fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58679510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa8b7c66d79a4b72f9b59a22d907f0b0fa5a90f6b54f9dbcb2f42360006f5b9`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974c8c3365ba7668e6213beaa30ac73851945fc04049ea10b49d43ed2ba9d9c5`  
		Last Modified: Tue, 02 Jul 2024 03:12:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bad7fb1f82528810a14cabb179a4928e2e20785432832e066dcad02284bee7`  
		Last Modified: Tue, 02 Jul 2024 03:12:57 GMT  
		Size: 26.3 MB (26270794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb887e8f63ed7262bc578c56492346bad6fb7016a8178d288eabfe8e0f849f0`  
		Last Modified: Tue, 02 Jul 2024 03:12:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:714c1b8e2952035a6da7adf2f75ad4cf65f41ebbb13ac0d8a713f3aca345d27f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d368c5b6650c63d196ec869d12a08c93bfd62817684fbd7be9ce2063c063e70`

```dockerfile
```

-	Layers:
	-	`sha256:02dc8f0746cace38a929f52c6528474921958ef1c2d8c6f709a213c12a48e92e`  
		Last Modified: Tue, 02 Jul 2024 03:12:57 GMT  
		Size: 3.9 MB (3916572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cdfce7683fc55571b9de3582de7941f1acb0c526a3599019cf86cf28cf7f1d2`  
		Last Modified: Tue, 02 Jul 2024 03:12:56 GMT  
		Size: 15.7 KB (15696 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:66c2e86dac48593713c03ded6ad7aac350139e0caea41f0c0c58ba7ace615bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53394395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ad25c21baf2e746d59bda118c5bc343dfd8139d6645586bb99fa7ba16e09bb`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:791d05eca72cc81080afbb76c7f3f02a74893142203b6aada9e3170404049223 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:59602b870d8ca1e13dffda9de0c5f866f86ff35c1e595ea481bb1b2c48c18b8e`  
		Last Modified: Tue, 02 Jul 2024 01:30:52 GMT  
		Size: 29.6 MB (29639850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215f042acc444f97af1cc88b6bb240b24b5bbcb492e3a2838ad1d8a5e29b7a6d`  
		Last Modified: Wed, 03 Jul 2024 00:11:33 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98070c2e65dd1195999764f823028dcc4a48de3615160d3154f47667b40cb53a`  
		Last Modified: Wed, 03 Jul 2024 05:37:45 GMT  
		Size: 23.8 MB (23754279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23bc8ec1ef4263098a2c680c8f5b1afc62801004b43289dede8ef88dc6f2f5`  
		Last Modified: Wed, 03 Jul 2024 05:37:42 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:86d77c96a343e38da64c46eff18b63fd9f7ac0b85a499bfabd795548082ed3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbea6ef7c1b1f15645036a37599ba7fafbe6e6cad7a05b2cf7fc9ea5c0d3ab07`

```dockerfile
```

-	Layers:
	-	`sha256:294e3462b93d27823c4e9f92c1a1ba15bbdcd7e27709208a2720fdb2186a8913`  
		Last Modified: Wed, 03 Jul 2024 05:37:42 GMT  
		Size: 15.6 KB (15550 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:92038ba7df4cf0d62e52023abae090083b94b50ca135a72c441a3d0fb6281fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60397313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4150f10bf8c712a82eb80b5460ac940498f45a5f34e2309ca82e3d104e6139`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:8fcbfde241e9377ada40ad73089516c86d20e018c99a8192ba63a50f0168b8b9 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:687d52b24394339ceb9470debd0e5f0d6b612ceb063cc228cbef23d23fb7f6a2`  
		Last Modified: Tue, 02 Jul 2024 01:22:46 GMT  
		Size: 35.3 MB (35299189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f338afe8b7bcff70cf7ac67a6d0ed8d4a149c0bcb998daffb05f9240f9c9767f`  
		Last Modified: Tue, 02 Jul 2024 12:18:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11827d1ac944e2f3b7d528e5604ae80a4d35c1812987a973c8ec07ed7c959f54`  
		Last Modified: Tue, 02 Jul 2024 14:52:54 GMT  
		Size: 25.1 MB (25097857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8007739768ec212b4d55e2d875acfce477959cd19535f9f694a7a732654cfc38`  
		Last Modified: Tue, 02 Jul 2024 14:52:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:d300ce090f310c993cbcdeaa80af46d43989842475d89c02aa8e2d225f0e4ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc4462d6e9cc16afee3ba516322719f0e256542221bc17c90fa73811b36f033`

```dockerfile
```

-	Layers:
	-	`sha256:93dbc6c47f0d34465cd323723a271cfddb5987d820402df8e5ae39d02fe62ff8`  
		Last Modified: Tue, 02 Jul 2024 14:52:53 GMT  
		Size: 3.9 MB (3901066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb458c68c165e0dde8eb3129ee73f743917b7737ad80006fd7e5f2e1b5650135`  
		Last Modified: Tue, 02 Jul 2024 14:52:52 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:33c1feff8efa6538d12e7e882d48a250d5a681870a2319f05c49a085824c161b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53729832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48837d810d6a9eed4853b5d5eb5a595f342cf52cc00e6d4cac115547190656a2`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418e7299459b433b529500afcc74654f060536e29945c6b2aee43d84c25fc28e`  
		Last Modified: Tue, 02 Jul 2024 06:47:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ddf003f9e7f675a1aca3963e0f3ffd6a94ec4df5517e8c1b8042c1053bf10ea`  
		Last Modified: Tue, 02 Jul 2024 08:11:34 GMT  
		Size: 24.1 MB (24067214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df3850d920f429057127b88626f844e31dd9c805b102ff9526c6800eecce66d`  
		Last Modified: Tue, 02 Jul 2024 08:11:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:19e2230049b53fb04eb9bfe89cb9f8895bb3d98258ba3a795235ce4e0243dac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb22beb7d82d0fb855179097b30dd9469acc4e656903506b1f706bc09815f4f`

```dockerfile
```

-	Layers:
	-	`sha256:05df499da26f08e54650a1efb4f30b60a409c263ba4012fc219f3a4c787f2bd6`  
		Last Modified: Tue, 02 Jul 2024 08:11:35 GMT  
		Size: 3.9 MB (3901013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00426d3b595855a2b11caae86a3573834d92896c5c561b2225f63b79b83b71f5`  
		Last Modified: Tue, 02 Jul 2024 08:11:34 GMT  
		Size: 15.7 KB (15722 bytes)  
		MIME: application/vnd.in-toto+json
