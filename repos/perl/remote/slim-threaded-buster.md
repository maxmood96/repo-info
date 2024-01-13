## `perl:slim-threaded-buster`

```console
$ docker pull perl@sha256:751474b0ee55fbda69f1231f4239a7ecd462451f2edff847188edfda42007077
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

### `perl:slim-threaded-buster` - linux; amd64

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

### `perl:slim-threaded-buster` - unknown; unknown

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

### `perl:slim-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:aac3af7260d0c45c905449b5c8f876df783921da8299a5d99c3b35129478f2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46720529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17dc78e3de21308694a6abcb47e10cfc0ec123565a3859b6ec659a2b0ec0f08`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:8461846d920454a66bf03cc7ad09cc57e04f7abb932ad830677815a3419e5bfe in / 
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
	-	`sha256:7a5d87426f4ef3b928342bdb0b7da4ac387828235c6d1392b9823522dfeddb25`  
		Last Modified: Thu, 11 Jan 2024 02:50:10 GMT  
		Size: 22.8 MB (22795616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400cad5aeb1bc70b83c8cfbbf180641c93a509f7ae10174c4ee45d8cb09e2ba9`  
		Last Modified: Fri, 12 Jan 2024 21:00:40 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13846aee63eba4d3879b0aaa4f6d90ce2c3c71c0137600dae4acc08e5cd6eaa`  
		Last Modified: Fri, 12 Jan 2024 23:22:55 GMT  
		Size: 23.9 MB (23924646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75eeeb4dddfc7145ce4515f6120a0866ef790024908a723be389974a4cb15935`  
		Last Modified: Fri, 12 Jan 2024 23:22:54 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:6c9b6cdd7f88edc777dbcc608b47eb210731d0c0ad7f6c8c55319ff600bb7756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2914881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b2bd56365b9d86d77c4df8cef6a7ff8be71f18581e521547c712f550cc223c`

```dockerfile
```

-	Layers:
	-	`sha256:f89d6d3e5200282098d8655eb03ab7cf681c22923bdfc87ffd032d26edb1c944`  
		Last Modified: Fri, 12 Jan 2024 23:22:55 GMT  
		Size: 2.9 MB (2898492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed6dfcea682f636cde1e217a3c2f191519207c07132fcef6392ddcfa65dbe4f`  
		Last Modified: Fri, 12 Jan 2024 23:22:54 GMT  
		Size: 16.4 KB (16389 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-buster` - linux; arm64 variant v8

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

### `perl:slim-threaded-buster` - unknown; unknown

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

### `perl:slim-threaded-buster` - linux; 386

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

### `perl:slim-threaded-buster` - unknown; unknown

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
