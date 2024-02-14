## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:d5c32a5bfe0ce765a03a63fcdb05b41d0c130819b7e86a5eafab53fd09d38fc8
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

### `perl:devel-slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:e7289d5f41db6ed425b436a995ebb126c1e496d0d896a23918b913a7cbc24646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56264040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5c1b62094a04f8a4e7c11089138a0578b02b7e12921ba0c9e46f696350fa07`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a216bcd790f7222673c764968feb8ce34357e85c732b01a0a67ad80186ab90`  
		Last Modified: Tue, 13 Feb 2024 02:05:36 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52b314ab52f6a9656c41922fcb67a87ab7cb4326526b3c6c6d190dbbe4fc799`  
		Last Modified: Tue, 13 Feb 2024 02:05:36 GMT  
		Size: 24.8 MB (24841350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd38da924c0d5c721883371d0371c78a8a304f53f16761b2922e4ce17c420d7`  
		Last Modified: Tue, 13 Feb 2024 02:05:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f0e56be40ca72e7271bf91d0cc10d828b788ee44bc74871c1cc0dec429e030ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3403199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8470b7d002797b238d22c9005b61b51ce8350616148667d11efc7f99068d887a`

```dockerfile
```

-	Layers:
	-	`sha256:7343c9b85c431729c3d04d33a2254f1623d096de614b997bd0077c494829e6bf`  
		Last Modified: Tue, 13 Feb 2024 02:05:36 GMT  
		Size: 3.4 MB (3387277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fed2454502c9ce45e441114ba760ea4740ce92018b0a3f76af74bc0dec5ae72d`  
		Last Modified: Tue, 13 Feb 2024 02:05:36 GMT  
		Size: 15.9 KB (15922 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:78e130acc504b132bc8ff3b2454abbc26581757401dba09639d187181027b514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51751124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1766bcc1bfcdd392bb956a9040d5a538e679bd0deec556b2515ee98d7062a4`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:2900145429df7cd46dd4818f44636aff96d0ef5335d5eb8cd5ed3106caa8b031 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
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
	-	`sha256:1dfdff681c8146f276615703a7134b952e9d0ba918e1e30890818c68181359b8`  
		Last Modified: Tue, 13 Feb 2024 22:04:51 GMT  
		Size: 22.8 MB (22826377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c3386872866b867b650c247b4560769b9016de9603c1e4a9401d24a0a09e2`  
		Last Modified: Tue, 13 Feb 2024 22:04:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:1e1886cf79ed417059a15b6c119f97b24185479443b445621408fc91f4e78d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3378321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977a6eb68c6def94a5096af4cbd32f79621721a56dd6bb6181cdec5765ca32c0`

```dockerfile
```

-	Layers:
	-	`sha256:91aa072d5a9da7d7b1ca94c2cc602187061f8ee477e9bd42326f63b8bdc2b947`  
		Last Modified: Tue, 13 Feb 2024 22:04:50 GMT  
		Size: 3.4 MB (3362504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fbaec0fc7b217055ef3904cc872b7e35d8cec20fbd34c5f5841ef5212c1eab4`  
		Last Modified: Tue, 13 Feb 2024 22:04:50 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:879c284402bf5d860b331323dfd8a5244ba50943cc6b8dc81803af804b606ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48597754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb0a8559037afa923bfe379b066f9e73336541971f94e148036547ae852eecd`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:65b9e2efdf2b09faf0d5ea0e2e00984ff3c8cf89b7959287bc6ca54c7772801d in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:4de6a546d77461a35cb9514c6432142adfb72460cf04bac21bd261d66c288476`  
		Last Modified: Wed, 31 Jan 2024 22:49:36 GMT  
		Size: 26.6 MB (26579212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797c15d22fefe5c8c8ff4c7464ff2a07565fbc7afc4f301b653c876a615b6a71`  
		Last Modified: Thu, 01 Feb 2024 20:45:39 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f265a410af289ba6d80b7fb1ab75f9c20b338036f694a182fa9adbb62b7bc65`  
		Last Modified: Fri, 02 Feb 2024 02:23:21 GMT  
		Size: 22.0 MB (22018277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79324d2e8ca725dbb7d389bd74eadaf6cab3601146690cf44f0cf9e3176942a3`  
		Last Modified: Fri, 02 Feb 2024 02:23:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:6e0e03e1b434bddbbc0ddf08a38fc45e5af3de5c6fe9aa4281a696e8b52d1274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3289273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651040516890e575dda0386a3a144f7c87c901c8cc4f6f569ab5f52f74770f1a`

```dockerfile
```

-	Layers:
	-	`sha256:71bfd3e9d8927a16c53044b21e9acad2641cb6c8061a994d83dfbea8343c7797`  
		Last Modified: Fri, 02 Feb 2024 02:23:20 GMT  
		Size: 3.3 MB (3273456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae1f755950f83595db7bd5e55febfdf86b770a10abbced80f4e68b5ecd8366b2`  
		Last Modified: Fri, 02 Feb 2024 02:23:20 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:33c2ac06e7eeb5650fdb8b1111b8af751c4e47627dee7f615d144cb4648e9c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54015451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea9fd04510a5023511ac1f3215830c904db5bd2b27c6dd28a69863a8db63a7d`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
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
	-	`sha256:8477f0313bb2e438d127d2cf0d957251b32fac84fe1baa6de4e7ddbfddf5dd3f`  
		Last Modified: Wed, 14 Feb 2024 07:30:53 GMT  
		Size: 23.9 MB (23944107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46a7f15ba2c3d59774312e2238855daf228cc2fc7bbd63efabc92076f115537`  
		Last Modified: Wed, 14 Feb 2024 07:30:51 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:af1fff83968b52a7a16e61e4b65b6d94bc40984e1451f25960394e89c98ba39b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3380960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f52111033b9e4de7bcb6c57a5dcea0b2b6739695a82cd9134ebb4eb79a85eb`

```dockerfile
```

-	Layers:
	-	`sha256:697d851fcd89fca2278901d157546599bc25e2c75d0ae9cac3bd1f32c238fbfd`  
		Last Modified: Wed, 14 Feb 2024 07:30:52 GMT  
		Size: 3.4 MB (3365197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea30c10179c3305d4fe8c72a498ed2279516c3f700a0b7bcd503d144477750ec`  
		Last Modified: Wed, 14 Feb 2024 07:30:51 GMT  
		Size: 15.8 KB (15763 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:24999f3bcd02637a6200909ee0a47ff2c95481df702cb0a36398502cdb8a14ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58710984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f95554811a36d415b88194171bccc33e64b2263447907b2817771057415c91`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc040da6cd6ab115eb2849e601c0f46ea3e8dbac5788eaa949eaaf08de7397a`  
		Last Modified: Tue, 13 Feb 2024 02:06:46 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9cc1040c450c999433061645fdc8bca3076bdc3baded72a3305b44e726b88`  
		Last Modified: Tue, 13 Feb 2024 02:06:47 GMT  
		Size: 26.3 MB (26303276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a1b7160f46bd98e575349f93c0bac1552d3aa21462778a429829685f53be38`  
		Last Modified: Tue, 13 Feb 2024 02:06:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ea2f2a1fe5b54e2b361469c05de43e2c4b9f5f861b1b2f4c530cce7888255dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f6afe21d6533f69989f73d7f67be616e61015639a6d28e0954fa6e50b55993`

```dockerfile
```

-	Layers:
	-	`sha256:d6be16b0e02041f241d4816a5a9581e698454abf978a7817fd9723fee855c0fb`  
		Last Modified: Tue, 13 Feb 2024 02:06:46 GMT  
		Size: 3.4 MB (3390586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b7433d19b97df8df75e3592815891212e2480bdb7476f86786071267909299d`  
		Last Modified: Tue, 13 Feb 2024 02:06:47 GMT  
		Size: 15.9 KB (15898 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:7210370e7c06445d9bd74cb807575801baebc395cc43c07df8e78fa14d4b581d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53191991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87324eed131dfab860e195d81389177e8ea4535c4d7a4f2559d6a95b92d6447`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:c74d2ef293040606b9450e82efd37b5ef0dc7ba25160e7762da18e804abd6338 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:231db420c5b3972aa42bcdfd7a71d4d6d22f911ebd5b7ed62d957cef65d0dddf`  
		Last Modified: Wed, 31 Jan 2024 22:39:47 GMT  
		Size: 29.6 MB (29636258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c307ba9095acb428edbd7b1bca9f016fb7729557be0a5edf11eecf4fc98f966`  
		Last Modified: Thu, 01 Feb 2024 22:48:33 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0324760d0d95be1565f4a949ff0e8cd4123d0c4eca236cd275047f07819f9263`  
		Last Modified: Fri, 02 Feb 2024 10:47:54 GMT  
		Size: 23.6 MB (23555467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcab98b932e538940d7abc4ae359fff4253a8e5b5d79dbe8fbd1914cbe65cb4b`  
		Last Modified: Fri, 02 Feb 2024 10:47:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:49aae29aa088ce079f3e0360f02634ee50a17605f390fa4d267a338f9e06cdbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84615757f4c9f952bfd9000dd7465726394f56b11cdec0cdc0b2a3111456356a`

```dockerfile
```

-	Layers:
	-	`sha256:697977d5db716a298c3913fced354b8ac9932af90f86c0476c3d681a8027df3d`  
		Last Modified: Fri, 02 Feb 2024 10:47:50 GMT  
		Size: 15.6 KB (15588 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:b2837481e238151caf84516b4e40e65feb84e92230fe4c010b5918ad9f098938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60419308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ab9ce8e2ac93a99e7793aa7d3bac770733e20d5658a1d7e7514779594931b4`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
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
	-	`sha256:41a5a47f63341855985b78468f3dd4dbbf547b83a087f936b7e58ad79183b31c`  
		Last Modified: Wed, 14 Feb 2024 03:31:36 GMT  
		Size: 25.1 MB (25121243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9871d1f7bd34df3ed6a69316dab15f9d9bdd44a6fbc3b156cb7aadb535f7eb6`  
		Last Modified: Wed, 14 Feb 2024 03:31:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:12031a7762197ef75fc1fe8a81695858146aeb4b2d866868e989854cf0240d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3394259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39596e15bcf408df0f93c1924e19ad9f7e8d18a19a50d1981d5d2ce672845402`

```dockerfile
```

-	Layers:
	-	`sha256:af40a6ed9d7d511f5a0ea951dedd2a80f78837120a30fd0627e39ce5da05ef08`  
		Last Modified: Wed, 14 Feb 2024 03:31:35 GMT  
		Size: 3.4 MB (3378472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c734b6b6d29268d3ee5b4b6c8475b9d2881d6c19aa518f8f182afeb3c5b5704`  
		Last Modified: Wed, 14 Feb 2024 03:31:35 GMT  
		Size: 15.8 KB (15787 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:6c1e9ce2590f58ad0b0ee0d3fdf31e11251d87b231344a16d055becbb8da9d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53506152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d0d1a6174fdbbef9e74d7746406269a2a887f1b18fb737fb7b0e2751dd34ff`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:9a48c9d7fde8a2820cff9dc06434dc4dca8967438fa75bb93e6646cb44682b18 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:16651f5430ff52661c6729a9dc23c80d76205b6bd77d7730f38e39aca6731613`  
		Last Modified: Wed, 31 Jan 2024 23:29:40 GMT  
		Size: 29.7 MB (29657133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a76b2173edbe448f074d25286d3e30d056d4433ad47cf253ef7870a60f49c3`  
		Last Modified: Tue, 06 Feb 2024 14:26:39 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4205daa4f70720c089038dfb8eaa1e57e542543f89aa25ff6117dad36efda35`  
		Last Modified: Wed, 07 Feb 2024 07:21:49 GMT  
		Size: 23.8 MB (23848752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86832042a6a476c4961135a9ccfab65d3b962b05bee4ac1fb17f1fd2ad1b2b5a`  
		Last Modified: Wed, 07 Feb 2024 07:21:48 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b790145fcbcfdd5e8ddbc0ed4d73d2ce00c96110ba4e7c88159e0f900c5e93c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45cc5dee2f64998fb284092b67f92f4d0218509fdcd44ef14dd8c4278923a7fb`

```dockerfile
```

-	Layers:
	-	`sha256:2a789335df7fba07d1d97a609fb8b4335a5783e4b24e1286ce0eb1d5c05c2c3d`  
		Last Modified: Wed, 07 Feb 2024 07:21:48 GMT  
		Size: 3.3 MB (3285593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c266f1b38aa7b9a4c0c2318425cc7045efccb2172ff9f7e8d645e83d9d62cb31`  
		Last Modified: Wed, 07 Feb 2024 07:21:48 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json
