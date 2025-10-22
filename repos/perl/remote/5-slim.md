## `perl:5-slim`

```console
$ docker pull perl@sha256:ba8ac7d93b8445fa0b18dedb5ae5f5aaf1974c5a6b5a9d43baa7156f09374536
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `perl:5-slim` - linux; amd64

```console
$ docker pull perl@sha256:5311b47b43d706a5ebd3078338893c16ef9a55b5908272c76b92cffa03c9723e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61723841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61c94417688ca1273af32eaadefc224922a7ec2d2047fef31180f461fa58eae`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ebd54bdaede33dd479cef1f113a4bac1c4bb32cb4128069299d7c69d8aae0d`  
		Last Modified: Tue, 21 Oct 2025 01:53:31 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7a5b0e1557b0f1ea1f0aea088fc64dc73979e330276c0c0ab26dc80f721748`  
		Last Modified: Tue, 21 Oct 2025 01:53:39 GMT  
		Size: 31.9 MB (31945652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7269e6144cc007bf7e568c9618350ecf5a8fba87e3d0f2aaab979d85a34122`  
		Last Modified: Tue, 21 Oct 2025 01:53:31 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:e935074e263d98fd085379701596da9c3ba5d52f92d1bcda7097b0d91d10f94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4030745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32777db8cbe5249d99076985f525834ce7afa66b0721135302a9f4734cfc28e`

```dockerfile
```

-	Layers:
	-	`sha256:3d104c0f882646c724d076b24e96ee47018ecbd617946a7beb52c80e3d6906ec`  
		Last Modified: Tue, 21 Oct 2025 10:38:00 GMT  
		Size: 4.0 MB (4010450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:801e8575a5c8295e7d23aa744780f05278d6939f0152fcfde78d43e8658a3c88`  
		Last Modified: Tue, 21 Oct 2025 10:38:01 GMT  
		Size: 20.3 KB (20295 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:f5da6fa5bc86a70575d10a0e5adb05d6f46a6008811d24bd63c0414972dcaf16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57145017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e96d9c3f7aa4c3f2cf361bea327224c28699a53dcc94b427278acc1ed26c532`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2be8eb057ac97d56cf0a3aee6d603a4164d1d546554a10988b983aea070e222`  
		Last Modified: Tue, 21 Oct 2025 02:40:25 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d7aacab279745a1e07bfc42f6e567965db296c009808e88dcd79a46db34619`  
		Last Modified: Tue, 21 Oct 2025 02:40:28 GMT  
		Size: 29.2 MB (29198468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9a1fcf0ccc41f62171ef76440f5c14781869cf401f3074b75d46214658d8ca`  
		Last Modified: Tue, 21 Oct 2025 02:40:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:43b05cf9518ec289aee46b888bddcd7d6200ccf894d8b98799c27196c074e32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0fd4cd6117dbe3d710bc7a4b6ecbd14461393a922e808a2514fc2f21d7ecc0`

```dockerfile
```

-	Layers:
	-	`sha256:18f2aeb139d0881d27bd5436c6fc709fff881a077d6a441fd294f002f251eca1`  
		Last Modified: Tue, 21 Oct 2025 07:37:32 GMT  
		Size: 4.0 MB (4003527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b605242d8c5d259858948a6970fbdcc6323ee189527a1a6f1e1782cee5d6181`  
		Last Modified: Tue, 21 Oct 2025 07:37:33 GMT  
		Size: 20.4 KB (20422 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:1d921fa408daa897f01bb51859d7c2a6362e8913ee6f86c63081767069a3793f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54486239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf33785819f14cb2e46ea9f2e59830713e1e939bbb0b605ad54b8b34aa21f92`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23962d502d75cc04a3b3014f775d28005db2a90b82d8db45a8e50d105ca3d1f`  
		Last Modified: Tue, 21 Oct 2025 03:15:26 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7fe38b2f79efb8be23f995b83d0fe06eb45a642773be1ba614100bc9050b1d`  
		Last Modified: Tue, 21 Oct 2025 03:15:29 GMT  
		Size: 28.3 MB (28273082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99a14aa6d465ecc1f730ea689c15d301ca45b8def718e7127ec137acf2788a4`  
		Last Modified: Tue, 21 Oct 2025 03:15:26 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:6d88a183d13d04ef6c30bb994c19892469bd04f4440912b32fa8dea335296c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57dd062ef377b0981a7032d58f604e07d60615456509ee17db2749cabcdcb07`

```dockerfile
```

-	Layers:
	-	`sha256:8a09f70d8a99a796fe9e35042081dced63af6ac9a1bec19b33296184f382843d`  
		Last Modified: Tue, 21 Oct 2025 07:37:37 GMT  
		Size: 4.0 MB (4002718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e3544096df50e2aa593f8ca2b9f30abee37e53e518bc5a7ad5f41358057a88c`  
		Last Modified: Tue, 21 Oct 2025 07:37:37 GMT  
		Size: 20.4 KB (20423 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:96e8568ff8477940ec6db4c982d0508f7da9d9a2bc83b4995ed6b5990a0425d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61757908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8cc74cfda4b537b0b63eaefe645be089193df3db753b82abdfbdd0e9a1fdcf`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dfb2a5d194e99964f9b81f10ea44b5b2976f7306d1cc95a0e684c1b9c8b347`  
		Last Modified: Tue, 21 Oct 2025 01:58:20 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b419c4558a2ef8ad059c44090f262405c5212c2973db0ff9008d2953fb926c`  
		Last Modified: Tue, 21 Oct 2025 01:58:23 GMT  
		Size: 31.6 MB (31615514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa2a0b6989c28c73d8e1e6c1a935c21e14d5b94490c656af29996d18e37d8c1`  
		Last Modified: Tue, 21 Oct 2025 01:58:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:b8c558cc25f1f51fe8fa56c9d0e6bd426506099da68d95137315ae491e59eb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd955046cbcc2fcc3741b9873962421d86072c008201774e98ac1d24758b7713`

```dockerfile
```

-	Layers:
	-	`sha256:7f89fabd6b475a89f4458b4bf0f410c2943989a88036b9d055be4dbac67419ec`  
		Last Modified: Tue, 21 Oct 2025 10:38:10 GMT  
		Size: 4.0 MB (4005593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74032c7121d2a5a4254f509a315d83959b2d473bdf0c2c1d6d023a5e20b44789`  
		Last Modified: Tue, 21 Oct 2025 10:38:11 GMT  
		Size: 20.5 KB (20471 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; ppc64le

```console
$ docker pull perl@sha256:f1a9cdc47cc5af45f855375ae960d2668f726302ea17a44d742822dd823bc308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66273744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafec6bb18cf8261910e0546b10ea6771d5b5f080cf12bf7ace0da3904eaf36e`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db7129308cd5ca6ff9876254eeef391297240738d01aef707ec2d963f4154bf`  
		Last Modified: Tue, 21 Oct 2025 08:32:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5196c53c0fe76fb7cb46dc0ab9f5bd3b9f68e1d92acb22a56dc31ff85cff25f3`  
		Last Modified: Tue, 21 Oct 2025 08:32:25 GMT  
		Size: 32.7 MB (32674959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beeea75f3284381fcf214e2e4cbd51ccebd41a335d74426f5a8cfd1fa631048b`  
		Last Modified: Tue, 21 Oct 2025 08:32:22 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:bc003f12ec97365c557dada3f44bfc46fa9ea97d1d9d2a594af3eb61724fe580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca53855f7bd36170fcc99b6e3314374700ce4c092aa8346706e0a23c900b090`

```dockerfile
```

-	Layers:
	-	`sha256:752c0d8754724d2de8ceb7cf3f446787aacf8c337e228d10c427d737a1de796d`  
		Last Modified: Tue, 21 Oct 2025 10:38:15 GMT  
		Size: 4.0 MB (4006486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58f19e0893ba62ecd9f5a006c27cbd8b00fe50e26f32b3795f00cd5787d91eed`  
		Last Modified: Tue, 21 Oct 2025 10:38:16 GMT  
		Size: 20.4 KB (20375 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; riscv64

```console
$ docker pull perl@sha256:7ef91164393b2bc0e80d71251f841b99d37cfb2dcabf20f64a7819c8877494e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68057595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11835bbfd149a7e6e39b164e6d2f676af75e269266a74b409d471e54ed00e576`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0e6a6abd3768739c5cc84a0210c76a03bfb86afcc4905f9082ae54678f7d3c`  
		Last Modified: Wed, 22 Oct 2025 19:32:45 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7e071f784165676df6a5605cdb2ce46b5f5abaf99c2c19f3c1ae5260223826`  
		Last Modified: Wed, 22 Oct 2025 19:32:50 GMT  
		Size: 39.8 MB (39781678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb35d30a4117a253585027a4d3f49d2d7b9c0bd77b215c65e6a4697c6de7142`  
		Last Modified: Wed, 22 Oct 2025 19:32:45 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:1675dd06d743bd81cb51e4a3f51b4269511350840bd08c939fbef1c19e86bd25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4018126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06583daa5c420b8bbe59730ef2eec4f419af1fdd82573641fe9cbbb8141872b0`

```dockerfile
```

-	Layers:
	-	`sha256:c1eff22d33a49c2ec9c8d5d2a23df65cd8831f8946b5f03a968103415c9c382f`  
		Last Modified: Wed, 22 Oct 2025 22:37:38 GMT  
		Size: 4.0 MB (3997752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3480d6d8acec8e5cdfdc6e27687c0aed5ba335374b88b917da4c509b2a262b64`  
		Last Modified: Wed, 22 Oct 2025 22:37:39 GMT  
		Size: 20.4 KB (20374 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; s390x

```console
$ docker pull perl@sha256:c583e1b72da49ee06ea9b6d2a0fecec7f458f169e625ea57e74999af41d6abda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61141066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636f832f2c1bb832bb2e5ba9d6c5aefcf91f9e196da5b8d49f2d8e6405cc4859`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731d7280efdc1c0b18b921937367f0e4f8cb53a1805763bc8ef06c861494bfa9`  
		Last Modified: Tue, 21 Oct 2025 14:38:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24629a6c627298be772c016b63c39dda12e696d2e65e8434b5bdf2c95a89d7fd`  
		Last Modified: Wed, 22 Oct 2025 05:23:54 GMT  
		Size: 31.3 MB (31303545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ec5e04400cca71eff5b421bf9847693443e39655961726edd61a3d1fdd861c`  
		Last Modified: Wed, 22 Oct 2025 05:23:52 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:b79ec0a00b340df61b61103b189cd59fb2f8477e92a1e3e49c6158670c2c07cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab870eb4427dd00ea782573068f12f1270425841a7a7ee9e1de0606650270bd`

```dockerfile
```

-	Layers:
	-	`sha256:091d73e73b5dd1fa1b702bc87a2956089822900acc8eced4b5ecf8897c484a26`  
		Last Modified: Wed, 22 Oct 2025 07:37:53 GMT  
		Size: 4.0 MB (4002778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7daf26609e541802dcd2dd0b24cac2dcebc496ce9f14b9fce714a5f168a0ff25`  
		Last Modified: Wed, 22 Oct 2025 07:37:54 GMT  
		Size: 20.3 KB (20294 bytes)  
		MIME: application/vnd.in-toto+json
