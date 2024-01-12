## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:bea7d3ccd15087823ac8035c85478e894178cd7961fb94bfb260edc497e28afc
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
$ docker pull perl@sha256:68b0aa3f8066428436a479b81b3ef8ac04ac239ddfc3d59fa9f9d4a8b46ee4a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55988605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bccaec0e96e5d6a38a83ad92e3c97d82086325cde510ddbde487740d1a42ae`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173ee9f35d3e46712779465f1b18f0dd66b495777e61d55b074d60ebac87f929`  
		Last Modified: Fri, 12 Jan 2024 00:30:17 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112bd3770ffe40aed6a3376d49410a9a8aa706e76f052cf4b71337d7c3affe97`  
		Last Modified: Fri, 12 Jan 2024 00:30:18 GMT  
		Size: 24.6 MB (24570382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b8714b926c8835c03ab7b8688f13504607221f0daf1cf2f70fc5ec5b6f819c`  
		Last Modified: Fri, 12 Jan 2024 00:30:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:857ff339528ce0fcbd20ef85f2f10112e665d2323c68984b9f14316ce011ce1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3311272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf4fd024b80f1055633d959efc0d8e13144a8464ed973d3a1e3b698f8119428`

```dockerfile
```

-	Layers:
	-	`sha256:490b0f7e77abf4bebc4dec89865b919495e01f619fe9faf36b4337237ebc3478`  
		Last Modified: Fri, 12 Jan 2024 00:30:17 GMT  
		Size: 3.3 MB (3295457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5f434a041253225c21a350d2b19091139ba17643e871e3e5035ba8184dbedf5`  
		Last Modified: Fri, 12 Jan 2024 00:30:17 GMT  
		Size: 15.8 KB (15815 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:a56a01b92acff503b339ac479dce6b0c975164afb5ec6cc9cc3f7dcdbfadaaa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51489501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbeef67ce394f5e54f60670c023b2427ecbc5949d097db12a3d8243b2c7cf38a`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:38 GMT
ADD file:831966ecbc1ad85566dda1f3580cd9306cc099069cd418506e8befd03c296d1c in / 
# Tue, 19 Dec 2023 01:55:38 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:fdebea600ba5b47ddd94c41d9d687679a030fdad563a3490945a5433dae01d54`  
		Last Modified: Tue, 19 Dec 2023 01:59:22 GMT  
		Size: 28.9 MB (28921283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d09100782a58afba16874286ee30ec7285f79cc6f039986cfc2cdccfd58f84`  
		Last Modified: Wed, 20 Dec 2023 21:16:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc02881eaa4f0a04d9ff1b5659a4b1d91e3a0ac3398217b837945c5785428585`  
		Last Modified: Tue, 02 Jan 2024 02:00:12 GMT  
		Size: 22.6 MB (22567950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4b09a0ca285966c5252da86c088cc2f8d71c873a8867b1ee653bf7f28443c2`  
		Last Modified: Tue, 02 Jan 2024 02:00:07 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f8ef3ee93a1ba092812cb4f031e1b953fbeccc1f3f9dce6ebc11d0f39a4ea5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3286394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133fc27f25b20ee0e212dfbb5e2c47f0b24459942943a392ec3e4cc1a0d7786d`

```dockerfile
```

-	Layers:
	-	`sha256:cbf2021f89338af691f0f7fd7f2ab3972c62e993a9a3bdd9723d6ca697e62b81`  
		Last Modified: Tue, 02 Jan 2024 02:00:08 GMT  
		Size: 3.3 MB (3270684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4ce4df1dbb41c03c6cecf47cd79898a5a74627fd4d6c22a2081209e95555ed`  
		Last Modified: Tue, 02 Jan 2024 02:00:07 GMT  
		Size: 15.7 KB (15710 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:70142e70a31f6b1c4bf76fb7a72854a5b33ea3636bf3ebadef07bed3191827ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48545838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8192c60e9509c6908208fb56e8c5a993534a5a8ea5110b450b0f2246bdd2de85`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 02:08:09 GMT
ADD file:496e70a34ff4dabb4eefdf40e4e2f0563bea0c120bb43206f8f52ab5a887b637 in / 
# Tue, 19 Dec 2023 02:08:09 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:19ccf4d6cc6956e4a5522352be94632923aa376a9939a4f45428a4f304c73bc8`  
		Last Modified: Tue, 19 Dec 2023 02:12:33 GMT  
		Size: 26.6 MB (26578972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ce0fc6c077576b885dfac395fee39bcab6ddd16b568951f15b1bb9ea749711`  
		Last Modified: Wed, 20 Dec 2023 23:58:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b21777192da66e108ea91c5b8b6aca205462b379e57769db8e5a0091a34cd7`  
		Last Modified: Tue, 02 Jan 2024 06:17:25 GMT  
		Size: 22.0 MB (21966598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052552371f1ee84d151f06b48e8cdcabe67fc079cfaf8e76596b0cb822894338`  
		Last Modified: Tue, 02 Jan 2024 06:17:24 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:315f142829b1c0af2224eb1e7b6c9eff3c672247f4960d72ff8af08835311f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3289112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a421650518edc1437b4bd1a69fd66c0ee10b4dc820b5e62e498803974a42fe9b`

```dockerfile
```

-	Layers:
	-	`sha256:6482539ab7552f61c395aef0c1231f441d1e22890c8795fcb2bac2d9a1d2fbee`  
		Last Modified: Tue, 02 Jan 2024 06:17:24 GMT  
		Size: 3.3 MB (3273402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75a4408f87db53aff05b0383d32e4a7dc6fd95540094f0fb095d1723d23e1ac2`  
		Last Modified: Tue, 02 Jan 2024 06:17:24 GMT  
		Size: 15.7 KB (15710 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:1e38671863d76465e951cba69e0038dadf9bdcc7342ddb3aa57da80f89252459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53751184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72699219b2efe9a7f37b7ceda67d7a0fbd5761bf1d6faa31921ce339a91872e9`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0569e7c2b692a59db8f5a87ae41c20bad23b07dcb8fddafe822a5e65058de9`  
		Last Modified: Wed, 20 Dec 2023 23:35:30 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01c61f23af346f40a82a4f524c5af9656f39c02260dfb7e55f4f50bec89fcc1`  
		Last Modified: Tue, 02 Jan 2024 01:16:06 GMT  
		Size: 23.7 MB (23686864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a844e73a9e57464bb0d07af11469523a140d92ead4f72a5ab7821e79a0aad0f`  
		Last Modified: Tue, 02 Jan 2024 01:16:05 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:d008b6e6349d54590e53d031ddbc025368723a5ae39597323a53364c8484862f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3289033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e2aed419d14dc75669c3f3e85ca9d6f9b2c879ddaeb175d72dbf6b14bea6e6`

```dockerfile
```

-	Layers:
	-	`sha256:06947c81fa263aeb32f1cec499802503ce4491706269cdab7302553c9414c23a`  
		Last Modified: Tue, 02 Jan 2024 01:16:05 GMT  
		Size: 3.3 MB (3273377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df6ad3aa1851523c7fa216920508ce25247cde1b48ce7ba1da8cb3e9ab405aec`  
		Last Modified: Tue, 02 Jan 2024 01:16:05 GMT  
		Size: 15.7 KB (15656 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:5f1c04c93b1691a270dec0cc74daecfa8dc5eeb942f9c8dd4ebd53c91436361e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58398352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd57015b8ddfa7a8a02260c623ad1ca3ee4451cb7382235cd865b3a38fd562`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:ed1ce84cc05c621c3311366a5ef8f9ed36bdff95d75ee1564c10e7a20f993b61 in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:d19cbf7b148868960150824d1e6f8ebc5f6d7542a422061491e92178f7db879b`  
		Last Modified: Thu, 11 Jan 2024 02:44:06 GMT  
		Size: 32.4 MB (32402672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74d6f2f9d15a9003966bfd44adb3a0edf5c84baa2840259f0b60adcab81a6eb`  
		Last Modified: Fri, 12 Jan 2024 00:31:40 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d099f028d8c9398bcdfae515565bfb097e3897e30cb37074cc4047782969d9`  
		Last Modified: Fri, 12 Jan 2024 00:31:41 GMT  
		Size: 26.0 MB (25995412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899243095ab4d132d6c70338b7da757f475b36ac0c061bdd039598e2db987362`  
		Last Modified: Fri, 12 Jan 2024 00:31:40 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:fb4bf8e81e83563dea355d172ba3948dc1683e363c528cab86651391c0739a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681f4f49540f0977bd9d6670b1875bcc1d12ce2e20735219d60cb0cd7f0d201f`

```dockerfile
```

-	Layers:
	-	`sha256:d2f786de5f6f7cd6387668421078c4d8a5308d47d4515cd4421587bcc46f1225`  
		Last Modified: Fri, 12 Jan 2024 00:31:40 GMT  
		Size: 3.3 MB (3298766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3672227429da8e23333b12060b245fc2fcaaeba2de7d00124ac47b8bddbd00e3`  
		Last Modified: Fri, 12 Jan 2024 00:31:40 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:91bc2d14949648833f1ae7f1b7f8ebc666cdf68a1f2d78e8368c4a5f7bfba3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53091974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1439fbef2c7da5f8a1d8b92753650e72a893e14a412b03d8653f51bcfd0356b0`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 02:14:50 GMT
ADD file:dcc77071aa6c677714230fd845d154c00ba6ba34a78f8f1073c224e90f17f543 in / 
# Tue, 19 Dec 2023 02:14:54 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:f9454980ac665cb2d7641130c738c2054ef7a7516386fc6742b46b5b60dd93ad`  
		Last Modified: Tue, 19 Dec 2023 02:26:03 GMT  
		Size: 29.6 MB (29635982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa63e76321f29384a33f538756bf43e42945119c70d8ad926f55be2908797a2`  
		Last Modified: Mon, 01 Jan 2024 22:38:08 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1105ccb1ef7e976a0ffa44982c41951d3963ce7a3d5136134026dc0aa28390f7`  
		Last Modified: Tue, 02 Jan 2024 07:48:45 GMT  
		Size: 23.5 MB (23455723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068844104fa4431c88282ab870829f9592cd861d1e0d3ab37a1a3a5e83a3902f`  
		Last Modified: Tue, 02 Jan 2024 07:48:42 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:18b04f370cbd72db898055d86756cc9633a8c0d8618b156bce59e2c774d288bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3dbc8997311b24885905f4b2a181f5c58beababca70f63b29d7f7b692606a1`

```dockerfile
```

-	Layers:
	-	`sha256:c986aee1ab903ba4ac98335eaaa1feec3ca4711dbe9f494259b662d3d2940cea`  
		Last Modified: Tue, 02 Jan 2024 07:48:42 GMT  
		Size: 15.5 KB (15481 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:6c97f614b4d76555c0fa18f41beca9abca7f70fbab5d094e27a65ffbf3e4fef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60091421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52179e16c71f62b7345fe25238eefc92ec7bda65b550767d427fa8bf74dda9c`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:19 GMT
ADD file:1cb772a6ad8ca6301624db3141029490564de7673bc0f2d4bedb5a1578ea85bd in / 
# Tue, 19 Dec 2023 01:22:21 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:c9f6fac7f65cfc65b7f8de8bc377b135ca95e45a3246cf2bd1bb90922679553e`  
		Last Modified: Tue, 19 Dec 2023 01:27:11 GMT  
		Size: 35.3 MB (35293807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11036b9609acf58122ae19b79e91c30e52886036c3305dceb4d0139ce911ebd`  
		Last Modified: Wed, 20 Dec 2023 21:52:30 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2084e5a8e065974fe42469d4f57f208de370ed9d3b802b20da5d6642350aaf40`  
		Last Modified: Tue, 02 Jan 2024 00:01:06 GMT  
		Size: 24.8 MB (24797347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ce9b0e09630792a4144c2a6ea9446b97c7cd7ec28d84a2e6332728fe6ab940`  
		Last Modified: Tue, 02 Jan 2024 00:01:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:6a1562d5f2baabad6571f18a6d7ba6610faa82edf3e04723fbcd6d364c4bbdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3302332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9756727af1eae24b70a798f8d1d28f967cc5664eb0d9c92e59b8dd49394837`

```dockerfile
```

-	Layers:
	-	`sha256:f9f1930f02dd7c702a682da914b8e0725a0b29333ed4870e51201a51cd529ceb`  
		Last Modified: Tue, 02 Jan 2024 00:01:06 GMT  
		Size: 3.3 MB (3286652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b75b88d6d483cb4d57e9cafcd7ad9437f7885f260b1adb25cc909edfa20bf84e`  
		Last Modified: Tue, 02 Jan 2024 00:01:05 GMT  
		Size: 15.7 KB (15680 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:f4f4f4ce2c9d8ab7bd61cd9fd94eb46f714c46d71ae383ff489ad0c5dcdcb08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53431719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1eeb4681f1f4a99444c7797507eada70b193cce337f3a95492b78b6bcc465a`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:43:11 GMT
ADD file:36a070457acddafcd6cdda22a3c41efcbd4e2b1694831eb74c8143520ebf1cf2 in / 
# Tue, 19 Dec 2023 01:43:14 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:eff2a4367cf88d5103011eba9299da2b4d173b0bde5dc0455020febf72b9b1c4`  
		Last Modified: Tue, 19 Dec 2023 01:48:08 GMT  
		Size: 29.7 MB (29657006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d9a7afb7027beec55ffdfc75a29a35a4bb7ce6beeb518238f728fda590fddd`  
		Last Modified: Wed, 20 Dec 2023 21:57:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ae04ff5fb7c113ad23bf15e9735061790c4e198c4069a62242ea874088293b`  
		Last Modified: Tue, 02 Jan 2024 00:12:48 GMT  
		Size: 23.8 MB (23774445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ec2f5ac5bbf231ceec75ea12728f3496e0d56df6e0bce055f033b378a3387a`  
		Last Modified: Tue, 02 Jan 2024 00:12:48 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:05785e252c9938bc7afde19810761869d2b91f7c9437aa1660ea52ec8a9bd03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6457e39b2b3dba8c69257ad9679c8f82a04faa0a8b22ad71fae82c691c80375c`

```dockerfile
```

-	Layers:
	-	`sha256:62edec669e6a80668e39d1dad99561a028893cd0c9ebbb68b476ae6825152491`  
		Last Modified: Tue, 02 Jan 2024 00:12:48 GMT  
		Size: 3.3 MB (3285539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c02d606274b2cb0914314a48046706e334043de6284fd0ffa807c46f106c764`  
		Last Modified: Tue, 02 Jan 2024 00:12:48 GMT  
		Size: 15.6 KB (15647 bytes)  
		MIME: application/vnd.in-toto+json
