## `perl:5-slim-bullseye`

```console
$ docker pull perl@sha256:577476a499ef1246306349295e57c8ac973509988d95a498b2bb95499a2ff6d7
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

### `perl:5-slim-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:6ad4059adbd42bdcbda936caffa4a01ff46e67f6f034363eb6be0e454a016206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55800362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec79b54f03bb391cd4d678a1d4de5647a25a515dd72717c9e54254a668eb1e4`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc69cf4e72328fec9b62e4602f055e2ceda65ede9170b869c64badb4d2ed5892`  
		Last Modified: Tue, 14 May 2024 03:03:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4e95639e41a91d2d4c77e7317e7890d8dccce09b72b8f740b21c40018972ff`  
		Last Modified: Tue, 14 May 2024 03:03:14 GMT  
		Size: 24.4 MB (24366166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce14971246aa907c1ea77bb90e53742902f292ce50842390ffb296bb34045cb`  
		Last Modified: Tue, 14 May 2024 03:03:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:aff20cd6a8b46bd43cecbed2bfcf41c6488430f5b8b8ffdc2e1ce2277bc54a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3807a19a8508f5f1019b1650a46ebd1976844af54133b487776619cb81c3da20`

```dockerfile
```

-	Layers:
	-	`sha256:fcfb5957024cf8602dfa74792a20c4b0be6b6a9ee653b06a9cf6c2a750fede48`  
		Last Modified: Tue, 14 May 2024 03:03:13 GMT  
		Size: 3.9 MB (3912927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a7e5047b77812b692e9df8d2589448c3bf92636e9883dfd6c2d8b4e2c327d65`  
		Last Modified: Tue, 14 May 2024 03:03:13 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:5766a79f40d4db8534d3f3a1aaac666c2dc52dd00dc8ed2f06b7cfe3ce0463ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51612891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85d06fd9c905ac83924eb65c343b3a27000d9370c7891a5411d9ac308c703de`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:48:50 GMT
ADD file:7a63cf2b5d16adf102fbd2452be219224667c4ea55981247f398a4a867ef96c4 in / 
# Tue, 14 May 2024 00:48:51 GMT
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
	-	`sha256:b6ea79e472ea80a508a2732ddeb0e19de51d3f0aaf8f0fd18c1cdd1c939d49de`  
		Last Modified: Tue, 14 May 2024 00:52:17 GMT  
		Size: 28.9 MB (28936721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656ce8de806a5c0242937e20e5affb8a2662e6cc2ee1288e7ecfb2814b955808`  
		Last Modified: Mon, 10 Jun 2024 21:30:41 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f72464088f497ce031e56c982e24aa43fbf125803c960d366dfe983873d22e`  
		Last Modified: Mon, 10 Jun 2024 21:30:43 GMT  
		Size: 22.7 MB (22675902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e0ba76bc1cf7417bc8815e42fcd15278adf3f66887038afb5ef57612bfe613`  
		Last Modified: Mon, 10 Jun 2024 21:30:41 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e313a06f219e6d04a8c7f72f7bb09b4c847b5f162328150bf2d3edc81fc58f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3900475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04ed2626110fc0c23e0906665a7321a4b22408386a4d54fc943a6eac965ead3`

```dockerfile
```

-	Layers:
	-	`sha256:b49eda7c842e2abe451f055cf102d8fdeb0388cd769a17ae707ec498c3de0faf`  
		Last Modified: Mon, 10 Jun 2024 21:30:42 GMT  
		Size: 3.9 MB (3884139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8727ae93c78166e323c077f96a94e0e14a39762f8f1305aba9ec919e22038790`  
		Last Modified: Mon, 10 Jun 2024 21:30:41 GMT  
		Size: 16.3 KB (16336 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:30665ae9603b077f216bf77ed0bcb5d8f7780af46de00ba63356be85ed1513cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48673286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1675f9bec818f288b98a8d68fce60dc2fbdfe32cabdf13261f0c6c67c62525`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
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
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c17c6e1804ea35c9500ab48d6ac57c68c7875887550ee2c77a13a31a0acc36`  
		Last Modified: Mon, 10 Jun 2024 21:29:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7251972ebd68d51e7a2e45322d05ef4b0c3a956715f62353ea354c1b6453d0`  
		Last Modified: Mon, 10 Jun 2024 21:29:17 GMT  
		Size: 22.1 MB (22078525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38dfeb5191d6f47ffd9d7248bb51c8b66fc7a678fcc1857c7dbe345eeb29f2e`  
		Last Modified: Mon, 10 Jun 2024 21:29:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c36681fd915e2a958c616da5c65faafee9129efec81d39df4a1fc944efe850e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3903193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615ed96dc6574b3d85cd874d20a1f04604f00f072a5a9943f68339efa88d870d`

```dockerfile
```

-	Layers:
	-	`sha256:6ce07b5ccd60fb356d2a4a18a275b6da904734aedfe40a23f64c69a5af13f88a`  
		Last Modified: Mon, 10 Jun 2024 21:29:16 GMT  
		Size: 3.9 MB (3886857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10fa29229a710008cc09b08006c8ae8bca4749064d46e7a43af359d944943ff2`  
		Last Modified: Mon, 10 Jun 2024 21:29:16 GMT  
		Size: 16.3 KB (16336 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:9813be50fa5aad279373780467643c15580b7bb94b1322baac54bca7197d2009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53588330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7b4c2d619960cd05ff8e4a75294fd588cff8b52138031b69bf93031ced44fd`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:d9f47b8ec1087ba52b5376bb1219899ae9f030fdd1bf05b9f75d8f8dcea667e4`  
		Last Modified: Tue, 14 May 2024 18:24:00 GMT  
		Size: 23.5 MB (23501157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042fb8d819141d8bc563e89e111641eb7651eaab9ec0f7f04cfb5f94ce836ecf`  
		Last Modified: Tue, 14 May 2024 18:23:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:22a7ba0442b0e2a69eac089ca3f72742040daf522f67590e91949342c83fb338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3903467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc121db83ae15aa5d8a91d7c5b1a1be6fdba7085fb676f8330277d5f66cd17f`

```dockerfile
```

-	Layers:
	-	`sha256:2f40556d8dc9c5aab1e0fe2d5194ec10bc56aaa60f103ed75618b127f4fbff71`  
		Last Modified: Tue, 14 May 2024 18:24:00 GMT  
		Size: 3.9 MB (3887245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:045e48cd2db736ddd785900142c9b72f2006e7fbc5ca37d00adb6c816b1e4386`  
		Last Modified: Tue, 14 May 2024 18:23:59 GMT  
		Size: 16.2 KB (16222 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:2fa7c5061692298202bcfc8e7768eef6425ddbe326a9a5f0d4f520c82f5e336b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58519445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8f068d54aadd40a45881df16494959cd8dab4c21f89f1bbd50a376435b1b97`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:47:34 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Tue, 14 May 2024 00:47:34 GMT
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
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4116612a0c90c236ca4bf50bd272fea4a46d1aebf3e0fc71b07cd218187d8956`  
		Last Modified: Mon, 10 Jun 2024 21:02:40 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baea51f709ff0fe36b1b8ee94dddacecb3429901e53c3c3fea375fbe022b157`  
		Last Modified: Mon, 10 Jun 2024 21:03:21 GMT  
		Size: 26.1 MB (26095134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0163e24dd3fca6e9251c68d847232bab22a4cc95d97d66ceaa936743b6681afa`  
		Last Modified: Mon, 10 Jun 2024 21:03:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:de8ebe8532afbbc68371b48c4b5f8c1a0d441c3d5deb5fd89f452b7e96982b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3933401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e94a7454eb84c8189a3b26826d6aee2198c040952109b0ed50b5d45206c8064`

```dockerfile
```

-	Layers:
	-	`sha256:e4ccadee9dc96e3f63660475370e49d4b6c138c98e9a7b672ab4323f6acb8190`  
		Last Modified: Mon, 10 Jun 2024 21:03:21 GMT  
		Size: 3.9 MB (3917177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04ae39c73d7afe0cdd56e0fb3f3d2188c388ba09abddbd16ec670b6a0f1d3003`  
		Last Modified: Mon, 10 Jun 2024 21:03:20 GMT  
		Size: 16.2 KB (16224 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:9bb9bec1d332fd9486a481d1385b23c8f2f120c29745c5afb6e839ee55074919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52930269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b1dc68e77a1739f190220dc939e496a18f89b3cb03fd175757af030bef5867`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:ec3acf4bc32b149c2b67d1b2c5f3a6d1f16fbae266ac16c115e1fca276b970e7 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:7aaac58a10ad3fd36e45994e92a0e6e34e20410c25bec96da14843c57fa0c2e9`  
		Last Modified: Tue, 14 May 2024 23:26:35 GMT  
		Size: 23.3 MB (23278134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebe1fbd5a329bb76aad32b082c7be4d33fab4d4eb3b641e328eb1627a991f9`  
		Last Modified: Tue, 14 May 2024 23:26:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:cfc6df229e6b30fcba812ff67797fa3f7a271442fdb974c27b9e954f81f72c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 KB (16057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a081d7e4c3f98782722bfdfaeb268d5e3772ddec96a9a8d881a1f42beb128b3e`

```dockerfile
```

-	Layers:
	-	`sha256:1509fc37cf712bbfcffd3570e95032cf589a69cc776b8992ab1badebb1257ad9`  
		Last Modified: Tue, 14 May 2024 23:26:32 GMT  
		Size: 16.1 KB (16057 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:924401abc264f93e44b7ebcd4abeb0089c210abc2f7b4efa6cb2decf368779ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60234045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ad9cc79e11f20294dc2dae88f2c855757087abeec3f3e00f5bf8d97106dfc`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
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
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7d0b18e0fb0223429492b8ec9e80f171858d408724fe9a9c1d9aa6de3b958d`  
		Last Modified: Mon, 10 Jun 2024 21:23:06 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c39236763bcb0da23ae87e1e8878fc60f48f6f200326ed09c3c1e5391a9040c`  
		Last Modified: Mon, 10 Jun 2024 21:23:08 GMT  
		Size: 24.9 MB (24922617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e007388e3aadb7ff5a37940fca1fbfeeb1a196fc04156c446e2b7cdd873e0b`  
		Last Modified: Mon, 10 Jun 2024 21:23:07 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:08a5505bb9f6a72ae293ed732f64fea80fd7646689b83fef7366b9662b9ef234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecb27961acd12fd6a1c80682cdb0a115ee70a4889efc5dd4b09b622f824786c`

```dockerfile
```

-	Layers:
	-	`sha256:80b1c79d595688c2d4f3d0d230e6712a1a35f78aa5e38aefd60911f838de104b`  
		Last Modified: Mon, 10 Jun 2024 21:23:07 GMT  
		Size: 3.9 MB (3901693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33af2bbd5aae1c0f6dd28781dbb677b9ac2d82d4bd4b508d6fdb2a7683f3d4e3`  
		Last Modified: Mon, 10 Jun 2024 21:23:06 GMT  
		Size: 16.3 KB (16302 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:c14ce965d78ac94d736d36b866019d51b4d1f86fc439dbba6f54e35a817a5500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53565963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0488dee4c7a8201c8ac8fae645c311162cb22a8a47bf09d2b7aca659167b2e6d`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:43:11 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Tue, 14 May 2024 00:43:13 GMT
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
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74947b03974ae200f8bb034b21c35ceda57fdac74a5e45f0d29ef587767cbef8`  
		Last Modified: Mon, 10 Jun 2024 21:32:16 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b753c9bccfcd64faa2661fc2ff5a3b087bc4285c435d9c1de82f448cfd0071c3`  
		Last Modified: Mon, 10 Jun 2024 21:32:18 GMT  
		Size: 23.9 MB (23892038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66052d2c46e95e4d6ac7acafe302e7cc68b51eb6d1aff71e3dc706fd941aa7ee`  
		Last Modified: Mon, 10 Jun 2024 21:32:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:42c6d4f37fd3e4942f02f748eb4e4c2b4bfa22707d10fa9f7a7492d6ac008c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d369d599001133f2b6a128bdf88a833ce2baef0214578f56dfe0a03de7304b`

```dockerfile
```

-	Layers:
	-	`sha256:a757810b3c3c9b30af717e6e3ffdcaae069c519563f39730d14361f723735bba`  
		Last Modified: Mon, 10 Jun 2024 21:32:17 GMT  
		Size: 3.9 MB (3901628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f6d627aa5fad19fc0f5b8379f87dd4bdf2f3241a34d73fb8b276078be91c36c`  
		Last Modified: Mon, 10 Jun 2024 21:32:16 GMT  
		Size: 16.3 KB (16258 bytes)  
		MIME: application/vnd.in-toto+json
