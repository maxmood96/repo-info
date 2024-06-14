## `perl:slim-threaded-bullseye`

```console
$ docker pull perl@sha256:9dfe5e9d472bf1971c875a270f3a6862be890daf21b5793c440cac0e8213301d
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

### `perl:slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:1452862a486ca050844c20f073dbbb13f1fd229079d0692e84711730a8653b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56158629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a48bd40f5073800dd3199a8a340989abae2f6dc112a31e20668814e7e0dfcaf`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cce2df6334676aa42b65bbb1001812654679b8a1b4e9c1c0d40403e404944a5`  
		Last Modified: Thu, 13 Jun 2024 18:23:23 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d6508d59458d797d5d17d87186697ae75a7a710981e09f91e9db91a7082720`  
		Last Modified: Thu, 13 Jun 2024 18:23:24 GMT  
		Size: 24.7 MB (24724322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13885c846c5bdafe9ed8c06fe5cbf715121540d6ebd8852dc0b4af099f8c8a7`  
		Last Modified: Thu, 13 Jun 2024 18:23:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:373b309b860779131aa70e84e6b687d7d63a7b8578843471212b78112ae3de89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543008dc057a5a29bcbf2b4a2c96039c124e2b0d787e19516eb8e144d99e2ad5`

```dockerfile
```

-	Layers:
	-	`sha256:0129944e72db30651ad7771e59714644ea4d288c00f1c91d8fb3df31823f7a79`  
		Last Modified: Thu, 13 Jun 2024 18:23:23 GMT  
		Size: 3.9 MB (3913016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c38b69e5218d912ce5fbb64b798ef2a867f2f6555af835dd91435cd4876081ed`  
		Last Modified: Thu, 13 Jun 2024 18:23:23 GMT  
		Size: 16.4 KB (16395 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:6ed267a4cfaaee3c61e6f4425958fa27e6f3e5618f1f731488e72ad9742ff55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51644679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f0c88c87a79c89355b47a50919be1bb0656474612bce262d649d98277c1193`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:78cff0ed53bbaaa1d7680e733d50b8fc9042e257b78718ad822f9ac57a5d1dbb in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:f8a34d14f57d3fcf2d97b9fc0fb4439a2d00afe9411fdc788629eb4074186288`  
		Last Modified: Thu, 13 Jun 2024 00:52:21 GMT  
		Size: 28.9 MB (28936731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0ae8f294749be539a40bd366e564e2d03b722925a4033234d75ffd0f1da80b`  
		Last Modified: Thu, 13 Jun 2024 16:17:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b03dc81cc1235c3193e5a33b9dd2fc3eb2afba9abbed53eec99ef1b40ec734`  
		Last Modified: Thu, 13 Jun 2024 16:52:42 GMT  
		Size: 22.7 MB (22707681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3952594206167041a733969ddfd1c8fdedfb5887ce22d98c372aa6d210dce53`  
		Last Modified: Thu, 13 Jun 2024 16:52:41 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b927b6b3c8083e091c515a03f75d4857bbb6c351347056ee4620ca40c40bc7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3900702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678b16ab64d671585b5f9b6dbbde5bec783a4aef9d6a438216e057c0377e9a35`

```dockerfile
```

-	Layers:
	-	`sha256:3904152a26ce7416f9ca1305370a3a0f6a5150617356363353837ed125c695a5`  
		Last Modified: Thu, 13 Jun 2024 16:52:42 GMT  
		Size: 3.9 MB (3884229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b13dee592b09debda36a77554909f15eb41ae699e63f6d0fb4eebc152753369f`  
		Last Modified: Thu, 13 Jun 2024 16:52:41 GMT  
		Size: 16.5 KB (16473 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:2b70c4a4744bf17581a0c1fc8c4bff13bb0ba93de39dd72533f198408a74d1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48698077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e97dbb9bd17bf6d1066ed1c36ce64927c8a3b3adbdae038f33991a831bee9fc`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:b23992f77c1f22e7bf9048641d6da1d6ef922d78b4118f6d513e183ae6de7e34 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:4873d96591a32d2d686ff6c86338fc9a63b9d60639482601b5402eb76e56a566`  
		Last Modified: Thu, 13 Jun 2024 01:02:22 GMT  
		Size: 26.6 MB (26594507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc64ba5c0a09acb44449e9f17060150c215daebad392198774a82abad9a28a21`  
		Last Modified: Thu, 13 Jun 2024 20:35:35 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec6d85ffce76c15bea84487b0720a490104d030dfd86c5589c908490c09767d`  
		Last Modified: Thu, 13 Jun 2024 21:16:43 GMT  
		Size: 22.1 MB (22103302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730edf9c14514fd7834ee60cd273b5dbee3f574c9466006d2ac06da21b81fe17`  
		Last Modified: Thu, 13 Jun 2024 21:16:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:7a6c2e1b940e19206f6f19192b2cecced22237e375711d19093e0ab3e384f53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3903420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538626f8799220f4f2d3c82575bda652abb67af88faa24a94fcbe10d1a67eb2d`

```dockerfile
```

-	Layers:
	-	`sha256:c44a898246b28fbe158d34cb36a859ad03852bd0b85d392b36da24552d935e42`  
		Last Modified: Thu, 13 Jun 2024 21:16:42 GMT  
		Size: 3.9 MB (3886947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a446d6d6a42a3a25a3ca4fbebf117fc84a0eb8fd08df33065a00ccddae4ef3`  
		Last Modified: Thu, 13 Jun 2024 21:16:42 GMT  
		Size: 16.5 KB (16473 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:9ac43133f76ee64ae75213910e7e836934261fb30d5b714e0431a6b7c4158907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53922496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9917193854b969a53174897bb0bf17c51ffe6179e8cd36936affd6f39b715b3`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44faf59f76a42bb4eb0bafc838ae6caa176097b389c1636b798e3f9bd5ca08eb`  
		Last Modified: Thu, 13 Jun 2024 20:27:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d3c1649844f32e972e8a37198379c79fe1303242c7f30081410473a62d2e2c`  
		Last Modified: Thu, 13 Jun 2024 21:12:07 GMT  
		Size: 23.8 MB (23835256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50e7da23f6d603e2a9e700f24bb4e5e6996619ea3e21285fc8491ca59f194cd`  
		Last Modified: Thu, 13 Jun 2024 21:12:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:98ce4d4681a9c80d01e0de851f04c0f4df9a749308ebdf691b26710db846bc0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3e6cc51d3a5e086d5e2e956d3b554e49b9ce97ee43d8b88db0810afe1ff123`

```dockerfile
```

-	Layers:
	-	`sha256:4ae039a9c850b05514f09b264f276a79df70c20a89c8fb79527246104a0e4004`  
		Last Modified: Thu, 13 Jun 2024 21:12:06 GMT  
		Size: 3.9 MB (3887389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06799e97d0b3c264d7bfcbf418ecb71b0c34296fcb7aa8c2002c1d2a7658d372`  
		Last Modified: Thu, 13 Jun 2024 21:12:06 GMT  
		Size: 16.7 KB (16716 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:f82f820ac1345c7f5789d4b88dcfa0c68b7970aa906012ac6c914524cf54908e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58614794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a5422c6a37d168b98084db7694345114895faf9d94f667e2a7e7369922b78e`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:ef80ad838dee1f170442a02f8d0808e624e7c317df766c49aec042c1f3ac4732 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:71e749b27156c50e0706f9267afd1ca9fb38d6272a353964948602fb62336fd8`  
		Last Modified: Thu, 13 Jun 2024 00:44:08 GMT  
		Size: 32.4 MB (32424179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9ae3e274dfc7601668652743cc5d2baab3fd891b9a015b6c5cd73b60135b90`  
		Last Modified: Thu, 13 Jun 2024 02:14:17 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88624333e6d848b685d729a3ca68d70ebbbf267902f221cff32cbdf7eca80682`  
		Last Modified: Thu, 13 Jun 2024 02:14:18 GMT  
		Size: 26.2 MB (26190348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a88ceb4009128edbdc1957751af93245bc9f2bf4a66af0998a880a51906dd9`  
		Last Modified: Thu, 13 Jun 2024 02:14:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:70e645674ee8d473cdd4a29acfe73882377d85a1f92b59ad0597b8bac75f33bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3933628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dcf80f3fc278aef85b1d801687fd9bbd811b4855b75ca11c14508e086e7dd0`

```dockerfile
```

-	Layers:
	-	`sha256:045857edc63d0d08225d8d967d457e9dd7d12935ea0d58af11472157f8ec4e51`  
		Last Modified: Thu, 13 Jun 2024 02:14:17 GMT  
		Size: 3.9 MB (3917267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55a1d72521ea40abb68349578d85dc53c7ef873098c890868e153e6b4bc3355d`  
		Last Modified: Thu, 13 Jun 2024 02:14:17 GMT  
		Size: 16.4 KB (16361 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:1de61f42f912ccb1d2a5a1531593f16a90c78b7d694ad994ee2059e77c542454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53282269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eecdbc85436b17ec88544118b8fb64a601839af66e72da2f0074631d946cd1`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:12:23 GMT
ADD file:ec3acf4bc32b149c2b67d1b2c5f3a6d1f16fbae266ac16c115e1fca276b970e7 in / 
# Tue, 14 May 2024 01:12:27 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:38917083d8284ce1ec7533351600bab5d64f8295f3edc5dc651be130fb9a4bd4`  
		Last Modified: Tue, 14 May 2024 01:23:44 GMT  
		Size: 29.7 MB (29651870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe483630a5cb8e6c8d1725076f5d5a8635310f06c789c5625ab06d20cbf74814`  
		Last Modified: Mon, 10 Jun 2024 22:50:17 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fab323897a2ba756484bf97ded828b53c6b022831d44cf30913fe250c65775`  
		Last Modified: Tue, 11 Jun 2024 00:49:33 GMT  
		Size: 23.6 MB (23630130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aec074e36b8c5d4bc78a6fc5f6cc10d9cb24c121542e0cd9bce16b799f3e5f7`  
		Last Modified: Tue, 11 Jun 2024 00:49:29 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:3056b62fc66e55aa3417e0fca9256bd729bcacbe5888e79ab0acb8c95ce9cb46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 KB (16240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1479f9bbe22e4e1c899874cbccb198e6e967738873977d3257a8dc0d9ba959b5`

```dockerfile
```

-	Layers:
	-	`sha256:f9fdc1423a01f2ceb41d42cfff19cc0511bf65bded26daf49bdefc5f5e157dae`  
		Last Modified: Tue, 11 Jun 2024 00:49:30 GMT  
		Size: 16.2 KB (16240 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:69061b7d90dbc3ea5895eb64fa3e2b207b614f44c20c8e88a715d54c3f444be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60320169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be72626eebcd2664c68e789be0eb17ae4f3891462216176d21d47e4cd44b99b0`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:a150537fc528657f8fa98f90c4629e38f111c3c3ef60bd40c28205959899c1a3 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:64741f366161eb41a5c86810e08ceabb9f4e4b69ac16c725aa2d48f19486e1be`  
		Last Modified: Thu, 13 Jun 2024 01:22:19 GMT  
		Size: 35.3 MB (35311302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487ed6caa49eccf6882b53c3a997df7895565e367ad4f42bb10a1813b2db795`  
		Last Modified: Fri, 14 Jun 2024 01:41:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7707b8d1b5dec40f54fe160e2dc3cd97898c985455c06f6945a57cfca43c9af0`  
		Last Modified: Fri, 14 Jun 2024 02:08:35 GMT  
		Size: 25.0 MB (25008600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbac1cdcc3cc3a1da89d4dc53e4966c7847e90446d90779208dfd671150998e4`  
		Last Modified: Fri, 14 Jun 2024 02:08:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e24a05f5290bb0644aaa23ae463927666040412b2d7c730eec7f38e84afa030f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944d314f656ecf46593ba8276720456fce72b50a2c19530fdc3220f13f5c9a8b`

```dockerfile
```

-	Layers:
	-	`sha256:23b93c783c247afec4dc7816b9273f041f68088cb6e56e8ff2acbe687897f4d5`  
		Last Modified: Fri, 14 Jun 2024 02:08:34 GMT  
		Size: 3.9 MB (3901783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf50ed32eed370619bf56a4e34e71f565eb85a0448cb4f14f7e8598ddeb771c8`  
		Last Modified: Fri, 14 Jun 2024 02:08:34 GMT  
		Size: 16.4 KB (16439 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:761a4e015d81029aee4bd870f996c719cc86e0d48cf8c974eccdb41b06912eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53623967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fbedf38bf983960ff4b3a3cd761836b02acfe65fc91d02de5317aee226855b`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:dbc45f2c1dc4ae2fcf0e05b8c9401406afd0f7aa3623659e470bb7d0fb97f9ec in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:b9966e11fe1c4138e9aa4f0356568463c21e36009b72062413bb596e0e57738f`  
		Last Modified: Thu, 13 Jun 2024 00:48:17 GMT  
		Size: 29.7 MB (29673762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f42879926bc8b1feecb767b5ebd156762636935180d3837a897af9070639ce`  
		Last Modified: Thu, 13 Jun 2024 10:20:12 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac90ae7a55041993e0fa957c81fdca68ec48c05f85675ac53dca79a7822872`  
		Last Modified: Thu, 13 Jun 2024 10:41:15 GMT  
		Size: 23.9 MB (23949938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53282195044a94ef0f5103702d1df8640cebd876d1da6673c033b4e7cf5d588e`  
		Last Modified: Thu, 13 Jun 2024 10:41:15 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:88c63874b4d59a45d53e767d0b8c02f182e6e6993abd617e8edd34e7a5a4bcba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2bf207f19675c227d855f459c126b13b1c9f129dfc71dadb90b2bd5e4145f2`

```dockerfile
```

-	Layers:
	-	`sha256:5e98158c69010dc04efb32db92845598b12cf0f0f0192c5d5750ab5853d1dc82`  
		Last Modified: Thu, 13 Jun 2024 10:41:15 GMT  
		Size: 3.9 MB (3901718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b68c36a0d745ab0ad8b3f70383d01378638340d6e4c2470de7f443fbb07808c1`  
		Last Modified: Thu, 13 Jun 2024 10:41:15 GMT  
		Size: 16.4 KB (16395 bytes)  
		MIME: application/vnd.in-toto+json
