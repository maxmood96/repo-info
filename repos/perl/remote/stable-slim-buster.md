## `perl:stable-slim-buster`

```console
$ docker pull perl@sha256:6e27a0c7f287ba1b48e11d4bed2e8bcab5414fe698b0f7eb5a22e929cff10923
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
$ docker pull perl@sha256:b5fab584ff3e772819d02f6637c9bcbf708fedcc8e17f4e2628b61cdf995376c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54510868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4997f682e6db3b2c56046d7afb9431a32f5a1a460d40f7a714638b0604e85261`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:08cfc7bf77cc2291c96890f44a435216cb1168c45cef77f7801430982c43ca58 in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:3f132091c0e96e4de35fd4230d92afad0cabb1e0d2f1dfbf8fc70e05010a7740`  
		Last Modified: Fri, 12 Jan 2024 00:39:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc477491405d108c2085d5755c8ea9a60f87f9aeee6c02fa57fd5a94585f461f`  
		Last Modified: Fri, 12 Jan 2024 00:39:16 GMT  
		Size: 27.3 MB (27322381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45aa032244cf2cf2ba9da8105d314c30644e9f669a8e7cce775dd7977fd6558`  
		Last Modified: Fri, 12 Jan 2024 00:39:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:6583d1e6089c0738e425cf278ab6125b38db6796c4668dfc873f45ceee889834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6aab311814b142ae3d197666f5aecbaafb02511559e24dc857e8c3814b90e04`

```dockerfile
```

-	Layers:
	-	`sha256:4f6bb9aef49531ecfa765aad92064e03328171edadb5f5afddeafc55d2b85cde`  
		Last Modified: Fri, 12 Jan 2024 00:39:16 GMT  
		Size: 2.9 MB (2919368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ee31d1cdb767254db3f1c2e16d9094f1e3761bf4e01e547f6002380281f53d`  
		Last Modified: Fri, 12 Jan 2024 00:39:16 GMT  
		Size: 16.3 KB (16335 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:cbb00ffe5dbc787523e4e8b0e19ba8865786cb80cbb8c7fd5d2c4fd22008b406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46698936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d5b5e8ef51b8ec700387d7183eecd9ba460c391476e167278261d8ffc21a9b`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:8461846d920454a66bf03cc7ad09cc57e04f7abb932ad830677815a3419e5bfe in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:403d50e55b087d78e88384c96fe8767002b0eb98fb0ef039cfc8387931571e32`  
		Last Modified: Fri, 12 Jan 2024 21:00:41 GMT  
		Size: 23.9 MB (23903052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c00096777bec254ee820722ad490cecb78ac40dcdf808e939c8889dd6a2a52`  
		Last Modified: Fri, 12 Jan 2024 21:00:40 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:4dc79c3c8002b900742521e618487e1fab448fdb9845272a4ef0e9b50b7232bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2914650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92d95494b2af82f6d8133022ffc10f60a2073a01399f8214470fba152d3cbce`

```dockerfile
```

-	Layers:
	-	`sha256:161e1596b553ee4aa6d7b03ea13a6ae13b6762d8174df08e143ef8f5cb34a3ca`  
		Last Modified: Fri, 12 Jan 2024 21:00:41 GMT  
		Size: 2.9 MB (2898402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde96cf8598150c957cd558f21a8b102cbafab3937d83b2374a378ad5ab565c4`  
		Last Modified: Fri, 12 Jan 2024 21:00:41 GMT  
		Size: 16.2 KB (16248 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:1ec8a430be32a4c88cdc7bd28e9078ed902c9c07e4d9dd14d707aab85dd5e1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51927188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e428602e6343f398feff9dc38d40fbeda25cb1ce7f1af89823cc55c2ab964093`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:0d7c08c3a192fbaded92a14e5eed44f5df7d00cd932ed45984ebb6b6e21446a6 in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:6d1d9f0f80467ab00a167ee330c1d9baf930c8e430ef65e24af7f0ff8df9db6b`  
		Last Modified: Fri, 12 Jan 2024 10:28:10 GMT  
		Size: 26.0 MB (25957108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49e46ec4403268eead22d93c3ede6217c3a7b8d4589a7def6efc21af84b34c4`  
		Last Modified: Fri, 12 Jan 2024 10:28:09 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:ec0d06529bc4911a91a6cd066ee3e10885a2dc484b08574cd9d7402dd4991c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfc498a581a80e11b8612d3dd67e4ab717afa10f8d36c40e8b0fb479503e6ff`

```dockerfile
```

-	Layers:
	-	`sha256:45a68afea6b8f2650686bc1952e4498a62d14eca29049c8faaf77bc52f8e9ba6`  
		Last Modified: Fri, 12 Jan 2024 10:28:10 GMT  
		Size: 2.9 MB (2893080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:118961b35da704fdc0f555da426b2664aeedadbe787fcc4ff5d91d415c2f1d5c`  
		Last Modified: Fri, 12 Jan 2024 10:28:09 GMT  
		Size: 16.2 KB (16182 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-buster` - linux; 386

```console
$ docker pull perl@sha256:208b091267b415debf125e1e6cefdf6793492c667ce75d7271fdc5156f676134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59294138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71735be7b19c90714f5836fbc599ad8ebbae0fcf8965052d7737521f0dd998e1`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:71b9e4d4a69cf226be8618530ca01bf58a3220da10468a570ca3fb1a110462be in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:7419ed4ba123d31992b71346cf258d72a25dcb939dac3e8e49f8e46d74a2de9e`  
		Last Modified: Fri, 12 Jan 2024 00:40:13 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc54e38d059774a998479e9394ea8df351be9efeb53ec9de66a95dfb6bbdd6`  
		Last Modified: Fri, 12 Jan 2024 00:40:15 GMT  
		Size: 31.4 MB (31447035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3a7a3875b627382bde92e83f1dfad77e32e472e64e435c91629eef8dbb3500`  
		Last Modified: Fri, 12 Jan 2024 00:40:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:3491475db0827a87ef0f447ab75beacae560fa1ad5976de0fcc59534182c2cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2951606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b147c539c426b3befca1b4dcc25d0a9014d83fd56c88436bea3260227730fb`

```dockerfile
```

-	Layers:
	-	`sha256:cb991e734871a144618db645870d1c9b447a48d1f299849165191498d116be43`  
		Last Modified: Fri, 12 Jan 2024 00:40:14 GMT  
		Size: 2.9 MB (2935303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d1a580308e2b70d90302c42dfb0878ffeecfc3aa35fa842d5f176a0b715501e`  
		Last Modified: Fri, 12 Jan 2024 00:40:13 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json
