## `perl:slim-buster`

```console
$ docker pull perl@sha256:13c54faa94d57789d2141318cfdce6d6d0012e566d2908885f44701d251a2aae
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
$ docker pull perl@sha256:806fafbb1296169f38d2de456cb7434696e8343785caab715181eddee365f3b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54515779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878bf4a24a03b883113cc6a284c5d0e08f2c2fc96b35f06d91dc689222abfc55`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:a857ebb18123e76fc79a7d720dfdcc496ba12a79af323564b965627d399a5b04 in / 
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
	-	`sha256:b992ca815489079dcc6d19cf381c63d057e1b924edd453734f694be5ee23dfd9`  
		Last Modified: Wed, 31 Jan 2024 22:41:30 GMT  
		Size: 27.2 MB (27188593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d3c6c0b274ad79ebcc8371e90c635e89ffb1389572bff97b29b566a6eee4c1`  
		Last Modified: Thu, 01 Feb 2024 00:04:44 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74679d911952269d2f5edc33ac0acec0797d18fc2d9839eb94a5a153020065a`  
		Last Modified: Thu, 01 Feb 2024 00:04:45 GMT  
		Size: 27.3 MB (27326919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd01b6363e0039f509901f4ba19f64c880a7129dd3e2ddd33b8da8fddee01782`  
		Last Modified: Thu, 01 Feb 2024 00:04:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:300380d9571e02e7139fd83016f063ec14992732112fc262fa59cfb6fc0d5515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854a3788e238cfaeb5527e3b93494918fc981830a2c5b6117f53494e4fb58977`

```dockerfile
```

-	Layers:
	-	`sha256:73bbece4aac94c2990f09e65b99d7041c0f0215a48b0d96eba431b16ada4f8b0`  
		Last Modified: Thu, 01 Feb 2024 00:04:44 GMT  
		Size: 2.9 MB (2919368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1de53321897cf1434948eea8dd5b3ff6d6fce5eaf9ce2b3da2c4512383e451fb`  
		Last Modified: Thu, 01 Feb 2024 00:04:44 GMT  
		Size: 16.3 KB (16337 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-buster` - linux; arm variant v7

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

### `perl:slim-buster` - unknown; unknown

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

### `perl:slim-buster` - linux; arm64 variant v8

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

### `perl:slim-buster` - unknown; unknown

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

### `perl:slim-buster` - linux; 386

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

### `perl:slim-buster` - unknown; unknown

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
