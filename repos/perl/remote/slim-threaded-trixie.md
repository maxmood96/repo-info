## `perl:slim-threaded-trixie`

```console
$ docker pull perl@sha256:f3c753e0c5ed4fed121ce8bf5f4136e59c7df67e0f695e75a59a66418f32d235
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

### `perl:slim-threaded-trixie` - linux; amd64

```console
$ docker pull perl@sha256:d5eec8cfe208ce95e2c7498c60fec153b7058bf4e6e69678cc24edca981f9b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61786400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc744df86f93b7ff0cd3512484d5ec866ebf75ba16f6bd03a6192ccfa1b3f8f`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:49:55 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 02:54:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 02:54:39 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 02:54:39 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a609eade86340811d1bc53842297ea9cc49f23064ec53518c0b201995630a91`  
		Last Modified: Tue, 13 Jan 2026 02:54:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb9b58e109650584a7cbf8da398bf5dfa35db857f3cc1fd205bd4b46345936b`  
		Last Modified: Tue, 13 Jan 2026 02:54:51 GMT  
		Size: 32.0 MB (32012448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f556424eefa5f97e09c116336f4f24b1dbf93513b213b10e56e5cc738b079dc6`  
		Last Modified: Tue, 13 Jan 2026 02:54:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:fcec1c9c880995aba57c85efc4a411c2b633f4fde161a7b67a1f3410ef7d2e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9773df44b7b942d95c95657a3c530e2b64ffd7bbcbce77b88e41ad75997efe`

```dockerfile
```

-	Layers:
	-	`sha256:533e0042138b12d2d715b23e8ab54c3334e7fd9477406a16d54e8d4cd922fd7b`  
		Last Modified: Tue, 13 Jan 2026 05:39:41 GMT  
		Size: 4.0 MB (4010792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5a12e7558f45709c77c66b5c31803f64a20ccf6855cb982653addf3881099e`  
		Last Modified: Tue, 13 Jan 2026 05:39:42 GMT  
		Size: 20.5 KB (20483 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-trixie` - linux; arm variant v5

```console
$ docker pull perl@sha256:fa7e76be2db33f422f584a694c265bd8f3bf9cf8ec59ad8886f845cb6c12ec40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57165857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e876799fb7331b352a413cc397ca098459c06a4f2e20737238ac98927e9fe8`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:41:16 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 02:47:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 02:47:13 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 02:47:13 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909d3e45ca29f4675eabf626996be35b9f7efccfb585175e503f3023ef128d3d`  
		Last Modified: Tue, 13 Jan 2026 02:47:24 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a023135ef3cc5717724028d71d7411b54466c1d30140721a17e2718e8aedf4`  
		Last Modified: Tue, 13 Jan 2026 02:47:32 GMT  
		Size: 29.2 MB (29222868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e580aed811eef5d39886467fd02acf39e8297873d3984f8aa1422b8a359a11d`  
		Last Modified: Tue, 13 Jan 2026 02:47:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:47d6d5a2bcfe138f5eb1b5483463823f3475b1e79f27bdc25ae5da51719e6707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5fc1dc748178bb4c1bfd40af52fc3b83d5052a908260dfb8e9502f715eee22`

```dockerfile
```

-	Layers:
	-	`sha256:7aca398dff6dfb6e23d3670cb644d1ae29f565fd67da5438bfb53c21da79ee60`  
		Last Modified: Tue, 13 Jan 2026 05:39:47 GMT  
		Size: 4.0 MB (4003869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4cbb82a97a8320f58f537b1a603bc428c1d47d18b7f7de2d4baf7c06a651a4`  
		Last Modified: Tue, 13 Jan 2026 05:39:48 GMT  
		Size: 20.6 KB (20611 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-trixie` - linux; arm variant v7

```console
$ docker pull perl@sha256:f7ef5ef68efc877459c3176cf0ac6b32c06a41fba5716d6a6b8259bd95ee98df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54509120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24379a8e57dc81b2268e2114094e8570d82edc9531efea0645609b6adc57179d`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:27:23 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 03:33:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 03:33:09 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 03:33:09 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777d50fd1d0b12e7f52a1562381338db12bd9ddf76b3972b33de592125a220fe`  
		Last Modified: Tue, 13 Jan 2026 03:33:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633b988d6ae020a56d9f4e6c283f9bff6b3f879ec31b9a5d4a95d0e391b39894`  
		Last Modified: Tue, 13 Jan 2026 03:33:30 GMT  
		Size: 28.3 MB (28300275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ccea98e9ecc37b8ca03299777d04935e13ef8a46175592c005be6b9aef2047`  
		Last Modified: Tue, 13 Jan 2026 03:33:26 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:0cbdf74811cb470e5fabb42d3bb400af29fe62a3ae16490c91a6219fd9bab8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018d623d34fcdfc9824412ec97da72d8c3937a02f82a0daec04b46653a4df716`

```dockerfile
```

-	Layers:
	-	`sha256:452cb6d357d928cf510af31e54a0a173aeb3546abc088693f178dd632f6e17b6`  
		Last Modified: Tue, 13 Jan 2026 05:39:52 GMT  
		Size: 4.0 MB (4003060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95c9aba898ef4852742b5b81c40c1ad74130182917045687074199ffc5b4d107`  
		Last Modified: Tue, 13 Jan 2026 03:33:19 GMT  
		Size: 20.6 KB (20611 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-trixie` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:b6d4d7e866815565136807dfdbdc6e3aebefad3cdb77cbf2f0b1899919de3b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61797503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1358390052254b295f2aaba65eed8f183acf1f09dd7b3361b60db6bf9f4156f5`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:49:39 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 03:00:05 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 03:00:05 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 03:00:05 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e1a00e459ab2d44696270e7e3eebcaae50468d9243e270e198f3466c896b60`  
		Last Modified: Tue, 13 Jan 2026 02:54:37 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aca1ad2a3438cbf8f6abff56c0ea6984aaf5aa986848603abdee83af1f5f785`  
		Last Modified: Tue, 13 Jan 2026 03:00:18 GMT  
		Size: 31.7 MB (31663194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59622e052715ff90958330a5be0e7151be428908d55f70737dbdb76b309788a`  
		Last Modified: Tue, 13 Jan 2026 03:00:25 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:b8f4a133a30a7328434a0f8f55e1256e91fe76d0c959f156aa5d25cf91584f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818a5c6053107e6a302133e327d08689463993bb9b2b513be984abcc6b3e81dc`

```dockerfile
```

-	Layers:
	-	`sha256:4c81d14888ba827b577fe1760aefc6dc3cb1b23c704a71c6efd20cea55645e03`  
		Last Modified: Tue, 13 Jan 2026 05:39:58 GMT  
		Size: 4.0 MB (4005935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40c8fe0b5a99b852f3280ce487189c979b2fe9d0e8c69e440794bcd7cc0a72fa`  
		Last Modified: Tue, 13 Jan 2026 03:00:17 GMT  
		Size: 20.7 KB (20659 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-trixie` - linux; ppc64le

```console
$ docker pull perl@sha256:86f5f7189ddec95a691023feb8819db500ce4e0d995b3da309447ec7bad7bd94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66367678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c3b2c65f4a4e116c5c7ef4d629fdd091aebe2d27c5376aca5f82d4e7aec92b`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:49:35 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 03:57:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 03:57:43 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 03:57:43 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c14ab110b3c82c729759c65bfa26157bb22a6969a060c1d30432bf641cf94d`  
		Last Modified: Tue, 13 Jan 2026 03:58:00 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01b979421d8a465fa4ba1af8ba9aafda7281d3687e582f73471c0b10c9d3ea7`  
		Last Modified: Tue, 13 Jan 2026 03:58:21 GMT  
		Size: 32.8 MB (32771812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4974cd8c37826a20c8334566fcf03f26f7e132062caff61c34876b0904b49470`  
		Last Modified: Tue, 13 Jan 2026 03:58:18 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:98cc63d35dc307e4bef4352549acc79348d5043ccf7a27a82873dff137bd5cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4027391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a70f523dcf48a58cb87982b3a6bb46abca5a280cd86c3f18839d985469677d`

```dockerfile
```

-	Layers:
	-	`sha256:b997e011d190e56527ccd36cd220421617f37a6cf0c6566a4ac9fe094f227d3d`  
		Last Modified: Tue, 13 Jan 2026 05:40:21 GMT  
		Size: 4.0 MB (4006828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6498beac72e5d85c4078e62aebd2692d98f27610b143255e0213c6c4818ba331`  
		Last Modified: Tue, 13 Jan 2026 03:58:11 GMT  
		Size: 20.6 KB (20563 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-trixie` - linux; riscv64

```console
$ docker pull perl@sha256:5c13400e288a1000465cc55773e40db3414c4b7ae922af30c5b292f4b875f1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68081372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcee04a5f394ea4dc02c7d9bb765dbda5929e22ba2bbe2a65e460e8c5b86610`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 10:41:11 GMT
WORKDIR /usr/src/perl
# Fri, 16 Jan 2026 13:02:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 16 Jan 2026 13:02:32 GMT
WORKDIR /usr/src/app
# Fri, 16 Jan 2026 13:02:32 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aafe801f5da32dc274751371574154357ece7f579429d89a7c95774813a6ec1`  
		Last Modified: Fri, 16 Jan 2026 11:50:52 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16ad9f74008401ff23d6db857f25880d6131c9df0bf9167dc36731473f408b2`  
		Last Modified: Fri, 16 Jan 2026 13:05:09 GMT  
		Size: 39.8 MB (39809418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae3d6354556c2516dc37023f8adcd383dc28fb5b43a90253afbbf0aba3ac605`  
		Last Modified: Fri, 16 Jan 2026 13:04:51 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:9036c986e66790ec1df7403e178fc721dff6b2577309cbb5f687a74d4cfcc353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4018657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ad3f2ea90454f9cdd1283c9796be03ff2b6da3365c72e160b7074b97ef4f3d`

```dockerfile
```

-	Layers:
	-	`sha256:8f46062791b5f24b10b49a581ed0b4712bd01ea4f6c8711bafb4531ad656b1a3`  
		Last Modified: Fri, 16 Jan 2026 14:37:52 GMT  
		Size: 4.0 MB (3998094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffeed56ad3c0576fde84befb5aaff59c7744cd83517530d04a49966c121d3d4d`  
		Last Modified: Fri, 16 Jan 2026 13:04:51 GMT  
		Size: 20.6 KB (20563 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-trixie` - linux; s390x

```console
$ docker pull perl@sha256:85191b7490a6ec7d9302ddac4f90781e1a75c808b2489a2ddf86548b8ce2cf06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61188155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0af5d6aee8f9ce5106b22dc95f30fd6228aa88c99fc7ddc837e6f7718a49758`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 15:02:13 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 15:08:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 15:08:40 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 15:08:40 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697782aadcb1e9ad5d77a2da727c42e5d6a8e3d8a38e63140e0d508e8ea8b217`  
		Last Modified: Tue, 13 Jan 2026 15:09:04 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da8a1b241751c65c018401f156c3452b25361b0126976cb477a83db70ae5e43`  
		Last Modified: Tue, 13 Jan 2026 15:09:09 GMT  
		Size: 31.4 MB (31354479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e8c0ca6b6985e32c10794d331270a5552c33ef78985b7ec676a8038759f989`  
		Last Modified: Tue, 13 Jan 2026 15:09:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:2a9ae520b9b50c7ca80ea42db04b92a939f2708758a7b03f45e87206fa9af2c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5382f5f1cfa9502825d3ddbc56abb5d2de3d0d5d168f28adfa3636eda285dad6`

```dockerfile
```

-	Layers:
	-	`sha256:143c1754f0ed17257a12d6945189e98808dc91dab21dd7258e55c069db4c779c`  
		Last Modified: Tue, 13 Jan 2026 15:08:56 GMT  
		Size: 4.0 MB (4003120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e83cfc9038d35427963233d3d9883017da82246fc9879e7118c13e7ae2bdac2`  
		Last Modified: Tue, 13 Jan 2026 17:37:57 GMT  
		Size: 20.5 KB (20483 bytes)  
		MIME: application/vnd.in-toto+json
