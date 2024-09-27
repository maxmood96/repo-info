## `perl:stable-slim-bookworm`

```console
$ docker pull perl@sha256:9a1738f68e4860a00987431f6112e79e81c595bb69be3918f0b1d026e2f67c1a
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

### `perl:stable-slim-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:7e5c3000e3c29fb9035477eb8cb6a7d1391a3e5423a44aee54310694ac8dd3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59281290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e17d02cab05407de891e51dd2d418785e8db46b0f31b8aea8632c3692fe061`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 20 Sep 2024 18:57:44 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["bash"]
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c8058e14315f0b1ef046b965f8e4987930302963e5a19113ec030657371f86`  
		Last Modified: Fri, 27 Sep 2024 06:14:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1537b6822d30b4f76f6c083be26d8637bc7620daa931d0b77501e3af8a9e0487`  
		Last Modified: Fri, 27 Sep 2024 06:14:14 GMT  
		Size: 30.2 MB (30154749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db166bf551a3fc5fe9c11fb655d36a744d8a3f7595922f8b1a6d85b224ab2b43`  
		Last Modified: Fri, 27 Sep 2024 06:14:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:0f0b0ee2ae659ffc460482a6a4a611c60decbcd8bd6a1f0e9ee685e9adaf0c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3819923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b5cfb86b8db768f1366c49f6d614291aa47cc704aa724779ee53f3e07517fe`

```dockerfile
```

-	Layers:
	-	`sha256:38f4ca92fb26c87237804c1ac20d928aa325dea58fb3c302038735c185520b87`  
		Last Modified: Fri, 27 Sep 2024 06:14:13 GMT  
		Size: 3.8 MB (3799824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bdee49655e58a4ae89a3c270fdbf5761743074eb33aeab8a9eca7d1b4cea9a4`  
		Last Modified: Fri, 27 Sep 2024 06:14:13 GMT  
		Size: 20.1 KB (20099 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:2b5f7371304f272d75e6453cc446d9d0788be7a791faac38f69c21b6772bfb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54074557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7814f72ef671180ad4c83291cf36b1ddf1eb81c6575258b033a4ce989b8f2785`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83e3763c3015113b5770ffa9e9254b4751b03fbbd833e55608804eef4fdf7d5`  
		Last Modified: Thu, 05 Sep 2024 03:41:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4a90f2d2d2467e0b75a6def1fc3951d2ab5b617f6a3fe14bd3bb615f61911`  
		Last Modified: Mon, 09 Sep 2024 22:41:29 GMT  
		Size: 27.2 MB (27186882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec826bba204c80081d7a099a5286e0e019ed052225486e952737bf19ffe2249d`  
		Last Modified: Mon, 09 Sep 2024 22:41:28 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:bd9dbfbd05b682ed16c337e124a78244a7ca07cf7e9a4cde6e8c400fad086f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dac20c4cd7ccf77f4d0d7f39282eab65d19ddce3f34e3ae28d2f044a31ae9ab`

```dockerfile
```

-	Layers:
	-	`sha256:e8bb20c3af72676aaf6ef3ea7cdaad631c6aadf38435baf27ec03002eab4bb1e`  
		Last Modified: Mon, 09 Sep 2024 22:41:29 GMT  
		Size: 3.8 MB (3770261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:858386d978dcd0aec11c32fb071419eeedf2ef23eec6fd96531a942fdd9be819`  
		Last Modified: Mon, 09 Sep 2024 22:41:28 GMT  
		Size: 20.2 KB (20217 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:1ffcb0ce111940426d77b2cdfba583d2680016f5383820e01fcc6f8dfd769f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50999241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd464fd72f2e066087c71a12ea0378e6123a7aea52a49d1d24823d94f37347ae`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe259c7d9c3a03c733ddd0b165bf883b08fe0ec3de94c259a26191ebc38a8c30`  
		Last Modified: Thu, 05 Sep 2024 04:52:57 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759d9cff6993971334d68d1deb6a9709379c76fc7c64e511a74ed137e34500a3`  
		Last Modified: Tue, 10 Sep 2024 01:17:49 GMT  
		Size: 26.3 MB (26280711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b74e5f00365d786c41bc076c83134033c7d45764dcd69b2dc753e95e86bf214`  
		Last Modified: Tue, 10 Sep 2024 01:17:48 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:f1670f31e4717ab2a219f4023191dbe28d3e8f45bc8473664c633fc41299a233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279a42ac1296f2fc78654358c56afbc1ff6a6f74ed4b79ab2f69b02775627dd`

```dockerfile
```

-	Layers:
	-	`sha256:109ad0bbc2e942e96cb956c3d3589de6883d9e8cacd849d6486bc5b55827033b`  
		Last Modified: Tue, 10 Sep 2024 01:17:49 GMT  
		Size: 3.8 MB (3769900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae2d51508e230034d5249758ea74283d56a066fe834b027ff9c2f8c5ff82bae5`  
		Last Modified: Tue, 10 Sep 2024 01:17:48 GMT  
		Size: 20.2 KB (20217 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:c8b8bf5a741b37c10e808fce4441ad6af80e8ff9f723438f0d2e3d454890dc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58103096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ccaa8366d2797317e3825f27bd75efd4a372d03a0dd09deaf3e926c8d01c5f`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606cc29a2878ad3e7b275883a3fdf47c0b6ac93c6d4f5dcfb0c7a51a72ca94be`  
		Last Modified: Mon, 09 Sep 2024 23:27:56 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6f39491d31c6d0a2de23b3ed5737f60e82c54a3db39fe2e161fc2e94e2a169`  
		Last Modified: Mon, 09 Sep 2024 23:27:57 GMT  
		Size: 28.9 MB (28946285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68af9f6aea26f6a133330790e4ff721f5409a274dfbe98d6a3f0593c7d726dcc`  
		Last Modified: Mon, 09 Sep 2024 23:27:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:62d5b3276372d63f789af1fd5eb05cbdcba5bac965152ad7710f92cdcd4aacc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3791573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe3cac1f05265263aa1a0e048f5c1265de948cc2edfd7c8546274791503f8cb`

```dockerfile
```

-	Layers:
	-	`sha256:b80358de76a4e0959c4327085a94951a29e99c39b5f627207a0bc20c9006eeb2`  
		Last Modified: Mon, 09 Sep 2024 23:27:56 GMT  
		Size: 3.8 MB (3771094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:988d4b562293b1d28b50d9f0a8312d10649b13c0b391ee098b177aad53a2f516`  
		Last Modified: Mon, 09 Sep 2024 23:27:56 GMT  
		Size: 20.5 KB (20479 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; 386

```console
$ docker pull perl@sha256:555c51d0dbc1311ec742145725b5e2d7d4bbb6862a965ed5e5cca7645c7126e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59392684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cd284e35bd8381c94717e1a1e58b31efa0aab07ba95ef458a45aad4157a841`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 20 Sep 2024 18:57:44 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["bash"]
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850cd7717db3fee082f635bfd8f8c9a8aad01ed32abbfb3ba09d60eb410b7cff`  
		Last Modified: Fri, 27 Sep 2024 09:14:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab26ced899df8a95da9f82eaaf7d8328c72e579e645ffbb5f955cc896295f69`  
		Last Modified: Fri, 27 Sep 2024 09:14:14 GMT  
		Size: 29.2 MB (29248202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0c8bbf00bddc99a02b47e48e06769b37b84081626626fef7b2ea7967393552`  
		Last Modified: Fri, 27 Sep 2024 09:14:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d31257c7097c2e20a1bbb310523a106db3a6685ff74e1d7778f7b22d356c5adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6478ccb5d13af6dd6f92341d90b0c62653436d12e9412a944b3f157c640475ed`

```dockerfile
```

-	Layers:
	-	`sha256:9bca4edba5b8ff49ae92247c9a9e384e2079c76f715a15dceb5b10b4f37be664`  
		Last Modified: Fri, 27 Sep 2024 09:14:13 GMT  
		Size: 3.8 MB (3793664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f734d0163bedcd4a04cf162562460d8f8f79dc66b3570d80a5438dd711b7b903`  
		Last Modified: Fri, 27 Sep 2024 09:14:13 GMT  
		Size: 20.0 KB (20040 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:a493f0f825d60564b268b0f2db17ad4fd3cd8edf5ff8229f2c7879f7873ebabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57410856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a978c50c93b2d3889e521eb5e4e5559bf2520046f82dfb436961d1a2f956baff`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08209d32b30463539b5ac51103554a38b8f591c659ab44c1668cdac31b8f8cab`  
		Last Modified: Thu, 05 Sep 2024 12:26:25 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24604a0d1a0c907f59c1619ac5383b28f9a9d689d4d57dfa70a32c523e5ba03a`  
		Last Modified: Mon, 09 Sep 2024 19:54:05 GMT  
		Size: 28.3 MB (28285537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310077ebd01b014a14125b30799a264c65f60bafbca5c099cc0ca90bffa9c278`  
		Last Modified: Mon, 09 Sep 2024 19:54:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:429e0d0a4a9b22bdd480d9ba67c07232182cf69d14a795e92b4e132cb0b66d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (19991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5090d7a63dc391c5085528fb8f8bb1e4f3e4580cbb8c35babd9d37878b5e4e2`

```dockerfile
```

-	Layers:
	-	`sha256:265685b00ffce4121efabc33f53a12223b23b15bb28d4209323f9467c7ceb974`  
		Last Modified: Mon, 09 Sep 2024 19:54:02 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:5e4469c46a5fee837c41783c8461bd89f5abf6b81391cb9e5b41ab5eae71a4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (64036087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4b7d68562408006f28d5a97cce07d0fed425891178c6b580eee57f692adc3f`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951bd9f86080012eeea51a02f1e1b08407ed886484e33df2e65c13f504b2beea`  
		Last Modified: Tue, 10 Sep 2024 01:18:17 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5179fe55f7d990e97a436dcc79331387180a0b309b4d549d2538da1842805c`  
		Last Modified: Tue, 10 Sep 2024 01:18:18 GMT  
		Size: 30.9 MB (30913464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31956058c70294c3a746664cd639914349a93075c16398b34cec7840b18e09e5`  
		Last Modified: Tue, 10 Sep 2024 01:18:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:caf7bc57db5edb746adfe0f96f9bebd8447c82b128b425c05ee02be6539a53fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3805789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcc1907d0ea8895f997037b20e3b6ebfa90db2847edf8b4efd4022c0a6d1c89`

```dockerfile
```

-	Layers:
	-	`sha256:0b7da3e3bbf3456d87201cd4896ed88e7e3cfba6ff977efafa97b58943889e64`  
		Last Modified: Tue, 10 Sep 2024 01:18:17 GMT  
		Size: 3.8 MB (3785616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c18fd89470dd278bf50d57778321aff3439ba3ac62433f4760447aa3a09dd0e`  
		Last Modified: Tue, 10 Sep 2024 01:18:17 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:711bfda20dc8104305779c6eec26a75987aac1ed9440e4577be1259605684ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56160137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77bb0887d7a60e25c8085342182d3a118c2fb6fd99f896c0764633d86ceff7d`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfe75ef7a285b19c2cbb20a21dc24bc52dd4874b4686b0eab8cc01df1199cf5`  
		Last Modified: Tue, 10 Sep 2024 00:23:36 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb39beef29ba97bf2e8a5c3d031ab1a037815adb998aad9dfdb508644116215e`  
		Last Modified: Tue, 10 Sep 2024 00:23:36 GMT  
		Size: 28.7 MB (28669551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabf0d7f264d4241226f865a0d6d531d18c26e33aad79d23812807017780c23c`  
		Last Modified: Tue, 10 Sep 2024 00:23:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:ee49c63529ae47c316afcffd29c59c0c62112d0299d327fddffdbdb3657ec595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3808168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a0391effc091c157ece4e97c0909fbbbba76e91642a5ef824ed965a0316eba`

```dockerfile
```

-	Layers:
	-	`sha256:49538eba7d1b181fd1035d7e2dfeacb163f7d91e449118f6e1c32eba56ccdc98`  
		Last Modified: Tue, 10 Sep 2024 00:23:36 GMT  
		Size: 3.8 MB (3788069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14e43c51cc93a92c12f87b237058dd689ed2057c06d3c89975ae727e30928cdd`  
		Last Modified: Tue, 10 Sep 2024 00:23:35 GMT  
		Size: 20.1 KB (20099 bytes)  
		MIME: application/vnd.in-toto+json
