## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:5d4974f16b31d983a5e37dcfbe830ffd61ecb66d4b9de8aa10f945ee01bf7f6e
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

### `perl:devel-slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:20f4674d20d2052d3073bb6c3bcd00056de6543c0276010f36f11b842587fbd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57448996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee6ce51ca283baef801be35cfd0059bd93dece11ef3668da0714c50f8160986`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/perl
# Thu, 21 Nov 2024 11:29:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.6.tar.gz -o perl-5.41.6.tar.gz     && echo 'efe7b25a353e2f370818bf6cf1545807c144acf2d9a48368a990827aa71db21d *perl-5.41.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.6.tar.gz -C /usr/src/perl     && rm perl-5.41.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/app
# Thu, 21 Nov 2024 11:29:59 GMT
CMD ["perl5.41.6" "-de0"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7afd08c49504b22bec06fe094464bf8aaf070833722e6e22b18c68073eed60e`  
		Last Modified: Thu, 21 Nov 2024 19:36:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da6b27192a0ce37d6278e6595bc5cce69c2cfe88643395c6d644abceb21c62`  
		Last Modified: Thu, 21 Nov 2024 19:36:32 GMT  
		Size: 26.0 MB (25997168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4133cadf94ec4165d54a5da16dafd7fc646fbe7ea6a27139822c1675e0bf518e`  
		Last Modified: Thu, 21 Nov 2024 19:36:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:dac1f8e11d9f8b176b51278ae1ebdcefcbe81588939160698b7e476b2e65115f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eae2a68855ebb92ab4e51449991fc5a33e2b1a62bcc9b8a9aa752037d1b189b`

```dockerfile
```

-	Layers:
	-	`sha256:87c1cc38f1c2ff026f761375ae2ca1044be0222ae436d932e33ae12a67ecb923`  
		Last Modified: Thu, 21 Nov 2024 19:36:32 GMT  
		Size: 4.0 MB (4004640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37bb8d86479e529568b89bd68010f8accbce912cf104b151995109d23b14669d`  
		Last Modified: Thu, 21 Nov 2024 19:36:32 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:d5a2eabf16fdf69ef4c850c7c3b579340dca2e5b75b73205c50f28ffd223cc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49825316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c416697b91a1cfbc3da20acca9eb66e415ed646ea7a205a354544ab9bc66da`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/perl
# Thu, 21 Nov 2024 11:29:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.6.tar.gz -o perl-5.41.6.tar.gz     && echo 'efe7b25a353e2f370818bf6cf1545807c144acf2d9a48368a990827aa71db21d *perl-5.41.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.6.tar.gz -C /usr/src/perl     && rm perl-5.41.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/app
# Thu, 21 Nov 2024 11:29:59 GMT
CMD ["perl5.41.6" "-de0"]
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073e6b36d0e09e104502ac6fb989ded77b947117e03fed556c85e1bffaa3edcf`  
		Last Modified: Wed, 13 Nov 2024 00:00:23 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9036e5c9971d8a5b3297ff3660a59075679b32320383a0ae9669836eb2fba4e`  
		Last Modified: Fri, 22 Nov 2024 03:35:29 GMT  
		Size: 23.2 MB (23215791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daabb7846004899080f328c49c9a7c8226e1b4cee2a08b9946cfdedf72919f99`  
		Last Modified: Fri, 22 Nov 2024 03:35:28 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:78ad80c4d91529bcab10c7d4f4f5b46ebe8d9472c849b2f272c3195a1475cdda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9fac93fb914032b2ed94e7b8f3b5cc42ef9b36ac1e17ef270a31f65b40718e`

```dockerfile
```

-	Layers:
	-	`sha256:314f9488cf3340f042e13c849d30028bb23de280c298e545a12d927849c054da`  
		Last Modified: Fri, 22 Nov 2024 03:35:29 GMT  
		Size: 4.0 MB (3978591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aba668f69df2a66fc6b89915f44c01d76065b6ecd25ac1c191b63221920cdda`  
		Last Modified: Fri, 22 Nov 2024 03:35:28 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:1f9bbce196ee33056fdf94efcda583834758f8dabfe89e4f6bed1e031c1fd4e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55205613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42eb86eaf854e02fb678675fb7677c94e307e30c61cb916b925bea9df1821ca0`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/perl
# Thu, 21 Nov 2024 11:29:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.6.tar.gz -o perl-5.41.6.tar.gz     && echo 'efe7b25a353e2f370818bf6cf1545807c144acf2d9a48368a990827aa71db21d *perl-5.41.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.6.tar.gz -C /usr/src/perl     && rm perl-5.41.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/app
# Thu, 21 Nov 2024 11:29:59 GMT
CMD ["perl5.41.6" "-de0"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bba1a2317f5b09c5a013d516164f8063e6affa6822d75dbc5e89d81deca640`  
		Last Modified: Fri, 22 Nov 2024 03:39:25 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ab8625bf316b5306ca2f53323535d77d3949b316179ea60bacfc3992187277`  
		Last Modified: Fri, 22 Nov 2024 04:01:51 GMT  
		Size: 25.1 MB (25113746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c424a8103d1465404220f176985eaa27af91ddeb927c0970dc9f917fa5631058`  
		Last Modified: Fri, 22 Nov 2024 04:01:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:398409b15574ce985e4e282007ef98e5f4163601af301f45aef98ce8a9841b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba18e3c285473ce554bf57a2ea3041534f10e6a4f38ba3e1ad4fa155550b931`

```dockerfile
```

-	Layers:
	-	`sha256:fde44873b153b122a39d3a0d976ad4c694089adbeb8edfc45f84ca8a088e8646`  
		Last Modified: Fri, 22 Nov 2024 04:01:50 GMT  
		Size: 4.0 MB (3979001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f4ab433f20c787dbc5325a17077d467de59b8ba471c43b5ca4485623f3e04d`  
		Last Modified: Fri, 22 Nov 2024 04:01:50 GMT  
		Size: 18.5 KB (18459 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:ff76db79161f5e796e9a64132b7d41ddabf815a0addb029f8b9ff449e9107195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59960950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445509d2136a5f3875798fe83d7662b522c04cdac6197ea996c3706edd3321b5`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/perl
# Thu, 21 Nov 2024 11:29:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.6.tar.gz -o perl-5.41.6.tar.gz     && echo 'efe7b25a353e2f370818bf6cf1545807c144acf2d9a48368a990827aa71db21d *perl-5.41.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.6.tar.gz -C /usr/src/perl     && rm perl-5.41.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/app
# Thu, 21 Nov 2024 11:29:59 GMT
CMD ["perl5.41.6" "-de0"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e078dee1e636724ac590ed626c57405a60df6979890de87c1bd808c8d125e9`  
		Last Modified: Thu, 21 Nov 2024 19:39:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8a0d34dfa28f54448df18ce588731d29254b0de547f32472afa014f3655442`  
		Last Modified: Thu, 21 Nov 2024 19:39:17 GMT  
		Size: 27.5 MB (27537332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a394036fcd78849a7c181cb107bd3e214da059945aad9c9ceb2ae08db508b`  
		Last Modified: Thu, 21 Nov 2024 19:39:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f332765a7e1f61cdc858def4afccc6c4d2b6306f22c54102d785865813a1a391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4027208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd3c175acec0562503e129a4dfaf74717f5466422f2053dae0343201fd68faf`

```dockerfile
```

-	Layers:
	-	`sha256:840c0f267bf794a4578b68dabf68c7e207843344a878dc19ce0a0c618e9126a7`  
		Last Modified: Thu, 21 Nov 2024 19:39:17 GMT  
		Size: 4.0 MB (4008868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb11efb7586506f6ade5add7941c4e103143d6d1cab4d02ede6d69c9d8708a3`  
		Last Modified: Thu, 21 Nov 2024 19:39:16 GMT  
		Size: 18.3 KB (18340 bytes)  
		MIME: application/vnd.in-toto+json
