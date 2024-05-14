## `perl:5-slim-threaded-buster`

```console
$ docker pull perl@sha256:e40b6dba56621df8bec9d420530cc0053a8c2b053c803aa90f55dce377f559e6
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

### `perl:5-slim-threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:68c21e307c9444c1a4ce59778e52c49cd0b34a6db4d3e8dba6abee7b5821f328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54728632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e4d64f3212de8732f98205e72252435a58b912e23c3c0b74af2408cacf2b14`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:ea1fe4f19165d885a1f3d523e0ebdcc3e863e6b93717c8022529edb674a52e2d in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:6299ae3fea5d052b297d91a57200563362b8f2c95358c6e3010d6fa3ed44e7c4`  
		Last Modified: Tue, 14 May 2024 01:33:45 GMT  
		Size: 27.3 MB (27337664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc69cf4e72328fec9b62e4602f055e2ceda65ede9170b869c64badb4d2ed5892`  
		Last Modified: Tue, 14 May 2024 03:03:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38c99f1826713edd41e983afa2430f1b7584d7a5279fad89ef7804981ce3e82`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 27.4 MB (27390704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f83c451a70651071301ff49c8b41c4db07df24625753fbad649d2f69edd1a52`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:f8c4a4c2c4598e8ee0bec770f42abe54ef7ed67d99f8e684b5801d9a1abc0c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a63ddc6ad56fe5588eb53ef9f372ff6b8dee23553adb6d69d6990d9d4270eb`

```dockerfile
```

-	Layers:
	-	`sha256:b5c11741f11e2100b5c81be98a305a1cbf46beb97ead16554d69e646f6bed07e`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 3.7 MB (3721604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b26985cd2eb9ababcde5205b6b1ee8f663fac4100bb30847af59e023bac27f6`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 16.5 KB (16482 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:3a21959636515d3c6e3f3b14bd8ae6dd947e243c4a527968aeede11ef4dd946c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46876843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65db9bc73b1dc537095a46e54160bcdfa3338beaf281d7b1213b150c9e1e9d90`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:e48e4c164cd443d649cca91f392a3ddadac422905ad4f48aca0f47eb2243561e in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:30a8958fe0d5b6c3e6d6c11772c14c4b85029786ca86968f09e078645df26b2c`  
		Last Modified: Tue, 14 May 2024 01:14:02 GMT  
		Size: 22.9 MB (22944934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3302b6eb2b02d477c3be352a2aac53a866176bd72676bb7b56d2b5233e6b21`  
		Last Modified: Tue, 14 May 2024 14:35:58 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51d27835872a81f9d5620e12ba3b8be633a846c44a9b58c55c5570d5e9ca716`  
		Last Modified: Tue, 14 May 2024 14:56:48 GMT  
		Size: 23.9 MB (23931645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89759710a94aa7f3ea6a141a38ec637e4bea1b6da8fca81e347f06d800c7e38`  
		Last Modified: Tue, 14 May 2024 14:56:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:e6f3460b0d8d8b7a5431ebd119f8252bf84a22419eede0c0999580ae44c00aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c95a4b5d47c7f94b2ee6591b4a26f62ecda8b946e50af98d706b327eb328d3`

```dockerfile
```

-	Layers:
	-	`sha256:acbbd8ce473f21f4a6efead7e4472feb91ae78a3ba7e792d607bf3fc3d839f76`  
		Last Modified: Tue, 14 May 2024 14:56:48 GMT  
		Size: 3.7 MB (3696822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57692c041b52c8f2f0d9c6278203354955cb95cc65850d2ce6e1fc26208416e`  
		Last Modified: Tue, 14 May 2024 14:56:47 GMT  
		Size: 16.4 KB (16393 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:ec1b91f9aaafdd55f83a9e1333f5c4a2d208af3c63cef31f836014a6bcc210e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52110407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870a7ae26708da9b934f15a297fa3f5e5dd276a5681f2b727320685888b086a1`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:bd84662eb5c566f361c169149ba683475c50ddc528270daf67d40c8e98ed12a7 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:57c62469eb2b8cb9a971714401ad24a78c171e2f6dab20314e1c5f0dab7a8639`  
		Last Modified: Wed, 24 Apr 2024 04:15:23 GMT  
		Size: 26.1 MB (26109830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9818ad4e40511aba9f841ac03199998117ddacd38408adfefa7ae2e5b030ff`  
		Last Modified: Thu, 25 Apr 2024 08:39:19 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65737d168a68039be203713357b72cb405010ed3e04a488b897e6088f3ca29e`  
		Last Modified: Thu, 25 Apr 2024 09:49:56 GMT  
		Size: 26.0 MB (26000311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeca1027c8bedb6c6bb2c7ec3fcb8d933ddfa1dac5fe5b2f40888ff5b271b668`  
		Last Modified: Thu, 25 Apr 2024 09:49:55 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:24ae57231805c3263d8a4ad48d553bbd2096eef739893565d976d104ed7613b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3707403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27254fd556dbfc5205862bf3d5a8170d78e9e7773adbda7e544fed0e2100db81`

```dockerfile
```

-	Layers:
	-	`sha256:df7fbbdace958449aa5933dd9d53b8bca65e1fcee69e93fa409215cb1f4c0b45`  
		Last Modified: Thu, 25 Apr 2024 09:49:56 GMT  
		Size: 3.7 MB (3691076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:def0ec6df820a018457d9b1a49906a287d654c52d328ad4b0b350009afcf44c4`  
		Last Modified: Thu, 25 Apr 2024 09:49:55 GMT  
		Size: 16.3 KB (16327 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:07a1c484c294114e6791590c8b75cc9a200de8fe7cd8bc40ff213eb3667ea213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59555595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c07325cf2634446a7ecbceac071bace4dcc37bda4916ace26f0c9bfe42949e0`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7803436d972e2323c81400e847d22c14ce8d4c69879d6cb53f4b7852a169a`  
		Last Modified: Tue, 14 May 2024 02:01:25 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf4223562da974f5f9cb32cf66b9bb7bf3295d095a276a0936bf636cd754edb`  
		Last Modified: Tue, 14 May 2024 02:02:22 GMT  
		Size: 31.6 MB (31560855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13f35c442f14698d2de1268bffd82c58a2b4a2fe87558fd12f932bcc0983bd0`  
		Last Modified: Tue, 14 May 2024 02:02:20 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:e104a54dfa595974a9ea00c7f76d20a9a48959f483d98f525875e19843426ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb697efbbb37083f09ca4203003c51abc9b57dfe0461ed61857ec31a6e0d5aa`

```dockerfile
```

-	Layers:
	-	`sha256:490ca68af567f8e6ce4d3df6975d4a7cc19c8d95b6731cb2468cfe32da8e3349`  
		Last Modified: Tue, 14 May 2024 02:02:22 GMT  
		Size: 3.7 MB (3740401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:552098906905756fea7cbee3abd0ef1de26b380db856e7178bb80f848bd2c0e0`  
		Last Modified: Tue, 14 May 2024 02:02:22 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json
