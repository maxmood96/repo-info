## `perl:stable-slim-buster`

```console
$ docker pull perl@sha256:b47838165dc0d3e238acdec5d95e8bbcfa89f4d9c52ab115ef9e51f84e6a54b0
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
$ docker pull perl@sha256:02ed6c9c38a495e976ceafa81ccec81e238747a6a7a19506f86bf223930f77ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ee22c586de0b5cd9efd26319b1d31ba96a8bcd82c773894b7dca07a15575c9`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6528f95d41202ca8d1c6d911ecb81bd278b653a11068da26fe51611d54169f7f`  
		Last Modified: Thu, 13 Jun 2024 18:22:56 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac8e12b8e3093d75e41c92f6f9ddee3ec5aabb8a5ec58493432d8658cb19f12`  
		Last Modified: Thu, 13 Jun 2024 18:22:57 GMT  
		Size: 27.6 MB (27629889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bcbd12ba31c36651f0ad50d6f8dade0ecf01c1041b7710774edb798059023f`  
		Last Modified: Thu, 13 Jun 2024 18:22:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:e2e7ac8252e2379684a320ed871e7723fdcd03788ba2f364c624992647006729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf2bb8ebb5beb3d2da777d554f60db1ef2ee11232d0f7bd823ef4c923a89b22`

```dockerfile
```

-	Layers:
	-	`sha256:7242498ccb96b3f588b4de758b5e42cf8fd2f56ed90cd21826228be8234311ba`  
		Last Modified: Thu, 13 Jun 2024 18:22:56 GMT  
		Size: 3.7 MB (3721513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:176da09d5c3b2ca75491a5baa730f867ee8c03cdfed8971386d279b943301f42`  
		Last Modified: Thu, 13 Jun 2024 18:22:56 GMT  
		Size: 16.2 KB (16221 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:2fbea2e1055b2a271eaeffe2890cedac6c569042b99152a3c68082066d17a31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47153189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65016bad45c5792371e195df3fac7e88da95fd7a2ef8b8f5d26052b8b27da813`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658c5ada6e8c0a45991e1930c7547e406dd011eaa1254db1a0e8d0c9ec903edd`  
		Last Modified: Thu, 13 Jun 2024 20:41:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55142a4c4de1b3239aeac288e922499d4222a0b87012f5fb02e45d2987592053`  
		Last Modified: Thu, 13 Jun 2024 20:41:50 GMT  
		Size: 24.2 MB (24207923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff531c01d78691880c386dabd8278e40d3d1b5d569100dc09a98910a9ed2c84c`  
		Last Modified: Thu, 13 Jun 2024 20:41:49 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:c9a3bc09062f9c5dcac9362cb9ae70243274a475bb7d3fe81a9a383bdcbe1e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bc242a588c2c2509246a43b18c5284dbe40d8a0017c17229d27d9f69fe44e8`

```dockerfile
```

-	Layers:
	-	`sha256:28e8a9d3b8b40607c4598d5a33a4388b1b7d79c27e579fa7389ceef91c0af0e1`  
		Last Modified: Thu, 13 Jun 2024 20:41:50 GMT  
		Size: 3.7 MB (3696731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:057cb6dbbd243af38f6f136959e11c39dfd5313171683c2d0be85d55d0df28e4`  
		Last Modified: Thu, 13 Jun 2024 20:41:50 GMT  
		Size: 16.3 KB (16300 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:2a3efd9f824183f6c6c4d34e227e61b4d7482d2009a6d3d2c472ab487fe6f8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52373590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8248ebbb25f0cf1eb705ff77f03d5346dcfcc66606964d56f96aa901092d0e`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3f9298c7f02650937c93175bbdc2b0ea273152865f7e8843f02236c49e74de`  
		Last Modified: Thu, 13 Jun 2024 20:33:12 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d481ff84abed2e6bd2523d4f32441f47c8dd1d5e16b790538e31c266f38cb0`  
		Last Modified: Thu, 13 Jun 2024 20:33:13 GMT  
		Size: 26.3 MB (26264050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a4a83be7d3af3c3bde2816e5cb29fea715794472fe8dd4cbc96dacd3f8e13b`  
		Last Modified: Thu, 13 Jun 2024 20:33:12 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:533bba5dddc4092ffab76d4c5a05d7ba4af9b14df7d507a6d8763d92cffb0aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3707581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f77594963f30d02ab9a6da54c92970e64ea9cb9902064981d2664213905aa1`

```dockerfile
```

-	Layers:
	-	`sha256:f09ecb77392af8866dcb1a32b3c6d32bada41c9de1fc23aecb2aed1edec33062`  
		Last Modified: Thu, 13 Jun 2024 20:33:12 GMT  
		Size: 3.7 MB (3691040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a982bef26c2ec7ce62bac77a39e576dc9bea4a3c1709570ee39b4e74c6a53c5f`  
		Last Modified: Thu, 13 Jun 2024 20:33:12 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-buster` - linux; 386

```console
$ docker pull perl@sha256:0dccc0a8d351017ce09c716efd8ec2979c94a778efbeda26e760d8228b98b8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59755277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941ead62cadb4e598352800c6b665040da19ac44a553856e017bfcd3f78561e1`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1d343c9066849c940931daf49aac8a64ac58cde9e2dad40fce7fd2a5e2e1e7`  
		Last Modified: Thu, 13 Jun 2024 02:12:21 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130c80f9df9d8406afc306000f733642f049c0da4dabf339ed786bfadbdb0c3a`  
		Last Modified: Thu, 13 Jun 2024 02:12:22 GMT  
		Size: 31.8 MB (31760370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403add8f1b305aa081223d74416a1f10888cc759530427f24d53f1a88d925ff6`  
		Last Modified: Thu, 13 Jun 2024 02:12:21 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:970fa0b537baa33922129b1935b7b5c7246f057bf2dce7e0dd3eb51bd4cabfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041822f7f571ee9e8a3b2df414ed71fd7c1e58af193d42c15151f5dedab0d867`

```dockerfile
```

-	Layers:
	-	`sha256:83a2bec33b92364f1ba0ea560f4a01a6e3853b16eb553f8b0f4617d4036285e2`  
		Last Modified: Thu, 13 Jun 2024 02:12:22 GMT  
		Size: 3.7 MB (3740310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:741c563b18f9f4912450fb8995101921345f608beb961df261f1b6989bda48d6`  
		Last Modified: Thu, 13 Jun 2024 02:12:21 GMT  
		Size: 16.2 KB (16187 bytes)  
		MIME: application/vnd.in-toto+json
