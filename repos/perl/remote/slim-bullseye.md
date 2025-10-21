## `perl:slim-bullseye`

```console
$ docker pull perl@sha256:23f8c6dd11341dceb08e2ddca48d88994463fbd6129e81453452ec62630fe477
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

### `perl:slim-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:f5fcbff0faf1bbaef987ef8603343edae5b2e5776c3926a96fcce03604d85b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56429272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10162b4b4667e2d633a1b708c168a44f67ba6ada24507524b98c624e551f0fd`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
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
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1e5b32a0d921378e11fb6741d866fb21dbd5216a67213194401f2266f3ad0d`  
		Last Modified: Tue, 21 Oct 2025 01:53:42 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e3fcb6c8e21893a441e9d37de4e48a085b5d23c6db37704856d401a8f05161`  
		Last Modified: Tue, 21 Oct 2025 01:53:45 GMT  
		Size: 26.2 MB (26170640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f963bae789e21064e0c700dd36aebbcd604779f0f0da4d1ccaed0b9855171fd5`  
		Last Modified: Tue, 21 Oct 2025 01:53:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:5ca6dd83ba2b7f9e3216264f8a04688b4211ced206567ce9d60b32c176da3235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0713b9fec81e5cc3551ca48fe82366ac2ba102536f86719d1fe150773fbe1b`

```dockerfile
```

-	Layers:
	-	`sha256:19dde96e2200ae7df6fa26c978c75bf80049cadf0e21d597f70d321af7091643`  
		Last Modified: Tue, 21 Oct 2025 10:38:28 GMT  
		Size: 4.1 MB (4121265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ef85b9d789a9c5910557e733ed93bdcda39b62eac241b46bca38c231dba4003`  
		Last Modified: Tue, 21 Oct 2025 10:38:29 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:431817fe3db1bb229ee04f851f94c58060b4917a06c01978d0fce1d45db77b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48961429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883bb5f49feb0b4c37358efd37e17ac4100c981df16cb3a84348c4c6732d8726`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
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
	-	`sha256:4b897c04dec26603bcc1b01b4283220cd1ffb208f0ec4c0db9e08dab58fcfb5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 25.5 MB (25546187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9321fdda721fab8e4e0babb922fcd72d3616ee247c53bc250b5c639c325196`  
		Last Modified: Tue, 21 Oct 2025 03:17:33 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f4bcb9cec7f02d4aebc5480dd3df29aaeeb6ac2d7eeb6974d9fb07b5aa709d`  
		Last Modified: Tue, 21 Oct 2025 03:17:34 GMT  
		Size: 23.4 MB (23414977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0ce3fabfdf86f91b8a6e62fa2a647771e0d8e3b00c1ab1971b4d76114362fe`  
		Last Modified: Tue, 21 Oct 2025 03:17:33 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c02588a4fc14c045d1e11946b3ffcb7c247f2edff7e6f271d41a2367963248e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae87ba80465fe1a6114f0e0e92cd1be8e054ded7f735106378bb15a54a2b6747`

```dockerfile
```

-	Layers:
	-	`sha256:e5458239c22afbbd4ebb63c1ef429f67f0c52f2c759554db87a74d8e1e679554`  
		Last Modified: Tue, 21 Oct 2025 07:37:47 GMT  
		Size: 4.1 MB (4095270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975437ac04da3a21f6dade0b1fe249d91ec32396e81fa7363bd37620d2116c01`  
		Last Modified: Tue, 21 Oct 2025 07:37:48 GMT  
		Size: 18.9 KB (18921 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:2efc6e210ac54022ae971e52e1f3d3d900ee5ac8a18d5e607b4cbc472a924899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54049101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3675a545a95fe11a305b80ecd4191c89c383231074b28491f98295b7bb35313`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
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
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9890b57c601c9f317d759561bc639841f8bf153c1e15008be41bf0633c2fc88`  
		Last Modified: Tue, 21 Oct 2025 01:58:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9457ab7325ffe2fe26dfd46b86f32def4a553a0aa65ce27682b3f4fea0b2e137`  
		Last Modified: Tue, 21 Oct 2025 01:58:17 GMT  
		Size: 25.3 MB (25300435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df50ce0518062c29e0e246fba79f8fb795dace2ef1c554594501f62c5e08444b`  
		Last Modified: Tue, 21 Oct 2025 01:58:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ad6e9135d2de772e74f557daffd59e33e8cc1133ef60cb66896e53f309e8074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b70bb0eafa6d3c3140401d80602bf87cce75d85d9abd5a622408a74e9a224a2`

```dockerfile
```

-	Layers:
	-	`sha256:b4e05d8b2a229a71d05db3da79adeef667324985ea110debf3117ea0c35d8e1f`  
		Last Modified: Tue, 21 Oct 2025 10:38:39 GMT  
		Size: 4.1 MB (4095684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2e594a25e0e620dace4e318b6e1d3ba81cc517a3bc31a504afac11de6aa6754`  
		Last Modified: Tue, 21 Oct 2025 10:38:40 GMT  
		Size: 18.9 KB (18949 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:a5fddf95dd9c45aa9273dc4a2271e142305293d0dd2c3c33d79e05d1bd49cd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58872563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4789aa4ebb272c8d8e31caceb2b4d6deeb27fb0d01722b0f0aa6d4e1e9bc54f`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
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
	-	`sha256:ed9b7a4c5998c0d248e37f414fa0883c2b695df7b879c0ba096280f29fcb2660`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 31.2 MB (31191494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d33bfa6d4bd882274f8531a0b1b0637cc1d9077d904fe9377e9e1aeefaa2de8`  
		Last Modified: Tue, 21 Oct 2025 02:01:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fccf4072b22f28a522f4f7fe0dc502909e04a488b97a2557b4c7377261ad249`  
		Last Modified: Tue, 21 Oct 2025 02:01:21 GMT  
		Size: 27.7 MB (27680803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ceb11b5f79da39e413b8e1add4eb930174335f015a0474a78112dab991bf2a`  
		Last Modified: Tue, 21 Oct 2025 02:01:15 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c46b69e24bd4e31cf069c2570684363cda351dbb0f3a1f370d0a4f20b7f7fd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4144333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71af150f59d31a1b6945bb79454a7b0f17aa189a82da4b80b5fca40f35aa95bb`

```dockerfile
```

-	Layers:
	-	`sha256:1bfdfa0af98c62f38a2a33bd57adb9806483856824e22ef11d0b0b97ed811f63`  
		Last Modified: Tue, 21 Oct 2025 10:38:44 GMT  
		Size: 4.1 MB (4125537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d90ad0d385c4370a9e5a4ca8669758703e3cf1e1071b750b21b9ba802894725`  
		Last Modified: Tue, 21 Oct 2025 10:38:45 GMT  
		Size: 18.8 KB (18796 bytes)  
		MIME: application/vnd.in-toto+json
