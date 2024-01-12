## `perl:devel-slim-threaded-bookworm`

```console
$ docker pull perl@sha256:606a9ee461e34d2e4e5fde6d768f809afcfa066211676ec78130d4df78d3677f
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

### `perl:devel-slim-threaded-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:c7c974c13db985e0e3e4502cb116470c16194847f1efd79ea8fa3fe651977fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57869350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0770d1ef0a1c2ed721cf8c85fe40d69a53d1d5c2391862c02f393298820e6a5`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f4d9773aec148ef8bb9a9bde0392a16d03aa65652e6c0a48cb23b5816977d6`  
		Last Modified: Fri, 12 Jan 2024 00:31:51 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767cb531e38e07debc3d4b3478237e05bbf99d15a5b569fab89b0ef432049ac0`  
		Last Modified: Fri, 12 Jan 2024 00:31:52 GMT  
		Size: 28.7 MB (28743162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc609035bc2b51f5ca18795816e461ed12c3bb7a691fadb65830af61634e9a`  
		Last Modified: Fri, 12 Jan 2024 00:31:51 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:1bffe536481103fefdd4ce732999229ceabb8c89b8c021dac300cee6bc18a2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3248590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c382f6a202505947802515a797ad523d3045c3ba794b3a99dd3f25f41c1bf0a3`

```dockerfile
```

-	Layers:
	-	`sha256:b6aac7d784e6976c0994b2551ad24beb8c5248430e5e6688bc97f7c4b42c5226`  
		Last Modified: Fri, 12 Jan 2024 00:31:52 GMT  
		Size: 3.2 MB (3231710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d01e430854741fb21b03fedecd63bfaa93fa6bad58fd29fc5fc42e7a2787b22c`  
		Last Modified: Fri, 12 Jan 2024 00:31:51 GMT  
		Size: 16.9 KB (16880 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:d73ea03391b7de8bdf0779d750c0d18cb2af70f941b78cb89796b94990a8bdb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52700784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7605d3e9e2c72ba0f9f8be21b07c0bf2a4f29823b6760de6ab065bb700c24e75`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:22 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Tue, 19 Dec 2023 01:55:22 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
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
	-	`sha256:1cb1711728134c18aa14daa5c8ba2c4d535dc7f16e5623f15fe8d5d477c415bb`  
		Last Modified: Tue, 02 Jan 2024 02:45:46 GMT  
		Size: 25.8 MB (25815077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3648db5e7f2f90c7b018cea830e0eefae33c7fc5497946a00540ec5f8d25c0e`  
		Last Modified: Tue, 02 Jan 2024 02:45:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:0aa0e9e60b32fb2defbb1771af4fdba241130eaf4717a014eae012915c96f75b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3223223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c4e49d1c9803392fb0d4b39ca46d8321a7543f4f3cc8606e1016e416dd4e08`

```dockerfile
```

-	Layers:
	-	`sha256:8c03303b2db40b0523ce0e47481cb1e59e2165ccbbed21173dd91025a50526a9`  
		Last Modified: Tue, 02 Jan 2024 02:45:45 GMT  
		Size: 3.2 MB (3206425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe97c7bd704dc920a921c23257ee06931a9f21f1d2123721aac95ad66dde6067`  
		Last Modified: Tue, 02 Jan 2024 02:45:44 GMT  
		Size: 16.8 KB (16798 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:0694eb571f72f2f03fb281c78d7335128803b9f076bcf8e6f65cec162823512f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49739437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a757299b9900c901bbc78f42fd6ed7ce61fe9634565970a2a4c3e864c6a0e62`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 02:07:50 GMT
ADD file:aef112919e7924ad6da32181b1df5099cd692680c104118da3a24cd4dfe55a1d in / 
# Tue, 19 Dec 2023 02:07:50 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
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
	-	`sha256:b4173f9aefa8c96de1975c14931f2443087e425e534109cf87a1e176b87518f9`  
		Last Modified: Tue, 02 Jan 2024 06:57:12 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda66b39fe6e03ab16b56cb2e945b022b0558a01d511e4944c7a84fd5edbcc2a`  
		Last Modified: Tue, 02 Jan 2024 06:57:11 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:c6950efc19d07f5968d9214e77842342b0dbcf10e09d02e1f6045e52dc2ec0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3223088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096454eba7b131645678ae06eb9badb95c3aa63b139b4eab00f7a00f6bdd0d9c`

```dockerfile
```

-	Layers:
	-	`sha256:a24b35dddc6a2c4fa1d7f6be1e32bcfdfb621f8f7d361bc203593ba9ad55df25`  
		Last Modified: Tue, 02 Jan 2024 06:57:11 GMT  
		Size: 3.2 MB (3206289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b6241d6bc5f8551653be20e49ab684c480a24aaeac597c47541bdbdd7bf3526`  
		Last Modified: Tue, 02 Jan 2024 06:57:11 GMT  
		Size: 16.8 KB (16799 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:71baa349e1ea391ee45d9ce454fed4eb0a5611ae5c734f842402c36ddc372db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56662801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f2656118bb340a2e4fc13f940fc2740d7aa4daf5b88063a7c857fe78065398`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
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
	-	`sha256:ed207f166bcc2956b986f742e1826c39cba4d9c6c8c4c2475fd2f26d0b11d3aa`  
		Last Modified: Tue, 02 Jan 2024 01:32:48 GMT  
		Size: 27.5 MB (27505265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9184bd75aacf41ac7d982e25e98cc2290dd2315b6c938f2ddcd4267ccf884cff`  
		Last Modified: Tue, 02 Jan 2024 01:32:47 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:114199d3ca738e401b07acdbd8cb61194fa78b4c3ed1222ea98079e4ed789cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3223623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f4fdd42f3c87a1dda79108335e69d224ae4f6b230bc4b2d3652387add174b5`

```dockerfile
```

-	Layers:
	-	`sha256:6dcf65076d7e0e08e18898b71a77041b43eb9ee29379e2a4eb2bd1286f80c643`  
		Last Modified: Tue, 02 Jan 2024 01:32:47 GMT  
		Size: 3.2 MB (3206896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ee4617b8492d0f05c4322c036ef164680e010439672332288266ee10ef806d`  
		Last Modified: Tue, 02 Jan 2024 01:32:47 GMT  
		Size: 16.7 KB (16727 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:32fb2f90c027d1dd331c9beb66cf7302adbb27a3466be2ced061de87803eadb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57938121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f5b465d9d20444b19169b7186621e5fb7c9179bdc13959a4c0401ad29df620`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:48689786b7812032adc0d36643501f16ddee15750a8f0f8b614dba58e5037b2b in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:de2bfe459016bec412fddc313b793adc6d47c8a4540608a6f3e217998027f073`  
		Last Modified: Thu, 11 Jan 2024 02:43:20 GMT  
		Size: 30.1 MB (30143875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f4d9773aec148ef8bb9a9bde0392a16d03aa65652e6c0a48cb23b5816977d6`  
		Last Modified: Fri, 12 Jan 2024 00:31:51 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a84bd90a89f25daa64f9a3216843e45fa2c46faad88eb9336c47d9b9dba002`  
		Last Modified: Fri, 12 Jan 2024 00:32:45 GMT  
		Size: 27.8 MB (27793980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14276f8685f35adce323e528bbb3084c9115181679f99cdc8fbb68802e58f87`  
		Last Modified: Fri, 12 Jan 2024 00:32:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:5dc605e8bbdd6c0b6a455f70610413d83b7313a836a6973bda1d142e3c9f203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3242868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0e68317824b1db91f1d59af043398a02c19fa30f3eb5fe44ec9c2e907a2144`

```dockerfile
```

-	Layers:
	-	`sha256:8ef2daaa9480d9354bf539d510195ed8f47c819438dff4ff052d942b2fd0dcac`  
		Last Modified: Fri, 12 Jan 2024 00:32:44 GMT  
		Size: 3.2 MB (3226027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f724b952f94f488b8403813c49d5d6399d0617f420a147772d7d48621e4d01b8`  
		Last Modified: Fri, 12 Jan 2024 00:32:44 GMT  
		Size: 16.8 KB (16841 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:e9263a8e1d1e0c3f1942de4fc08ae3655016bffa1f8a9675e323f87a9d6cc719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56009790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d60548c2c99df959730dea058455636991f42135e62050ead6a38404dbac49c`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 02:13:36 GMT
ADD file:dcd5696ac281b24df52a518e2402c7f7a4caedfcba0d82e195b7c06cd3a38fdd in / 
# Tue, 19 Dec 2023 02:13:40 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
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
	-	`sha256:d338ceebc7cc7e5ac10216ec50a1efc7e16fae76017a3e1cea8539699c1e5bb7`  
		Last Modified: Tue, 02 Jan 2024 09:24:32 GMT  
		Size: 26.9 MB (26888095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc54a1554400c6f0ecbb5b705136b283e09159a05788b2d2bd91cc7df65c061a`  
		Last Modified: Tue, 02 Jan 2024 09:24:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:68e9a724dc63190c1ea356be22f2c4bd70fd525730881cb54d93b9f23efc2695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 KB (16572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4c42e1c444114bd49bb3b49db9b8ac00848e09eb00e5dd008a5e3a7f638fba`

```dockerfile
```

-	Layers:
	-	`sha256:ed540915133b8d5ba33bcd90dccf1a138f085baf45d8ee6efd4f6322345c880e`  
		Last Modified: Tue, 02 Jan 2024 09:24:29 GMT  
		Size: 16.6 KB (16572 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:fa944a6f07ed5f4ea383eb1f269f0420b8e3d74b27d1729654a1b1e623a3016c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62440768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cf26f6520b1d8636cccefcdbef9c36334b8169d4afe0f9b58734eda031fb2d`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:50 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Tue, 19 Dec 2023 01:21:51 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
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
	-	`sha256:9e21d10296e353cb5c2696443f66c6ef086716bae1b1b51593245465b6e3bd43`  
		Last Modified: Tue, 02 Jan 2024 00:22:05 GMT  
		Size: 29.3 MB (29319942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252c076bc6f8d614216a3c92173b00488cedb79a0e50494f237ea539689773eb`  
		Last Modified: Tue, 02 Jan 2024 00:22:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:ecfd6150a72b05de1093bd0303a6b81d6bb5d9e1ea6c932c8611bcbb12edd527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3237038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21edc8d711d3178c0db3da39e30ed9fbd0640956691bdbb7923581dd9461af46`

```dockerfile
```

-	Layers:
	-	`sha256:476a10e7e174938d4a4f286594eb73ff10eeda22eba32462732c5d40927bd0cc`  
		Last Modified: Tue, 02 Jan 2024 00:22:04 GMT  
		Size: 3.2 MB (3220275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13569d1b2fbe331dbde6c748b8089fcf148578a3a71039cdb104813b08abbe39`  
		Last Modified: Tue, 02 Jan 2024 00:22:03 GMT  
		Size: 16.8 KB (16763 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:5c1348c451f411c28ee5ea7e69e6f07cfcb410b4f3d1dfb0afaa3749051c05f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54760635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f27a21f6267c5f306486bf3c3649062ad905177016a8d90e7beebb0c9d75d6`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:37 GMT
ADD file:f06f12fa5a93afc3a79ac4371d24b0a471a5a1818cf34c1d90004c8f410914b9 in / 
# Tue, 19 Dec 2023 01:42:39 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
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
	-	`sha256:06fd6bb6758179501878b6da99cee08830a8e0f80b2e4f99d3504c46eb827a38`  
		Last Modified: Tue, 02 Jan 2024 00:36:57 GMT  
		Size: 27.3 MB (27268493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ff9bce7db0dae04303d4a3d0fa2f380c77fd8eb1edb24ce2e95612e1ad2851`  
		Last Modified: Tue, 02 Jan 2024 00:36:56 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:18243bedb4e91678e04bf887afa40edd9778ab3015018c5de8eaac51b8ec247a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3237965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fd2d274dc70cfc375c70fe26d3950b82b1135c0b851280ac5e2c4c570ee848`

```dockerfile
```

-	Layers:
	-	`sha256:ee8ca076ddbfc2d0a19f66ae4c3389eb79a5836505fed62dbd36612451cb7713`  
		Last Modified: Tue, 02 Jan 2024 00:36:56 GMT  
		Size: 3.2 MB (3221252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a76b39a37b869e5d749df919ceac8af634f6c42661e77d7603b6f0bad269e549`  
		Last Modified: Tue, 02 Jan 2024 00:36:56 GMT  
		Size: 16.7 KB (16713 bytes)  
		MIME: application/vnd.in-toto+json
