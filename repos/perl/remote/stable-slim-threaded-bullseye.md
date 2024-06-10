## `perl:stable-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:1fe8b92e306784ce0ca6989e723d738be1c4c98df628a6a7dc86212398a5a816
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

### `perl:stable-slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:19d0a81776e031a1b83df57e6511709a7460869aa09e5e3f5037395d5e82171a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56158703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f384d151c114f9ea679b50dec229e46aef667b4c6ec9d489a63e041172b842`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb446f359498d4e7b7c82fbde13a63f35ce73d6f51c68dea2d5347e7397f79c`  
		Last Modified: Mon, 10 Jun 2024 21:03:36 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c78e897ce133146d918e4be9677dc03b5513e1972eb43d65a3058b35f78eec1`  
		Last Modified: Mon, 10 Jun 2024 21:03:36 GMT  
		Size: 24.7 MB (24724504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103416014ebbf757f0d00ff9334b0e197feb4258afe6f6047738bae687299605`  
		Last Modified: Mon, 10 Jun 2024 21:03:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:9071b5f4157e89e0d328bc04f92b4e496e0ae8eb347780f8fd5c36e1e8805489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503db7ffde8d00878230bb7430846b21a6b9cf8b7ee314208a0634a89c0cbfdd`

```dockerfile
```

-	Layers:
	-	`sha256:258254a3d7a40dff8e1e1ca9f42028267d209db221f2af40c4631292d3fd9589`  
		Last Modified: Mon, 10 Jun 2024 21:03:35 GMT  
		Size: 3.9 MB (3913016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6842aaf53cc833ac43cd38aa45631d9ba37ddc78e4bdb5c291dc188af74e28`  
		Last Modified: Mon, 10 Jun 2024 21:03:35 GMT  
		Size: 16.4 KB (16395 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:3f6b97793ad11bcf3646dbeb1fb017f1a378ce5daf7c381d624b6bf150b6a632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51644795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662d7391e026936198a6a5af055216ebd8b4c141d974cc11e739320fcb135d51`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:48:50 GMT
ADD file:7a63cf2b5d16adf102fbd2452be219224667c4ea55981247f398a4a867ef96c4 in / 
# Tue, 14 May 2024 00:48:51 GMT
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
	-	`sha256:b6ea79e472ea80a508a2732ddeb0e19de51d3f0aaf8f0fd18c1cdd1c939d49de`  
		Last Modified: Tue, 14 May 2024 00:52:17 GMT  
		Size: 28.9 MB (28936721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656ce8de806a5c0242937e20e5affb8a2662e6cc2ee1288e7ecfb2814b955808`  
		Last Modified: Mon, 10 Jun 2024 21:30:41 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d5b8b7614241e63b1e450f8188c4911f3f3a3e1d703db83de891df44b83c2f`  
		Last Modified: Mon, 10 Jun 2024 22:00:23 GMT  
		Size: 22.7 MB (22707805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2ac51374dd0e2cf0d42a45ed4b47f175ff74582419b4e76b946a0a61799a0b`  
		Last Modified: Mon, 10 Jun 2024 22:00:22 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a07d4f3eb573d7f4548b6f8fcfe2449b66baf6c70dee906cfe40e6abd1df76df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3900702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e0958334a2a23b1e2a5546b080dce7f84683426fefcaf1d3784d8ea4d3d686`

```dockerfile
```

-	Layers:
	-	`sha256:0ff2e13c8016c759b7698ce4012ecdc38b3bb4c4e71bb4c5de8ee00704b968f5`  
		Last Modified: Mon, 10 Jun 2024 22:00:22 GMT  
		Size: 3.9 MB (3884229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97b4949e3d9c42080fa4c2bf242ae9050f80b03638353589909b5cb141a6f922`  
		Last Modified: Mon, 10 Jun 2024 22:00:22 GMT  
		Size: 16.5 KB (16473 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:bd7f1d517230f05eda999a5b3fcd96239662c410bedbba9a9bc5dc7b276b8d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17412666346af4639e49c4789b82813dee5934ed214d51d948026bbabbb0a05`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
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
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c17c6e1804ea35c9500ab48d6ac57c68c7875887550ee2c77a13a31a0acc36`  
		Last Modified: Mon, 10 Jun 2024 21:29:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3285c2b8c5baefa2f0ade239d43cd76fa8e7210c95ff2545744064961f9b0da9`  
		Last Modified: Mon, 10 Jun 2024 22:11:25 GMT  
		Size: 22.1 MB (22103138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d44a59ebc39fdc5498d555d25ffb0ae2a763ae45bdcba34a8bc552c9f9b457`  
		Last Modified: Mon, 10 Jun 2024 22:11:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f4d4867110120cfa1cd1e8bb53092c5eda333e0aa3c1030d8e3280d6ba0c4e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3903420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689d143f5a4d58e84d1430c376932735a3b306454053a06ee3f078bf8c846f32`

```dockerfile
```

-	Layers:
	-	`sha256:ca80bab8da605430f69a7b8208dce8e3f42a7f5261ce1f91790732adc8d9732b`  
		Last Modified: Mon, 10 Jun 2024 22:11:24 GMT  
		Size: 3.9 MB (3886947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:237df64cbc62f5997eaab2e82eefe817e66e70acb3c83e9a818a881769ac2dc4`  
		Last Modified: Mon, 10 Jun 2024 22:11:23 GMT  
		Size: 16.5 KB (16473 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:16eaef2fe17e912ecd6613497080439ab896a3872533d25b5265f6401915e4b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53632185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c481f030b84c6d0dcfeb2fdcb444d006830a2be5bdf3fb382a31498a08b4e8`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacccfa947f9296f4e60b6b2eaa847fb68e0cc89210a0c5cff7436cbd685f18b`  
		Last Modified: Tue, 14 May 2024 18:23:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04337510ff74048c36b324807cd17bdf177c23274c1889d10db453bca85d002`  
		Last Modified: Tue, 14 May 2024 18:41:04 GMT  
		Size: 23.5 MB (23545012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67806f14f0eeca6d6207d7cb9ad562047209c4792dc7ece09067a73ad330630e`  
		Last Modified: Tue, 14 May 2024 18:41:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:5cdf1ac68260f187ddd20657322cde57b6af763e2cb444eb839c5472a622cbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3903694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92015364a77bdf634e4e71aea972b0f627316d5f5aa0613fa67236799eb5b4ab`

```dockerfile
```

-	Layers:
	-	`sha256:c4f91704f6ed506459ccded40738d6f151878534300aef39932406cb9a42e281`  
		Last Modified: Tue, 14 May 2024 18:41:04 GMT  
		Size: 3.9 MB (3887335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5283ddd32439d49f7fd00ea12d3d9390412976d1b9bd6bb02b15c7ee85a949e`  
		Last Modified: Tue, 14 May 2024 18:41:03 GMT  
		Size: 16.4 KB (16359 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:7e4171131a51d4306c6d322d35dded02b24d9f1f9a62aa658738566478719780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58614206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b967e75c421dba428d7b890896468ff0622bb608bf0077e5ec6a0ea96d5d4a80`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:47:34 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Tue, 14 May 2024 00:47:34 GMT
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
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40536b15959552c5960fa54fb68d5fdee9ec7f36ef2f03ecc25679fedab3bb2`  
		Last Modified: Mon, 10 Jun 2024 21:04:22 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955aeb277da3756ec8dd988a16af681b1317ab8d7f983f99f89c5e525ffa5789`  
		Last Modified: Mon, 10 Jun 2024 21:04:26 GMT  
		Size: 26.2 MB (26189895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa18445c1fe934466bb4f4bbbda0a5227cfccb66fc3ae2af08f6a7b98a3d2302`  
		Last Modified: Mon, 10 Jun 2024 21:04:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:3f725ad98974a8a66b67b7c87f0e9e6ce06fe94b3a561f93aa868235bf7d6e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3933628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd4cac52450d9eb954b9cf9fc6bb0fe6438d494640972bc9631a7720e068a95`

```dockerfile
```

-	Layers:
	-	`sha256:8f5a64dd9745e1cca7bd4fe2149b48875345ce7979edeb017e1b95c0cfe0d2f9`  
		Last Modified: Mon, 10 Jun 2024 21:04:25 GMT  
		Size: 3.9 MB (3917267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d5298a0fc3e552309b147405b0f0e4c2c04c0e2705e065a10f0d96da9e1adf9`  
		Last Modified: Mon, 10 Jun 2024 21:04:25 GMT  
		Size: 16.4 KB (16361 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:10fff12b4bbedbd1830394668c39a5883210ecdc4fe48166756cefd511f82a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52989168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef8d9f891522a83d95c4066e34c799012a01c5f487a25cc042db4ba107996cd`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:ec3acf4bc32b149c2b67d1b2c5f3a6d1f16fbae266ac16c115e1fca276b970e7 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:38917083d8284ce1ec7533351600bab5d64f8295f3edc5dc651be130fb9a4bd4`  
		Last Modified: Tue, 14 May 2024 01:23:44 GMT  
		Size: 29.7 MB (29651870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864f2634f3fa0d01e4755e1380562b9015e1756bb6db04ec0de54e37d941060`  
		Last Modified: Tue, 14 May 2024 23:26:32 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a5c02cc55f551e0abbf36d95d81781bb2ffcc84a8dde522b508511737d77b5`  
		Last Modified: Wed, 15 May 2024 00:23:41 GMT  
		Size: 23.3 MB (23337033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709e1b0c271b08b9f97acbf03cb0508d2ca6470b48987cfb8454302a0f7ff961`  
		Last Modified: Wed, 15 May 2024 00:23:38 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:6c2b2f01f7772658231447d30a19d95aaadd7d437a9b2a0dfec4a0d61477cf9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 KB (16193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0f194034b895e456d4166edf63374e6cdc4cb3722e75f3d5c2df5232e706ac`

```dockerfile
```

-	Layers:
	-	`sha256:2b1946c5cc874c44ffe45fcfbac3ba2d61298c6d7cbdac2547dbf44d4b27a912`  
		Last Modified: Wed, 15 May 2024 00:23:38 GMT  
		Size: 16.2 KB (16193 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:aad866bdfc8e9d62c097944626954c00d54f4b048708c17bf76660082d3871e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60319922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6396064ba138e42fb1876f89cdd72f32e854e930cd13e134d9da99458a4c75e7`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
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
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7d0b18e0fb0223429492b8ec9e80f171858d408724fe9a9c1d9aa6de3b958d`  
		Last Modified: Mon, 10 Jun 2024 21:23:06 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f72f95b7c5338942cd8a60dfe8dcdbe5a0e824d8c13d670ee0fc74a3ef12e4`  
		Last Modified: Mon, 10 Jun 2024 21:50:26 GMT  
		Size: 25.0 MB (25008494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563aa415a441013b435b3a3b362766e1b2aa05ea9fed1009574fe7053229e89`  
		Last Modified: Mon, 10 Jun 2024 21:50:25 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ad6a77f700ca88773093d31cf32fd3c2c611956dabf34a68fd8e230923f1acaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e2950194fb72bdef998de3c8df980f286e1544fd21950d2ef84be83c942803`

```dockerfile
```

-	Layers:
	-	`sha256:59567ca1ba485c4e19893e40f3d09b6db68926c3f717232cc66f85f0db69f26a`  
		Last Modified: Mon, 10 Jun 2024 21:50:25 GMT  
		Size: 3.9 MB (3901783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cde182740aeda07ccdcad4fb5df6e233a2373d264a7c2caff496def34b6aca`  
		Last Modified: Mon, 10 Jun 2024 21:50:25 GMT  
		Size: 16.4 KB (16439 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:bcfb7774748b1a0b3973ea47133eb853b4748e9bf3ad284eaed35f0fba85842e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53623804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6774ec78e8ac6ba01a691310452234eb63094d7d6dbfa9bd1e7f4971e77b11a3`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:43:11 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Tue, 14 May 2024 00:43:13 GMT
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
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74947b03974ae200f8bb034b21c35ceda57fdac74a5e45f0d29ef587767cbef8`  
		Last Modified: Mon, 10 Jun 2024 21:32:16 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5658b1c6f6dcd685aa253fbc4fdf4b64788ebeaf00251a6aa6860ebedf03e02a`  
		Last Modified: Mon, 10 Jun 2024 22:07:14 GMT  
		Size: 23.9 MB (23949879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e68ff5f147d829cffd37cea4d21a60f6171721f60a478e33e826bcb581a8e39`  
		Last Modified: Mon, 10 Jun 2024 22:07:11 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:08076bbfa4d2a20aeaf931504c09a79943c066b918ba0e891e690d34aed9b659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6896c169aa124df58f33b308602e35a4e5cf0b0c382a2d30eae4361c0d5491f5`

```dockerfile
```

-	Layers:
	-	`sha256:95b0b88627c6dd79dd9f67fb9202b3be09e182a0423f8c751f4240e4b4fb6d0c`  
		Last Modified: Mon, 10 Jun 2024 22:07:12 GMT  
		Size: 3.9 MB (3901718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f35b9bcf9026874d09bb6fa2f3f340060ad882a9aa0f1b0852fc7267c1fe2b13`  
		Last Modified: Mon, 10 Jun 2024 22:07:11 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json
