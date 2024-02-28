## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:a780178d20a27df596d714e1979cb8413ee282a83d11701c409cd9baa72bd42d
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
$ docker pull perl@sha256:dd999b4486f6635a267538ab73a0736fc7f530427571bd693e8c41cf0f327eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56226593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875e861568bcf2d4536caa48c4befd321f2566c1696c68dff246f05566ec7c10`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
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
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d7b5da8de63df08dfca75d1788e1c4b3980bf37fb12f13000329fe43ad3f4`  
		Last Modified: Fri, 23 Feb 2024 18:58:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d9691847aa7c7d8e309aa131d86de0e4eb86c9281f39ba082876f6a07172f`  
		Last Modified: Fri, 23 Feb 2024 18:58:12 GMT  
		Size: 24.8 MB (24803901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f604a4e4387a78187111a91d874b71eeee6680e316a331edf7ae7a54d5feb9`  
		Last Modified: Fri, 23 Feb 2024 18:58:11 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:59e8803853590956b85f96fc8ede5cca4d38344b9d91645d09e0508a4e01a24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2917cd4cc44c9e0e8c8c11e0de0e629fae0190fa87c0d02965cca4b3f63f3f2`

```dockerfile
```

-	Layers:
	-	`sha256:62755d45e1d5409f2352efc7ca77c62320a28c03a3e4a76be41144de5b3be024`  
		Last Modified: Fri, 23 Feb 2024 18:58:11 GMT  
		Size: 3.9 MB (3912135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7eb052668de5a0bc5ba1fa4dee4f2b1fc3a925ffbc54c92a29978254e9ab20a`  
		Last Modified: Fri, 23 Feb 2024 18:58:11 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:56aab66a743258bdf33aeffa93ad22aa27dca097097f6efdb2e158c902c5de01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51733187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c719b513237b6ea398b6ebd46a488da39d5855b669eea4ee0e121681308bfb`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:51 GMT
ADD file:2900145429df7cd46dd4818f44636aff96d0ef5335d5eb8cd5ed3106caa8b031 in / 
# Tue, 13 Feb 2024 01:08:51 GMT
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
	-	`sha256:237c1c7c36842faaa132f240658a3f42b8e6adb150f7850dc25fb4b50ed242ba`  
		Last Modified: Tue, 13 Feb 2024 01:14:18 GMT  
		Size: 28.9 MB (28924482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da666543b4d0f9348cdbd248edcc4410b1f285ea1785e67ea343bed4312a1b64`  
		Last Modified: Tue, 13 Feb 2024 19:03:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ccd40c430175124f53700bf15cbcf9eac7be791f5af7f7c37f01de63b46787`  
		Last Modified: Fri, 23 Feb 2024 19:52:07 GMT  
		Size: 22.8 MB (22808440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9db1bb3d65383c3d77daa5ca8892f08d0f26a40898c3f00e68c09b3a11445b`  
		Last Modified: Fri, 23 Feb 2024 19:52:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:1a1b0c0d62a29a5d582329385c4920c35452624a64594bfaaa5f1286032ec128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3899050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaaceaf4c747cb17b843ce9a1f95ec3519b95b62eb018f74952370f5b30e684`

```dockerfile
```

-	Layers:
	-	`sha256:a328faa7dfd671177be27a2004c1201ca31246f9ecd0410e4ca992d80ac4c44b`  
		Last Modified: Fri, 23 Feb 2024 19:52:06 GMT  
		Size: 3.9 MB (3883334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9793c82e9ac1ec3dc04cab930d093f2dbb1534bc4c0787c2045f53ac72897d5e`  
		Last Modified: Fri, 23 Feb 2024 19:52:06 GMT  
		Size: 15.7 KB (15716 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:8e3ae9314775a03d92d1e885b8b737e89bc60be59c82a60ef5b8ea2352fc26a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48800797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ecc1dd969d7b16a6e63ad2462df893bde0ed10876de3fbf365c1578638dbed`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:39 GMT
ADD file:8904abb8948cc1601202f5f3dd63ae52e3b980ac6acafff765b9424bfd5defef in / 
# Tue, 13 Feb 2024 01:20:40 GMT
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
	-	`sha256:7c57dc7cd6a5cd2a6636e8cbb774969d6394ce3ef35cb0d229f5cfbcd8ada61a`  
		Last Modified: Tue, 13 Feb 2024 01:27:40 GMT  
		Size: 26.6 MB (26582672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747b2e1c3235665a1332104c30fd195ddf61f88a0958bcb327bcc0946161f473`  
		Last Modified: Thu, 15 Feb 2024 05:13:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e462d50ec35c2ea91f7e30489571dbf1179953223d18c11871beef45c136f2f`  
		Last Modified: Fri, 23 Feb 2024 21:31:20 GMT  
		Size: 22.2 MB (22217857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b84f143afffb160cabce6d60909222aedbd8937972b402fbec0e3bd8f6ac41`  
		Last Modified: Fri, 23 Feb 2024 21:31:19 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:0a26d3872294b254e5fa33d0347bcfb5fc0205cd4fbc9590d1b8f67e841f987d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3901768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba822602507f182670a927eb99dfa7bf8f080ecb1e69766a307b7f7e7c3200f`

```dockerfile
```

-	Layers:
	-	`sha256:71fd7dbc136090d24d48635202070aaf6781ee4e6ba0f41b56a0c82fc1b55a78`  
		Last Modified: Fri, 23 Feb 2024 21:31:19 GMT  
		Size: 3.9 MB (3886052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5fadbf38d66eae5d46397567cf1ba26ca52bd1ceead80424bcd9ba70761ff98`  
		Last Modified: Fri, 23 Feb 2024 21:31:19 GMT  
		Size: 15.7 KB (15716 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:0b77101ea55711ce5e270795154b0ae034644b643cf6e18291c367c0188bc0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54010368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0021da894533dc3f3089a3ce6e9eebacdf3177c68672eb264bcd57cc7779676b`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
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
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02913a28b83b97057689db6abc20e6038fa7d6ecf743479e7c2c131b466625d`  
		Last Modified: Wed, 14 Feb 2024 02:30:38 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f033ecdb21bc79e4872986d7da47ffb1232267cb2b6d89c15c178ecdefc7b02a`  
		Last Modified: Fri, 23 Feb 2024 19:47:26 GMT  
		Size: 23.9 MB (23939025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c4e0fa6f767e2cce5d4e9b629aeb7e3cbd8e3e0f5eac16f94ab9e06a9264bd`  
		Last Modified: Fri, 23 Feb 2024 19:47:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:27ac2262391f69f5c3e61dae9c7e02884d4e5270efc217cd421e5f93d0581f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3902113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedc96428caa1b3f03db76391428f9ef1a9d4c69b8a66f99d64f7a4f79b719b5`

```dockerfile
```

-	Layers:
	-	`sha256:da075a8813102c9487e3c518739fdda94cadc20c3e2181710d0c42c2b8e9e4db`  
		Last Modified: Fri, 23 Feb 2024 19:47:25 GMT  
		Size: 3.9 MB (3886451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3b7cdcaa6bdd97175a6d9fd1a26535d9bb0e1963ef9f84cf7e2096e0088303`  
		Last Modified: Fri, 23 Feb 2024 19:47:25 GMT  
		Size: 15.7 KB (15662 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:5bd80ecd0cb7599d2287c4dc121c171781d9f89067848c9135654ee36c5f358f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58635988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05825efe4556526db7fac0d267c07618d3b81d30d12b3ef7de7d67a9c5ea952`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:18 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Tue, 13 Feb 2024 00:39:19 GMT
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
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c10ee28b53046dc58d75063f694d053ee62b608ad42849d0ccaf38439e731d4`  
		Last Modified: Fri, 23 Feb 2024 18:58:47 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f87db3bad359688f01d3fceb9fe9c7614f5fe16d4d9cad3d3ac59b91341fc9`  
		Last Modified: Fri, 23 Feb 2024 18:58:48 GMT  
		Size: 26.2 MB (26228277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18865cb39aa5141ad5f72f23a1bd9da8c904ac72704d0f6a053d532200dea3a`  
		Last Modified: Fri, 23 Feb 2024 18:58:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:80d90f1a8a6d9a72e0b20fe51c2da39544ae38259ea0a5638a175ab9bd7f971f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae8b2eb56d4729124bbce385dfa31a885e46978cff2aeb34aea201a8bd449c1`

```dockerfile
```

-	Layers:
	-	`sha256:a814b58c240e3e92ee5d511cbcc87188bf6f3e73515670764a583b770d6aebf2`  
		Last Modified: Fri, 23 Feb 2024 18:58:47 GMT  
		Size: 3.9 MB (3916398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dbe8bd0f33522c24f53c82a04d291a6a8551fcba33b2695696fa588b454117b`  
		Last Modified: Fri, 23 Feb 2024 18:58:47 GMT  
		Size: 15.8 KB (15796 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:e676155678af122e4060ee61419e973e09233b556091b7c1289984593a322718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53341705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74864931f4341a9325735d874f09e7971c437e4dd01d1dbc087c3eff7f98366d`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Tue, 13 Feb 2024 02:05:30 GMT
ADD file:aec249f679ecc1ccad460833afd79f8f10ccd9378d1275ed1f23fa98cf3f99b6 in / 
# Tue, 13 Feb 2024 02:05:34 GMT
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
	-	`sha256:c99d8d33768bdc2aba62f6b3cc956b807c30b43339ac2ffa3db52a47112dd416`  
		Last Modified: Tue, 13 Feb 2024 02:16:36 GMT  
		Size: 29.6 MB (29640432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb544dbc731cdc51c6df2d3b407b92413557073375a6863ede76d56c703d0c8`  
		Last Modified: Fri, 23 Feb 2024 20:31:19 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cf4ab7bf82030bcfcec518927a52852abb16a526140322e7a2f5e7cec639f0`  
		Last Modified: Fri, 23 Feb 2024 20:31:22 GMT  
		Size: 23.7 MB (23701008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0998ce7c0d6fd1148fc7b01f7c3659960480cd7cda7887da4b3ed7767459065b`  
		Last Modified: Fri, 23 Feb 2024 20:31:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:5b53b4bd67424e13ad821a1c0aa502a4786a567f402eb5201e0eea5b9576cea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fa04b6842dfc09532f97a069e56a58fdb40a02f6e4a3c2bb2622f5ccd08d77`

```dockerfile
```

-	Layers:
	-	`sha256:5c5b6ff54cc8da4002dedcec3b306e054efcbfb90e8e9bd1341722e8a4e5db94`  
		Last Modified: Fri, 23 Feb 2024 20:31:19 GMT  
		Size: 15.5 KB (15487 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:074f4b12785ebc5ffc63861ac2ad7fdc2886d00225eb3c93dddca32ef4976c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60346671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120820110a2b3bcdd34bf2e0feee4796915fc381828ff418f56217f0021ccdb5`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:33 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 13 Feb 2024 00:39:36 GMT
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
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5fa2395561c29fcab6c2af2df46909d89e22188240f9fcda7a13cf9c82a6ce`  
		Last Modified: Tue, 13 Feb 2024 22:58:39 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eae4f322b9e035db9475033dfb5f2a85efa7d83136c9a46f01c4591a08803c`  
		Last Modified: Wed, 28 Feb 2024 04:23:52 GMT  
		Size: 25.0 MB (25048607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2134e0055663032961f7d01993a9899d76d1036bb5b7579e608f7af6301bb002`  
		Last Modified: Wed, 28 Feb 2024 04:23:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e00035b06f756f6a8415d144a7eb75fa9a9e21972bb74a71fb2ef68ec8eb5d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7524838f51a0adf833f4cf38f5465254c0eaf9063aef700cabedf39974f64a8b`

```dockerfile
```

-	Layers:
	-	`sha256:6da568453eea258e17aa737e3023e77d2b88d5a792b448ec0938d92038ba8938`  
		Last Modified: Wed, 28 Feb 2024 04:23:51 GMT  
		Size: 3.9 MB (3900892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfad3126327119be57b1aa5713781c2efde39ea4c2d2862d7bfaaca7efb63ed0`  
		Last Modified: Wed, 28 Feb 2024 04:23:50 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:35e547d9a31bf0841276f073c2e1c3018d359841c305b7d1b9bf77efff1f1d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53677221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8fc17d5e7c9f5234315b07fffb9d4f1856324bef90d9e322f1b6823e05de52`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Tue, 13 Feb 2024 01:06:13 GMT
ADD file:08d247ddc5feae7a34870daaf7096c41de9c1bb9fc04bc305db02fe94b34d2e5 in / 
# Tue, 13 Feb 2024 01:06:15 GMT
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
	-	`sha256:2ac5fae051fa0d97737a12baa9ac705d62ae16e9a4ae39eed54e3f977616ce05`  
		Last Modified: Tue, 13 Feb 2024 01:30:53 GMT  
		Size: 29.7 MB (29660168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75e6830cf0f38e67c061f6b41fa477c04816afb6ab159f3556c578338b09356`  
		Last Modified: Thu, 15 Feb 2024 06:59:02 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b23f828cfba71107163cb191a73fe472b8808ef6fac5e19655e9c0312d84818`  
		Last Modified: Fri, 23 Feb 2024 19:34:07 GMT  
		Size: 24.0 MB (24016786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91969123ab4069140f30e02a49e99a7101f44d25fe176d81428d2194c0763ad9`  
		Last Modified: Fri, 23 Feb 2024 19:34:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:74f31983eaf179523d4057bcbe1ea2dc105c22c3be87cc8978cf20e3f1e81d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f62e40d7c5584d1301d9761cf8f3283be87ec25b1aee9a82f451e0124b77189`

```dockerfile
```

-	Layers:
	-	`sha256:895445d7a519036db7496a2845d3882bd881a5560c5a8d03ca5ecf7c68b9520b`  
		Last Modified: Fri, 23 Feb 2024 19:34:07 GMT  
		Size: 3.9 MB (3900839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae30044b6ee4f54ee76ed25fa68728e58861b82c08f4096b70d197d550483400`  
		Last Modified: Fri, 23 Feb 2024 19:34:07 GMT  
		Size: 15.7 KB (15654 bytes)  
		MIME: application/vnd.in-toto+json
