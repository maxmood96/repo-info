## `perl:5-slim-trixie`

```console
$ docker pull perl@sha256:5f599cc8a05b66a5760adc31b6a08394bcef42ef20c4f1826780d3574eb7a356
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

### `perl:5-slim-trixie` - linux; amd64

```console
$ docker pull perl@sha256:4e089645edb490be7a46f9a4d5a47b17f8f990ecf822c1bfb357447633778ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61739013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e8035280479e7390c16286f1651e78aeb838612c908c157755be38768ff6b2`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:50:22 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 02:54:49 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 02:54:49 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 02:54:49 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2490e60133d902442267dc88d03af2ba556bc49ebcc788dee4529d029736ad9b`  
		Last Modified: Tue, 03 Feb 2026 02:54:59 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771ac480d0694d8d5e8c6d6cc79cd7a593dd1c397a2bdf5f2c31bd8014242500`  
		Last Modified: Tue, 03 Feb 2026 02:55:00 GMT  
		Size: 32.0 MB (31960148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007e18ed958ecb7d87eba82215afe788a51172a5aa13718d1b0bed1751f8388f`  
		Last Modified: Tue, 03 Feb 2026 02:54:59 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:410b725e685824dea624cd61196a78ea2c271af91c8b026d5de5826f85c23557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4030864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356e8dd2dce38b89ea6fdb9749792edff0b9dc803cd55e31a74ba22012d46b0b`

```dockerfile
```

-	Layers:
	-	`sha256:7357b28073b8998a836771cba70954f96e966a61efb9a65deb3971ae5cbfa572`  
		Last Modified: Tue, 03 Feb 2026 02:54:59 GMT  
		Size: 4.0 MB (4010612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff83e1bd6b500d6d8537f97f8330b88d8c40cd4e48989afd4293efef07132f4`  
		Last Modified: Tue, 03 Feb 2026 02:54:59 GMT  
		Size: 20.3 KB (20252 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-trixie` - linux; arm variant v5

```console
$ docker pull perl@sha256:86745f2b70551100ecba4f2f737d6388c48fa3b73250a4599bc161df0e180356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57146613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c2e283cb45072e206a06dc0cbdcd9907cba68aa18b0395f775185db1e2fec1`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:28:01 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 03:33:29 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 03:33:29 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 03:33:29 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9182b58e46688e829fb0808f93295d81434fe6b4cab5ea9df7b1eeab5c1688`  
		Last Modified: Tue, 03 Feb 2026 03:33:40 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d96bf05c088b0c46729743b19252f6ce9b4f38189d0bf9ae62ada56b480d68`  
		Last Modified: Tue, 03 Feb 2026 03:33:41 GMT  
		Size: 29.2 MB (29198789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa66d939804884a12b08d088325e4145d41a9b24acac7f5faaaef9edaa7b2b82`  
		Last Modified: Tue, 03 Feb 2026 03:33:40 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:990fbf2095e1c20e032832dcded2f26ff2a3fa505f43c226430fb1292f69876a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ad67f37276aa4ce282948ffd5f7b9cad911a56ea8a103b3387cf359e0539eb`

```dockerfile
```

-	Layers:
	-	`sha256:00d66f13254914d2062c3ec744f31ef74db341ac04c2979101be20d7a1df961d`  
		Last Modified: Tue, 03 Feb 2026 03:33:40 GMT  
		Size: 4.0 MB (4003689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:028309d924be8ddeab669b0c4c0b9f57f36b22767d9f175c42935171e8c90443`  
		Last Modified: Tue, 03 Feb 2026 03:33:40 GMT  
		Size: 20.4 KB (20380 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-trixie` - linux; arm variant v7

```console
$ docker pull perl@sha256:ffb1161fd96b3e344780503b2cdfdd060aad9d0f11ed4f43b1d884a90bdffc89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54484756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58fd706ba794de3951367bb766798f198f93ad6f860835d7df7c4bfff6d7c684`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:26:01 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 03:31:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 03:31:22 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 03:31:22 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be725bce2368bfe96f1e3785c2a151b361f8fe2dbef4a8781c8383e4a3ad8ad2`  
		Last Modified: Tue, 13 Jan 2026 03:31:33 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5524b7cde6b7c6331f0267679bd2480426ad7d4c795a2e90d8572a70aa720783`  
		Last Modified: Tue, 13 Jan 2026 03:31:34 GMT  
		Size: 28.3 MB (28275911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d23cc0bef3634106ec0b2a12815525350a9a135972883166c931ed79c780c0`  
		Last Modified: Tue, 13 Jan 2026 03:31:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:4189ea942b655d336826e5cca963caf5cc580f0b120e7dc1de0ff08f94327e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f84c11dfe88c298221c1741fb27cba1f27434b8c98e334a4875000c063e766`

```dockerfile
```

-	Layers:
	-	`sha256:d6479e2d11d157e399dc1693fc56c06914068bce8710323465c1c63f0dbc24d1`  
		Last Modified: Tue, 13 Jan 2026 03:31:33 GMT  
		Size: 4.0 MB (4002880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:505932073754c9b6c6da2165984a22381379036ac21d1993f19e06ffdfc3a780`  
		Last Modified: Tue, 13 Jan 2026 03:31:33 GMT  
		Size: 20.4 KB (20379 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:f78da4b275e88dc6dfebcf4faba35845a5d67de4184180e65a27ac3fde4b27a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61752335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77040359ee7d8f6523b17ad0ea77f0e4cb0be9097e6f53af52485b29f52d9f8`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:49:39 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 02:54:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 02:54:19 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 02:54:19 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e1a00e459ab2d44696270e7e3eebcaae50468d9243e270e198f3466c896b60`  
		Last Modified: Tue, 13 Jan 2026 02:54:30 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a26c7a902bf13dad3c771a810a1fbb6e1214cbfd29d3bb3d1458a6021728be`  
		Last Modified: Tue, 13 Jan 2026 02:54:31 GMT  
		Size: 31.6 MB (31618027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84a191b1e1d7499faedffff47716d5e78e1fd6910b237e188acc1010aed0c94`  
		Last Modified: Tue, 13 Jan 2026 02:54:30 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:5c3b05d9673aeb756d0b7227854f0ee2bdecee4859cbd5c69d193bf856986275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f7aaf01f4804fe739b40a5583d3f0064a0a499fe8f72a2fae5110ba7c2721c`

```dockerfile
```

-	Layers:
	-	`sha256:d8ce266131a7d0d62a8561874d20965e06da0a923c766acae7dc2846c9d7391d`  
		Last Modified: Tue, 13 Jan 2026 02:54:31 GMT  
		Size: 4.0 MB (4005755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751f6f48bc651f023644b9f6528a8b49979c5678c96fac2e184101df6dc74f89`  
		Last Modified: Tue, 13 Jan 2026 02:54:30 GMT  
		Size: 20.4 KB (20428 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-trixie` - linux; ppc64le

```console
$ docker pull perl@sha256:70491aba03aed22a83f398eea824dec6435a78f7c8efae139f3fa561827404d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66268358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49db53847f779e75ecb11dcbd0befa325d313af6a9f038c693af424e4fa43d42`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:49:35 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 03:57:29 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 03:57:29 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 03:57:29 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c14ab110b3c82c729759c65bfa26157bb22a6969a060c1d30432bf641cf94d`  
		Last Modified: Tue, 13 Jan 2026 03:58:00 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555a52f63154273c55aa03f2bfc88dd347061733759c7576661f0ecc7907cb68`  
		Last Modified: Tue, 13 Jan 2026 03:58:02 GMT  
		Size: 32.7 MB (32672492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1869529aeb84f0ef3baa9118072915b922bb1d0d25e1fe3e3d502be910d699f`  
		Last Modified: Tue, 13 Jan 2026 03:58:00 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:0106e98dccec5c7c1ef0cad07f13264cb75da643823a85ed3c2d26cd524b6ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0782cc2261ddc444ac112945b581df388f0fba42d8f3024caeb2489f45e03ed8`

```dockerfile
```

-	Layers:
	-	`sha256:843a46888d35efadbf0ce481d589bfe6ead1875aa71d2813d16c82e9127fe115`  
		Last Modified: Tue, 13 Jan 2026 03:58:01 GMT  
		Size: 4.0 MB (4006648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d4d9283cda1f0a7d6630a3cac3c2db67416c81551d940dd59cf9e5b0330a663`  
		Last Modified: Tue, 13 Jan 2026 03:58:00 GMT  
		Size: 20.3 KB (20332 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-trixie` - linux; riscv64

```console
$ docker pull perl@sha256:076c7203dce22406c8f9154917091e1edc7b685c58e2c57210c393c3a831e891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68050134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462ace2978f8a1f89720441e1bd792f17f6b3379f62fa92b7a7bd7dc1fdc8a30`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 10:41:11 GMT
WORKDIR /usr/src/perl
# Fri, 16 Jan 2026 11:48:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 16 Jan 2026 11:48:31 GMT
WORKDIR /usr/src/app
# Fri, 16 Jan 2026 11:48:31 GMT
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
	-	`sha256:c2b12208a048edb8cd2afafda631c550201a6f2c77e87764330f9af033b05545`  
		Last Modified: Fri, 16 Jan 2026 11:50:58 GMT  
		Size: 39.8 MB (39778179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43470dfddb96429de374809684c460210c81c8c88ae63fa538ded8f48d2be8b`  
		Last Modified: Fri, 16 Jan 2026 11:50:52 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:94480239d50289721ad680bf47295ee8592c5a357da1c8085adad6961aae6db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4018245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1097ff916bc12499c0c10ace051b89a10372c3c7d604fd4c1daf7dffdaef0ec`

```dockerfile
```

-	Layers:
	-	`sha256:fbcd25280f732a20fe34be7fb693b89bcc040194498678443a17b6c4bc55b9ad`  
		Last Modified: Fri, 16 Jan 2026 11:50:53 GMT  
		Size: 4.0 MB (3997914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f28d84b25fe4d3d8dde7f2b6c1bbb471e49a863afffef7fc46c5b11a532f55b`  
		Last Modified: Fri, 16 Jan 2026 11:50:51 GMT  
		Size: 20.3 KB (20331 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-trixie` - linux; s390x

```console
$ docker pull perl@sha256:04ac620199ac3c90e2692fb569970706b0558f120cce2be6225587cc138c1ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61148396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47784c7f9dcca5d8a34a48aade63c15dad5bd35dc7846175f756fe256e53ff52`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:52:43 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 03:58:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 03:58:52 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 03:58:52 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e546a7529553e82150e83c720e4c7894370af6f94f06ad4cc06f47a36d3b4d1`  
		Last Modified: Tue, 03 Feb 2026 03:59:10 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234639e2147a743225d4ad40b7762ba1a15970e982f6dc7d4a7cd14d7016f438`  
		Last Modified: Tue, 03 Feb 2026 03:59:11 GMT  
		Size: 31.3 MB (31309979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268d45e9f4000cd2617b4c1965d429b65ad119086504137bdc9c4a21c80c3a72`  
		Last Modified: Tue, 03 Feb 2026 03:59:10 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:20156890631a6fec5d66cbd4c9058aa370d2cd1fa06e20d37b8f71e1a8e9b005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10236a8303e30eb0366b8bac86e5bcc425480e0cf715d186c58e9b13c240bea4`

```dockerfile
```

-	Layers:
	-	`sha256:744b8e9a5de4819eca2660c73c1bef96d00537f1aadf9ec5963021e696d4575e`  
		Last Modified: Tue, 03 Feb 2026 03:59:10 GMT  
		Size: 4.0 MB (4002940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:992bba19b2c9edbcd8e01af7c563e9437eaa4c5b0d63245651ba30c7c6be8980`  
		Last Modified: Tue, 03 Feb 2026 03:59:10 GMT  
		Size: 20.3 KB (20251 bytes)  
		MIME: application/vnd.in-toto+json
