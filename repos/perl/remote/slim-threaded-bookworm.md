## `perl:slim-threaded-bookworm`

```console
$ docker pull perl@sha256:81d7cd811403e05d3458766859aa91e968a962599de27fcd9bec87205dd2baf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `perl:slim-threaded-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:6ab97d53094b18e429231d6e47204bc6a00f0c5486b39a304669917519961959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58494954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39bb795da228d73f73ea777ce761fd9c90d5f2526963709ffae36330ea21ddb9`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:20:18 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 00:24:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 00:24:56 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 00:24:56 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb933f11ea061c625da8e3e3da64eee42d467a7720c259ca1ed31a49b3de2692`  
		Last Modified: Tue, 30 Dec 2025 00:25:14 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226b3e6f0ddcb0e7e92fb823aead7c76e5bcebd4c2c68cc39334df857d91d44a`  
		Last Modified: Tue, 30 Dec 2025 00:25:18 GMT  
		Size: 30.3 MB (30266265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efaab5981e778bfdc2ce5afea14065d3c4267b6231ee90d136b92c4d9615ee6`  
		Last Modified: Tue, 30 Dec 2025 00:25:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:4051bc656ebbffb761b8adfbbb883fc9596cab6faabbefbb96aa121e9e1fb94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409cbe7ec2337828bf3010ee406a1e8359a578e30ebe41c7ae2d115a0719fba3`

```dockerfile
```

-	Layers:
	-	`sha256:638b0a05e8ec8b069548e562ad4e895014f285a21c2174f40aa744e11880050a`  
		Last Modified: Tue, 30 Dec 2025 02:39:34 GMT  
		Size: 3.9 MB (3940042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7a032f61a2a0f0dd571e4288a30adb5f2ed8aa9659328e3722d8c1c1ea36305`  
		Last Modified: Tue, 30 Dec 2025 02:39:35 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:e134959f5d68b53aa0b2e3ea905eccde055e3d1c123bbadadbfaf48ebed9f466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53062883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009e10072e7b04e977f2b76e7044c5a06528243adfb22b79fdbce827efd1f31c`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:32:53 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 00:39:05 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 00:39:05 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 00:39:05 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f2aa60e784330fb0b7736ab13247742eb86cf7bddc8da60140526b44d259e0`  
		Last Modified: Tue, 30 Dec 2025 00:39:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8c5417a727ef6f753f630c02e3ce26474260e400eb90f5af757849c702d3ac`  
		Last Modified: Tue, 30 Dec 2025 00:39:24 GMT  
		Size: 27.3 MB (27305040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f5f88f60ee3c5a10ec876cbe33be97531c4ab1ddb61f0acaeafda6b1d4daf0`  
		Last Modified: Tue, 30 Dec 2025 00:39:22 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:ae652fd266a9bac89bf42a26783dd462978846cb95af00c2108cd6015e25514d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804480f42144848bd64ff40508691110c7557914f96d2c12f656dcbf539488cc`

```dockerfile
```

-	Layers:
	-	`sha256:7ae0265102701bce95772416e1a470863a187e5742bc9f8cc6fe087dfe35499e`  
		Last Modified: Tue, 30 Dec 2025 02:39:39 GMT  
		Size: 3.9 MB (3910909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68090a1d7b731c40738d5beb0968c9704b628ae15429cc12a4500f4f066d6bab`  
		Last Modified: Tue, 30 Dec 2025 02:39:40 GMT  
		Size: 19.0 KB (19015 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:6fae6cb1bd0ff3192698c7ae944fc68adedbeb88c7dbd7f8b3e46256d539a497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50337431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b636a568589258d692a104d904b38c2af74076c1830da84de9e9bf41d645e6f4`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:06:47 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 01:12:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 01:12:42 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 01:12:42 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a1ed528084deb61d0310fe207091f1bbf8c988db30639f1bc2116c4a50a8fa`  
		Last Modified: Tue, 30 Dec 2025 01:12:58 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd83aef935daa1f4f82586ef2cafb5eb2846c3f516f50624e78ca6ba0d1fa7da`  
		Last Modified: Tue, 30 Dec 2025 01:13:01 GMT  
		Size: 26.4 MB (26403111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e92623c0d9a9ace3274213e312242f643e0e47a23f7b4ed96c54831b3dabdf`  
		Last Modified: Tue, 30 Dec 2025 01:12:58 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d09ccf0caef60762c0cf8e40096557501da3388a2a2e674105137b17dc1c3d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d01c871c43894383a4d69242737e972f98d4e0829ef7432fb0b9f1b95f63f3`

```dockerfile
```

-	Layers:
	-	`sha256:99c4c91b4070fc3e525e76f1df3af80b1c212e18503223e128b42b1f3dc842ca`  
		Last Modified: Tue, 30 Dec 2025 02:39:44 GMT  
		Size: 3.9 MB (3910134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a698fa45252d7a45e68c499d5c87b8a87df56f3ed5350e8eada045a7f4e649f2`  
		Last Modified: Tue, 30 Dec 2025 02:39:45 GMT  
		Size: 19.0 KB (19015 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:9a0ab868b17c79cba5f084089f10ca30432715015c6b7552a1261b8134986da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57215665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935afd4f4a9d991535b67ea7c95275abaecc8afbfbe357cceb8366f454b12717`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:20:48 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 00:25:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 00:25:48 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 00:25:48 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc7ca6e65cf37fe192bfed79096c6fbba06145e0befd53ff174da11858047dd`  
		Last Modified: Tue, 30 Dec 2025 00:26:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89224a9655608767c997366f8e413b122272d1235a7a7b846c3cd2861ea59e38`  
		Last Modified: Tue, 30 Dec 2025 00:26:08 GMT  
		Size: 29.1 MB (29113188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eeb5223e8097e2947f5bdecac9a48b5c704621034c80fa95dbd020e23e6c23f`  
		Last Modified: Tue, 30 Dec 2025 00:26:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:5f642296e7a614c3a3fd4f2096a0c36118da77798fe8d73bc59bf0e737914064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadaa0d7529c5998343d3715a719310efea61e8ad9c542806b4970a126457e66`

```dockerfile
```

-	Layers:
	-	`sha256:4a8f41b818cd2d45074c2972f4d65fe913fdb3180b8e5a327bd2e3c8987588ef`  
		Last Modified: Tue, 30 Dec 2025 02:39:49 GMT  
		Size: 3.9 MB (3911303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbb6b857f9a4e4b60d415f32521796fa7393d283938fc09e7b61ebe8869b7282`  
		Last Modified: Tue, 30 Dec 2025 02:39:50 GMT  
		Size: 19.0 KB (19043 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:7f13ef1dbc63675a50551458e9637c212c68cf4e0bb3807a8fa9c9d2e3087036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58650292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d127e82b4da57bd2cf07c950de4b7778ea7c8655fb852dbee0a3fd11767eb363`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:50:44 GMT
WORKDIR /usr/src/perl
# Mon, 29 Dec 2025 23:55:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Dec 2025 23:55:54 GMT
WORKDIR /usr/src/app
# Mon, 29 Dec 2025 23:55:54 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7afa424b7b5ad3ed79affccf6f2c3458b8fd920e537b0399ce247bfc013594c`  
		Last Modified: Mon, 29 Dec 2025 23:56:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bd3751cd155266ea494eeff89c0f60c26259ec614c7887d6f62867ae8713a3`  
		Last Modified: Mon, 29 Dec 2025 23:56:11 GMT  
		Size: 29.4 MB (29440252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fb348cb4aa6dacf59dd166127eb8bb9b14f1f7e9942a98724c5cc117f98bd1`  
		Last Modified: Mon, 29 Dec 2025 23:56:09 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a86f1e043f1f9bfde6cdf09be8e4975289c64e95a04e9b164aa1c6bc297a8ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60a4ff56a6ef1f5aa6d0d597e809da34fcb79df6a2b4336221f3963cd5660e4`

```dockerfile
```

-	Layers:
	-	`sha256:899682cd689c47f648412f3d722eb552419ca6990b721e8b260e79e2b54b0916`  
		Last Modified: Tue, 30 Dec 2025 02:45:48 GMT  
		Size: 3.9 MB (3933974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d728ab7c17f33482b20a8c1ddd143a584a3d51bfc298d9402536eb99d9522ad`  
		Last Modified: Tue, 30 Dec 2025 02:45:49 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:426f887347b8f032c9785ea7f2cf906bdffd1353d00c265ee149fb9b574e6af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56946838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32818525fc74c2d7d112d5e26c1612be4dc51b9e3521335e7865da815169d551`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:03:03 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 16:56:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 16:56:32 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 16:56:32 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:b2b054f3a77e8800c8f5fad5ed6594164acd9d6bbb1409af308aa485c7352cac`  
		Last Modified: Mon, 08 Dec 2025 22:15:08 GMT  
		Size: 28.5 MB (28513802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8837d81354100718ad7cce78f5f15467a818ddf99e36f730446231d01d8b32`  
		Last Modified: Tue, 09 Dec 2025 16:28:55 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5887094d718c65aec70f616c78fd64d5ed798888a47f9e97fcda423b8d41f4`  
		Last Modified: Tue, 09 Dec 2025 16:57:26 GMT  
		Size: 28.4 MB (28432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f83a840e51f5ac33d5871bd596416994c45a1156961b674f9d07aae8b502b9`  
		Last Modified: Tue, 09 Dec 2025 16:57:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:88b2a5db4ccd62eb8d47d6c587269b188de2fe03ba85ab83e98724b0d6c41f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dbab9e50ef8af71475d3cdd364ca27ad0812088af825eaaa75e5b749047edda`

```dockerfile
```

-	Layers:
	-	`sha256:965425a0c85ca7675251c75ac11758664e5b19222d9fa55b57f122e9cd738d00`  
		Last Modified: Tue, 09 Dec 2025 17:38:05 GMT  
		Size: 18.8 KB (18787 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:77e1d84cfc47387edcb6e38bf140d0faea0becd387b843f8e87fa5159fdab7a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63172511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ea4521d4c3fb63b286e76f109807354f9da2cbdd65a8129612d65d91c1202c`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 03:27:23 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 03:35:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 03:35:03 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 03:35:03 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105d44cac00c0bb7f66d433d61581c854539c83113f5051db03276ac67f073c4`  
		Last Modified: Tue, 30 Dec 2025 03:35:32 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057b04feb0660e6460a3696dae2cea14416bdbaee6e1ca5c4a024af25fde4781`  
		Last Modified: Tue, 30 Dec 2025 03:35:34 GMT  
		Size: 31.1 MB (31103399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725d3aca8ccea74929a3924bbb205fc933b5f79c4cf9e8a28dad0296dc49af06`  
		Last Modified: Tue, 30 Dec 2025 03:35:32 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:27beb6b842b4bc31dac8eaba3478f20367e118ce14a88ced8d59fa1c8bc5ecb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f839d3b9e1939e4eaa1aa7b36faac619c056cfc5c953539286014777222478`

```dockerfile
```

-	Layers:
	-	`sha256:c11113dfaf7af015e6cbe688b22da47a43018ef25a53542cea5c54640349f847`  
		Last Modified: Tue, 30 Dec 2025 05:38:47 GMT  
		Size: 3.9 MB (3925982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a32735e50a6d0d4f703aec175996ca455309e2c75e69de4506ab58c4372408`  
		Last Modified: Tue, 30 Dec 2025 05:38:48 GMT  
		Size: 19.0 KB (18977 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:1f2bf0017ad8dd9715cf357e19318f4592cbed3cebfe66c5b8f070a540d01d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55692622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0df4ec02fe86d463b8775177e38d30d804f0e422ba8dc2b2f10262d082ed80`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:51:24 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 00:57:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 00:57:43 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 00:57:43 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fdac1aa576c7af6f516f6fb3c68a9872cebab60ed3845804f54386a45d4879`  
		Last Modified: Tue, 30 Dec 2025 00:58:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6981ec6753d6403a1f9265e7999fbcbfd4811b38f72dffe257019fdc43bd09`  
		Last Modified: Tue, 30 Dec 2025 00:58:08 GMT  
		Size: 28.8 MB (28807957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab6d8e6526d26cd43e390c58ed4edfade639b2a150962e1df3ed9795affcdfb`  
		Last Modified: Tue, 30 Dec 2025 00:58:05 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:fcaf4c3b53f1aa690d95f19ebd30a5d903ebf92c35801aff0ba3353328a2d1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36f489db3867bf0d5de502c9a5f41e026cf045327119274577607a347975200`

```dockerfile
```

-	Layers:
	-	`sha256:29f8ad3607c6fcefd6574459085aed15eefab0cada01edb724945573143ffc9d`  
		Last Modified: Tue, 30 Dec 2025 02:40:03 GMT  
		Size: 3.9 MB (3925315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6634e80f546689f2d56a8ae498a280042c92611029f7d2eea9a83ffc54bc2020`  
		Last Modified: Tue, 30 Dec 2025 02:40:04 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.in-toto+json
