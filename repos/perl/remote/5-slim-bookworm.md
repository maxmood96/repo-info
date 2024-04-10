## `perl:5-slim-bookworm`

```console
$ docker pull perl@sha256:a90a82719584fe1c1a361d57df085f75df11fc1b2f2344c09e1f5f754dc86a59
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

### `perl:5-slim-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:aeac501f5e7cd3f137ba0816967d287f9a13d90835969324962353cf9d2186fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57616924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ae6790333be6aa95bff891595afa13f209d154c5077df7b62e6331b145ff3f`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57aff238ccb1f548a27105db47b21f14bf9d1ce85c39109c04866de851c98940`  
		Last Modified: Wed, 10 Apr 2024 03:01:37 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e292b412e0083d9e252434f3da94ed94867a6c130b9d91e6c94c7034e6e70b`  
		Last Modified: Wed, 10 Apr 2024 03:01:38 GMT  
		Size: 28.5 MB (28485299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb3afd79251181e6634b314bfde0d71023201e1080569663a943a26daa397a8`  
		Last Modified: Wed, 10 Apr 2024 03:01:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:b376dd9aac6bf4750ee93f93e09e87a7eed86ed53fca0b2a239834f0cac0e89b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ce9e9afe3ca5dd518d4dcade7b5f63737590c314dda9748ff23854fa18cf9c`

```dockerfile
```

-	Layers:
	-	`sha256:70bfb904477d49ad59c4667bda2765de8233ea35cf8697961cf08fee7494b1f1`  
		Last Modified: Wed, 10 Apr 2024 03:01:37 GMT  
		Size: 3.7 MB (3720340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03cb2abfa8718cbb80a6df887e03bbee2d2af41dc6753514aec2d4b11ec5d38`  
		Last Modified: Wed, 10 Apr 2024 03:01:37 GMT  
		Size: 17.9 KB (17865 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:42537e812eef2fe21571772afc3e63fb3c3c47f145a0e6c6985d486773b73634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52470531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4155d64dfdffdbb83ef901513717855085a959da1cf27bf9fbfcb1a52408873f`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:00060478396b8897d7f0dbc75ae01667a1df5fc48cda17f571d041ce4571fbdb`  
		Last Modified: Tue, 12 Mar 2024 15:29:42 GMT  
		Size: 25.6 MB (25586242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b8a49481f018d5b87f7b9a1cd5874caa7da04e7ade1661e2ab8cbe534206f5`  
		Last Modified: Tue, 12 Mar 2024 15:29:41 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d45440068d8b32cb1b6cf1604ecf919f0eae8b635be412b1edfe62aee196f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45615414871160648c2a6a0840826ef879e8822ffad825e76204edb9fbd6431`

```dockerfile
```

-	Layers:
	-	`sha256:124a8a4df4927010b65be24b955c8a364e46fbf7a514f90b497d2ce42edc2cc2`  
		Last Modified: Tue, 12 Mar 2024 15:29:41 GMT  
		Size: 3.7 MB (3691919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aecd79efd53580e31e718da9ca7536c280f2a827ca60b85f1f764a4d0e292f9`  
		Last Modified: Tue, 12 Mar 2024 15:29:41 GMT  
		Size: 17.8 KB (17816 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:904198ab1ce0b23e7c3310920e5cdae06d13aa04a0a5e9bcb70c25795729354f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49526220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28af7de014c048e8339fef12bb498f21d716bf6bbec948c4cc6d508eed5f4e79`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:297524ebd0c34fc6adeaa181037566e90f34de388ebb06776b594987a1193a76`  
		Last Modified: Wed, 13 Mar 2024 01:20:10 GMT  
		Size: 24.8 MB (24809227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82153e32d20e5feda8311bc978b7d9b209d2f795b40e3af197e21caf54c4a00`  
		Last Modified: Wed, 13 Mar 2024 01:20:09 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:151d8529ca0a19c716cf3b841c4511edd40417b5eb8c631dc5936b36f4f2bc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c1b653eb0d864e712c57e22ddf485801d28ce644e0a6cbbbbdb9b0abc09695`

```dockerfile
```

-	Layers:
	-	`sha256:61d5ae5330a2dc6e31b180484cf24d81798f4a6c8478f238d4617656ba25ace4`  
		Last Modified: Wed, 13 Mar 2024 01:20:10 GMT  
		Size: 3.7 MB (3691677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b0ffc7fc698a93853d412a3bfb5a532c2174d1dc31266c8e51ab9d11d357dbd`  
		Last Modified: Wed, 13 Mar 2024 01:20:09 GMT  
		Size: 17.8 KB (17816 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:02874f2fee2fcf2d947324991977cfb15353620d3691fd1ac19737e3db178d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56436045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6217819ae3e11ac870f895440b6c4997f4755c49ff7219b6bb1c2c41e9ad928c`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:194d1dffa2402f8bcba914a2ee85072a23ec297730ff74962d2c4379057968c5`  
		Last Modified: Tue, 12 Mar 2024 23:02:33 GMT  
		Size: 27.3 MB (27279343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8f19fc50a9cacefb89e329f3bb3083df324e5540b386c3c78b51685b2d62d8`  
		Last Modified: Tue, 12 Mar 2024 23:02:32 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:62a6db959a001fa6e27989fa3bb5f1a4218db4bc9391e15ef2fe543a23226a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fef8251864df70c8bef5ebd0773c4786ae823b171dfceb45a204f2584db34c2`

```dockerfile
```

-	Layers:
	-	`sha256:7b9d0397fa4bbf9af798e0781d2d3359b56a826c81c36164cb5060ded0f46213`  
		Last Modified: Tue, 12 Mar 2024 23:02:32 GMT  
		Size: 3.7 MB (3692790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f071c61b6914d3800a29602e739104e8cbfa2c258688946bab03c5ac8bff7f`  
		Last Modified: Tue, 12 Mar 2024 23:02:32 GMT  
		Size: 17.7 KB (17720 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; 386

```console
$ docker pull perl@sha256:49120b5aa9a7589d314fac572e4c8259e82103519d2d77cdd24b2c80fcbfcc9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57632491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099cca9cdbdafda9a6416724e2c94539ccaed7595115bf55aeac644871e3bb19`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77811e91c67ca36fe43c3bbe314b8e47034b35846f8bacef1524d9d9c63f8269`  
		Last Modified: Wed, 10 Apr 2024 02:00:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901050601ab56daea4d37719e124b789029ce52cc693860584a6c54597a93059`  
		Last Modified: Wed, 10 Apr 2024 02:00:47 GMT  
		Size: 27.5 MB (27485708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845431b9cee13ff71179086d1333c92333766889f392eae2a8700c449853b13`  
		Last Modified: Wed, 10 Apr 2024 02:00:46 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:74bc505ba1bd7fb1042a54cb4f3ddba5f17202a7687431c07564254659dd28e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80345211610d435265c697a3cde62d43913bf55f8a7679f2eb7cf9f52ac2034`

```dockerfile
```

-	Layers:
	-	`sha256:f3dd31f27a56f8dbd57b4d03cdf1bc8c6f6a30500291930e931634dd2c773807`  
		Last Modified: Wed, 10 Apr 2024 02:00:46 GMT  
		Size: 3.7 MB (3714213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4d3b0b9ed8b8c5fd7c831db75974b7262924b64fc923d0ffb30b3cb428ceed`  
		Last Modified: Wed, 10 Apr 2024 02:00:46 GMT  
		Size: 17.8 KB (17806 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:047c3e83d9bf312930c75fc0428a3a1a46aea89d7f85197eb64f16419e378209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55766428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df3e078c569df3c17417325243cf0cf3d7db0defecf9a4dd4929d2a050745d2`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1629788e0cfa96ddee49c53d8a3ae580ceba7f901dafbd773847a02e4de4ee`  
		Last Modified: Wed, 13 Mar 2024 04:40:38 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ec56c19f9b41f73e823360bef7b133c735025dc2a770a40a53f3141f09f5f0`  
		Last Modified: Wed, 13 Mar 2024 04:40:42 GMT  
		Size: 26.6 MB (26646955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879b577ead3affd4a4306baf48ffb8076fbd2887d8336e9bbc0b60e821b3720a`  
		Last Modified: Wed, 13 Mar 2024 04:40:39 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:526372d2a3bee5f523b9d1a41d3cef7cb6e94ec0874225451d149959e1b4ad67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080364b145d2c759e95ac88c45c114fc20f22d89f9c02fb86a1a155e8c826c98`

```dockerfile
```

-	Layers:
	-	`sha256:de40c0924f1621de817991cbe69541f3773869f0de527c553c7c294f8f66b545`  
		Last Modified: Wed, 13 Mar 2024 04:40:39 GMT  
		Size: 17.6 KB (17594 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:f2f280cb0ec1216d2c819a50ceb975e2e1dd08cef4d166f5b25065f779a1626e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62169031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e544228e219ba766a95f030469fba59281b7690e9e267e918f00f0b7d6c083`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:9d734b2b111623b1baa0bfafd7acf7f9e6397d9f701dbb76f0b2ad743d6a0808`  
		Last Modified: Wed, 13 Mar 2024 02:47:58 GMT  
		Size: 29.0 MB (29049741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6ab0a338a1300e0282e061af1ecfce53925c41d7e0323cb4689a064d57df1a`  
		Last Modified: Wed, 13 Mar 2024 02:47:56 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:783ad1fcf92eb098e05f63481c85fdb319867263fdc09b28ed484e76482de6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e7121cfed9be5ee47c03a1c93a755c84393e0a4c1cc96a53b75b16d0bb3b47`

```dockerfile
```

-	Layers:
	-	`sha256:74ae75b831394c38dd7d6b8248d1336538394cb67d5b971175fc8a5590de062e`  
		Last Modified: Wed, 13 Mar 2024 02:47:57 GMT  
		Size: 3.7 MB (3707351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cd4b4da21eef25273c28c44a4c3fe5d1f71e869ad6d91e0cec322c4c7d74a9a`  
		Last Modified: Wed, 13 Mar 2024 02:47:57 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:2f68c229a09bb82a7f396c085f134e32671ae31c3a6718a4d2498d357d69e910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54519625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f55b3bbbe7c9fdc1e54882e57cdc28237a419c54308b908ab1e91c13b479988`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65f94c12fa6b8c3bac191f9823b7379c053a155fd5720587220e03889dd0504`  
		Last Modified: Wed, 13 Mar 2024 17:35:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29819de8bf6190b2b2d51dbe805da26210f794f85d9b4bce770328f414a8fcb`  
		Last Modified: Wed, 13 Mar 2024 17:35:53 GMT  
		Size: 27.0 MB (27030673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09717881482eedebda2f8d31d540cbb8eb27e11d4dcf135b53ea3e28f46825b3`  
		Last Modified: Wed, 13 Mar 2024 17:35:53 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:e1586eb3321296669652dcf2e4f9ec3936592e7d403625b5c2a136fb01e51f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53529afcab51ee3805997885a671f4adcb510089fedf17390cbd87d189730ecc`

```dockerfile
```

-	Layers:
	-	`sha256:c2fee91b27e41b71c7cd1dd9c7df8e7293e3c60c9ab2b65db21155b6c4a6f5e0`  
		Last Modified: Wed, 13 Mar 2024 17:35:53 GMT  
		Size: 3.7 MB (3709894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea724a8e5d366c8badb89cca1980bf014ab7d0bf0a48a5c7bc7cfe6afb454506`  
		Last Modified: Wed, 13 Mar 2024 17:35:53 GMT  
		Size: 17.7 KB (17698 bytes)  
		MIME: application/vnd.in-toto+json
