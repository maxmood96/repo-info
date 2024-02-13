## `perl:slim-threaded-buster`

```console
$ docker pull perl@sha256:e92c010e94ce0cdf83ca468737fe62ffc1ab16c44e5d4e3b12b5c30cb5e37d2c
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

### `perl:slim-threaded-buster` - unknown; unknown

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

### `perl:slim-threaded-buster` - linux; arm variant v7

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

### `perl:slim-threaded-buster` - unknown; unknown

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

### `perl:slim-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:34cd6085ef17a076f397641f34f51695a01c0080f823ee7b67e80ebb4ba4784b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51970925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c172cd90d45c02ba9ca19c62d80a34410f9d0d78adcbd888662a741adbe3c5`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:de90e50e142aa92c29d5128e1cd025fd5c5b91f879a19a06a8b49451a4e6afb9 in / 
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
	-	`sha256:42641f7bf1512c205041cf7899e52e2185e49bcd6cfa0cb8ebfc73e3009221b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:34 GMT  
		Size: 26.0 MB (25970227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72a89351b50fe548498df8b973c933cc6e8eb9bbbdf1bef89e8b681a4c70dc0`  
		Last Modified: Thu, 01 Feb 2024 16:38:55 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849e9347ae271360e5a8d7991aa3d79af8c80965fff747d0311720422d9531fe`  
		Last Modified: Thu, 01 Feb 2024 17:25:06 GMT  
		Size: 26.0 MB (26000434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf27d8624990711d92474f9008ce420817849c15e395fff7bd9110317382230`  
		Last Modified: Thu, 01 Feb 2024 17:25:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:d029686e91eec76796dbe8f1a80e7d4a7e859b3668a893989688c6cd1e77c5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d478482c15b14f459bae9e864efdae2408915b49c63d581bc0e4b8f653bc3f`

```dockerfile
```

-	Layers:
	-	`sha256:f1f1520982429eae68dc52fac044783980317ec684352c52fa8a0d12ca0b0de3`  
		Last Modified: Thu, 01 Feb 2024 17:25:09 GMT  
		Size: 2.9 MB (2893170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97ff761298407475f9441a5e8fa5f70ea5179d73449a37c3a5c757c0bb01f043`  
		Last Modified: Thu, 01 Feb 2024 17:25:05 GMT  
		Size: 16.3 KB (16323 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:b4f5f9d879c9fb539e724eef946b6f50fcd15aa23034c1a8344fb2fec94a7f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59404812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9605f8aabc48b4b9c1613a64a670dc7cc7ebd7ffee8aa3ba97ae5d3cb0d624`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:08f96b15b2da153843e0da5de223845c3e2687e03502857416effec0f1070da2 in / 
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
	-	`sha256:d96589ec9f6e89924970de1915516d7b8a4e8fe3da0fd37bda398d2d3ae5b529`  
		Last Modified: Wed, 31 Jan 2024 22:45:26 GMT  
		Size: 27.8 MB (27846800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1679bde493774c1bdae384371c7c7d96587530be579315669b9722a2e0c3ad`  
		Last Modified: Thu, 01 Feb 2024 00:06:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56945e9080e3d570b53e868847e9de10840557f34e703c338066eb6b8cec24b`  
		Last Modified: Thu, 01 Feb 2024 00:06:44 GMT  
		Size: 31.6 MB (31557749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b9042b7a3f9bd2a988aa950d22e5fad551776311358cd7a678dcea9ae49df2`  
		Last Modified: Thu, 01 Feb 2024 00:06:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:b6736b9acd1169a7377031e040f85e3c2ea1865c29cbcaf68f5a1b02992bfd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2951837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6966b1a2644eb917d922dd9f6984b0601157bc0f41a5fb5d4e6e37b8a21b4a2d`

```dockerfile
```

-	Layers:
	-	`sha256:fa11276627713a7022609cd9fcd876c70a07ac2e5da80c4c39dcdf8f09a6666e`  
		Last Modified: Thu, 01 Feb 2024 00:06:43 GMT  
		Size: 2.9 MB (2935393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e2940f2c7714eeaaa6c0d5a36638b3c392032866f879ac93ca2dd8eecfff30`  
		Last Modified: Thu, 01 Feb 2024 00:06:42 GMT  
		Size: 16.4 KB (16444 bytes)  
		MIME: application/vnd.in-toto+json
