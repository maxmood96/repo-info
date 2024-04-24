## `perl:stable-slim-buster`

```console
$ docker pull perl@sha256:5144cd8387940018c4ffb9be1f1d473940092ca65b399e4f328c106d6de71da7
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

### `perl:stable-slim-buster` - linux; amd64

```console
$ docker pull perl@sha256:d0a0ff0c7b12bd211a5dffee09b691d86d89f2529189dc0c363251a1575fcab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54665534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7c613967fb3b53c8a0eece04ea46559184de1f44f83ff7bfa112f493967552`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
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
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627771faa3070873537a04465741422eb81355aa131d0cb25b0f90182f7823fb`  
		Last Modified: Wed, 24 Apr 2024 05:05:12 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909a0e33d0bbbd73b79b060b48617bab3e45f79031de3e6136f04021261eafb9`  
		Last Modified: Wed, 24 Apr 2024 05:05:12 GMT  
		Size: 27.3 MB (27327692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18697688294a3820ce30fead54c52005080c0b266fda7d9bbf56446fcaa70b2a`  
		Last Modified: Wed, 24 Apr 2024 05:05:12 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:cec141afb6706976670ad5aa003d29e4d7f5e49809adc0b73e894d7da6d22429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c8da11239e27b40601c7b3a2b8bfe099932e924bacb422e8d08a679078e3cc`

```dockerfile
```

-	Layers:
	-	`sha256:6ddb580fccebdbe282b93edff9398227f57b0fc277464fd5731f6ee7c106ce4a`  
		Last Modified: Wed, 24 Apr 2024 05:05:12 GMT  
		Size: 3.7 MB (3721514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d6065fb3ca161791905dca445f37be24476119da8c71ae543d8d09353fdd40`  
		Last Modified: Wed, 24 Apr 2024 05:05:12 GMT  
		Size: 16.3 KB (16341 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:6f68d9243b6d8906ef859819e86255b39c2334160fc442cce72e3613df3f37a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46708180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b9a7740567a24ce9b45ae3e289ce5684b2de746c0edf3a10d8376a711342c3`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:e86d8ee2244a2861682ace2739976c78678da8fd684b3dd3df6c987b51ae0a18 in / 
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
	-	`sha256:f598da777531a3a9f90bacdb8114a97507c4692676f8ac75a87fb08f03dee891`  
		Last Modified: Wed, 10 Apr 2024 01:05:59 GMT  
		Size: 22.8 MB (22795982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639a854d7c3596f7d7b67dcd30061b8ab3e90e82fc4f9445f1099373a966df30`  
		Last Modified: Thu, 11 Apr 2024 02:33:25 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d3a34f0c1f45391fa2476ed259d54517b6acdb23c94b709adfc1e36cb553e`  
		Last Modified: Thu, 11 Apr 2024 02:33:26 GMT  
		Size: 23.9 MB (23911932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6150a2108e4a7883a567c640da9a20f649392f9fdeef5298d001f02d593dd13e`  
		Last Modified: Thu, 11 Apr 2024 02:33:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:5bf37b2fa09f1c10752a303aa0e0645f1dc714f861d03b09ead34b86f84f2ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3356724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bae46ec5cde956821c91bb904bf276a773b78483bc012c0e549d0b24a22af7`

```dockerfile
```

-	Layers:
	-	`sha256:2398e6da4775bef21f78a14c7384b12a614154b6501093da996254e195d6815f`  
		Last Modified: Thu, 11 Apr 2024 02:33:26 GMT  
		Size: 3.3 MB (3340476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:306b00837ff2ea2b6d9222884a844141e02b6a5cd87a9f236adfb81bc7cd76e2`  
		Last Modified: Thu, 11 Apr 2024 02:33:26 GMT  
		Size: 16.2 KB (16248 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:50a0b45f2d2d82e204e63d5c0bb94e8c05b46161852f1d5eeeabd0c661ce3ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51930216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e887e7b5cfab87296db2070b564bdf36e84588f363c65951ead4042fedf27b6`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
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
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1812a739984a1efc367a9d7653f7f339da92ad7a6bf6159f5cfc60f8dd1155`  
		Last Modified: Wed, 10 Apr 2024 17:15:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a132e6fbff0cff84be5e0a40cd9eb83c225252943a1b5ef3b8c7f5d00ff3589`  
		Last Modified: Wed, 10 Apr 2024 17:15:14 GMT  
		Size: 26.0 MB (25966489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488fd0d922c1b5f44da71d8b7772f37d4331e0911342db9054cb37bfc8cc418`  
		Last Modified: Wed, 10 Apr 2024 17:15:13 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:a44caaf2874d8ded7c231bdff7030fa531302358827eab1fe5528b1b1a019747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3350912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02248059e5488b0da743df54262d9e220ab77026a7086b5111ca252f5481efd4`

```dockerfile
```

-	Layers:
	-	`sha256:80778b1be430ff1cfd70a888ed04d11105d48df0af8a3a4a98d5af2e88480ee1`  
		Last Modified: Wed, 10 Apr 2024 17:15:13 GMT  
		Size: 3.3 MB (3334730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb8cfb3f99e61c9370f253d8c6afe87f210cdca7750324e0186dcc0a257ff2b`  
		Last Modified: Wed, 10 Apr 2024 17:15:12 GMT  
		Size: 16.2 KB (16182 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-buster` - linux; 386

```console
$ docker pull perl@sha256:f5235b28a9bfadb313b937f8b3a52bf7ad3c86bc62dc9d8fc9747f058f1672f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59300185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba2e1767e256985ea08d730aa2faa686813b195723ab10c2175fc696e19b2f0`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:6033d014a0c5c8d87a61d23e20506ec550ea93ef72866e76bfe5a468ceebf619 in / 
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
	-	`sha256:d349bc9800fc6053f91af64b3ce845b5191cc9e0ae2d2001951381ae2d08e46e`  
		Last Modified: Wed, 10 Apr 2024 01:03:40 GMT  
		Size: 27.8 MB (27848331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2ca9a5c5f916f79dcabaf26928ba397f2a6d4de41017b20b2f8b380c21cfab`  
		Last Modified: Wed, 10 Apr 2024 01:59:45 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1e15c349fdfcb91dc870d16e045e268041e3afd41a0047492182dc0ec8b733`  
		Last Modified: Wed, 10 Apr 2024 01:59:46 GMT  
		Size: 31.5 MB (31451587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df035c78e71c0e0dd8e2b1a27d0793e16a1ca79836ec6d9afc26c8382a2ff6c1`  
		Last Modified: Wed, 10 Apr 2024 01:59:45 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:40fe0028419896dfadefbfa6893279b9a1c8fba6a9780000df8826c32810d143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3400358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4fdf86a4b2d260b0a6787b9d36dce444ceaf2762395964b6c1aad8e343abd4`

```dockerfile
```

-	Layers:
	-	`sha256:310423f112df95a548db7e903920efde4cb72d641c28fa3af0391079732cc664`  
		Last Modified: Wed, 10 Apr 2024 01:59:45 GMT  
		Size: 3.4 MB (3384055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4311e6f9314520fec8e2b06515212ebad9661a0b4bc95ba3a59db55677bdaf26`  
		Last Modified: Wed, 10 Apr 2024 01:59:45 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json
