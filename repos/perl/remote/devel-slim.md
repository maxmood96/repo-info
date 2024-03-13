## `perl:devel-slim`

```console
$ docker pull perl@sha256:050376b9f75d856db46c9aec78b31152557f8d7d77e65c73174e098ce305c177
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

### `perl:devel-slim` - linux; amd64

```console
$ docker pull perl@sha256:7296bd02cba63b1ef9903bbaf0f045b794b2b1d701d2ab898e9ca7f69ce43392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57852518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334a9cf686698eb88a7ab046244b3e7fa4eb4d3585636b57eca25d5ca4b55f21`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f36cc7a958c045013b1189b44811dcf7323fe3b7adc33b5ed41596645db614`  
		Last Modified: Tue, 12 Mar 2024 02:06:34 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2c5ccdc1251e613429d994629daa4ccbc58544775ab2833639e833f8f6bce0`  
		Last Modified: Tue, 12 Mar 2024 02:06:34 GMT  
		Size: 28.7 MB (28728069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55128fe1de742a630e05508182105446437dbc0aa0110aa855fb20c895068f5`  
		Last Modified: Tue, 12 Mar 2024 02:06:34 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:b002ed08fbe8b72de2437104794ef26304922b2197d1b79a5dc5b343ca6a200a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72eb87d2ce7a87b2551b4d42342da53436d98c4176bd2b5a6f762424f03a2ad`

```dockerfile
```

-	Layers:
	-	`sha256:eb3304545bbb9a0ca75e39064660bc02e3e51ada758c772b98371cba8bfe0a4f`  
		Last Modified: Tue, 12 Mar 2024 02:06:34 GMT  
		Size: 3.7 MB (3720416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a6ef1fccdb14b409a0f0d4eae8978635144ab13e9b15f79535dfc7673b0e88`  
		Last Modified: Tue, 12 Mar 2024 02:06:34 GMT  
		Size: 16.7 KB (16727 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:51a91f07cfcf2f13a6745b7b038069f89f90c171d6c6603b285d5186c4899ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52711215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a67d2c8b099d8f36353a8cad8beb42f5ddadaadb55b40b3b2b28b9aac78a859`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78dccbdbe7ac504672c76d21148c58c9cb0430eea4823a902bbb908902de059`  
		Last Modified: Tue, 12 Mar 2024 15:29:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cd2fa41fabbe97585d7a62fefe499a4e574152ff47fda62fc0ff51d1df19bd`  
		Last Modified: Tue, 12 Mar 2024 17:49:19 GMT  
		Size: 25.8 MB (25826926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09917cd74aedd1453176c030deb4758b77c49745663549212bb91f8acd72132c`  
		Last Modified: Tue, 12 Mar 2024 17:49:18 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:134c929792ad1de1a29af16ad9538635b5c8f9e1221eb93ccf94f100a8259b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3707325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f251bbd330fbe26b612d0995aa365a67211d7697dedbc6e85949fe34282dfb15`

```dockerfile
```

-	Layers:
	-	`sha256:d29b9b1c0f359e6ec065c9366408e068bf3a82bc3bd9b930400dae5a6a8dbf7e`  
		Last Modified: Tue, 12 Mar 2024 17:49:18 GMT  
		Size: 3.7 MB (3690679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d75453bf9ee4ed91b01bf2568be97c5fa16e61cf6447be43b5abf8e0a50378c`  
		Last Modified: Tue, 12 Mar 2024 17:49:18 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:b67fb546f37731dde8d0b33a188d1b6ff0569cc536773c6b0826d646588d2cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49749759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42573fb7c6b8b7733e00a61f55d36e75b12d0c1089f1854b341d3a017ce23262`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1928a97698fe8f3044c4a65448c5f70aca4b7f1da8e045bd2ad301a54f1264`  
		Last Modified: Wed, 13 Mar 2024 01:20:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1712b27ad902a1a537562e168f434af95acc5deec1c48d6cc89565e5373023c5`  
		Last Modified: Wed, 13 Mar 2024 05:00:00 GMT  
		Size: 25.0 MB (25032766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83964297b488e2ffc225f4aa9466234066ebcbe673e6fa6d3f7069fc4a1b6a7d`  
		Last Modified: Wed, 13 Mar 2024 04:59:59 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:471e7ea0deb905bb6aa12fe07beb275bb85e6ee69706e0f6b741fa6346c844fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3707083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819c3be3d749ffaef66810c2cdc80b95e1f83c777ea43e4efd7304ee55a33dda`

```dockerfile
```

-	Layers:
	-	`sha256:2097a68902800b1e42aeb7e50473b0be67ee79c2e04f20336060506c06e8c92f`  
		Last Modified: Wed, 13 Mar 2024 04:59:59 GMT  
		Size: 3.7 MB (3690437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72fe43b42b3a14ccf873cf116da3fd9a266a9c2fdc3253b6f13339180c3dd4fc`  
		Last Modified: Wed, 13 Mar 2024 04:59:59 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:70f7d3bc3a10c6e1f7e6b7e48a34002d07cc439ffbdb12d062bba7f63ad9dfc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56662287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab761e4c9f32f248536e41711b1635069fbd0e99f481c2d4147fa1782d6c95e`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab808a42ee88b4748bcef5638fc52156ca65590e7197f43fad02801b710d72c`  
		Last Modified: Tue, 12 Mar 2024 23:02:32 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed284fdf6f0291031046006622020222f1a277a06aaf30f41cfea1ef38b4da96`  
		Last Modified: Wed, 13 Mar 2024 03:05:06 GMT  
		Size: 27.5 MB (27505585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2229615215432093efba30ba638703648ff3350532603ae5068456c516198`  
		Last Modified: Wed, 13 Mar 2024 03:05:05 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:ca5d254429bf30bdbebdd1e3a084e15a5ed1bbdc7b5fcf0f1f6ce2f8e79f5e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3708148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da24cbdf83077e4c1c450ae12faefd0bfde3635416d437470447d042cfcba69`

```dockerfile
```

-	Layers:
	-	`sha256:5b2b31cee5a5878cdbe14c0fd9873d270c6b3c0f25d94853385755b81e274b71`  
		Last Modified: Wed, 13 Mar 2024 03:05:05 GMT  
		Size: 3.7 MB (3691574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0c69c0f216ca95581424c7999b992e0ba61947d8bc1b1d8f4a6468a4997c53f`  
		Last Modified: Wed, 13 Mar 2024 03:05:05 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; 386

```console
$ docker pull perl@sha256:b485fd9fadb2a326b7cfb92f6de72319ac63c86be791628d1736ebf49645c953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57861214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f247ff16eddd430893221996df49fcfc14e28cb9632b2f3d561ee671c41984ce`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8602170235c3240971e22cf13d5b262e2f7ad99c74ebacaeb77740ef34f451e0`  
		Last Modified: Tue, 12 Mar 2024 02:07:02 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9352130cfc4e39c9bdd5eed456ca3f3002df702a144b3b89ad148472d8d20cb3`  
		Last Modified: Tue, 12 Mar 2024 02:07:03 GMT  
		Size: 27.7 MB (27719076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6af3a900bee50d404119acc64ddd9fb87cbff19745c597889c64781ef98c766`  
		Last Modified: Tue, 12 Mar 2024 02:07:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:52fbe64dff43d3b688548b5e6201e63f6770a621d6c937b93c93be05b0c51720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696e30a0594cfe9c1b272cd3c02d16a228b57de7a831998ed861e4c0b205b4d1`

```dockerfile
```

-	Layers:
	-	`sha256:2e00cb68ebaa83050996dcc1f4af3822797a255e08c97baf5717a002913583a2`  
		Last Modified: Tue, 12 Mar 2024 02:07:02 GMT  
		Size: 3.7 MB (3714309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c24d60b00d83596e831bd3f2a708124f4b7c0f107e8eb47deb6eed62365c0c2b`  
		Last Modified: Tue, 12 Mar 2024 02:07:03 GMT  
		Size: 16.7 KB (16688 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; mips64le

```console
$ docker pull perl@sha256:209af537d6857acc13b39b37b58452888f161caca1bc170d17fcfcd19cf78420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55994272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a9bc311b146449c69fc274e562edfd8900a1547c60e9687ac7a52853c6d3b0`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:14 GMT
ADD file:7b0bbeed7888e49f58bdffd816596bc88b87bd4a3761c5a2590f3123c077899b in / 
# Tue, 13 Feb 2024 02:04:18 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:78ede1ea2c0b185708583060a40bd2aeddee7b533566b4df729e98e5e5de458b`  
		Last Modified: Tue, 13 Feb 2024 02:15:10 GMT  
		Size: 29.1 MB (29119092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781e0db7b4b5c420568723a747e801dff60e8a693fe141a742020787cf651525`  
		Last Modified: Fri, 23 Feb 2024 20:05:34 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae104ec3163c17211bbe5a57f3d5a36d8cac71e0574cac708f55f038210ddfc`  
		Last Modified: Fri, 23 Feb 2024 20:05:38 GMT  
		Size: 26.9 MB (26874914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581a66e4a923101f17488c8e153e7c26a13243d7d4809c7f7d1b0f5ef7ef1406`  
		Last Modified: Fri, 23 Feb 2024 20:05:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:7cc9e225f2168ee277a5db0fddfc90b6f4cc8d15b8eab3a181160d28a3b49df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 KB (16420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a4fd4441658a0812886ce0b8a9eacade0862e5226f57f5708b3cef9569f6c0`

```dockerfile
```

-	Layers:
	-	`sha256:b7649d3ea54843b78709587d3694a34b9dbc9460b7f06ae55410a7e9a46f6bcb`  
		Last Modified: Fri, 23 Feb 2024 20:05:34 GMT  
		Size: 16.4 KB (16420 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; ppc64le

```console
$ docker pull perl@sha256:3b4e496dfc26b086f77ad6786c1d9a462657b3c6ed4b1f3ba57a3f6a5ececb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62392241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff8c92a490759d27273d341106247f9e4ad4bac345643fbe1f6330fb14b4ded`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b9e030924eb17cbfcc26bda085f55f7adc8517bdcddf933ca947b0843cbbbe`  
		Last Modified: Wed, 13 Mar 2024 02:47:56 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d954c236c98483fe3ec12e47de49f0655aae30de300e3a2bf72d2a3221a5a19`  
		Last Modified: Wed, 13 Mar 2024 05:37:31 GMT  
		Size: 29.3 MB (29272952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3936c7da4c9cfa2c859d8a1d777a8f64b5b3f900dba4b93667e1070ecbc944`  
		Last Modified: Wed, 13 Mar 2024 05:37:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:ea1ced4a1123a3e38c20cae426fbe45eb5a19ff2d9fd2d2f57d5a2c06e88dfb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2616aebc5f56e75f9611f97cd3a4ac9769b9f2f52ed53df09d5c88a8feafbe`

```dockerfile
```

-	Layers:
	-	`sha256:2cdd4953094898f4764a27bab3d37d5cb75afe93d8c8e91b8e90110a01e2eb95`  
		Last Modified: Wed, 13 Mar 2024 05:37:30 GMT  
		Size: 3.7 MB (3706119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3331cc2913086e847907c31707526208149955bc1b96c7049c467358d940fdea`  
		Last Modified: Wed, 13 Mar 2024 05:37:30 GMT  
		Size: 16.6 KB (16610 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; s390x

```console
$ docker pull perl@sha256:f708d327ddb79289d2255c81e35bb794800c5db5f95039fa00642b7ea72162b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54751757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf471c482eec35d6de58e9f32704a3a6eec83df0682c6ebaf8f3b2b2c5f99f5`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe4cd4eb0306d8c8639424f378f0080906b98c08e0dd5238af056d92390fd8d`  
		Last Modified: Thu, 15 Feb 2024 06:31:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a945a26074d5eabbe088985d8e4ae4656568d03c01052ba7c9b2aa3cdd64d98`  
		Last Modified: Fri, 23 Feb 2024 19:25:48 GMT  
		Size: 27.3 MB (27262903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b320c933bb890c3a6beb8bdb18f2380767536ed3140b761a28f45c8f3063f`  
		Last Modified: Fri, 23 Feb 2024 19:25:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:4bd5606486a09a6d3434c9ed383dfa7354284d2b3fa147bbeb5e943ebed73001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be757cfaa1ca90db7d5cce448e81e2fc6b55a31c9d9a83ffc499c67732506f1`

```dockerfile
```

-	Layers:
	-	`sha256:87e15692a2b1302fc833b57763df8557bd3b11c50beba7c02058b4859c8faaf2`  
		Last Modified: Fri, 23 Feb 2024 19:25:48 GMT  
		Size: 3.7 MB (3708686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2306914ec66a4cd2094186fe433e30cbfe2661a505826e10942729a4f0a16fe`  
		Last Modified: Fri, 23 Feb 2024 19:25:47 GMT  
		Size: 16.6 KB (16560 bytes)  
		MIME: application/vnd.in-toto+json
