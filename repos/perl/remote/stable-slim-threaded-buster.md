## `perl:stable-slim-threaded-buster`

```console
$ docker pull perl@sha256:d4a4ea30ffce1c0d3f38dfcb040f9be3de3722b5763b36b549193bb5b4b96b34
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

### `perl:stable-slim-threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:b5714b8696a88de5ac3eac85138bc84a477fe9a04dfc217eed9c16cb799105ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54571366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd8b7a1628775f7889acdc34f32a345460a587e79b2f80a2b997e1721a57b94`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:08cfc7bf77cc2291c96890f44a435216cb1168c45cef77f7801430982c43ca58 in / 
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
	-	`sha256:4648efdf070b378f12737b5cdacaded7b6294f27d0a0c1fb33849090813e920a`  
		Last Modified: Thu, 11 Jan 2024 02:43:48 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0505006c8b7f9f2fa9b3eabbe938d9449bc9ea05510bcaaf459f9e60e07e598d`  
		Last Modified: Fri, 12 Jan 2024 00:40:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9921defbd3a26006ec11bde842b8cb65a93ab9c13902d317b7b4fd7392373052`  
		Last Modified: Fri, 12 Jan 2024 00:40:49 GMT  
		Size: 27.4 MB (27382878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2676121dfec625a9632779cf96202e369637d9b562aaa1c73c3541742415c6f`  
		Last Modified: Fri, 12 Jan 2024 00:40:48 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:6307473c61cd5d6421d64c19597af353b4da8547d580411cc500a3af2a7faa99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00563ccdbd36be571193ce5289f28ccbdce0c44631d72731f3852f9f84bdeafe`

```dockerfile
```

-	Layers:
	-	`sha256:d3ff958be76a6c7b890b65ab4b4f146e7b8b07989e6cefaa14d32e861237399c`  
		Last Modified: Fri, 12 Jan 2024 00:40:48 GMT  
		Size: 2.9 MB (2919458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1697b8e7764e011b1f1a60d91bfc4ff54806e89d4b8c12d67430836b300a447d`  
		Last Modified: Fri, 12 Jan 2024 00:40:48 GMT  
		Size: 16.5 KB (16478 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:7de5609601b3a08b4fef55f823cd6a3974c43a9ccc39900400dc3af0b75174a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46699787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c3e2ff0b6c0189a0f6860fe30272d3d6cf19a08163e30d60d1c28c1ead4270`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 02:08:27 GMT
ADD file:24df0653e55efc5ba9ec22911758d187c26dbe6bda2d417ff56bc3d9a9072dd4 in / 
# Tue, 19 Dec 2023 02:08:27 GMT
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
	-	`sha256:99a10db9a1b078c63980e0e4fc7242bdb6d9ba7c91dd8e0883a55756584bea0f`  
		Last Modified: Tue, 19 Dec 2023 02:13:13 GMT  
		Size: 22.8 MB (22795803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110a77920c4e8e13d75a747c4dd1291a9052ca8a68c2510f25052f407938ed13`  
		Last Modified: Thu, 21 Dec 2023 00:05:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1e9b159d2570c53e5dcaf32738bec31aec0b4be2972df887472feb7dd2d126`  
		Last Modified: Tue, 02 Jan 2024 00:06:24 GMT  
		Size: 23.9 MB (23903717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c687c4557775e639313f75469c9479dd73d0a16476aceac80518ebdc9b4acb85`  
		Last Modified: Tue, 02 Jan 2024 00:06:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:7ba25e0881d0919c7b62f7a0daded5e38b433d4a41e94a53947373d3c02ed43a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2914881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f01170b334b88637d910850d7a0e91eff99c5807f64ae368b2571a2e69b5ec5`

```dockerfile
```

-	Layers:
	-	`sha256:32769f12d2d90faa14e5d9cbf28828c2c2886f8d83178cfd6c4bd54d005fdcf0`  
		Last Modified: Tue, 02 Jan 2024 00:06:23 GMT  
		Size: 2.9 MB (2898492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c674d83f5421cc05f813ac3f96f522f413df24c7052017e759db3321fa42fa8`  
		Last Modified: Tue, 02 Jan 2024 00:06:23 GMT  
		Size: 16.4 KB (16389 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:fbb9277e1c123da331f9e75b0d671d3a849577bd8123de12ca6f3d4807da3b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51966136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0852bb1b3ee85cf990d4df1540a27f9e369e199c82bcdc1936d965736046b9`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:0d7c08c3a192fbaded92a14e5eed44f5df7d00cd932ed45984ebb6b6e21446a6 in / 
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
	-	`sha256:0d982983796daa327ca72ca687e0d8417bb909e8256d666725dae5ad846525ae`  
		Last Modified: Thu, 11 Jan 2024 02:45:24 GMT  
		Size: 26.0 MB (25969811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2177363340fec9a2d340888deec7451b1b99ba5327fc9b994cf875ff2a593b36`  
		Last Modified: Fri, 12 Jan 2024 10:28:09 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5c9f06ff7f0a91d7ed9d73a8ce3c72f0200576a4fed5a6d37ca3be709dc6fb`  
		Last Modified: Fri, 12 Jan 2024 11:31:52 GMT  
		Size: 26.0 MB (25996056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6967606820d1eca3166fdd9fdc4c47f3cb630b78229fff92eaaf025a1c51f47c`  
		Last Modified: Fri, 12 Jan 2024 11:31:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:f8cdcc573991ff8577633b76ac5e9ff7550b2b2c0a0a09785332aed4bdeca496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce723234de1adce292177ff34621e9f5cc2e4fc5e36dc1c2ac137343164deade`

```dockerfile
```

-	Layers:
	-	`sha256:96865da788432d685e91d9844ad189c2046b7b7daad48c064961c60a841372f6`  
		Last Modified: Fri, 12 Jan 2024 11:31:51 GMT  
		Size: 2.9 MB (2893170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ee766d39085ead85c0a26178c4543e7842964999adc612cced0f99212897651`  
		Last Modified: Fri, 12 Jan 2024 11:31:50 GMT  
		Size: 16.3 KB (16322 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:1cf398791ba63d6aaed2200372ada92634bf366313492f64d62725ae64e14526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59398693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86e7252e898bfac6e04a3b1031e829f6a2e4e3b101a4dba7cb440b7adbfb077`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:71b9e4d4a69cf226be8618530ca01bf58a3220da10468a570ca3fb1a110462be in / 
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
	-	`sha256:ab357b9ea3980779585df5fa6cfc0b3cfea23242969bdaabef51d23ffa5492f1`  
		Last Modified: Thu, 11 Jan 2024 02:44:52 GMT  
		Size: 27.8 MB (27846836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c695c2097ed82dcf243c13bef9802b60b27698254a478fc2b36f918b6feb419`  
		Last Modified: Fri, 12 Jan 2024 00:40:55 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c452a5637c5a4ca760e3f4a7550dfe4f97d2bfc0dbc9617dc7e07a5c66bfb55`  
		Last Modified: Fri, 12 Jan 2024 00:41:34 GMT  
		Size: 31.6 MB (31551590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc20057ac7554845a5896a95b3f54d706e2cb656adb5e054a851c9e65b5a401d`  
		Last Modified: Fri, 12 Jan 2024 00:41:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:6100d2b35d4e0a4a4cb43fc3920a0daafc665cd3a7a73d2a4a31e4aa438c1f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2951837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f3cc8ddb90f8f8b28880ae9faf2e8a9df1be3d25631a460c134a7c6f99cbc9`

```dockerfile
```

-	Layers:
	-	`sha256:515aeefe7b3650a0328dc76ca335fdfff13b916e7045d493efaf80ae448b7e80`  
		Last Modified: Fri, 12 Jan 2024 00:41:33 GMT  
		Size: 2.9 MB (2935393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06262d13bc2ca0ac9abf3ae6cabbf8b3a1861d798dd32d003e5179161df5aa51`  
		Last Modified: Fri, 12 Jan 2024 00:41:33 GMT  
		Size: 16.4 KB (16444 bytes)  
		MIME: application/vnd.in-toto+json
