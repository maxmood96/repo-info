## `perl:stable-slim`

```console
$ docker pull perl@sha256:620a65fdbd8c186b4afb9f190a1c4271d80f253a7392593a9f5b73a11c44fd76
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

### `perl:stable-slim` - linux; amd64

```console
$ docker pull perl@sha256:9f2e3dc8a604abef7d37c4f6c509cfad2e9876e80a84b6db6d062f150cc4b666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61746776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a65de07141221a07e2af3a6283fa4b4ed38ab9524ed06152c6e0671885a34b2`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:28:10 GMT
WORKDIR /usr/src/perl
# Tue, 24 Feb 2026 19:32:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 24 Feb 2026 19:32:44 GMT
WORKDIR /usr/src/app
# Tue, 24 Feb 2026 19:32:44 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ed7e727c4ad87cdca2f3dea5748f9729c5aa8a19367b4e5da2bf4dd2098c0d`  
		Last Modified: Tue, 24 Feb 2026 19:32:54 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d1c44c651a14e92624e41c767b7bbaeaa347b376e07254a6e69d402b6b3894`  
		Last Modified: Tue, 24 Feb 2026 19:32:55 GMT  
		Size: 32.0 MB (31967876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbde75c3747d202328e4090286005aa99558fcc5d0891dd16a05504b648b4437`  
		Last Modified: Tue, 24 Feb 2026 19:32:53 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:f4ea5739d7783c30b03d8a37d501bc13e0970e3047c7c34cd9c23bc41feff7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4030864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41e600885aac627dc7db1a81d329c605a845156a9bfe721b3d589744f0dd2ab`

```dockerfile
```

-	Layers:
	-	`sha256:b3fcfbee7bd11a3bd7336895317c72a432f8a2b0b39d954da3602bad06cb2877`  
		Last Modified: Tue, 24 Feb 2026 19:32:55 GMT  
		Size: 4.0 MB (4010612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab76f236d4fb12906fe77657be6cf4affb63ca0c8f907c0389fc8607122ed37a`  
		Last Modified: Tue, 24 Feb 2026 19:32:54 GMT  
		Size: 20.3 KB (20252 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:1fefe4417607149fe31624d3d6eeea28049e52ebbda5c851bbb5b6e01cfc54b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57145693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75849e1ad529fbfa0b0c0a6e0b33225a9aadb86ac185ae05640fedb2fbd37211`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:59:32 GMT
WORKDIR /usr/src/perl
# Tue, 24 Feb 2026 20:05:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 24 Feb 2026 20:05:10 GMT
WORKDIR /usr/src/app
# Tue, 24 Feb 2026 20:05:10 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98893044a03d87b30cbf84a6066b62f88a1ca634b6cfd57ead6b298ae370f328`  
		Last Modified: Tue, 24 Feb 2026 20:05:20 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e629cf9cab71168f201886cf0b7aef1b34c6c3d955e80ad9c0f1a1dbe7466c41`  
		Last Modified: Tue, 24 Feb 2026 20:05:21 GMT  
		Size: 29.2 MB (29197817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51503ade03220d0a5efa84c9c2ec7b355af0d9ab17b0fa2ce63361bb9694ff1c`  
		Last Modified: Tue, 24 Feb 2026 20:05:20 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:ce95782f3527fe99d235085f4c1ef8bcf43ea3d67f6e56eb70b129767cbc4619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd573f6bc6e1f2e1a5c7c3542f56142ca137f7355f6bb03dc909a22635c56e3`

```dockerfile
```

-	Layers:
	-	`sha256:628725990774debae51d4111a8a48941d1dea9d9f39e8f1c7243370c7b28d81a`  
		Last Modified: Tue, 24 Feb 2026 20:05:20 GMT  
		Size: 4.0 MB (4003689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abedbade1aa9e1a9934f46e40921819cfa99cdfdf14f9faac5cab499f01bc1e6`  
		Last Modified: Tue, 24 Feb 2026 20:05:20 GMT  
		Size: 20.4 KB (20380 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:5eae42add93849edab271f734032746688bf6eaca054596bbb51ee9bdfba0b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54485488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99590c66283e433ffdd31b9cad0ffd8fd45ddfc7bbfc9741c9000b8480b5f0e4`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:22:22 GMT
WORKDIR /usr/src/perl
# Tue, 24 Feb 2026 20:27:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 24 Feb 2026 20:27:48 GMT
WORKDIR /usr/src/app
# Tue, 24 Feb 2026 20:27:48 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7e11d74177c95b35574d21ad9cfc34e7a00c74f0aeb1c9f565b14d8a6d1b05`  
		Last Modified: Tue, 24 Feb 2026 20:27:58 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fb2cc2095fe968acdddea74649064256c917ff6493b70862bdf1b5b0e5db8d`  
		Last Modified: Tue, 24 Feb 2026 20:27:59 GMT  
		Size: 28.3 MB (28271477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a8ce2022ef5b331073a812fcd12fa0725cddb7aa3adee2034c5bae6f7926cf`  
		Last Modified: Tue, 24 Feb 2026 20:27:58 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:c0da24dbb5057b13f00c437162b7c42abd946e7d040c7a6eab853aa8142a6cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e073b227d255c331990a0fa3511f4f4d13169730e5622bb7e5aca1985be229`

```dockerfile
```

-	Layers:
	-	`sha256:32eb6ecfddcb08ea187eb4afcebe482736006f1b8b78ce79cbb87ade4c55e8b8`  
		Last Modified: Tue, 24 Feb 2026 20:27:58 GMT  
		Size: 4.0 MB (4002880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69dc1e0348b70bf7ade924c1491b5e95f430ed5a1f963cbb028b203653f8074f`  
		Last Modified: Tue, 24 Feb 2026 20:27:58 GMT  
		Size: 20.4 KB (20380 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:c99a80eb7ba863cd0f717cf3ee45fae548c15d1f817c73d4132025e60db9f702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61765745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a683942232642af80cf26facccdeae694d82ba865908885fcedec0021454e20`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:32:51 GMT
WORKDIR /usr/src/perl
# Tue, 24 Feb 2026 19:37:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 24 Feb 2026 19:37:28 GMT
WORKDIR /usr/src/app
# Tue, 24 Feb 2026 19:37:28 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719466403a92d37d6b023467106f474fec41d63dcf58f4c6197aa119e32aaa0d`  
		Last Modified: Tue, 24 Feb 2026 19:37:40 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a63beec3c145619e9143be64835d80c697ba2718387fd4c9d6497c4a150d74`  
		Last Modified: Tue, 24 Feb 2026 19:37:41 GMT  
		Size: 31.6 MB (31625379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352a5bddf4cdd3df0c1631518cb5e239dbcfc1ea2481ce9eb5925f874b8cc35b`  
		Last Modified: Tue, 24 Feb 2026 19:37:38 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:da439e862c6888d7f9ec647e4d391e72beb4062537bda1b4b42b1ed4a2bfd642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e69a8a59836add6659cc49ed1a9e53f80d8099ae36b443101990f7fa56fd111`

```dockerfile
```

-	Layers:
	-	`sha256:863b17d5b8f8175516a240405008bf287771edf0dd71de446de7ecc5b48226b2`  
		Last Modified: Tue, 24 Feb 2026 19:37:40 GMT  
		Size: 4.0 MB (4005755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86437e7c284d2d48d1911f214b16ba2e0f4ad0233a2cabbbb6455be2cff7c380`  
		Last Modified: Tue, 24 Feb 2026 19:37:40 GMT  
		Size: 20.4 KB (20428 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim` - linux; ppc64le

```console
$ docker pull perl@sha256:2c3a5270cf5a31d7971f8c2050e1e7f2675803a8c5b0e4b032a277eac6be82d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66273501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224e49ec3aeaec2fe83adce5d4e0706b8b4255ab1de18a395710339ac7ee481e`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:46:18 GMT
WORKDIR /usr/src/perl
# Tue, 24 Feb 2026 21:55:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 24 Feb 2026 21:55:18 GMT
WORKDIR /usr/src/app
# Tue, 24 Feb 2026 21:55:18 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab3bca8ad66fffcbb2fb312a596d9d35942e0cc687cd99a34a53967b51053f6`  
		Last Modified: Tue, 24 Feb 2026 21:55:40 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d8dbc3ce1a5ec07dc0e16930c32469f14afc5c7f0234d4fb55b1e694f2618a`  
		Last Modified: Tue, 24 Feb 2026 21:55:41 GMT  
		Size: 32.7 MB (32673016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15051d50ee363f9da5d9a1183a7c8e1143663c72cceab3b184c7a9f7655f9557`  
		Last Modified: Tue, 24 Feb 2026 21:55:40 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:a9cae76345f23a0514b062be645de10ed756bdb0d33c7c7c7a9296449e1947d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94487b8572ee44f12d99c61263e8b4712e1dc267d394d75ae64411201f24f39f`

```dockerfile
```

-	Layers:
	-	`sha256:a87967d01de870023d55c76ceadbf55a2ae8fff0b8c555326e6dd4e703b71976`  
		Last Modified: Tue, 24 Feb 2026 21:55:40 GMT  
		Size: 4.0 MB (4006648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39aef72be6fd5c28845fc2164b0101c3cb09b13b53e860d4b5e0a6013b007b78`  
		Last Modified: Tue, 24 Feb 2026 21:55:40 GMT  
		Size: 20.3 KB (20331 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim` - linux; riscv64

```console
$ docker pull perl@sha256:a3efd97d30e55ca0b6c5d886f5f419292eada5b9d68957597e67a8088aaab391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68064615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baeb32ce38a0bc12953b480673629479716bcecb8c2d0cf2ef2dbcfcad2834e6`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:59:06 GMT
WORKDIR /usr/src/perl
# Thu, 26 Feb 2026 23:06:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 26 Feb 2026 23:06:34 GMT
WORKDIR /usr/src/app
# Thu, 26 Feb 2026 23:06:34 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195627fbbda9b60918f227dd345b9e530095bd286577d0139a8cb67387002a9a`  
		Last Modified: Thu, 26 Feb 2026 23:08:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3327f556f280c40b771efa74c8028c8dfd5b8070603a42abed8f948a72276821`  
		Last Modified: Thu, 26 Feb 2026 23:09:00 GMT  
		Size: 39.8 MB (39787930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babb6344233a4571edcc6af03222f7bb8bb5ab334e0aa8d7201d517edadc136e`  
		Last Modified: Thu, 26 Feb 2026 23:08:53 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:51e4979dbf400070e9f1e1125d143a6e80c1b46aed89ce64f330f126a6933a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4018246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2d16894ee24fddd16e7abdca95d9b5fa43c711d7344f0627b15b5477dc0fd3`

```dockerfile
```

-	Layers:
	-	`sha256:0290b3b5360f9531fd719bd900a2bfadcf5707cfc71d0bfced132030fef101ce`  
		Last Modified: Thu, 26 Feb 2026 23:08:54 GMT  
		Size: 4.0 MB (3997914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5316ef317f84bddb8e2b38aa027cd7f6aa0d9ad53db6f94b07d6184d1c1be9`  
		Last Modified: Thu, 26 Feb 2026 23:08:53 GMT  
		Size: 20.3 KB (20332 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim` - linux; s390x

```console
$ docker pull perl@sha256:8d110e13ca5a2e71754fc5e4f7084fd94fd62f6fb1bd38e685c23b7aa133dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61149125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3b6caaffd350e36db155c7283085358bdafa62b603c3d5027511cbef1d6e90`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:14:54 GMT
WORKDIR /usr/src/perl
# Tue, 24 Feb 2026 21:23:29 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 24 Feb 2026 21:23:30 GMT
WORKDIR /usr/src/app
# Tue, 24 Feb 2026 21:23:30 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966e6798093ed2d9ec8b41e60ab9c5743b776bab7382b198e0149ff1168b1bd7`  
		Last Modified: Tue, 24 Feb 2026 21:23:55 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5cc1b6804dc186da84c6511bb973b77c51f35196f76fc5728b0871da818fb9`  
		Last Modified: Tue, 24 Feb 2026 21:23:56 GMT  
		Size: 31.3 MB (31310678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866096bc788120858e528e770581451baee2b3e5a4df9dc9adfd2cca3af33307`  
		Last Modified: Tue, 24 Feb 2026 21:23:55 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:3a4d7b33c69bf6af8aec54dfb27bf5069f992d194111a4912b02108c7a14c755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ab784cd0d1e1e9ccd69311c03382dd47125add215cd421a02e165f58a57067`

```dockerfile
```

-	Layers:
	-	`sha256:e8bac87785ab590682fc799727bcfaf2107e600fefa2accf6cb80f79faa93f8a`  
		Last Modified: Tue, 24 Feb 2026 21:23:55 GMT  
		Size: 4.0 MB (4002940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6af3c0ee625a846bc99d4b89cc3571b5299ee248ae757057284241a5cac3ed7`  
		Last Modified: Tue, 24 Feb 2026 21:23:55 GMT  
		Size: 20.3 KB (20251 bytes)  
		MIME: application/vnd.in-toto+json
