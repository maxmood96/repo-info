## `perl:5-slim-threaded-buster`

```console
$ docker pull perl@sha256:f5c906cb182f05f113da383181df1da4b01a8a4328930fd44dd61f34a7f15a16
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

### `perl:5-slim-threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:966db9974fc237756e1015d1db0c550eacc343aadbef1497085e0ce64ca321a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54576822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763be24edfd9da4cb613d88ab7a69a54d114238c5b5a7982648364c7924626a2`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:232125261662ceeb0126b96defe05092c121fecd55c99db5f76a03ab0c87d07e in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:789bca57d694bdff72d9fcb5bdc3f4684b63dee11402ed28245ae1c578d62ba3`  
		Last Modified: Tue, 13 Feb 2024 00:43:30 GMT  
		Size: 27.2 MB (27188190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239cf874c9adb444e29bc89055db53240ea03af3952ab62221d8d270ee56e7be`  
		Last Modified: Tue, 13 Feb 2024 02:03:57 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582646463c73fc002783c79e520e89bd752c848045099fd0df41296cab8cb1f2`  
		Last Modified: Tue, 13 Feb 2024 02:03:58 GMT  
		Size: 27.4 MB (27388367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0252a9a553745851d16742e1ab730147ef81a0fcbdb1465a9a06c76945e3f9c`  
		Last Modified: Tue, 13 Feb 2024 02:03:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:a8532cfc1e73b2620eecb242cb1649c75b232e13184359083a30cae22e3545bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b09e8fc607a84c38d96899992dc9eb1cdb72a6a0e8226a07c0778dba0fc494`

```dockerfile
```

-	Layers:
	-	`sha256:2004a4bda007275a4847cb9daf1e7c5b092f3b9d9f33fc438e3513b34da40af7`  
		Last Modified: Tue, 13 Feb 2024 02:03:57 GMT  
		Size: 2.9 MB (2919458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:022e4c0fe39c94e6505f6efb34d3a0405991e1cb8d179b1169f33812d32358f8`  
		Last Modified: Tue, 13 Feb 2024 02:03:57 GMT  
		Size: 16.5 KB (16478 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:c1fb2b7f6b6ebf5063b607d1e614fd877f400493a11a0fbf8a0f9c4b1960bbd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46725780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729c828c0d9eb71463790fb652ca5a95985d5f088dd144a5d57ef832ea768de6`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:34e8fc4544a9986a7bf091ba5d31dbe51ee7c3c403fc9de427ca8944fe91298f in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:342befe29912bb1e1d01bf5c9c9e8e50b3a65a92b7f2b1d90c33a723259aae09`  
		Last Modified: Wed, 31 Jan 2024 22:50:19 GMT  
		Size: 22.8 MB (22795569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c02eb97121922ce781a1b387b33360b30d0a17a30d5e1853d3edc9fa1cbb74`  
		Last Modified: Thu, 01 Feb 2024 20:52:05 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11b56a0a17218c76f8f59380eb2606d8c97457f0949da016cf82992ff8d3591`  
		Last Modified: Sat, 03 Feb 2024 17:50:19 GMT  
		Size: 23.9 MB (23929946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246157f6fbcf6bb3239f981c5b105fbf6a251741a0823c36aed01f3572c194cb`  
		Last Modified: Sat, 03 Feb 2024 17:50:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:1bedd85e203e268ed4c7bf3194e572ca58211e5852dce1c3245155292f21f38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2914881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502730a13b7ecd74eec2ebb0d59798fa840d8f22790f0befa6e06f3453fccf90`

```dockerfile
```

-	Layers:
	-	`sha256:e4f8309bb808276b634674c1dc71352593586084688bb1ab8c3b1deb8802ebde`  
		Last Modified: Sat, 03 Feb 2024 17:50:18 GMT  
		Size: 2.9 MB (2898492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26e580f484e1e06dc0169fa18eccb580a4363b8b21eeb61c17188c208a09e40`  
		Last Modified: Sat, 03 Feb 2024 17:50:18 GMT  
		Size: 16.4 KB (16389 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:180de120762eeec4ce64c1b210b17bfb205cebc20f649088ebf49e15ebc23d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51970476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b322790af2c2ca7be97324345e78bf1564b2b7b428cba569224be0e9e4c1de32`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:56f9fb4bf0b803f4553b7fe668c34676467e662e3ab02af10e815a93ebbde1d6 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:385d4b469e017d252e714475f8232bbe934f4fd96bc217969a221a1039b1aedc`  
		Last Modified: Wed, 14 Feb 2024 03:37:31 GMT  
		Size: 26.0 MB (26000400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479a6068502de0d7c2071b572bb1495d171e07b93df3cb354e0627f3bac763e3`  
		Last Modified: Wed, 14 Feb 2024 03:37:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:815acdad705a5f159dff07c0d104bf853bb237308ce51fda9521e4801da32e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b328cc5963d88df18d240b4747200f7b376330231d957125005493394957ff34`

```dockerfile
```

-	Layers:
	-	`sha256:f32b81953b08e82dbad1aa0e5b2c9ee1a49d1de6500ab2639415cf2c2867ab03`  
		Last Modified: Wed, 14 Feb 2024 03:37:31 GMT  
		Size: 2.9 MB (2893170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08426387a0e73e731393bbb1a84c5d460eabb7298a0d393539c2149ed3cb2418`  
		Last Modified: Wed, 14 Feb 2024 03:37:30 GMT  
		Size: 16.3 KB (16323 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:ea0702191f82526789e282bad6b4e4cc17c40e203e60b10daaf9c3cc618db7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59405079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c7842558ba18f8ad534466ed5a9b6aea70516cf294c4e9bb50f5e2b4ac7a28`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:3ff71d8500563a5fdf27e800f24879e0da378a12b7855b0b22093604455859ae in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:84066ea3430e479cab8d0a4e50aa533239bed5e2e80e3f35e4b706965223b696`  
		Last Modified: Tue, 13 Feb 2024 02:04:25 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e9dc8045a9630f960a0493649dc6f410fb7b5e9ed1a527ef458a0b1a9705a6`  
		Last Modified: Tue, 13 Feb 2024 02:04:25 GMT  
		Size: 31.6 MB (31557953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ad7f3f01e507bb3d419dfe0220bef293cca6f0ed320600a351076e114c62bc`  
		Last Modified: Tue, 13 Feb 2024 02:04:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:92ded459bf60a8c70c78eeffb2a6e5217bd07a79ae24d48789f32fe140262e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2951837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75d4ee63d9aec24287074c09febf0cf36668c23d9bfc8a09bcea373d2a94965`

```dockerfile
```

-	Layers:
	-	`sha256:d31ee188f07699d056c82b85766a647c36ee95d5e3a6e0c01a2e99758866a268`  
		Last Modified: Tue, 13 Feb 2024 02:04:25 GMT  
		Size: 2.9 MB (2935393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:582a5dc21df2684a62ea54842b1ab35a4aa38bef53f8ef0dd7e81621d988880d`  
		Last Modified: Tue, 13 Feb 2024 02:04:24 GMT  
		Size: 16.4 KB (16444 bytes)  
		MIME: application/vnd.in-toto+json
