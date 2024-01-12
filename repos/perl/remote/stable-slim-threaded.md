## `perl:stable-slim-threaded`

```console
$ docker pull perl@sha256:4a30149faa11d1821e7df4e2bd9341aff70f12098ce5233b0e8e23523c6e4c10
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

### `perl:stable-slim-threaded` - linux; amd64

```console
$ docker pull perl@sha256:ea4e35f5857481dfa294a675029821310d430e57752e0047cb06d68364d75a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57661030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd52933977cdbf45a88f460ee9ef6c271e4e10372c78da2faaf978691bc690b`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
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
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1a96f54e3ab69a9d7fa74690e81eae91c0c99c4201f248340b8cdd00e25b57`  
		Last Modified: Fri, 12 Jan 2024 00:40:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19476285917325cd7c4b15e6efafca937b7e9bb288dc84573c22e287a415b8b4`  
		Last Modified: Fri, 12 Jan 2024 00:40:59 GMT  
		Size: 28.5 MB (28534842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f201da3699fa873da1c2b7c07eb873d90636ca1d64dca201644cddd24b42e39`  
		Last Modified: Fri, 12 Jan 2024 00:40:58 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:b8921a873908746a93d8225c26b94ec8de314906c93ac619f9adfdb1a6294643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f79b974ba28ee1abb0e7054e9e68a4f205898406edbeb840b7cdf6b830482b7`

```dockerfile
```

-	Layers:
	-	`sha256:cc96a5790d556cd3ad3a37a19c82eac42c54ce47dc1d0d673755015362ce5bae`  
		Last Modified: Fri, 12 Jan 2024 00:40:58 GMT  
		Size: 3.2 MB (3232990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:151dcddf9e084b0b232c2c73cf32dda2ceefdc464d6e65237e462c8a563f2fdd`  
		Last Modified: Fri, 12 Jan 2024 00:40:59 GMT  
		Size: 18.1 KB (18092 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:abe3d90c359206bdeeabeca98b46de64e84ac813f4ed57d69178f9ca686dacd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52482403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e66ef6f081c9d62cc73ee0f2ebb6229e948412788cae87f5c9b52427b889cb`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:22 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Tue, 19 Dec 2023 01:55:22 GMT
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
	-	`sha256:1ae9a2844c8c70942d2220553689b62e841cc706d77284fbfedbd770080fd699`  
		Last Modified: Tue, 19 Dec 2023 01:58:33 GMT  
		Size: 26.9 MB (26885440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb33750918ac7bd05e898c5e3298ab4f7a4be54436237b690dcdf2522fa2a84`  
		Last Modified: Wed, 20 Dec 2023 21:07:04 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618de2b36e27e4028c675dcaecb2b9b41c97dd828223fba80a797c1211c38da6`  
		Last Modified: Mon, 01 Jan 2024 22:32:36 GMT  
		Size: 25.6 MB (25596695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fd5db2d2aae891632ed42591395b2f423d479a258a864b4da33ab12553a056`  
		Last Modified: Mon, 01 Jan 2024 22:32:35 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:df5f0bc22915f790963cfd4faf9bbe412fd2bde29783de08aee4924277e9285c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3225780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6870a0b066a366039a556c095997610592b0c4f5f3e3b9f4c5663a7578605b`

```dockerfile
```

-	Layers:
	-	`sha256:0305d107970b434d5371ff0d4db0fb7d255021f6c33401c38a81d0f2567f0b5f`  
		Last Modified: Mon, 01 Jan 2024 22:32:35 GMT  
		Size: 3.2 MB (3207737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b98c8fd0e8bd0b6819360f3678916370d12c1eec396934070e8c2ab5e49b80d6`  
		Last Modified: Mon, 01 Jan 2024 22:32:35 GMT  
		Size: 18.0 KB (18043 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:b622578d93daf012bf17f4a2e7b99b596dc0e06b8e4b699bfb2be5ac9539e79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49537820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d9cec6a6a7dd7f1547fc4577c970be454c3cfd5e71666bef703a347bf21b92`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 02:07:50 GMT
ADD file:aef112919e7924ad6da32181b1df5099cd692680c104118da3a24cd4dfe55a1d in / 
# Tue, 19 Dec 2023 02:07:50 GMT
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
	-	`sha256:65ab19615c01a3b542f77fadb3bd27872b6a20cba3e9269fb951de36d8fa6805`  
		Last Modified: Tue, 19 Dec 2023 02:11:52 GMT  
		Size: 24.7 MB (24718157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795fbd555a3d7b806e169b3c6883dd85433e85bf20598e85fc94b2c27f2a5b1c`  
		Last Modified: Wed, 20 Dec 2023 23:52:25 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c7309744f824442a54b6b8d1214119b2b2af9ec14f573c7ec242e5405b3a69`  
		Last Modified: Mon, 01 Jan 2024 23:44:52 GMT  
		Size: 24.8 MB (24819395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0472f6e9f02557604e4580f49773fa68596e17868ede4be3c1ad1aeaca4f9a`  
		Last Modified: Mon, 01 Jan 2024 23:44:51 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:a015a5783c1742fa2170c01a648ff41aca1a401a1a13efef55db3bc7514fbb91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3225644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b34749861a7f9f19938ab5455440ba1efc383c3e37a6d36d809a43e3a9c410`

```dockerfile
```

-	Layers:
	-	`sha256:061ddc9b037cba7ddda89072ca1ab4e8f4a16a35cb78b5ba2912ff04724b1ac4`  
		Last Modified: Mon, 01 Jan 2024 23:44:52 GMT  
		Size: 3.2 MB (3207601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a38b9f74c6d6da98e4d0488d4d9ac5fc19a58d9dca52bd55bff8ec19e2f742fe`  
		Last Modified: Mon, 01 Jan 2024 23:44:51 GMT  
		Size: 18.0 KB (18043 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:c865f453782cdb5d59d09c13432eae2569b820707820988d127d1195fae0e8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56458378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c43b048f458aae08e57f3c66cf711c17b37bf13c5b1510a47d46964fc1dfaa3`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
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
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9c66806b05448cba83c70a91f2a4bfb5488c92b8189737967cd97934c35001`  
		Last Modified: Wed, 20 Dec 2023 23:10:48 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb60409255d798763e734591fa742a42b485aa2766948a206909a5d4621ea006`  
		Last Modified: Mon, 01 Jan 2024 22:32:05 GMT  
		Size: 27.3 MB (27300842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0978f9018f1f0fcc271404afe3f8f95e66c0d3257d0d028b941b0d859d8d756`  
		Last Modified: Mon, 01 Jan 2024 22:32:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:403d06ca007ae37c34a116aba6a5763d5ca896e42da9043ce83099198b863534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3226131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e87a63fdf7d6f99ce94b33e5615040f509d565af1e4ce407a4f28022fb2de25`

```dockerfile
```

-	Layers:
	-	`sha256:b38d7c5c7c0406a11e9902a7feff21f050767485005b026fc02a170ec8de6453`  
		Last Modified: Mon, 01 Jan 2024 22:32:04 GMT  
		Size: 3.2 MB (3208184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a27f6ac67b6ffdbc4a81fcf6fcf4747d3e1501a08f859a497cf11e0f5586884`  
		Last Modified: Mon, 01 Jan 2024 22:32:03 GMT  
		Size: 17.9 KB (17947 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded` - linux; 386

```console
$ docker pull perl@sha256:57dac4c61dc6c2920d21797faa60a9f7d5fafe1c68d69fe9d3fd152a98441d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57727065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623dc12a7a48726af445a6dd2ff79f20151ff9d95846c46f97a83869bcdae4c7`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:48689786b7812032adc0d36643501f16ddee15750a8f0f8b614dba58e5037b2b in / 
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
	-	`sha256:de2bfe459016bec412fddc313b793adc6d47c8a4540608a6f3e217998027f073`  
		Last Modified: Thu, 11 Jan 2024 02:43:20 GMT  
		Size: 30.1 MB (30143875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d622dab9aab4421d9bcfd851300460aee846bb9c1027cd4b502940d676cbad9`  
		Last Modified: Fri, 12 Jan 2024 00:41:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20ee90bacc43e68097b695a3fbbfd4d2c8dc5d93da2e57fa11b739c279c721`  
		Last Modified: Fri, 12 Jan 2024 00:41:50 GMT  
		Size: 27.6 MB (27582922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8109424683563e67ce40ff1058a39eb85639d4ff4378d73adc70449cb64a42e4`  
		Last Modified: Fri, 12 Jan 2024 00:41:49 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:2c8c6bce98ea51c5c2dc2921e37b8e3a3b31033e6fe7e48bdb34694b374b691d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3245319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9257e02a9633be37a6f2d1e6ed8a71b7c6d07b1667ee3199e9ef4050ee709e38`

```dockerfile
```

-	Layers:
	-	`sha256:3395658637c54c49f694b8b204cf1e6d331408ae5dfd2537181a252e42b35fad`  
		Last Modified: Fri, 12 Jan 2024 00:41:49 GMT  
		Size: 3.2 MB (3227287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aa720148d27aa987a418a492b285b614180f019ee766538706c52ac0e889a9a`  
		Last Modified: Fri, 12 Jan 2024 00:41:49 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded` - linux; mips64le

```console
$ docker pull perl@sha256:93b6ab4bd377b37882c65e420e03e897a7fccd843e9d535f3915ae511be8abbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55804608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2b2ded04327eed2d1c39e72a663d88d8bc10f3753c48fa7595ced1346958a1`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 02:13:36 GMT
ADD file:dcd5696ac281b24df52a518e2402c7f7a4caedfcba0d82e195b7c06cd3a38fdd in / 
# Tue, 19 Dec 2023 02:13:40 GMT
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
	-	`sha256:12b1322ffb17b8e81ca1c6d9d7118e2fcee0b9d971aa3c90601e6345804a60d1`  
		Last Modified: Tue, 19 Dec 2023 02:24:36 GMT  
		Size: 29.1 MB (29121427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a73938a18f530616b5206e6bd2c5b2c974da3595b0e7248e1698bf2d6f2a7`  
		Last Modified: Mon, 01 Jan 2024 22:13:17 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfd19344befc17d4fc6f1e118aa960d745cd58397aefefb50566fe9299349a3`  
		Last Modified: Mon, 01 Jan 2024 23:58:31 GMT  
		Size: 26.7 MB (26682912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e2f642a9204591377e7a66d836c0a47b9cdf88a5613e12134cb9db9cfa6cd8`  
		Last Modified: Mon, 01 Jan 2024 23:58:28 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:a0bdc73e9d2907aaadaad626b2373ff65e2a580003fd2fcb00580472c0ad9a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 KB (17821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e2c27244434c2185af9aa707f4bbd5577a8139f13a4818240c5f214a9c1c7c`

```dockerfile
```

-	Layers:
	-	`sha256:dafa46b69bda8443d9d1ff57e15abc5c07fa6bef4a43f021ce3306c5349a6b4d`  
		Last Modified: Mon, 01 Jan 2024 23:58:28 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:3dcf6d8b8977cb050231ff5048f7ca4cc7f322e28f7d5d0b18c86258d9e62788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62241219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fdacf4b25d8a55c5cde0ba9a2de49c2f8dc452469e34f3d00ed1e984c85df9`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:50 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Tue, 19 Dec 2023 01:21:51 GMT
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
	-	`sha256:fc9b8f5eec3aa37ab3aace05165427479352f290d53904cea87dca6349633a09`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 33.1 MB (33120558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1da38e97da6a26aeb168fef4c89140f2a35cfce62a3cbe9c6741c30783003d`  
		Last Modified: Wed, 20 Dec 2023 21:45:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b4feaabed5a0a954c80c40a7ae7090a8530eb3481c7a6cb736b00ca2e09c0c`  
		Last Modified: Mon, 01 Jan 2024 21:58:40 GMT  
		Size: 29.1 MB (29120394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8196a647b1459d8736a631a2f2433d402f4fd18a8870ade58341934be5b4d63`  
		Last Modified: Mon, 01 Jan 2024 21:58:39 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:c64edc195049572392935f04bb9749e096423cc58867968141a01602e2676b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3239578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed10189023141041b3b08c4c29f5dd08c3f459ba00d61f563c5408caa82aef6`

```dockerfile
```

-	Layers:
	-	`sha256:997b6a95b728ee9b899f16dace5916c55015dcc21f12327ca56661253725e7ff`  
		Last Modified: Mon, 01 Jan 2024 21:58:39 GMT  
		Size: 3.2 MB (3221579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22666d6716010c5ead4fbcabd134502fcc590fa060608c6354d57e29ce027212`  
		Last Modified: Mon, 01 Jan 2024 21:58:39 GMT  
		Size: 18.0 KB (17999 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded` - linux; s390x

```console
$ docker pull perl@sha256:086868b2d7628c85403455e2e34a690b3a376c80ff51aa3c71b00a307b4200e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54550028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f453a6148d1df51d05c84e2a2e031c6c57cccb04a90bb41c333396579f1cc716`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:37 GMT
ADD file:f06f12fa5a93afc3a79ac4371d24b0a471a5a1818cf34c1d90004c8f410914b9 in / 
# Tue, 19 Dec 2023 01:42:39 GMT
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
	-	`sha256:bc6b1888979d3ceb063da848b2034e980e2c2613642159c1e856550b79aa620c`  
		Last Modified: Tue, 19 Dec 2023 01:47:38 GMT  
		Size: 27.5 MB (27491874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99d0690f588c171aa5e9a610966654592952c0b2087bfa4dba439d487de7e79`  
		Last Modified: Wed, 20 Dec 2023 21:51:18 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9b86c876fd32bd7c5a4a72d7469c3ae2e4e302f52cafdc4df8c7ace144b1b2`  
		Last Modified: Mon, 01 Jan 2024 22:05:04 GMT  
		Size: 27.1 MB (27057886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79368c645ec90df37617e0dd86d29ec2b50e2c9d1509a28c0329c50eb130fe2e`  
		Last Modified: Mon, 01 Jan 2024 22:05:04 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:bd5e334d191f7e251c422de852d8874c3af83cd4a5723b9024fd56cb5d20731b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3240457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acb986fb97ada9647afc8017b9df25355fe2ad9306aa1e33aaf60a646351b79`

```dockerfile
```

-	Layers:
	-	`sha256:15be461f3b4f645f323f1eef69724535e3f6a3677a8cc4c59fa892312a857c6d`  
		Last Modified: Mon, 01 Jan 2024 22:05:04 GMT  
		Size: 3.2 MB (3222532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c1ba0a0100ba1ad54cd81389871441e38ef51d2404ebcb2f430edfdffaf84ea`  
		Last Modified: Mon, 01 Jan 2024 22:05:04 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json
