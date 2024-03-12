## `perl:slim-buster`

```console
$ docker pull perl@sha256:d4fd65728976bca968edf8e17a7afabec08fa5e85e451b6ce614b6e8ce16f46c
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

### `perl:slim-buster` - linux; amd64

```console
$ docker pull perl@sha256:03d46dfeccfd1470115cdeb25b03cb2c8960e7627118b190190ec42c99339839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54515801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf01652f42d77e4f61cb755299adccbc49e783a89f1f292c5b4e14193d2d75d`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:e64f92c07598d7a1e58a8116342198e837ea4ed870cac2c252323c261b270566 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:4a21b857313366ffd622f19e31c4300a81dce92b023b4ff6583ca167179804ac`  
		Last Modified: Tue, 12 Mar 2024 01:26:59 GMT  
		Size: 27.2 MB (27188304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008f5509bda97b80ed18df81226954af40b9949caa108c95292e03b39bf79a17`  
		Last Modified: Tue, 12 Mar 2024 02:04:51 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d543a49c24373aed2b2da6a4be39c5742246d1497abfd323666aa81cd1e56588`  
		Last Modified: Tue, 12 Mar 2024 02:04:52 GMT  
		Size: 27.3 MB (27327231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e54f71058cecec870a1b88d0d2ee1c462e45fd47695acd7d596e0993572c8c`  
		Last Modified: Tue, 12 Mar 2024 02:04:51 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:c8e2dc3ef6ae90a8210a8ad13f39e98a1fd46b4d9f5037a06b9fc05f4e949f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3381451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee6da2812431d8f181c5de5ef49222c55523c34eb73c010fe81602979c024ff`

```dockerfile
```

-	Layers:
	-	`sha256:7d789078a501af244b7079f03c3abf27a06499488cdeb9d6df0101e0e68ba0e9`  
		Last Modified: Tue, 12 Mar 2024 02:04:51 GMT  
		Size: 3.4 MB (3365114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebfcb0b7975c442a2ffd7d0b46ccb4739646db0fa49ccbd2e6b009e1acf03fc`  
		Last Modified: Tue, 12 Mar 2024 02:04:51 GMT  
		Size: 16.3 KB (16337 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:895482686ab0f78944ccfcf20c1287536dbbdf2bdcb0daa845cf6c0999173986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46705478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1faf4797b67831340f1ef8bbc2cc1ecc3d9dc186285634bd10380e79e970af`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:3bb84527315f3c157a6224d42c0b9c078d85e8977d02365719d3fa69b9b7544b in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:1190235a63a2fd50345e786cc24ebcb4ae4619484192480a44a203616017624f`  
		Last Modified: Tue, 13 Feb 2024 01:28:25 GMT  
		Size: 22.8 MB (22795757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c1758070da333860499bd22df5f5afccccc434c1e630f9fd168d20dea6f5ae`  
		Last Modified: Thu, 15 Feb 2024 05:23:28 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996142c0a38ea209005fd727ac7309b2e9c842c2507623c70772b6fc8650dc84`  
		Last Modified: Thu, 15 Feb 2024 05:23:30 GMT  
		Size: 23.9 MB (23909454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42762d0155a0864d3710c68d0bfab78440f5ed4a94fc4644bd8da6a75b644101`  
		Last Modified: Thu, 15 Feb 2024 05:23:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:852db6c0424aa824b981ad5dc199e83e310ac9e726e9e36ad37f79d72dba3ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2914650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f4af9ae52b7afd86fbb5aedae19f24c60b247811fa4a84c43ca8a090194026`

```dockerfile
```

-	Layers:
	-	`sha256:fb2e376d7f28a80a6cb012bedb1ce3d9e0ca0dc2ff3b495769d7d3850a12aa45`  
		Last Modified: Thu, 15 Feb 2024 05:23:28 GMT  
		Size: 2.9 MB (2898402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53ee7bee5692329abeaedefaf2013745af93bd882d8638bbd6679322877ffb1b`  
		Last Modified: Thu, 15 Feb 2024 05:23:28 GMT  
		Size: 16.2 KB (16248 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:67748347b6d846b1f54f7ff3fcce179796b0caea99131ead8542d820729f3e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51933511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695410a39606f8b6c87682e56738e82128b6d662309e9a19ee1c528b9efa992f`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:56f9fb4bf0b803f4553b7fe668c34676467e662e3ab02af10e815a93ebbde1d6 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:e4e871d0a0087a92c664052d6406ee23eeb537f0b5f01894052aa0363fed45e3`  
		Last Modified: Tue, 13 Feb 2024 00:46:17 GMT  
		Size: 26.0 MB (25969810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0dea61d740b142bdb6d33c601e26023c3e99da5ad684a70d2817171a7f1809`  
		Last Modified: Wed, 14 Feb 2024 02:52:39 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824b606d2fc287804091e3859193f5bd0d9b3e6a40f87262be3d68a9d36add1d`  
		Last Modified: Wed, 14 Feb 2024 02:52:41 GMT  
		Size: 26.0 MB (25963436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bb9e2411da1dea832090821d7d1e7d9b3df83e34d8126d96b0ae5812f4c909`  
		Last Modified: Wed, 14 Feb 2024 02:52:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:e727a573e7239f10b915ddf0b3765088c6813aaf43f686f016c3762e5f302ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5155334f50fa352af5a5cc62ed6259bce319597e39cf2789ee5b9d9ad438697`

```dockerfile
```

-	Layers:
	-	`sha256:a2392a7a80c44d61df3dfa6d69bc3102cdbd721b642fcf7905cab49017fe93aa`  
		Last Modified: Wed, 14 Feb 2024 02:52:40 GMT  
		Size: 2.9 MB (2893080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa181c0187dd6af2685848ac96ca36daf82a6939519dd94965de06b53e671ea5`  
		Last Modified: Wed, 14 Feb 2024 02:52:40 GMT  
		Size: 16.2 KB (16182 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-buster` - linux; 386

```console
$ docker pull perl@sha256:3dbf8afbb22e65267ac4292a4bdc57c9b4d37da0c9faea479a6aaa1748b3ac2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59298033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4d6246a9efdf775d78d5367e65830e399a7c6a59696f7bdd797e5bca7d6142`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:3ff71d8500563a5fdf27e800f24879e0da378a12b7855b0b22093604455859ae in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:157da6991ef444d47f503ec5cd3d6e3043ba6dca39090f157c423c1f8097d0ac`  
		Last Modified: Tue, 13 Feb 2024 00:45:25 GMT  
		Size: 27.8 MB (27846861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b15a88dec876392d4741549940fb12732bde327e3630e248d67dcc3b82d79ab`  
		Last Modified: Tue, 13 Feb 2024 02:03:04 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1791522cecaddb2fae57912fb5e6c91384b5b6e0c9d0ea0881523226b36518f5`  
		Last Modified: Tue, 13 Feb 2024 02:03:39 GMT  
		Size: 31.5 MB (31450909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c815aed158e210e3bd0e12f520b8534540eab9aec524faecb4a94dc826ad74`  
		Last Modified: Tue, 13 Feb 2024 02:03:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:c6fb4f3451adf1e649ff1701a03d1c4495952495d4a00e36f4dda8dc53f84b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2951606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d023df7fe81b219e47c2459a9562d86af6c266505097e1f6313f61ccfb1bf85`

```dockerfile
```

-	Layers:
	-	`sha256:acfb381c09b2990326e621c87141416ae7e44e633cfd70f228227e7742844127`  
		Last Modified: Tue, 13 Feb 2024 02:03:38 GMT  
		Size: 2.9 MB (2935303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a184f779f0a8457ab667145f966d29493a395fab37e9a6990c625308909fe1b`  
		Last Modified: Tue, 13 Feb 2024 02:03:37 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json
