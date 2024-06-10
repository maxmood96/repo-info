## `perl:5-slim-buster`

```console
$ docker pull perl@sha256:eca0a5ff6505261bc789823aac5f753166f5d4b0b7d96b75442466c23143f63c
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
$ docker pull perl@sha256:07938d1db587370bcae96bc37a603990fe41145ae12a07128d3b3d336cc22d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47153187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c59b0ba133c37c2997c1a6441b7aba97dfc36f54def2e1af1791afdb3a94d42`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:09:18 GMT
ADD file:e48e4c164cd443d649cca91f392a3ddadac422905ad4f48aca0f47eb2243561e in / 
# Tue, 14 May 2024 01:09:19 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:30a8958fe0d5b6c3e6d6c11772c14c4b85029786ca86968f09e078645df26b2c`  
		Last Modified: Tue, 14 May 2024 01:14:02 GMT  
		Size: 22.9 MB (22944934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25a99f46ff124a1f0b32543fed81f02fb157235f368ebd139dad111d286efec`  
		Last Modified: Mon, 10 Jun 2024 21:35:53 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cae4f54760b69677de3fecd9dafc53c212133d1551c08518109c015cd14adb`  
		Last Modified: Mon, 10 Jun 2024 21:35:54 GMT  
		Size: 24.2 MB (24207985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb19644a93acf4eb35d4ff0849d113a47855973a46d0b4f6ca6a338790048eb4`  
		Last Modified: Mon, 10 Jun 2024 21:35:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:cc92d512701a7318123b3c35eeb76acd02b8f8b7e3684e6f05c521aee9ae45a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac54c17215bb51bcd5d2c09031e7874b1c0cf331a1cba51ed13da84587fd05b`

```dockerfile
```

-	Layers:
	-	`sha256:d322efd94bc84db89ec041c1859b673b0cf4206385fad28ac04c49026a8f1de2`  
		Last Modified: Mon, 10 Jun 2024 21:35:54 GMT  
		Size: 3.7 MB (3696731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae5e2412d8ffceac0d36d87b2602b389f77e1a0179e4582bebbfbf9d69447447`  
		Last Modified: Mon, 10 Jun 2024 21:35:53 GMT  
		Size: 16.3 KB (16300 bytes)  
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
$ docker pull perl@sha256:da1048fa5db4c2214a7df377dafb294ad3c05c05f70aa21ba3505852223a58d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59755200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d64e94de459025216843957ce0cba0258ae0248b0118c418d18c5928ec4c2e3`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef28198671105e454dac6c0ee7a345900c7870e10899decf970ee8938a761d6b`  
		Last Modified: Mon, 10 Jun 2024 21:03:25 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d53dfe962c17f67576c0d7fca73a6ea0f47ccf07d4a0ce47899d1592ce4f124`  
		Last Modified: Mon, 10 Jun 2024 21:03:27 GMT  
		Size: 31.8 MB (31760456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e08cc94d47546214a6e4be943ee9cc293d85376a3497cefc7b4c358bae9537`  
		Last Modified: Mon, 10 Jun 2024 21:03:25 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:a3dd4456d99717afc850ca93a43e7e6da67754f029fdd73e6570ff4745a6edce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8150d000f4bb7151a27a41ea90fce40526c9e79953f5960673d152ae720a6cb`

```dockerfile
```

-	Layers:
	-	`sha256:3f15257c4d5db1449b352862c0bc9542165c80301cd2123e154d93a48e7ebb14`  
		Last Modified: Mon, 10 Jun 2024 21:03:26 GMT  
		Size: 3.7 MB (3740310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41dc6a73a8d1e897e0edfcfdb63d18cb11c8c1228b4706b2127a24cc093d54de`  
		Last Modified: Mon, 10 Jun 2024 21:03:25 GMT  
		Size: 16.2 KB (16188 bytes)  
		MIME: application/vnd.in-toto+json
