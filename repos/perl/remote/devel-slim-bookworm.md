## `perl:devel-slim-bookworm`

```console
$ docker pull perl@sha256:0b45d4be1d58d44932a6c5a5b30f8b8643ac5c88a19d2de50a12d7a52853b450
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

### `perl:devel-slim-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:31f48a6cae89fb320c8b2049f6f7b0f6a62f161c1020889b2ba8481f7f41275d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58444919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8516db79dcf41969d3f71469262f4757843ecc84c8fae1db63bd28ab9f3644a5`
-	Default Command: `["perl5.43.1","-de0"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.1.tar.gz -o perl-5.43.1.tar.gz     && echo '5221ebf5badfbb943d168ff589ce93456a11f219105c930cc01e8a82a62adb65 *perl-5.43.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.1.tar.gz -C /usr/src/perl     && rm perl-5.43.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.43.1" "-de0"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060020b98927abdd2fda1bf811beb2123c65ab9c675d77c6790a4d40524ad325`  
		Last Modified: Mon, 18 Aug 2025 18:10:36 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4651d9d30554597ba954113c5b646c0e92dd217bb56573099c523e0f9e0382ff`  
		Last Modified: Mon, 18 Aug 2025 18:10:39 GMT  
		Size: 30.2 MB (30214396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb432ad4428900186e1b832fc121532ef47f9d9931301cd7492a59ddb725344`  
		Last Modified: Mon, 18 Aug 2025 18:10:36 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:3347c44c92873a521780390b67a02624a25413ac764c04d9422536d576c0a6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3955502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6544fed5f6f24edd33d129770a96983baf5e299c9d1dc01723c846fa45bb14f`

```dockerfile
```

-	Layers:
	-	`sha256:f428767029e5e795ce39fd3c0d5f8e1878a19a3f403e0d9a14a46f6f984f116a`  
		Last Modified: Mon, 18 Aug 2025 19:47:20 GMT  
		Size: 3.9 MB (3937215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c9f835291670f81289da9807cbba1952b20042bc08fe564b0e74c791a3fdb41`  
		Last Modified: Mon, 18 Aug 2025 19:47:21 GMT  
		Size: 18.3 KB (18287 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:0732fb923aee061d349643aabc6f541357785d22168f652d524e72422db937ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53023937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffca7ae4e8dd3ef8383c7582a5b09f6cfb768418bb1974f479d51b8f8e6182b7`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 04 Jul 2025 18:45:50 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/perl
# Fri, 04 Jul 2025 18:45:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/app
# Fri, 04 Jul 2025 18:45:50 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:53f325cb4b149fb7bd7e6ed7f8dfc1c5a37b5d828d75b4e6ba65a5cfd25aec56`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 25.8 MB (25762718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146752a9e897d66d698515c5012882014c92eb5ee3ee0d05222b55fbaa6d4a38`  
		Last Modified: Wed, 13 Aug 2025 00:19:39 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57396a1884eac6d25c29b4d7392714d6a1dc802aa98c97d8ca8d22da49a129b3`  
		Last Modified: Wed, 13 Aug 2025 01:01:36 GMT  
		Size: 27.3 MB (27260953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3c06e74d42c6d19c9a11b0b66144a9291b23daab5a1d9a371a2064d511409c`  
		Last Modified: Wed, 13 Aug 2025 01:01:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:df3cf420b8e30fbe831c248a418e863a03cea5ffebb66674e4fa423aca8c2221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db01af08d890271113526323c371aa808d1a976dcc031261f947371341fda494`

```dockerfile
```

-	Layers:
	-	`sha256:946cbe0c5c36eed4da8d094b07a79848abb5b819f3c3e7fc8d4d00942582db40`  
		Last Modified: Wed, 13 Aug 2025 01:41:27 GMT  
		Size: 3.9 MB (3909002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253f8ee3ea82550b70c9d9a956b7bd367c5135b8732ed496d01612e3bd9b06d7`  
		Last Modified: Wed, 13 Aug 2025 01:41:28 GMT  
		Size: 19.3 KB (19275 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:c58e21d7f5b1ace10a26153b86bf13452ad5a1b6156c016f6463789927a58dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50303149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2a5230ec70d742e9541736170c8f090394868d2a4a1de4c668ec3c0d4fe221`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 04 Jul 2025 18:45:50 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/perl
# Fri, 04 Jul 2025 18:45:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/app
# Fri, 04 Jul 2025 18:45:50 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2322ccce20f0016f59a4479bc74c8f9cb061f15bd5e494c8f6e8e9dd61b600b`  
		Last Modified: Wed, 13 Aug 2025 00:54:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6a7416d59b3b5418749dbe4aadf6272caf443ee6fe2f0e96ced1fe2db123ac`  
		Last Modified: Wed, 13 Aug 2025 02:12:54 GMT  
		Size: 26.4 MB (26363953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3bee6b535651d05607db5e45184f2600fd644fcc4f53367c9cea99cf50137d`  
		Last Modified: Wed, 13 Aug 2025 02:12:54 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d7589a82ecd5b80b36db8a5ee880b005ab5c26a41fc88624e15e0f6231e42d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5e3da4f69b230a93741e8694c0750474fb5cf4880e54fdb77983ef406a5f1f`

```dockerfile
```

-	Layers:
	-	`sha256:b29649851feeefb3043320c90c0bec07dab7c048503bdff85518495bfc7c7466`  
		Last Modified: Wed, 13 Aug 2025 04:39:40 GMT  
		Size: 3.9 MB (3908227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0654b343114cbe544ac23afff19efb5def134d42a64ef95907d8515741c7be0e`  
		Last Modified: Wed, 13 Aug 2025 04:39:41 GMT  
		Size: 19.3 KB (19275 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:47705a1291c33f3afc428f9e1d55877473031053452eadd7bf125b1f7157385d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57120495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1710f6e5bb89250db6983db1730234198804117b7cca7daebfe36137f1fa69f8`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 04 Jul 2025 18:45:50 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/perl
# Fri, 04 Jul 2025 18:45:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/app
# Fri, 04 Jul 2025 18:45:50 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd251b062a5d8450cbde0e1c34a4cd183cde8f5c717cb9f90b1f865d2f8727f0`  
		Last Modified: Wed, 13 Aug 2025 07:50:34 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205c1fb7c22af0ac3af9cf75b36bfba748f157bae771deeae18690089f9b9b4b`  
		Last Modified: Wed, 13 Aug 2025 08:53:38 GMT  
		Size: 29.0 MB (29038225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f92111294e7eacee885eb832fcad8b607ebc64cdf5ad5a0c9028bba1a0484f`  
		Last Modified: Wed, 13 Aug 2025 08:53:35 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:aeab7a77c4488b5da51d7c85b03914eb883a83e2b1a1dd26f116c9c98ad869a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d407db696d94d49db53671030d8fbf46fa54ae77cfe8c7a26737070bd3c1558`

```dockerfile
```

-	Layers:
	-	`sha256:5129f6652c162f9923e26fd339f7a36ebad9a40022f0616ab427c79be5b0f974`  
		Last Modified: Wed, 13 Aug 2025 10:40:02 GMT  
		Size: 3.9 MB (3909400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2385ea71b273ad972558c6a96fcb1c092af0fd741412e40a6c7c06585b82426`  
		Last Modified: Wed, 13 Aug 2025 10:40:03 GMT  
		Size: 19.3 KB (19311 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; 386

```console
$ docker pull perl@sha256:097bc5bd2830f6c8475875d131a5fe99f5b6cec9c586f0b285eb360e326caa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58549065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac6521221a4ada2f7bf4b4dc891d36c895b5eab01c48592347d56d7d10fca5c`
-	Default Command: `["perl5.43.1","-de0"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.1.tar.gz -o perl-5.43.1.tar.gz     && echo '5221ebf5badfbb943d168ff589ce93456a11f219105c930cc01e8a82a62adb65 *perl-5.43.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.1.tar.gz -C /usr/src/perl     && rm perl-5.43.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.43.1" "-de0"]
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffab9b8da57143cd7f6ae7d4588b24767156f3e214a4e3c165264361605c3266`  
		Last Modified: Mon, 18 Aug 2025 18:19:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb9d91fb944bac752ac4dff82b11cd0dc2208b597cd23424387a036e17c2224`  
		Last Modified: Mon, 18 Aug 2025 18:03:32 GMT  
		Size: 29.3 MB (29336191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edcd36835ebd5e29a2c4f1952a387a2ded6af7d6a5e0cbd0bf72527817bc1ee`  
		Last Modified: Mon, 18 Aug 2025 18:11:45 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:01ea212801140e9e8c4c14fe6db487b90057a558af93ee833b8129eeb682600c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35009f0678121ddffe82e4859f1ea2e2e090a57f6dedb02fb5690132e6b8947`

```dockerfile
```

-	Layers:
	-	`sha256:44fd78be7934d8b46c7af7f68ab2bcefe7886adea65a7efa7a08e29316f3cb52`  
		Last Modified: Mon, 18 Aug 2025 19:47:26 GMT  
		Size: 3.9 MB (3931157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6393415c53954e8c42c990fd7de8ee24bf0af96d806732e51ddcd3c765539bf`  
		Last Modified: Mon, 18 Aug 2025 19:47:27 GMT  
		Size: 18.3 KB (18259 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:46f074d8d62c60884c40095d7008fe48b6574ec03cd7adaf9ada8c82d30c6693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56876967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0e7158b40d745e9fbafaa66f84200218d8333342ee117f1d65940d826a6a7d`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 04 Jul 2025 18:45:50 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/perl
# Fri, 04 Jul 2025 18:45:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/app
# Fri, 04 Jul 2025 18:45:50 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:83bd2d8e15bdca1c657f4e1229c9515648aa638816bf4ae6a4be5a7afaee3a81`  
		Last Modified: Tue, 12 Aug 2025 20:45:57 GMT  
		Size: 28.5 MB (28516923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d33da0c48d232122ba5e3b459be09f595e03bde969dd5bc007fccbd3a0c5f3e`  
		Last Modified: Wed, 13 Aug 2025 08:19:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8593c24f6679db7f3c916d138e27e8f04cc9c85d4173e3cf88cf0bed25b56a`  
		Last Modified: Wed, 13 Aug 2025 11:31:39 GMT  
		Size: 28.4 MB (28359777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17160e0757ea4287e6238b6f80311717e57c432c2525c5aacf174eaa9e51212`  
		Last Modified: Wed, 13 Aug 2025 10:49:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:8e99021416b4b24e662cb68bbe09e39cc25eb5fd2cd8fbcf96ccd2fe8fd3df0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957fee2bec0ddb12fcfcf57e0b4f6c8f315218000f4e08b2b4423452db456b26`

```dockerfile
```

-	Layers:
	-	`sha256:bb8cdcc750a9917eff6ffa378109c7093b8038904d7e978b8552a14999f1f516`  
		Last Modified: Wed, 13 Aug 2025 13:39:08 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:c8a969725c7d409900c8a79a0d78be038d3b446a7031d496905eae42e437ebc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63068083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb575aeb949825d047574a4a246d2638f96ebc9fd0b1a92df6c93a311463b04`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 04 Jul 2025 18:45:50 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/perl
# Fri, 04 Jul 2025 18:45:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/app
# Fri, 04 Jul 2025 18:45:50 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d191148f8669c21adae168084e9b9c42b94e15eb261549dffb23f39c173f8aea`  
		Last Modified: Wed, 13 Aug 2025 13:16:35 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb3c0b05a921122f1eecf855f2bda474cdd82f5621bae12651084b5ff0f2ace`  
		Last Modified: Wed, 13 Aug 2025 14:50:41 GMT  
		Size: 31.0 MB (30994395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8c04983e01f23aa799c8f95a5a901ee9efbd1a7eb4eeaf6a9f742c982cdaaf`  
		Last Modified: Wed, 13 Aug 2025 13:57:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:6d961eb10a19b686c9b2f4edb36e296eef0314dbcf046c8387cc6d8322719060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3943312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b15ca6c2e0b69cc35a799980e23f50c6ed79f7349e41fdcd4a40baf44bf34b1`

```dockerfile
```

-	Layers:
	-	`sha256:7836dc5c7a70e5d0c3edf8eb5d3a9e01bf596c11911366c8f7cf412032eb621a`  
		Last Modified: Wed, 13 Aug 2025 16:40:03 GMT  
		Size: 3.9 MB (3924073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:617708eb89140aa694635fade50cdbe8898e6d70e0e24a62435afef13ad07c95`  
		Last Modified: Wed, 13 Aug 2025 16:40:04 GMT  
		Size: 19.2 KB (19239 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:f93fafd32cb694aad3b425865cf703fa68ad2e85a26674f3fc8488b3233007f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55628933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddaa57128261d2516a35aa18a06d234303be0ba57de605e7451fa48a00701621`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 04 Jul 2025 18:45:50 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/perl
# Fri, 04 Jul 2025 18:45:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/app
# Fri, 04 Jul 2025 18:45:50 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfa5cc136d2c75a99e3d0dce35603e43594a04be4f7a76e49da7b0c69b6f0c5`  
		Last Modified: Wed, 13 Aug 2025 15:25:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d231a567c3d0bbb357e32263a2b2db404b1d2d924c4f708180d53f0fd0de145c`  
		Last Modified: Thu, 14 Aug 2025 02:35:57 GMT  
		Size: 28.7 MB (28740828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545169f14bc2ef994923d8a5b990c5bba408cc0ce76be1e32b7ef252f7e859e7`  
		Last Modified: Thu, 14 Aug 2025 02:35:48 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:da7b0d04fa0c7cca1bc1e14132502befe48091d113facd49cb96c9e966787425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c1d41b96516c289032f9f08be0a6903cee6ca5e3bb62be22c80d63db5579eb`

```dockerfile
```

-	Layers:
	-	`sha256:30bdbc27e117e060ab42601589c49063ba2cfcfdc8b1f041e1e23ade9c18b226`  
		Last Modified: Thu, 14 Aug 2025 04:42:46 GMT  
		Size: 3.9 MB (3923400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4714539412aaf89e89d27ffd6a26ca6af9a8d2d19248cf551a136c0f2394f1`  
		Last Modified: Thu, 14 Aug 2025 04:42:47 GMT  
		Size: 19.2 KB (19183 bytes)  
		MIME: application/vnd.in-toto+json
