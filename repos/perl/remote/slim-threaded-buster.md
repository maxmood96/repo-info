## `perl:slim-threaded-buster`

```console
$ docker pull perl@sha256:ed63d7a27a19ebff474da46a7d3a7b9ff9b77b5dcc065315d495172f6b1e941e
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
$ docker pull perl@sha256:b0096bd7cfa262ca7cefc490085df3f683613880c7c429bcb673185e1dab7203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54576799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123c3d1b51d9e0087988aa56a532e7bb6097fe082b07b1797d6c2cad8494b6f2`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:e64f92c07598d7a1e58a8116342198e837ea4ed870cac2c252323c261b270566 in / 
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
	-	`sha256:4a21b857313366ffd622f19e31c4300a81dce92b023b4ff6583ca167179804ac`  
		Last Modified: Tue, 12 Mar 2024 01:26:59 GMT  
		Size: 27.2 MB (27188304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060882f85d979d67452654f8e942c33ddf04ea6a3d40421745cd8c35f9038351`  
		Last Modified: Tue, 12 Mar 2024 02:04:25 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113979a0cd5dd297caca46a11291c5f0f93e71e2045da85ecb2cfa8ab121de34`  
		Last Modified: Tue, 12 Mar 2024 02:05:38 GMT  
		Size: 27.4 MB (27388227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9499f442900ba63451f07254a8b390a5af33a2286c9d2e9ee7d1bcaa67aa429e`  
		Last Modified: Tue, 12 Mar 2024 02:05:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:eb96902233a4d882282aaa22bf3039f8cd3992ec78bab020829581db1f5b177b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3381682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60a2704ed9f971ae1af6fc99cc625cca0e16b004e6776f23395352620465942`

```dockerfile
```

-	Layers:
	-	`sha256:721e95e74a979182288ea4830659a62b4308b0a0a772e517ad26c2fb4641f61d`  
		Last Modified: Tue, 12 Mar 2024 02:05:37 GMT  
		Size: 3.4 MB (3365204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0699af0fed696918527655fbf7c9e4091d5c361505d1f344261cc87aa3d7611f`  
		Last Modified: Tue, 12 Mar 2024 02:05:37 GMT  
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
$ docker pull perl@sha256:a5e99407fbcd2f2fc518b19b54dec538db3650a12e21de98f79673d2d1ede929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51971353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70565d962c52c53ca822fb97453510a0764be4852960ba98d66a7d733c1d308`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:01e6303e5bd3d7bb8200a616ab1d931421cd756c837936b3f897727814cb89c3 in / 
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
	-	`sha256:f109bca8a22fa25fc80b89d2ad693f6f3e7832d4386218a35d068f3b37b0e808`  
		Last Modified: Tue, 12 Mar 2024 00:50:11 GMT  
		Size: 26.0 MB (25970589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2281cf6618cd10cdaba7967449078edb12e3ce50b90f83facde00b79b01b630a`  
		Last Modified: Tue, 12 Mar 2024 23:12:08 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588984537af25bdd08135d3286bfd79f7387fecba74d79acef5e1a63a142b69`  
		Last Modified: Wed, 13 Mar 2024 00:03:21 GMT  
		Size: 26.0 MB (26000498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dac8033261dbb54902fde4ff9983aa4f21818b23335239974959123003a315`  
		Last Modified: Wed, 13 Mar 2024 00:03:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:ed9ad6ece732757d7e6e4ac959d857fbfe45571f3fa200f315ed255fa9b3fc06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3350999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba839d8bf28da4a35cf0f6d88422e777b5b8f47238fca8ed58feceb20e3e7a5`

```dockerfile
```

-	Layers:
	-	`sha256:c44e03b63bff17b08d725e972f7a3f6a4f4ec52f2f009a63c6eb189b10ee2d3e`  
		Last Modified: Wed, 13 Mar 2024 00:03:21 GMT  
		Size: 3.3 MB (3334676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065d5cf8782139bdd854a2750155f8eae72573e9a1a616138a1d25bfcf537403`  
		Last Modified: Wed, 13 Mar 2024 00:03:21 GMT  
		Size: 16.3 KB (16323 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:e54456c490ac9f0ff2c6c18b0125c47d97434078ba60c9eba9e5dd52d8d37eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59404957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4e28d06e556316bf6110947b8ac23a5f22d12766182a618003d99040f2740e`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:c79a5b18bf34759ac9ea36615400037e5c793216013e88cec1fe6bda9664a062 in / 
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
	-	`sha256:9e73dc674f1e3ae50c687941320c277d1320ed6eeda6f5f5ca3d1f70eee2bcff`  
		Last Modified: Tue, 12 Mar 2024 01:04:15 GMT  
		Size: 27.8 MB (27846708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32e114331d759d173394106d0aacfa1430b28882d96284117176620ebcece4d`  
		Last Modified: Tue, 12 Mar 2024 02:05:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5464d9eb3022c16da122f66a11d2248a2baaf33b81f4f307dc3c446d35f34d2`  
		Last Modified: Tue, 12 Mar 2024 02:05:59 GMT  
		Size: 31.6 MB (31557982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd4b581be2f53107c78f0aee3e84ac9ec7eaa62ebf200c9fecb28f06953dbea`  
		Last Modified: Tue, 12 Mar 2024 02:05:59 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:206adabde48ef85a37d66d1db2b38774a1ec8ddb7ff54b60644d6dae2820c831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3400445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23248d16463a626b15e46640cc9617a52fd45876a2f78170e257735ee106a99d`

```dockerfile
```

-	Layers:
	-	`sha256:0f9b908490fd27f81cd3bd3215ebe991735a7e8d903eab1b3e46cbd725e5ee61`  
		Last Modified: Tue, 12 Mar 2024 02:05:59 GMT  
		Size: 3.4 MB (3384001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6d266c7d03f52d8d90d70829f1d1f4fb3b1f370de1fb83ffa9d5d89ed5317fe`  
		Last Modified: Tue, 12 Mar 2024 02:05:58 GMT  
		Size: 16.4 KB (16444 bytes)  
		MIME: application/vnd.in-toto+json
