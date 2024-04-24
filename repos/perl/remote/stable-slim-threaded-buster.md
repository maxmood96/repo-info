## `perl:stable-slim-threaded-buster`

```console
$ docker pull perl@sha256:4f5aa4c97801b75ca074e539fb8ac419dc9c4f1d3de3f81d4ddb335f2c04f218
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

### `perl:stable-slim-threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:b8f7d7a16120d3f88e0c45410e6ed32658f4ac83dfd14edbe6f2226ee5e18500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54726716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929ba08fededc04e50986891c4e8cf94d657e9461136164c24d30dd23f42bed3`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
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
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8837f2260d82b2c1c49e415adf0cef3f6d40e23403b9d0ecff9e3fad67617d63`  
		Last Modified: Wed, 24 Apr 2024 05:06:28 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eef40f5be0fef927a1620dce523fe39f1fd416f77091ac09ffc89a1ff126bb6`  
		Last Modified: Wed, 24 Apr 2024 05:06:29 GMT  
		Size: 27.4 MB (27388876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472d525fa02e9103113fa854db79787bc0708277bafc0eead830a70cecc19718`  
		Last Modified: Wed, 24 Apr 2024 05:06:29 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:7dfbec004bf71d2c728a5306940e4f150ba3fc20708bcd391cd04507e885470b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4042af8861c6c1335943b2c5b52ed748c72105ee62b9596f2305ef3c62b6a72`

```dockerfile
```

-	Layers:
	-	`sha256:a08e509f2548db85c83011a5ef39c46e245cf752cef09e9a99370df9f0f9ad5b`  
		Last Modified: Wed, 24 Apr 2024 05:06:29 GMT  
		Size: 3.7 MB (3721604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9caca48c871ad5ff6f1333bb8c8a466b063f63cc4cea5ebc328ba803df37310`  
		Last Modified: Wed, 24 Apr 2024 05:06:29 GMT  
		Size: 16.5 KB (16482 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:a238a1bc524b15fc2878ac1d9c769540eb12b1e50c6d7f98662b1546f5298a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46876395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b0f8322a88ee331c61d936875860a747efe2f9ca05fd3c6d5c5c84efb5cb84`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
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
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be935c3939827efdfd0e1223b1fdc3adfa135d4724bf4c08d420f64e3c6baa5`  
		Last Modified: Wed, 24 Apr 2024 17:19:14 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7b5dbcc07c0d1ed6fb28086fe7faffe5ab83783e64a8dfd06a3b12227f7bde`  
		Last Modified: Wed, 24 Apr 2024 17:46:33 GMT  
		Size: 23.9 MB (23931064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ca29b2353968d577339b00f3f4ebf05c1975cb59ef6093aa2a052fac2e5e51`  
		Last Modified: Wed, 24 Apr 2024 17:46:33 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:1466f5f5177be20cec07e217aaef28d200ae7d4860f209a9ebcd036c2cc265a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592e73e8ae8cc664b0c87caa5ef2f1fed6e9ef4f89b6cb90e0a9143c1342dd1e`

```dockerfile
```

-	Layers:
	-	`sha256:c61d4a4e01c386aba572f8a42577c311e0fa59a331024ed07a3a56464666dd44`  
		Last Modified: Wed, 24 Apr 2024 17:46:33 GMT  
		Size: 3.7 MB (3696822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1616adabd36a159acf43b5dc5b5d16d720ffe7bb8d42b2ab20f9c03d1b29009a`  
		Last Modified: Wed, 24 Apr 2024 17:46:32 GMT  
		Size: 16.4 KB (16393 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-buster` - linux; arm64 variant v8

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

### `perl:stable-slim-threaded-buster` - unknown; unknown

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

### `perl:stable-slim-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:8c9240a226cce24269e71ecb044f6e950382bb2ed0c685af34575d2b4aa28016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59554726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d01bff3e8f624c78852d7ff7b00560aba5ba015a6d21d9580d942a79f47ce7`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:32f0f06baa0e4f10bff55aaa215b511838432ecc5fe547373d9ac99494556801 in / 
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
	-	`sha256:204b51fc41806ed93b4ccb6ce8272fa49b5f0b099ba6e3b5a940a9e7cd3ce202`  
		Last Modified: Wed, 24 Apr 2024 03:45:03 GMT  
		Size: 28.0 MB (27994678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afae0b2b3203ae03f0f299f9265295d464b9419283d52db86d557d5d992e510e`  
		Last Modified: Wed, 24 Apr 2024 05:07:18 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c879540253bc94cbae78b41f0cd997fb8fb9fb39cc93c0aa8bc7eb804149f17e`  
		Last Modified: Wed, 24 Apr 2024 05:07:19 GMT  
		Size: 31.6 MB (31559782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b03bfe2c26bf0cf87f29469eda231ca2560e7a44199f151024a0b626e4f5aa`  
		Last Modified: Wed, 24 Apr 2024 05:07:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:c74816abe8bb12b2c7c9fa3db38c67ca41df5968f5210d39d0026f6b804ebe80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4c2a0fd571f718d1143b3d51e6ae679c5b27620a0eb7faff15a42f740a3ae5`

```dockerfile
```

-	Layers:
	-	`sha256:37d8b13647bfd4ced9fe6edd4561efbc243570a85225a6474defcd7723d32c3b`  
		Last Modified: Wed, 24 Apr 2024 05:07:18 GMT  
		Size: 3.7 MB (3740401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c17af473acf9e88314d0db011a4c7a00dd1f004213b0167341fa3949880bf4b`  
		Last Modified: Wed, 24 Apr 2024 05:07:17 GMT  
		Size: 16.4 KB (16448 bytes)  
		MIME: application/vnd.in-toto+json
