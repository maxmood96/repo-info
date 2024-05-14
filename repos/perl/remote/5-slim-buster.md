## `perl:5-slim-buster`

```console
$ docker pull perl@sha256:e6bf64d1af8948623176e5050661ead6774de19837ee68e8c5c562ad73aac00c
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

### `perl:5-slim-buster` - linux; amd64

```console
$ docker pull perl@sha256:e5ce85810d0ca734e5fa825963fa1d37343dfbd62a8522104a3393d64c62d9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54666688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8671c3df672e7e29fcaf0a10ad0013c64b87aa55ba13d6f0a2e1ff4e94a23926`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:ea1fe4f19165d885a1f3d523e0ebdcc3e863e6b93717c8022529edb674a52e2d in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:6299ae3fea5d052b297d91a57200563362b8f2c95358c6e3010d6fa3ed44e7c4`  
		Last Modified: Tue, 14 May 2024 01:33:45 GMT  
		Size: 27.3 MB (27337664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c86afa10a77fd55f169a364edef4d42179109e126c6f1a512005cb6eeb3df46`  
		Last Modified: Tue, 14 May 2024 03:03:22 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47097fbc21d5151754658873729c672e1b144a6d8f6000432903aa9f00899d7`  
		Last Modified: Tue, 14 May 2024 03:03:24 GMT  
		Size: 27.3 MB (27328759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f325402a15c74b39af37f0d1d13f54433ecaf20763fac614a0fdac0d0d58f3`  
		Last Modified: Tue, 14 May 2024 03:03:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:e8dd178e18b7efce0e45fe53f518ae86101159667fd0942ad955b38c2535b035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1432d8073837a3680d584bdfca8dfd3fc8f40da56af89c03db65b1bbde27c394`

```dockerfile
```

-	Layers:
	-	`sha256:e4adebf80d2dd21e585577184abda7dd8bbdef87e34b7f96340bc12e05d41a79`  
		Last Modified: Tue, 14 May 2024 03:03:23 GMT  
		Size: 3.7 MB (3721514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4693961af030dccdd5016412141ceaec35919abfdd00abefa0f73fbe9f3dc47c`  
		Last Modified: Tue, 14 May 2024 03:03:22 GMT  
		Size: 16.3 KB (16341 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:a1f77415187b71be1da1a54edc8a914200ad6106745b22381aa149c16f8aa792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46857005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9853961809566a7e1fc6fc41f50a4e1ab1498ac82d3b99bbcefbb468376f36`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:e48e4c164cd443d649cca91f392a3ddadac422905ad4f48aca0f47eb2243561e in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:30a8958fe0d5b6c3e6d6c11772c14c4b85029786ca86968f09e078645df26b2c`  
		Last Modified: Tue, 14 May 2024 01:14:02 GMT  
		Size: 22.9 MB (22944934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3302b6eb2b02d477c3be352a2aac53a866176bd72676bb7b56d2b5233e6b21`  
		Last Modified: Tue, 14 May 2024 14:35:58 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be7e006283ec9c5ad95e6f46b2b45804973a3da5c50ebf8baa7ed9d2c5013b`  
		Last Modified: Tue, 14 May 2024 14:35:59 GMT  
		Size: 23.9 MB (23911807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb4246c36884db0fc55f5fc2abe7b1fe2215e6d399e737c78ef727ce3049732`  
		Last Modified: Tue, 14 May 2024 14:35:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:50a033c83fef1e03806523be39a3606fc677c9b536ed2a6c6152e5a1756463b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3712983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f735b9f25fe0feb98a0a0e075ee989682bbfe71be3af91ab847298a3c171b7b8`

```dockerfile
```

-	Layers:
	-	`sha256:0320419f4a247583d81ee9a6dfcf98078f1ccbcd4ed8224b730d5d2a6c7ea90f`  
		Last Modified: Tue, 14 May 2024 14:35:58 GMT  
		Size: 3.7 MB (3696732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66be381c7bca18c12523706f74a789e6e4264a3705b6b50e465a531759faa3c1`  
		Last Modified: Tue, 14 May 2024 14:35:58 GMT  
		Size: 16.3 KB (16251 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:b372c76aff373d379e516b3ef95a427ea8c54ba673f1c0663c6c4c3a089d6b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52075559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf7104c61f7803dec12c22e062267d3274efbf34d11bb9aa8f2f7d1490cd148`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3d516f7d827d5b517b0e2ef77e0fb446e94c45a0320f0c2b0afeaa8295ba47`  
		Last Modified: Tue, 14 May 2024 18:29:44 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765213ba13391cab8aa5144fa327759ccb34482d8a2c9a4480df7e486e83adcb`  
		Last Modified: Tue, 14 May 2024 18:29:45 GMT  
		Size: 26.0 MB (25966188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8c08cf93caa42d519d7d6ed5400d38da5bc4d0cd6a840cad03116b648636e6`  
		Last Modified: Tue, 14 May 2024 18:29:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:e36754381c765b3f6ef466ec90e7a333faeb5eb46b12645970b4742740bca26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3707172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aec16bfe4b01c29d831ec55e48a78053d16bbde20cf8e6af865bffde853c716`

```dockerfile
```

-	Layers:
	-	`sha256:899e5c1ded63d0ba6ddfcee9eed2de13b32efd39e2a36bf228cdd3d5d1992579`  
		Last Modified: Tue, 14 May 2024 18:29:44 GMT  
		Size: 3.7 MB (3690986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7874a2bf53434fbf4fc5bfd6409f047fd5dda70398295720d01f66f2bb9481a4`  
		Last Modified: Tue, 14 May 2024 18:29:44 GMT  
		Size: 16.2 KB (16186 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-buster` - linux; 386

```console
$ docker pull perl@sha256:2cbbaf8710ffa7df2b8663535396460c1dbdf0403267307b7f3f6a98f1093041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59448850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8928cb8d2584c5d1269844c0b915b8f9e6051306e8805b52d32ffb74ad295f`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7803436d972e2323c81400e847d22c14ce8d4c69879d6cb53f4b7852a169a`  
		Last Modified: Tue, 14 May 2024 02:01:25 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d793182b6e92cf3df4edbe897a1fee7940d9cec2a60860d6d7840e5f38a92feb`  
		Last Modified: Tue, 14 May 2024 02:01:26 GMT  
		Size: 31.5 MB (31454110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa92c77cdf971a200d632e13012e3a206064183cd7ed8e467b4d4d690b119473`  
		Last Modified: Tue, 14 May 2024 02:01:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:cedd0f727f3ff7612a2a03c9b5edb73045601ebb378a31ee577d9cf32f6346bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031f7e53750ef83c8ca1a3f5fbe0896e9291c116c87d3d231d218a898402522c`

```dockerfile
```

-	Layers:
	-	`sha256:56923bc3b9e38fa1accc6b2d25c819b740ec52706a02e5421c614e961b5943d2`  
		Last Modified: Tue, 14 May 2024 02:01:25 GMT  
		Size: 3.7 MB (3740311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0cd4089de7fbb0ef6ecc4a009829838e7a22d0f9e17b6ff693c2eab3921be28`  
		Last Modified: Tue, 14 May 2024 02:01:25 GMT  
		Size: 16.3 KB (16307 bytes)  
		MIME: application/vnd.in-toto+json
