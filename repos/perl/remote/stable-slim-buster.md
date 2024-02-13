## `perl:stable-slim-buster`

```console
$ docker pull perl@sha256:cf6b844c6b5c155fe4eed29a3acd58056c6199f1e52828f4d929401c016b21ca
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

### `perl:stable-slim-buster` - linux; amd64

```console
$ docker pull perl@sha256:edb8b89bbf0b35880fb0d774a968140231bca10ac470acf9cc7f386a57ea0099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54515869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc1cfc1f07c52f3d5a624a8c8c937c97548e2c16ee2c531a237c185db61a5d7`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:232125261662ceeb0126b96defe05092c121fecd55c99db5f76a03ab0c87d07e in / 
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
	-	`sha256:789bca57d694bdff72d9fcb5bdc3f4684b63dee11402ed28245ae1c578d62ba3`  
		Last Modified: Tue, 13 Feb 2024 00:43:30 GMT  
		Size: 27.2 MB (27188190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845f8640100ed066075d196636a9795f414d4b28dffeac9945f2060299fb5496`  
		Last Modified: Tue, 13 Feb 2024 02:03:08 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0757fd8dd08a0f983a0b1b284aaf839912b9c23a16399cef7f99fd2c2331b65`  
		Last Modified: Tue, 13 Feb 2024 02:03:09 GMT  
		Size: 27.3 MB (27327414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8d22abcea2f33ab7b123be08931ccadc4fff3311a6be35c00f858e2e1437dc`  
		Last Modified: Tue, 13 Feb 2024 02:03:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:d8c94b679f909f9a8e4a6242b24ecfa821be05c88c7d1d95d6730d0d0b4acbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15b0edf688c79151a531dff53365b4cef1847919cbaae3802a864d75130ed1c`

```dockerfile
```

-	Layers:
	-	`sha256:eede25403178cf166187abe1c9028b43806d2c8e7ba1747f232e8ee3ac399d59`  
		Last Modified: Tue, 13 Feb 2024 02:03:08 GMT  
		Size: 2.9 MB (2919368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6320d56d6c189491ee2d761ea2cb082765005b43908f918005fe7295af2d3541`  
		Last Modified: Tue, 13 Feb 2024 02:03:09 GMT  
		Size: 16.3 KB (16337 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:34aecd7b40f13347eff819b5bb4cba1a2c3348169a2a9a3d20dadf1134f6f3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46705382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e336d7ab8ebac9ef17b796bab4c7c4004d114c9c3d316606247ed9305599d1ac`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:34e8fc4544a9986a7bf091ba5d31dbe51ee7c3c403fc9de427ca8944fe91298f in / 
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
	-	`sha256:342befe29912bb1e1d01bf5c9c9e8e50b3a65a92b7f2b1d90c33a723259aae09`  
		Last Modified: Wed, 31 Jan 2024 22:50:19 GMT  
		Size: 22.8 MB (22795569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c02eb97121922ce781a1b387b33360b30d0a17a30d5e1853d3edc9fa1cbb74`  
		Last Modified: Thu, 01 Feb 2024 20:52:05 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8472f29ba58f1371d54389dc946fa4deca817045b150c493a6edd250aa913182`  
		Last Modified: Sat, 03 Feb 2024 14:52:43 GMT  
		Size: 23.9 MB (23909546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdce689f34c562ad543f0b1402c63b5bdb89f53d1ce8923f72a57d9b8164b4d`  
		Last Modified: Sat, 03 Feb 2024 14:52:42 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:45dd0727c80817f81cdabe65b86feb41284cb2cc76da036e3b6d1beb514110fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2914650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a262ac3c2c83e75495977b60028bd4f6be9b4cfd4a0056c22e57b42597c51b9`

```dockerfile
```

-	Layers:
	-	`sha256:3db2cd497953d2da3e2967c066dfa3fef337869078a52f43dca028c9f9a13b3a`  
		Last Modified: Sat, 03 Feb 2024 14:52:42 GMT  
		Size: 2.9 MB (2898402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b38772070b6b1776ae33f2aeeb460aa5424083b024a46acfb0d37e19adb23c99`  
		Last Modified: Sat, 03 Feb 2024 14:52:42 GMT  
		Size: 16.2 KB (16248 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:51fd330a2cd79d6f98bba390f22f5112511dfc457df8c51c0f7862d36ce0d214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51933501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccbe325b6943399d1c4e01fc8b6b358f90a8ed75c9cfba16932a32932e27fe0`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:de90e50e142aa92c29d5128e1cd025fd5c5b91f879a19a06a8b49451a4e6afb9 in / 
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
	-	`sha256:42641f7bf1512c205041cf7899e52e2185e49bcd6cfa0cb8ebfc73e3009221b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:34 GMT  
		Size: 26.0 MB (25970227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72a89351b50fe548498df8b973c933cc6e8eb9bbbdf1bef89e8b681a4c70dc0`  
		Last Modified: Thu, 01 Feb 2024 16:38:55 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1121054b73a11ce4b1d35ed3a40eb7c1449965b3f8448880b43568090a91796`  
		Last Modified: Thu, 01 Feb 2024 16:38:56 GMT  
		Size: 26.0 MB (25963010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39df84f17c12f1aebb1f8c90c248ae787f7aee5011d4abd315e165c3c592d16c`  
		Last Modified: Thu, 01 Feb 2024 16:38:55 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:871214a30c8481e0f76d4c4642de2fcd00003f0fa5f926bbc747faf7c76d6057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceede74a58a8200dccf01c18c3cb2847b9c3b766043f05b51a76c65c38a81242`

```dockerfile
```

-	Layers:
	-	`sha256:147c01c81d53ed8638adf52204668f50cc64423e0ea42b175db8beb939dc1f63`  
		Last Modified: Thu, 01 Feb 2024 16:38:55 GMT  
		Size: 2.9 MB (2893080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc723efb0a255d0f63323b706dcdef716d275ecc41df268e33150587751533d`  
		Last Modified: Thu, 01 Feb 2024 16:38:55 GMT  
		Size: 16.2 KB (16182 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-buster` - linux; 386

```console
$ docker pull perl@sha256:91cb90c9d1416680e2f043f3d3bf4a62658ffc869a8f8bccd3429cf5e88c1f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59297791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b175264bba5b025329933b2fd5bebf3567c2c02105889a28706ec58ec653d68`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:08f96b15b2da153843e0da5de223845c3e2687e03502857416effec0f1070da2 in / 
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
	-	`sha256:d96589ec9f6e89924970de1915516d7b8a4e8fe3da0fd37bda398d2d3ae5b529`  
		Last Modified: Wed, 31 Jan 2024 22:45:26 GMT  
		Size: 27.8 MB (27846800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c07d6fc22c3252fc1bea042439e5d1b4eee8872f2e001280dd31d1ead611502`  
		Last Modified: Thu, 01 Feb 2024 00:05:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b22fa709dc20bee3432e1a079170929cf066369eda271c9bbe38fdf790663e`  
		Last Modified: Thu, 01 Feb 2024 00:05:11 GMT  
		Size: 31.5 MB (31450725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8080d0aaf6b0ba64185b6562dd07133e5ae80a1f1db6638a941dc2bc554c051`  
		Last Modified: Thu, 01 Feb 2024 00:05:10 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:61abc90e77721bf48a93e470372a910277c167ad8d978a5a3362019c2b9edfc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2951606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d478ff9ce2f21927872f3b4793c0b316b7ae4e4f4c0edee528ad531575cac64`

```dockerfile
```

-	Layers:
	-	`sha256:8bf855bdca466aa5e41056b6769a617b1a5995429973ca69659820dcb8fcea52`  
		Last Modified: Thu, 01 Feb 2024 00:05:10 GMT  
		Size: 2.9 MB (2935303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d832dd248d727fd6767affd8f6eccf73cf7652a3c09384d2c5bd4807edc5ca0`  
		Last Modified: Thu, 01 Feb 2024 00:05:10 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json
