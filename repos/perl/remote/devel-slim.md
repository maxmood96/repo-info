## `perl:devel-slim`

```console
$ docker pull perl@sha256:39df6f685c89d9d97157b17541e1aff75f93d3f6f067e083a39f754a743f717a
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

### `perl:devel-slim` - linux; amd64

```console
$ docker pull perl@sha256:74b283102421b1241411730212d4932cf15ba9f70cb33d27600d377be2772ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58419388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4aae075ed9b5b4481801aadafaf3f9052a3ad6ada4610d8a9493d1abe96429`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b4d5a87daf8d194235845d432e82b0f19b6804fc3a226431bdfd8d06e5b07d`  
		Last Modified: Tue, 08 Apr 2025 01:35:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaacc56c437dbc3f21eb664ef4accd28d77cf4d1f9c0c5db8fad8b8bd741cf6`  
		Last Modified: Tue, 08 Apr 2025 01:36:00 GMT  
		Size: 30.2 MB (30191862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59028085d0f25b40d745eda8ec4dd5629be38043c526e90c77dc1f3464c474e6`  
		Last Modified: Tue, 08 Apr 2025 01:35:59 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:3a65ed0212c50ea0a524c8f52a6879dd3040f073430f4b22dd58fe5a9052048c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bb77dc7d67d778d3906f0d70adbaca39bb56bd334676f0ba30eb58cbee36af`

```dockerfile
```

-	Layers:
	-	`sha256:f24b8cb3e6caada88cbaba5cbef5aa3e6dfc309b7792250378faa7b53766a66a`  
		Last Modified: Tue, 08 Apr 2025 01:36:00 GMT  
		Size: 3.8 MB (3809366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c60ea2ea20204cdd3549407c705da2a5eb9a74d1f13aa2aeed7d0248b1d31318`  
		Last Modified: Tue, 08 Apr 2025 01:35:59 GMT  
		Size: 19.2 KB (19166 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:49c579db23ce4d660ebbe1d0e397dd6fa85290770046cd5602008187cbe28c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53020249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad3f7f88af7366a16943e36e3a87e1b890bf902d5c004607caa14f9df15b5b6`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112139abf4d4046df70c325c1e9a7edc6a3a614df8829b66870c0391e61ed1de`  
		Last Modified: Tue, 08 Apr 2025 05:30:58 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd8e943d74b54a5a96594c278d9f515f3d658686289203af46ef202578f72ee`  
		Last Modified: Tue, 08 Apr 2025 06:10:15 GMT  
		Size: 27.3 MB (27262163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccee9e6391f3918103437fd7d7e3e9cc07cf9ce7897bb44997b305844fe49eda`  
		Last Modified: Tue, 08 Apr 2025 06:10:14 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:c7b369dd5cfff4a0601fbbf0f4268358ad5cde25877e55c7881bddaa9ad31aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a38ba74e36397baff71bd4eea5da0a69a88deb435a09a8fca943e76a84e94ff`

```dockerfile
```

-	Layers:
	-	`sha256:436b982c69d5f8bf1651f2846eae782f3c757f21a67c8f89b7e1f3d096642b61`  
		Last Modified: Tue, 08 Apr 2025 06:10:14 GMT  
		Size: 3.8 MB (3779933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e132dde708f5bada059fb64985f058358c2b11ca22aa19e7d77093a33f41e767`  
		Last Modified: Tue, 08 Apr 2025 06:10:14 GMT  
		Size: 19.3 KB (19258 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:2580a126044b5d5be5cf95c4b529d0b620d83b8cdeb28c5bf34e94049ea591fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50294656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7bdad4422fb3015d47f26a6865db500c603754fc999eb7b4df479b06997d36`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f970e52b9a94df17ab424d02caf955a2f8c681f2dfa2e3250b67763fce3171c6`  
		Last Modified: Tue, 08 Apr 2025 08:19:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3e3c12d34e425cd5ce7d781fb1c51edc883dbe7faa7bd6b55788ff35a788f6`  
		Last Modified: Tue, 08 Apr 2025 09:40:37 GMT  
		Size: 26.4 MB (26356521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c950a39951ac8d9498f7e43a8a94ff118a46127e84a34c1ba853a3ca8ce1b4`  
		Last Modified: Tue, 08 Apr 2025 09:40:36 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:2537526db3a565a1bf6fa42257ae3f820584e73724c093998da8e77b0d428d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3798723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35734da468ecab6a6567ef74769cd5283b712b5902eb7fc4e96dfcc6a431d24c`

```dockerfile
```

-	Layers:
	-	`sha256:3d2aee76154c7538d7d931cb24c0c23900e7d38f8bb43f58e6fa05c0a6ac07ea`  
		Last Modified: Tue, 08 Apr 2025 09:40:37 GMT  
		Size: 3.8 MB (3779466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1aaf9645aa4a90e59879231f49033db07a08d834179257d27e09a984f337081`  
		Last Modified: Tue, 08 Apr 2025 09:40:36 GMT  
		Size: 19.3 KB (19257 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:6e646dc899b1bfc940e13dd30556e05198f93a9ef07ac695b20d21ce1a9771c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57079347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940207833f188bdc4447c2f581d43cbd500d18f92b2463caa9f18442a9c20c1c`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69c4cb63e6f0eacb629a0667c4631366411c23c9a2bcdb87a09e54693e32536`  
		Last Modified: Tue, 08 Apr 2025 06:54:35 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5350557ed3827431cb2383996a995eab2c24d97fa217da29648f2b9765e5fc`  
		Last Modified: Tue, 08 Apr 2025 07:57:18 GMT  
		Size: 29.0 MB (29012760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aeee2a4694dc698891de7f30f41a1317cb93337e72b1d09a6d0e4d34844bb44`  
		Last Modified: Tue, 08 Apr 2025 07:57:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:ab47b82a90217e55444e5ebf273369670ff9d5c85edc05364cdfd4bfcff97198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f736946e922515c502f2b21bcb4e051403d1c3f5709559a9c3e66dee6904aaac`

```dockerfile
```

-	Layers:
	-	`sha256:059f296404a6d00dd5f6cbe24b0de559ad229ca6996d4d8be79c79b83ea75679`  
		Last Modified: Tue, 08 Apr 2025 07:57:17 GMT  
		Size: 3.8 MB (3780639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457df12312e3738b550edf14c5587954da4712ed9246844125f0ba43f7138f58`  
		Last Modified: Tue, 08 Apr 2025 07:57:17 GMT  
		Size: 19.3 KB (19294 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; 386

```console
$ docker pull perl@sha256:674123fe6342af8395814450d21f5f43aa2521ceef5b87d93bf719efc333df56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58529674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112e2cd7c4980edb667b06490a12009f5405ac513f88fb369493bd34c7ccdc3a`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b743711dacab62250c659c9e083b15a70cc9ec900b89769c0ce3d48c4c3b69b9`  
		Last Modified: Tue, 08 Apr 2025 01:33:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6065cf63d9a5408d12aa0123d5e98eb1bc90a2d4c0d30485954e84b10a90afc1`  
		Last Modified: Tue, 08 Apr 2025 01:34:21 GMT  
		Size: 29.3 MB (29318676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592910605d3474b7bc0a4ef4dfae7f1a4639649072647f73b5fc650c0cf5af17`  
		Last Modified: Tue, 08 Apr 2025 01:34:19 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:1db6c5b2c5e65744a5fef8bb86d99c957786054023f4be45b3544231271e000f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec0e00e8d6e177d3fa061025429eaeb0f0eb3dc86495299540986a2f3a3af1cd`

```dockerfile
```

-	Layers:
	-	`sha256:ce71d6b3526ab1d8a4f581310096ae205a912a73de0ce3310e8b11d687de5dac`  
		Last Modified: Tue, 08 Apr 2025 01:34:20 GMT  
		Size: 3.8 MB (3803230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1ffe9916c9bff361bf354225722dec46920e9d78c83829b5b7242b3eb53fae`  
		Last Modified: Tue, 08 Apr 2025 01:34:19 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; mips64le

```console
$ docker pull perl@sha256:5355a0969baff73a0f4c525cb3eb547c36b5caf55692c4db573aac6e588330af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56883040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5e2b27d58956b04fc8bf15106bd3d9eddb560323f2b54d6fd6286e5d811b63`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc8deb84ffe76d23c92f7b413c1ab9f7a4f4d99bef358ee3e7d515b5b6bbbb0`  
		Last Modified: Tue, 08 Apr 2025 17:53:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ba381d29b1f699c59eff973f02844e57da72d8a503caa6116f9b0051ca14cd`  
		Last Modified: Tue, 08 Apr 2025 20:42:11 GMT  
		Size: 28.4 MB (28368818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420dba5e122e5feb38c9a7de5bf27d174aca2453cdbcf88103ecb58178ff96b4`  
		Last Modified: Tue, 08 Apr 2025 20:42:08 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:9cda5b2a9969b80752bd4932264b4ecd74340b8f5e021c1858238c3adf898481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69691145f2a5e3a69a74dabf8ef370f595c81ae9f7e87d1d77ee880495038fdb`

```dockerfile
```

-	Layers:
	-	`sha256:3badbf66c356068dade8a972b0e83b74ec32fd6e04ebe4d7f247b665e0cf6d32`  
		Last Modified: Tue, 08 Apr 2025 20:42:09 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; ppc64le

```console
$ docker pull perl@sha256:b6e34d0c9296159d76217a0a5904490432da582b1afab9fb67aa4b2a02ff11e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63061807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf63b92186c071bf989090ac95a6da0dcc48c21bc29aff4a6e3ea98afffdb1cc`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d634a4ae1b2661b5e8225ddb992ca4bcba5f28f16419ac70dbd0f1f8ccc59`  
		Last Modified: Tue, 08 Apr 2025 05:03:52 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37487e1cdc462bfeedd0ab4bdaac4c7f037882ba6cae9544850aa658fa29a3ff`  
		Last Modified: Tue, 08 Apr 2025 05:45:36 GMT  
		Size: 31.0 MB (30993310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3c4b689ebe380a150abaabcb27a8111417de7c3290f1c3adce24a654d6e56f`  
		Last Modified: Tue, 08 Apr 2025 05:45:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:2a643ea56fc5c98248effc0741387f72f92675a828e9b492441794cad4e97187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3814396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea8ad315a4e50ba28bda75ce4dbdca141fb04e55f9e6d70683a5e64b8cb864d`

```dockerfile
```

-	Layers:
	-	`sha256:a5f2378a5624101b962c4bd0c4b6a7497be6462c691b9122b02b89df14a7e31b`  
		Last Modified: Tue, 08 Apr 2025 05:45:35 GMT  
		Size: 3.8 MB (3795174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:156ae54e6e54c1a00d2efc3de751020ff7cad2bfe7d91aeb753565178b82fde0`  
		Last Modified: Tue, 08 Apr 2025 05:45:35 GMT  
		Size: 19.2 KB (19222 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; s390x

```console
$ docker pull perl@sha256:a8275f37faa91f23ee97d51a74b51384b448f5ebe9de0c0aeff09d0971d7798e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55624016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7cd68f276254ef9ff63fe2d93f130a32e1e5ff91751c2554fe4e06c339b049`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230d25ba28edf54dcfd82cccbf6f4c3ccc260a7a3892a38f64a4cb6e04ef3787`  
		Last Modified: Tue, 08 Apr 2025 04:09:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d112562610097df463d5a3cddb928b8ed698a4e2f86b840d8ad90d9a8015d3`  
		Last Modified: Tue, 08 Apr 2025 04:53:34 GMT  
		Size: 28.7 MB (28739143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69eba04545ba058afd592a694798ca4a8dd26989ec576d14155ceed198daf0f6`  
		Last Modified: Tue, 08 Apr 2025 04:53:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:e9b37acd9a48b5ec2cb8b91f191e1a252dedf4d8bfe12d984320dcc57160bd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c912d56b676264acf884b04d7e7d6f3f4cb331cad050235a5b2d02a3b6d78c44`

```dockerfile
```

-	Layers:
	-	`sha256:d3f805999a97e91163c45e6c578475f57f656eea15c88f6661b292812b2a17fc`  
		Last Modified: Tue, 08 Apr 2025 04:53:34 GMT  
		Size: 3.8 MB (3797531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5f619d22de74516f58f9ef6f295b111a4f49810680c7aa9e6a027db2fd92fe`  
		Last Modified: Tue, 08 Apr 2025 04:53:34 GMT  
		Size: 19.2 KB (19166 bytes)  
		MIME: application/vnd.in-toto+json
