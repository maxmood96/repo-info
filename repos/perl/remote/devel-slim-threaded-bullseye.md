## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:b04e627f1c05275ca0ba895726dc7fc043bbb1b7e3151017b80142fe7a62efd6
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
$ docker pull perl@sha256:985de58c7b5d5a56dad1c1e036616d29f3e741cd683e8f365e00a28b5e26d64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56117857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2330e4d7c8082fe959ca3c950a9df5c7fe0e3d47c0b8b05a276b21aca7248dba`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806d58e0444c2e75f4b4e07691096e7368ab68735e81630e7c90dc0414669c16`  
		Last Modified: Wed, 24 Apr 2024 05:04:22 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c380ba8399bf5c7eee10a6829b21fd477fe2fdc6b1ce85655b624cb96e3f7fc9`  
		Last Modified: Wed, 24 Apr 2024 05:04:23 GMT  
		Size: 24.7 MB (24683327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eda6d755194036854f20c9f86fa198cf7f1aea9913827604df618e74fb130ed`  
		Last Modified: Wed, 24 Apr 2024 05:04:22 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:264924794d47f971f619c8343370279c6cdad0d62a8f15e75f37a808ff9b72c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6fba7c23a832d1b98272d91e50110831d7ce4e382651b5c2e1005c3433ab07`

```dockerfile
```

-	Layers:
	-	`sha256:35c5fb2792bb7164804e4b309baa888f49f41f3f3d8a415a468179ac461fe090`  
		Last Modified: Wed, 24 Apr 2024 05:04:23 GMT  
		Size: 3.9 MB (3912349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39a814ba00402a3b4229023da2b38eae6b51317a02f7f23b6a4c909707822ad`  
		Last Modified: Wed, 24 Apr 2024 05:04:22 GMT  
		Size: 15.9 KB (15926 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:0f71bc59bb153ac18dba87726c4ea506a452e81aa58b6d065311a536ee39c515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51613798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f300676d9ba437a0a14eabc56e86890b9cd3059279f6ae545893503e7e85e39f`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:4ccbd1f9bcc76d259ba2b235681f1b749e86690e8805ee49f9fb44abc9ff5dc2 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:2438f3883cb848a901cb08a6c99ec3ef261d41ca6f0d5321f274d995c58fa24e`  
		Last Modified: Wed, 24 Apr 2024 03:57:14 GMT  
		Size: 28.9 MB (28936577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a245b2574bb51828f8fdb8c09eaf2db112a669383430da943e9d18f17441673e`  
		Last Modified: Wed, 24 Apr 2024 18:01:21 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c4e7b50609d731020c42cf1e8562164449f03c87d36e6a33bd6a15a3037fe6`  
		Last Modified: Wed, 24 Apr 2024 20:55:04 GMT  
		Size: 22.7 MB (22676956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70853eed4fa62b9702be9ddff53689830ccf61cd94db330662bc1c4f36e69625`  
		Last Modified: Wed, 24 Apr 2024 20:55:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:96e4a36045db0268d2487d7f0fe6af32ff27e882928c8ca003407aa70ab50847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3899367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3b5d9e571ed50d99eeb7abaf860bbe8c2ae184e7f2ee5f54694eed28c6b693`

```dockerfile
```

-	Layers:
	-	`sha256:6e948fb608e3439ecde45cb3bf2d34483f7a8b23fd7dc61d293d442f1b988eed`  
		Last Modified: Wed, 24 Apr 2024 20:55:03 GMT  
		Size: 3.9 MB (3883546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b23f541a2adec43ca4b9c3298552212d8b980ee90c8ae996539e6afd2cc2ae`  
		Last Modified: Wed, 24 Apr 2024 20:55:03 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:91b830dcb5994636fb27ce9747f3ecdd741b921f71aed18473f1fbee9b676218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48664767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac991cd3a83c257b7950a393020c0e65c025575ca4e4d4c012b174480069523`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7425d50c9183b9df607555e696ea81e0d344ff1049ad33cefdd571b8619f538`  
		Last Modified: Wed, 24 Apr 2024 17:12:43 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3810fdd832224c5de2699c53b364475def56061b8dd526cf6cc83aa1710bf1bb`  
		Last Modified: Wed, 24 Apr 2024 20:28:36 GMT  
		Size: 22.1 MB (22069760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e85044e57bd110ecb140cd5f775902cdda42b05dd748b40c90e89b7691cc4a`  
		Last Modified: Wed, 24 Apr 2024 20:28:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:34ac8e6c4a8d4ad1b87731eaae7a6803579dfebc2763e17ebe75d9615594ec6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3902085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf875572a3ff7f905668aa90709c1b8da5a1211f8b5fc177901ecf75751927a`

```dockerfile
```

-	Layers:
	-	`sha256:1528a2cf60121762c1c8a3f858f0c97aeed17f81530a1e1d7764e9fdd43342f2`  
		Last Modified: Wed, 24 Apr 2024 20:28:35 GMT  
		Size: 3.9 MB (3886264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25eb76d8e1715122e48188798aa8310fcc51502f05c92948b805636201f4f106`  
		Last Modified: Wed, 24 Apr 2024 20:28:35 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:b396fe05ab1764d5707a1f3cb61477fe1ec0ab74a1222b219c73d7cc0c8029a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54082759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1d6802e406d70e67a72c0672f84f1091b5b5ce5b15b574b2f68b80f95d07e7`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97589b9c1e05cfd5dc329dd026bcd71c9ec1abb7515b2e3668cc29eeacdd4744`  
		Last Modified: Wed, 10 Apr 2024 17:10:20 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b6f32cea59ca2bece515e52126f074767e17aae57afcb99d9d49ab058e1b5b`  
		Last Modified: Wed, 10 Apr 2024 20:25:31 GMT  
		Size: 24.0 MB (24006186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41316b6b786f6dd6cb0f4b2cb871351a5d2da32d54af6967f15b4d997fb1e0f5`  
		Last Modified: Wed, 10 Apr 2024 20:25:30 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:2d793a690d9f6fd8f5b876b15f4b48ee214cea90c357aeb821a7f361926bb0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3902268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1adc76257945c5d88aa24771b2b145129a8503a2626c4fbdaa44f7947fe0a94`

```dockerfile
```

-	Layers:
	-	`sha256:6b5657ce6ac46cdee05ca56747ae5bf339d39ea5b06724a61d694bc9e9ea041b`  
		Last Modified: Wed, 10 Apr 2024 20:25:31 GMT  
		Size: 3.9 MB (3886505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fed4ea20fab3647772c47a0ec40d5e571bd9e20308bb14743ddd5485321f65ad`  
		Last Modified: Wed, 10 Apr 2024 20:25:30 GMT  
		Size: 15.8 KB (15763 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:221e1e7e1a8f8b67a73ae08d83e333630e0d5080b5a920a52ee563bffea45bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58571251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b161e1e095d7cdf2463b740fb0340333906d2eac40d33be14f0221eb53f64fa7`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aaae4302272b82eeb4642541f02ed37535047711cd885387f08cdadadb59c0`  
		Last Modified: Wed, 24 Apr 2024 05:05:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdeee3e187a60923a2656a6187d8ec448c9d4c584d8763bc01868bab75fcf89`  
		Last Modified: Wed, 24 Apr 2024 05:05:09 GMT  
		Size: 26.1 MB (26146210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe578f963c394c75b6c83e3c9d88954c2610845423f778badf9823cedf9af56`  
		Last Modified: Wed, 24 Apr 2024 05:05:08 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:d6121375d8941639b783b8c4ece27e941e1948d6f9f7e9e8e8efd8b5e52612ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e582485cbc713e6e6a9534e01c8511a98cc052fafe93818747729ce53f7742af`

```dockerfile
```

-	Layers:
	-	`sha256:78458ac7753da74c0d8eb251fb6110cb45b770e98d8a70eb3bf68ca95b82c449`  
		Last Modified: Wed, 24 Apr 2024 05:05:09 GMT  
		Size: 3.9 MB (3916610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0c47394db963999f26d9c192b54688aa7e60972e0492302db36284d9818eb1`  
		Last Modified: Wed, 24 Apr 2024 05:05:08 GMT  
		Size: 15.9 KB (15902 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:df7685feec8c9fa8d2c6631fbbed1b53403042d34e47acfbf7901d311da4999a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53449253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7be2b0df57c06215ec04f1329fbd1bd44db84c13584fa0f6d3178b40c9fc51b`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:5a3b2305df619d313e2592819c382781fd774d11c3f687bc9ca004eba259694b in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:94315f37c06e4616cd911d9cfbe5597a620ca0249447454791c232fa7b1e2724`  
		Last Modified: Wed, 10 Apr 2024 01:23:22 GMT  
		Size: 29.6 MB (29645932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8719486561701d393fe94826abe7fb84d151c4ba63d7d456d16237a9b93712`  
		Last Modified: Thu, 11 Apr 2024 03:18:40 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1070a4417db2e8ebb16492649cf27030ee31a2d1e9e0cfb9aa50718199a07180`  
		Last Modified: Thu, 11 Apr 2024 08:49:10 GMT  
		Size: 23.8 MB (23803055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13ce3800569cb025c35183d1a49267d89d786861ad86521e54df751d950e65c`  
		Last Modified: Thu, 11 Apr 2024 08:49:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:78e58b9c6e15e6d505dcfbd454bc1cb0fdef15aea5ed61384428d9975bbf7ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d5ecf17ea943d4e7dbbc1a9219dcd82a47dea1d8d4df5487d1cdeb7ad88d3a`

```dockerfile
```

-	Layers:
	-	`sha256:19d836b5e56ea84d0c5ae91facd1216a6a3e2fdadbe4703aa92c85bbe7c6a20e`  
		Last Modified: Thu, 11 Apr 2024 08:49:07 GMT  
		Size: 15.6 KB (15588 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:fef05af0e3df453c29105e983378456de8000e0ee1f8cb4b705cc33bf4986acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60479804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e400a81cc5d5823e6d7c39f9e75fbdfc8f4dd503e442c8d765d42dee6cb95e`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:33f8251ee78dc536740a4ab4a9c9a75ab2c3f5d7be0a41f41dea318cc8e93dbd in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:2608681ad30ed92fce8f1b566ae32649b5bfa30cc4df8792977ed14a0bc7cbe6`  
		Last Modified: Wed, 10 Apr 2024 01:32:01 GMT  
		Size: 35.3 MB (35304089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5ebc4ebb4a8c723d56615d399ebb3da9edfd79b18901a9469f826dfe448718`  
		Last Modified: Wed, 10 Apr 2024 19:46:28 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56551dbe03a2c5a43ae5c02cd8665e34c916c90316da192b992f8d167da4299`  
		Last Modified: Wed, 10 Apr 2024 21:24:29 GMT  
		Size: 25.2 MB (25175450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c0453bba0393aaa9474f25e339e9ac0f9856064f6132e2677965acca38be6e`  
		Last Modified: Wed, 10 Apr 2024 21:24:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:162ce720c3ff5304769acd158810453d1918c54210c95ae2f2b7847017f2b05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf33ec79fc480be5bd76dde8e296b8d9e1d64a36e39c94f9083786bb161da55a`

```dockerfile
```

-	Layers:
	-	`sha256:7866af499954b76697086b8c332aa0c1fd1ad7f09d124ffd5fd9448734ea6de8`  
		Last Modified: Wed, 10 Apr 2024 21:24:28 GMT  
		Size: 3.9 MB (3900946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5655628e436c245ec849b99d3802c8931f653ece5dc3d760308df24283d44c14`  
		Last Modified: Wed, 10 Apr 2024 21:24:27 GMT  
		Size: 15.8 KB (15787 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:2953811a3e02918aec579154c302b24f4fba7bfa3c1d0c92509d6869e390b538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53767724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1387052810b9f28849254ac89c937b401b13139d6a253e3fe3809f8922f3eb9e`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:173b309178d19f7fccea713c7c575233510e5f065fd2d92a5378f001a1d33846 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:499f72f2d94381b6df4b58d8ad4918f9e03fc5d140cb0704842fd78e2e63e391`  
		Last Modified: Wed, 10 Apr 2024 01:49:00 GMT  
		Size: 29.7 MB (29666840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3902f37440d76b4aedb5ba4d46bf8d324c3a634c4e20575f2d365a2f9180ccd`  
		Last Modified: Sat, 13 Apr 2024 05:58:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2ef0f5e8852c00b2e6d258985f8be60eb026aede8c287459b072f6ac44138c`  
		Last Modified: Sat, 13 Apr 2024 13:03:42 GMT  
		Size: 24.1 MB (24100616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9742c17bdd3a97a473b5453fcf8b91936581397d7408c6c5b62d8c82a7a6389`  
		Last Modified: Sat, 13 Apr 2024 13:03:42 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:47294d9c9a21af2ff025c117c9ae89244a6f742910082f00aa4f0ed91a3a5d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e03381f3f93d9a27738f48f0aca43086bd9e207abd66526785ff412292dde1`

```dockerfile
```

-	Layers:
	-	`sha256:03af3c006bf855fe6175d6087721a4005236d840c36082a70de86577e36b8936`  
		Last Modified: Sat, 13 Apr 2024 13:03:42 GMT  
		Size: 3.9 MB (3900893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37e31475b7c754c5ec42cca4724f3aa8db09ce1bee48f70b02b3d330941411f7`  
		Last Modified: Sat, 13 Apr 2024 13:03:42 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json
