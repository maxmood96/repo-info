## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:6ccd33bae1a414921c7b14acde04fe22a142fe2115faaf8a37c86b402e17b6bd
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

### `perl:devel-slim-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:3dc6ae680f78918628ef9fa174227e826a266d25d1c500c06d19092395901150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57377366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81a9519f70810c8f66bc704b26e7f476991dc4cc7fa364c6ffccdddf315d725`
-	Default Command: `["perl5.41.5","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.41.5.tar.gz -o perl-5.41.5.tar.gz     && echo '844d47856b8347fba553c90fa10e76de7ae579f81ed5312acf5f638d72079df4 *perl-5.41.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.5.tar.gz -C /usr/src/perl     && rm perl-5.41.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.41.5" "-de0"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0eb59ddc48891eacdf35c8234d63f19da201163db98b64b56f7ae10a839fe1e`  
		Last Modified: Tue, 12 Nov 2024 02:22:33 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b460106518c4f3fbb2a3647ee05ac13a60c9a28fadade02da3a9045f09fdbf`  
		Last Modified: Tue, 12 Nov 2024 02:22:34 GMT  
		Size: 25.9 MB (25925539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb5944ba27d95bb280860e9219242b194de52f6fe74de8fa61aa531b32db1d9`  
		Last Modified: Tue, 12 Nov 2024 02:22:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:142a9c4c616ecaf73ce40fb7379153d1ce277f84f3eca57af04f381efe10f632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4022851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60906f12ea87d46f36d20f12f099d9e212f737aa88aab756ca5422e0cee207e8`

```dockerfile
```

-	Layers:
	-	`sha256:d893fbe26e947362d5ba71b25c9f4114ec4eacf41536e69f5908bcb620c6fad6`  
		Last Modified: Tue, 12 Nov 2024 02:22:33 GMT  
		Size: 4.0 MB (4004586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33ad52872d7c339560c646a88a621ee41bc8139b3900650d2e0c3fc60dabcefb`  
		Last Modified: Tue, 12 Nov 2024 02:22:33 GMT  
		Size: 18.3 KB (18265 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:20343632cd232a6957abb0adac047becfed5bdc97d41bc689b36b3fa86b8cbec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52053639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429d5e1fe69669b06ea877d72f2671212a4fd1aea609103286dccead1283cf7b`
-	Default Command: `["perl5.41.5","-de0"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:45 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Thu, 17 Oct 2024 03:03:46 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.41.5.tar.gz -o perl-5.41.5.tar.gz     && echo '844d47856b8347fba553c90fa10e76de7ae579f81ed5312acf5f638d72079df4 *perl-5.41.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.5.tar.gz -C /usr/src/perl     && rm perl-5.41.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.41.5" "-de0"]
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f78d99a3de34e91faa5092aae0e2c26d0628985f89ee5db652d387eb9e6cc8`  
		Last Modified: Thu, 17 Oct 2024 15:12:44 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e911f98d44599b2c51807ad5a784c06f5913b3510165ad58a436287d1959b0be`  
		Last Modified: Mon, 21 Oct 2024 18:25:52 GMT  
		Size: 25.5 MB (25463820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15094ab0a274cb93fe9b1099c6119b95947e23af74ed4e78008c6b9496c0830`  
		Last Modified: Mon, 21 Oct 2024 18:25:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e4859a5b8a6b639ba96a3955a9759bf057ebd84a49845a5384f808d04a325872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acb373fee94014e79abf5ba3debf441cb16ac576bf159ed0ddd6dde21323f53`

```dockerfile
```

-	Layers:
	-	`sha256:3d53f5bb901ade2914d69b14b75e4ee1767bbd3ae51842831dc67d3bb9faadd2`  
		Last Modified: Mon, 21 Oct 2024 18:25:52 GMT  
		Size: 4.0 MB (3978501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fd8672179a61d0e8b399e05cb80a5ef0c233458bde5b8038e2550273682c21e`  
		Last Modified: Mon, 21 Oct 2024 18:25:51 GMT  
		Size: 18.2 KB (18156 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:d9f0f65a67a358e31701baac4bb6e00fa1e5865adc1eae7fb684246f8f302f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55157277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098d817f4a47867fcce9441959ab627e6e33d976a98747e3c332b7b341033e2e`
-	Default Command: `["perl5.41.5","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.41.5.tar.gz -o perl-5.41.5.tar.gz     && echo '844d47856b8347fba553c90fa10e76de7ae579f81ed5312acf5f638d72079df4 *perl-5.41.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.5.tar.gz -C /usr/src/perl     && rm perl-5.41.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.41.5" "-de0"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591feb0874eac35869e3201fb6de6cd41276754487f7f5722a1f98ff0ae4a004`  
		Last Modified: Tue, 12 Nov 2024 18:55:24 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dcd80ed3e80a07c9c95996b6c2f59faaa4568943a6be737fa64f820723cf69`  
		Last Modified: Tue, 12 Nov 2024 19:58:31 GMT  
		Size: 25.1 MB (25065410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cb9b8fd3e42f3a0afbcfe2d36d87316f59189f771558a8499546285e00120f`  
		Last Modified: Tue, 12 Nov 2024 19:58:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:2a69526109f8bd4bfa3a8c7585ac19e916cab27b2f591e913bc6c7e0e6fbbd2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa9e39db437a03d563a34646c4a51919d33e1e56a599b3c0ce24ef59891ce13`

```dockerfile
```

-	Layers:
	-	`sha256:18af3aa1aac0d7b6c254b33f1c4a394248cb5ae9bef61595554b6f61d8bd6893`  
		Last Modified: Tue, 12 Nov 2024 19:58:30 GMT  
		Size: 4.0 MB (3978947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5a7798ac5c79d972d0a7fb2d8ee506e638868a6fc9f9f28afa8b0b856bae171`  
		Last Modified: Tue, 12 Nov 2024 19:58:29 GMT  
		Size: 18.4 KB (18358 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:4d48e90c20191cf2333006aded34be8202cdbbe3116c5b31e7fc95a97a1f3545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59865335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c001acd46051e97756961fce2e83443efff931a77056594f47b34a61de3232`
-	Default Command: `["perl5.41.5","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.41.5.tar.gz -o perl-5.41.5.tar.gz     && echo '844d47856b8347fba553c90fa10e76de7ae579f81ed5312acf5f638d72079df4 *perl-5.41.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.5.tar.gz -C /usr/src/perl     && rm perl-5.41.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.41.5" "-de0"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e89995311290cced5b2faa80f163bacdb785b03c63aed86a5e89b1603cca31`  
		Last Modified: Tue, 12 Nov 2024 02:23:26 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497fb0df68516b028a8336efdba986bdca8a4847b038b0f368a5f6394222ddaa`  
		Last Modified: Tue, 12 Nov 2024 02:23:28 GMT  
		Size: 27.4 MB (27441718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9076b05e42bff6f8b62085e946f0496f911156d16c633ce8758cca73644aca3`  
		Last Modified: Tue, 12 Nov 2024 02:23:26 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:6d59d69dad53e3864ba932a4e2f78dc603d265c7cd586d0b543e50503794fb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4027053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258f887bb4ce057257aede24091d94c78a40f744849fc595f1cb6de659e76af6`

```dockerfile
```

-	Layers:
	-	`sha256:18022223c84fdb112ce0d7f5c83ae7374811d411d75b1b538172c1c3ddac12d0`  
		Last Modified: Tue, 12 Nov 2024 02:23:27 GMT  
		Size: 4.0 MB (4008814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0196b37fcf1c4660998b7d5d8073475c3f13e0816d551091eb8b5ae97d622283`  
		Last Modified: Tue, 12 Nov 2024 02:23:26 GMT  
		Size: 18.2 KB (18239 bytes)  
		MIME: application/vnd.in-toto+json
