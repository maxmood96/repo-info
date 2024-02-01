## `perl:5-slim-threaded`

```console
$ docker pull perl@sha256:60ad88ab21eaa3b0e71630864a8a3738e06a2f2433e78abb36693d706ca8154f
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

### `perl:5-slim-threaded` - linux; amd64

```console
$ docker pull perl@sha256:4ad00546208bf43f8bad0beec3513ac579ea24189112e3602d93cd10c1e91d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57499166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53615a5c33fe38702b459a70cd90ecc8e397bde0331792bf0d22fda2e9066651`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60924d357370a0d6bf7c1fb78e2e961345e4d36cf5d2ddb93d522135b9004079`  
		Last Modified: Thu, 01 Feb 2024 00:04:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746b7e2ba9c9ef5ff3e86d97bf770363159e6e59f7aa53f5fbbf730c5b5ddcc2`  
		Last Modified: Thu, 01 Feb 2024 00:05:43 GMT  
		Size: 28.3 MB (28348437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5a5db9dea9c1d409e3fda305bb2d59ad6c6eeb7bb8924ac1ca22a221d66b10`  
		Last Modified: Thu, 01 Feb 2024 00:05:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:abd8dee3e6d0ad1cba0e8336a65320e3c6dafc0827c1ed8611dcd574a5928a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6243e5e858966fa33e2e5e7652053cd9c61f1bcc0d4fb97d753615324d07c9`

```dockerfile
```

-	Layers:
	-	`sha256:2cb4602485f656c9075d221469260cdedaad155152ad5a4089fcc205a197e33e`  
		Last Modified: Thu, 01 Feb 2024 00:05:43 GMT  
		Size: 3.2 MB (3232990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec700229a348bb1dbfc498f423091d482b59119aaf6b0cfab708d81ad7b77842`  
		Last Modified: Thu, 01 Feb 2024 00:05:43 GMT  
		Size: 18.1 KB (18092 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:fc1afd54501d151524689fcdef74f054eae07d818f16ac1fcda6a22cc534b13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52336368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5269a7676935f29899394040474d0220eee634e66d61a801050cb7d839ac554`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:557a5348da1e680593a9ba709ef059b96baf15e0c89d8f8343e97bf008d9dc05 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:b508f3272b9b70b8dd19c621a4da1be63880a1f6412063787647ceeb464d772a`  
		Last Modified: Wed, 31 Jan 2024 22:48:00 GMT  
		Size: 26.9 MB (26909323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0383c699e836d1eea534c0aa7357230b7eef42b680870e12c9aa3a7b6e772f53`  
		Last Modified: Thu, 01 Feb 2024 12:31:26 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1134725f49fb03fd815c5da168dda91243971aead947c891006328fb48ea3838`  
		Last Modified: Thu, 01 Feb 2024 12:57:28 GMT  
		Size: 25.4 MB (25426780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96cddff89e55a009824ab0bdb504e8c01b37c659ed032613d61b4adf90ed971`  
		Last Modified: Thu, 01 Feb 2024 12:57:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:e2f0f718d99f1550562d386919f9fb2c43cbac0383263157c3d7a12f1572f26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3225780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa85570b05e84c89fa5d138105be55ca0930f1fef97100732bd7804c1839af`

```dockerfile
```

-	Layers:
	-	`sha256:f1d428864d65345e6a079352ab3058f2f6c99b3dec0a5832ada6f3e5e0d0d320`  
		Last Modified: Thu, 01 Feb 2024 12:57:27 GMT  
		Size: 3.2 MB (3207737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6acf786968c40431e985b46503cd00e53678d2aa1705a1330e2412f167a52ff`  
		Last Modified: Thu, 01 Feb 2024 12:57:27 GMT  
		Size: 18.0 KB (18043 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:dae7b4f57584f79a85a3fcdd2a9508ae200c1fedffd5902033c6cdb42ff9ed12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49557186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad9454aabdd78a5301905c2404bf3e68bcfefd18cc25bfba0aea445725b6440`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5f2d303289ff6605957a6c86c67a1dd0cf7c3fb8455b2507d220775adfd096`  
		Last Modified: Fri, 12 Jan 2024 20:40:01 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a04b3e2ca26ae4667585d7d0355999af1cb0d68e118ff87e7728927643ce0a`  
		Last Modified: Fri, 12 Jan 2024 22:46:22 GMT  
		Size: 24.8 MB (24838793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459836a636453cceb146506fb1efcf6a32efe398a5f617ff41860544dabb2273`  
		Last Modified: Fri, 12 Jan 2024 22:46:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:c421251f6d1a0219edd221658ecc5fd86657f37e8cd1db5ef5f2dcac1673bd90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3225644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514579f96139b34c78eb133386b4c95ce4f881f91ecd804e2b12456bcb98d85c`

```dockerfile
```

-	Layers:
	-	`sha256:b193d897e74a4cda7cbefca2ea9901ae2e3d39876ac85f01c329b61398833eed`  
		Last Modified: Fri, 12 Jan 2024 22:46:21 GMT  
		Size: 3.2 MB (3207601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:217c2f7b5c7c575da792e28719ce6d720f094df377ce031ff96058bc76206248`  
		Last Modified: Fri, 12 Jan 2024 22:46:21 GMT  
		Size: 18.0 KB (18043 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:79289f2efbf9bedaf61f0cbb1a00fe0d93340feb78ca934e0e45c629b278d9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56475008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986431e621cf2691ebcb345b8d0e0a17d2c40bad19fd286055a49ed38b2d057d`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ea23939bd3b30b5813dec02bedfb73a5045ccc956bbe0e941e42c2e6e40f73`  
		Last Modified: Fri, 12 Jan 2024 09:59:33 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4a3dd48e982cc672cfc9a4c5089d14eb712e01cbe528fb3a5c3b50dda17ea8`  
		Last Modified: Fri, 12 Jan 2024 11:01:45 GMT  
		Size: 27.3 MB (27317406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c272513bdd926391b43568f760c77ba6b1640406090708b7a747a906614c33e7`  
		Last Modified: Fri, 12 Jan 2024 11:01:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:2ac5e7f881630c3db1c9d498d0056d82f42c26facee05e77477546df34b031a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3226131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a801e74c71b30f6f04f15e23f4d5f8b78674d960b489f44c8d954d2391d9d2b4`

```dockerfile
```

-	Layers:
	-	`sha256:50c4b97a1a12decc1dc656ca8d3f576ff80317025202b9473e4957c08464eaf5`  
		Last Modified: Fri, 12 Jan 2024 11:01:46 GMT  
		Size: 3.2 MB (3208184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6aa725d24d04c51f6d38ec1936d1169da2a1141c3ba891005f86008e47f1f4f`  
		Last Modified: Fri, 12 Jan 2024 11:01:46 GMT  
		Size: 17.9 KB (17947 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded` - linux; 386

```console
$ docker pull perl@sha256:9b894c94563f3250470cc8a67ddd0c4f0fd4269894e4f2f5694f6f33615c896c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57560877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caba9a52d46f3cb30514399f6413659bd56e80e5387ce1b2008aeb25f40638c9`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fad6d3fd16e9a650f9a09c7bd0d1d98832d80ec814d98d205e3e28e1556251`  
		Last Modified: Thu, 01 Feb 2024 00:04:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6444811cc60e3c7d0ea03db584f629c733fbe9d25bed80e11686a660984c3ab`  
		Last Modified: Thu, 01 Feb 2024 00:06:45 GMT  
		Size: 27.4 MB (27395597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d4cb954b5576d7d85112281c4a9fe6e3cbe0973b6d31636696f1e499fa4971`  
		Last Modified: Thu, 01 Feb 2024 00:06:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:3d9ca201fa9a63c7c1c5852b3b4cf0a111a96f5d8a07384a76a138e5f837dd00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3245320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f19ed01592df91ac3f0522fcf3464113a5064a18e84e96052716c9a44987100`

```dockerfile
```

-	Layers:
	-	`sha256:ceb1c2de7f640e9b1c884d2fa02089576f75f6d0ea8078e6c0afd9ac933572dc`  
		Last Modified: Thu, 01 Feb 2024 00:06:45 GMT  
		Size: 3.2 MB (3227287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf1606a1a2fb3dcf080f09849897ee7f83549618646b018caa90c1f46fd2833`  
		Last Modified: Thu, 01 Feb 2024 00:06:45 GMT  
		Size: 18.0 KB (18033 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded` - linux; mips64le

```console
$ docker pull perl@sha256:5e855375356f1806a0e7305af36859f88ec747fb54f9397f39442a6e5bf3fe21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55820128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0681e2a2accf8e5f71be10e0149caa2fa1021d51a0c2ee3dcabac7b0c5558c`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:61bc6da4a8a8247e6b88cf149051dbb04a6a5e6e1ffc5da16a85d1b4f24be297 in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:4f1541106f1f6cee2d65a870d8d3fbbaef35e04dbcb8abaa9623a9f7137a6ae5`  
		Last Modified: Thu, 11 Jan 2024 02:22:46 GMT  
		Size: 29.1 MB (29121397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dcd18743c2f4e0070ca9d8d5b7b8ac5f7f8d405be3530d395ba2aaf9a787a8`  
		Last Modified: Fri, 12 Jan 2024 05:57:01 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd8af82c6525061e08584d8c04f60c56aecb0bcb6c77b32cd0f262a745bbce7`  
		Last Modified: Fri, 12 Jan 2024 07:49:54 GMT  
		Size: 26.7 MB (26698463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e738d282ca65cc9c372596d75dd2505cd6658284d3794bba785f84451b3485`  
		Last Modified: Fri, 12 Jan 2024 07:49:51 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:d5cbcb250f26641c289db50aceb4a7e97fefc0f160ecbd1dca62068751f42782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 KB (17821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2c6b0a24305753b721e964dc311cae6ceb38fdbf88a13584c02955ca4e3912`

```dockerfile
```

-	Layers:
	-	`sha256:a3730e50f2213baf802faef09885a26ec1f650b54ec4fb02141bd79f323647dd`  
		Last Modified: Fri, 12 Jan 2024 07:49:51 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:ff276f008f625ce8c8e6941f8ae45aae038950135743a049cb2701612b707d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62261332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76d11946a6790e9f8bf134e8cfe6672c03dd6d760e7174b714c3668142ca3d3`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:fcbdad385ae78401c4f5aebfeed9ba8edc6adcc9870a328a756cef32458e50ca in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:5d34c3dd8c95d308ec07fd694f24411653403413305af18811f2d53cc052f152`  
		Last Modified: Thu, 11 Jan 2024 02:39:25 GMT  
		Size: 33.1 MB (33120536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f672263b4dcb09c8e02ace9429c79c1dcaad80ea87d90b00d95240adaa85f29c`  
		Last Modified: Fri, 12 Jan 2024 10:12:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a281f9e070f1094294757a1ea8a67a560ecfdf6c696e156bc62f859af06bc8`  
		Last Modified: Fri, 12 Jan 2024 10:40:59 GMT  
		Size: 29.1 MB (29140529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e29074bc74118f5ae7b6a9d3aee762a42e842b73fda7e1505cfc217a5b2663`  
		Last Modified: Fri, 12 Jan 2024 10:40:57 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:d73947243060dbc8755c483b4687880076b3feebbe234ddae7e525afc6b46e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3239578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6476a715ae50d095c1feac03625bcd7bc35ca3a07dd59514fd0f95f5a5c948`

```dockerfile
```

-	Layers:
	-	`sha256:0e71b49367d41e53dceb9d0a27059eb2592ccd2596419352f17ad3fba0cad8ca`  
		Last Modified: Fri, 12 Jan 2024 10:40:58 GMT  
		Size: 3.2 MB (3221579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18f50606d28bbda78361b87868a752b555a5a0289673243a6c509ab55f42819a`  
		Last Modified: Fri, 12 Jan 2024 10:40:58 GMT  
		Size: 18.0 KB (17999 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded` - linux; s390x

```console
$ docker pull perl@sha256:309611a1b21a56beeb50c8f717c1fb3d6c63b55d87dc8e21e87f1197c54ba308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54569076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbc843704f9369a69705e0e041b80a553ed07fd5604f7a82e9f222a8c1e5556`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0a331710561d1b0c32cf5ae4729c6bdc67cee4991756dcad73317924da1d9e`  
		Last Modified: Fri, 12 Jan 2024 10:51:21 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfb40d6605597fcd1154045e77832253afae372aa26815b13924d6af7d51805`  
		Last Modified: Fri, 12 Jan 2024 11:29:05 GMT  
		Size: 27.1 MB (27076957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc634b1051b605c11157b04818af197d321a38af2f15971ae60866a1b13a4cd9`  
		Last Modified: Fri, 12 Jan 2024 11:29:05 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:be3382d54b2db179e5191e22eb19b5fb3d186a08b289518fa739b0d55b46ce50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3240457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38f20d2276991ca979486f545b2b3e2a361c69223dc5a0d979e41218de45dd2`

```dockerfile
```

-	Layers:
	-	`sha256:21903dfec3cb351942170e90956f34922df5e321a99c1ea16cd32a3cee64b526`  
		Last Modified: Fri, 12 Jan 2024 11:29:05 GMT  
		Size: 3.2 MB (3222532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09dc1688fa90ea7157cce709b24745d48fa6599aac116a40ea2b8ef46c71bcc5`  
		Last Modified: Fri, 12 Jan 2024 11:29:05 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json
