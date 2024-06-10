## `perl:stable-slim-threaded-buster`

```console
$ docker pull perl@sha256:a911064f81c38f84a1516a5e0c9818802772c2a6397b7753bb5b78e7d223873f
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
$ docker pull perl@sha256:68c21e307c9444c1a4ce59778e52c49cd0b34a6db4d3e8dba6abee7b5821f328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54728632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e4d64f3212de8732f98205e72252435a58b912e23c3c0b74af2408cacf2b14`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:ea1fe4f19165d885a1f3d523e0ebdcc3e863e6b93717c8022529edb674a52e2d in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:fc69cf4e72328fec9b62e4602f055e2ceda65ede9170b869c64badb4d2ed5892`  
		Last Modified: Tue, 14 May 2024 03:03:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38c99f1826713edd41e983afa2430f1b7584d7a5279fad89ef7804981ce3e82`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 27.4 MB (27390704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f83c451a70651071301ff49c8b41c4db07df24625753fbad649d2f69edd1a52`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:f8c4a4c2c4598e8ee0bec770f42abe54ef7ed67d99f8e684b5801d9a1abc0c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a63ddc6ad56fe5588eb53ef9f372ff6b8dee23553adb6d69d6990d9d4270eb`

```dockerfile
```

-	Layers:
	-	`sha256:b5c11741f11e2100b5c81be98a305a1cbf46beb97ead16554d69e646f6bed07e`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 3.7 MB (3721604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b26985cd2eb9ababcde5205b6b1ee8f663fac4100bb30847af59e023bac27f6`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 16.5 KB (16482 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:3a21959636515d3c6e3f3b14bd8ae6dd947e243c4a527968aeede11ef4dd946c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46876843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65db9bc73b1dc537095a46e54160bcdfa3338beaf281d7b1213b150c9e1e9d90`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:e48e4c164cd443d649cca91f392a3ddadac422905ad4f48aca0f47eb2243561e in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:f51d27835872a81f9d5620e12ba3b8be633a846c44a9b58c55c5570d5e9ca716`  
		Last Modified: Tue, 14 May 2024 14:56:48 GMT  
		Size: 23.9 MB (23931645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89759710a94aa7f3ea6a141a38ec637e4bea1b6da8fca81e347f06d800c7e38`  
		Last Modified: Tue, 14 May 2024 14:56:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:e6f3460b0d8d8b7a5431ebd119f8252bf84a22419eede0c0999580ae44c00aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c95a4b5d47c7f94b2ee6591b4a26f62ecda8b946e50af98d706b327eb328d3`

```dockerfile
```

-	Layers:
	-	`sha256:acbbd8ce473f21f4a6efead7e4472feb91ae78a3ba7e792d607bf3fc3d839f76`  
		Last Modified: Tue, 14 May 2024 14:56:48 GMT  
		Size: 3.7 MB (3696822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57692c041b52c8f2f0d9c6278203354955cb95cc65850d2ce6e1fc26208416e`  
		Last Modified: Tue, 14 May 2024 14:56:47 GMT  
		Size: 16.4 KB (16393 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:0746cd2de9806f60e5e09145cfc6e771a6aaab304c92e5e429e66c6203dabe28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52110663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfc2da1ef2c08929cdcea382ab384e40bf5e68edc72263617baa5c2513d4701`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:e3332ce2f976efa68a92aa80f115b061503210fdfbf38774476f0a934a509e05`  
		Last Modified: Tue, 14 May 2024 18:57:19 GMT  
		Size: 26.0 MB (26001292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a32c045b3b785b949ac91373f1d6068e486ded4a4baefdc8adecc7925cea29`  
		Last Modified: Tue, 14 May 2024 18:57:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:44e3d64e75cf567c6796fd4f4b4e650c451bd2493df696466405fbf603a1bacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3707403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffa71425c6085cc2bcc9b675f6144de02f65fe0cf94c5a209e5aabeb84326d1`

```dockerfile
```

-	Layers:
	-	`sha256:ca773cdf4d60d3bec95c02d8866c3ccd06c04de991331eb3a11103f26461df16`  
		Last Modified: Tue, 14 May 2024 18:57:17 GMT  
		Size: 3.7 MB (3691076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aad64de120f941d48c7ac0984d75a2a47fd4209f6f99fef2001bee14d71c5895`  
		Last Modified: Tue, 14 May 2024 18:57:16 GMT  
		Size: 16.3 KB (16327 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:eaba74949184221a24c1faf726193fdfed62efbed46d0755ec06f31c9dbcee18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59853011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2f6883817c1db03173b6f554403d3dc51ca9c0006a76c373e7793f47ebff4d`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:b40536b15959552c5960fa54fb68d5fdee9ec7f36ef2f03ecc25679fedab3bb2`  
		Last Modified: Mon, 10 Jun 2024 21:04:22 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c49488414efe4191696c33af52c82ef79ff77cdf111c7be9619e4bdde4ce43`  
		Last Modified: Mon, 10 Jun 2024 21:04:23 GMT  
		Size: 31.9 MB (31858268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197aa3bfaa4c25f44cd15f7b55b6a0d3950a61e8f9401125e934bbdfb60dda96`  
		Last Modified: Mon, 10 Jun 2024 21:04:22 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:de37ff2fd3bff594ae0780139ac64150f21933e54cb46de11584806b5a3b0a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011308e9ea8fee423375d2bdf8a7bf552d087dd8ee1f27bdb686e8bdc3acb362`

```dockerfile
```

-	Layers:
	-	`sha256:40f82981bd24961a4b7de358eecfcf9b6befe01c80cbd24d0bc4da5c0c9ec894`  
		Last Modified: Mon, 10 Jun 2024 21:04:22 GMT  
		Size: 3.7 MB (3740400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db4217d5436c48edbf2172a6fedfc049fde4d254b972ff0bc8a7ea4260d5621c`  
		Last Modified: Mon, 10 Jun 2024 21:04:22 GMT  
		Size: 16.3 KB (16325 bytes)  
		MIME: application/vnd.in-toto+json
