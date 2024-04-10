## `perl:slim-threaded-buster`

```console
$ docker pull perl@sha256:0d5187b36660c5acddd378642a463cec809fd8a1d80bff3b3bf03b20cacee818
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
$ docker pull perl@sha256:238658bc6b543767d9ccdcf88b3e9d9cbd86cf331fc4eccc81d53521c9e88ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54580468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e6e94d11f3465d54478a8d09a32c29a54eb05c511b78b9a212ac2b22d07da`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252d638a159a2c18463c4afb7bd1dc4b446ac418d23c6db9b4231f014d159481`  
		Last Modified: Wed, 10 Apr 2024 03:02:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5ab9a3bed786afddfd2d20886911f0dfa9219e0c825abaa7561959659a0d96`  
		Last Modified: Wed, 10 Apr 2024 03:02:14 GMT  
		Size: 27.4 MB (27389340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2e08f9b08dc03e6c67bb4f3718b7f4f6c79dbe0b1e40ebe3a89d66b34deab6`  
		Last Modified: Wed, 10 Apr 2024 03:02:13 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:718bfd20f8c8029876da77bc622ce97b0622660dbb3123fc50535aac1a79ffc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3381826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c367b341071feadc3a9fda60e721eae5101cf87089b32f7f553291d5e02afd90`

```dockerfile
```

-	Layers:
	-	`sha256:490ea20b8f52a4a0b829671858fc4e716b878f82d54396a8427e3d52c838bd05`  
		Last Modified: Wed, 10 Apr 2024 03:02:13 GMT  
		Size: 3.4 MB (3365348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aae59c5ab162257aa81e6dd7f90998d5bbb6fd27f123730f8931f716b6d2bd3e`  
		Last Modified: Wed, 10 Apr 2024 03:02:13 GMT  
		Size: 16.5 KB (16478 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:0b0c44d6c8f7d3ff46bd8cfa79d324a8ad1565cdb044afd41be717b36ac1f341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46725713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887933287f3e5a0be2347a8b970376158ca976dae2b2b4853996592eceecac52`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:87f5e14c74c217f7538860dd43d6b1910663955972cf5270e3d1a8254956878c in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:3f02c84b2c1c85cfdbae8bb78a52226f2b54d86f3eb2466ac3a81fc25ffde9eb`  
		Last Modified: Tue, 12 Mar 2024 01:05:07 GMT  
		Size: 22.8 MB (22795622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de372dda0a886193e16274c3eaa61bc51a13f31b3da76144f8933f367ae4c1b`  
		Last Modified: Wed, 13 Mar 2024 01:31:37 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7bcf31e8418be0a611a01e2390a5e4aca0ee2288e30cfdcb85ede36603bc7a`  
		Last Modified: Wed, 13 Mar 2024 02:21:35 GMT  
		Size: 23.9 MB (23929824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7107749beadefcdf03fea0a429bea0b7c853cb2ee930d96035168ee57388c8`  
		Last Modified: Wed, 13 Mar 2024 02:21:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:425164edefa83a93a2baad914c13728150be4b56d84155dc8089c2c1127ebfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3356811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b51e0e36e56c1663477e9728fc813a9adacdaff6dc205c3ea5c345befd13da`

```dockerfile
```

-	Layers:
	-	`sha256:f23fd25d8864b47a4d4eb485003d0b331dccbda79ccb598b64f059cc993d2528`  
		Last Modified: Wed, 13 Mar 2024 02:21:33 GMT  
		Size: 3.3 MB (3340422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d26630c6add02c5c5a0fd3f28ae6ed84f7f82d2c65c1b84dac578e287aeadbbb`  
		Last Modified: Wed, 13 Mar 2024 02:21:33 GMT  
		Size: 16.4 KB (16389 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:cd5432fdbcc3d833fc783dd11b9f3190a1b78cbbb8535a8845f55b6caf14e670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51964374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb714c0ceedd20635191a8e129fb7c055d1c93e423f9070058e90760f21c5899`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1812a739984a1efc367a9d7653f7f339da92ad7a6bf6159f5cfc60f8dd1155`  
		Last Modified: Wed, 10 Apr 2024 17:15:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3747e3e66e061b6fd5ebec7aa2262c5fa2b99765eaa3df5cc06930dcc343b533`  
		Last Modified: Wed, 10 Apr 2024 17:49:00 GMT  
		Size: 26.0 MB (26000647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e772435718e6197a7d02f4f0c0c4ecce985ade02cb3ecf57528b770791304c`  
		Last Modified: Wed, 10 Apr 2024 17:48:59 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:2135ebf71e0b02b918ebeaf23af4378daff15c5d153d43a82a4a0264f5e41317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208141db382f267889b6435706a17777d723c6305559fea8b8bb4813bd44ecc6`

```dockerfile
```

-	Layers:
	-	`sha256:4f87690f167a74b5a53fe8b6950cb51493cb4bceac8b61f288b7ac330ab4aa89`  
		Last Modified: Wed, 10 Apr 2024 17:49:00 GMT  
		Size: 3.3 MB (3334820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12598eaa26be760fd90fb190c82a6254265873b3bb1449de6aa71247bee5526`  
		Last Modified: Wed, 10 Apr 2024 17:48:59 GMT  
		Size: 16.3 KB (16323 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:40023bd83b4cae85a5f3fc0bc68c70fcd521bbcd2922ad61bfa24b44ab82c9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59408823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192cfb7ab6f02e0d79ca1505223b56a84dbf57074516f401cd5bf28ad05482f2`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:6033d014a0c5c8d87a61d23e20506ec550ea93ef72866e76bfe5a468ceebf619 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:d349bc9800fc6053f91af64b3ce845b5191cc9e0ae2d2001951381ae2d08e46e`  
		Last Modified: Wed, 10 Apr 2024 01:03:40 GMT  
		Size: 27.8 MB (27848331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef316b5bba9d0487adcbc4647678e843bd31e7a228ef229ae1a4b2ead3db70cc`  
		Last Modified: Wed, 10 Apr 2024 02:41:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c511fabb98d329cb19d091d2c7e4d8bba1c3ac3cc280663dc2ee91f544ad9d`  
		Last Modified: Wed, 10 Apr 2024 02:41:11 GMT  
		Size: 31.6 MB (31560226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59541935416dc1fed4dc9d5ddded800c09d3b4c3b3bd479e6ec69864ad7d67ec`  
		Last Modified: Wed, 10 Apr 2024 02:41:10 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:116c1fa57c06605bb9d665a6d5cbd983917f2df6cc7063bdc7f69505bd827f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3400589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17167afde2e88e2382eb00c09aeeaf4e7451787efcbb0b0bcd7990ed56fcc22`

```dockerfile
```

-	Layers:
	-	`sha256:b6dca6e5730769ada1483d6f88c13ac0674d119f6b88f48569307e3d0c0a5d62`  
		Last Modified: Wed, 10 Apr 2024 02:41:11 GMT  
		Size: 3.4 MB (3384145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4626b5494244519abf660c4928cb6adcc5c52c0303d28598bfe017620f5fae4d`  
		Last Modified: Wed, 10 Apr 2024 02:41:10 GMT  
		Size: 16.4 KB (16444 bytes)  
		MIME: application/vnd.in-toto+json
