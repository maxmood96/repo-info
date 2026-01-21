## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:1908b123b19d5f5b5c4771117fb84db92866e8642cc4f38a713bd487bd165a62
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
$ docker pull perl@sha256:d4884e56f956d4c110db7080b5353ab21577c5ba7258bac360c621894cfe356a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56680371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313b2873bdd4f48bd9b6225771d22f4c840a77146b2f2814563aefffac907ef6`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:01:29 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 03:06:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 03:06:11 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 03:06:11 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bf6da1a5c30c5d426f3fb84d24f86033d94ccbd4273fc057d1b2d9b6734443`  
		Last Modified: Tue, 13 Jan 2026 03:06:28 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5163c78a8a92b5793f6b03962500d5e63a3bb9bfdaf300691b54da4695d143`  
		Last Modified: Tue, 13 Jan 2026 03:06:30 GMT  
		Size: 26.4 MB (26421607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e42ef6b8a139b2a78928c9fa90fe61c5847375536562076ea31f042c0f6fc8`  
		Last Modified: Tue, 13 Jan 2026 03:06:21 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:bf8f32c031398f563f85489e0c75f9d59770a49c42de9c75b4542dcfd8eb9f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4139036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56883a655d2cda3b38debe55587716fce1fdbcc6158b3529b819ceb3711d436`

```dockerfile
```

-	Layers:
	-	`sha256:3b2ebc986f6ac471359ae3fd1a0e4b182abc49ecbb9e9631ac88aac767f7b864`  
		Last Modified: Tue, 13 Jan 2026 05:49:53 GMT  
		Size: 4.1 MB (4120697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0123600ee1708aa4702e4b25db53e6f6d7fffcc52b95f3f25fa53bdca5c2cae`  
		Last Modified: Tue, 13 Jan 2026 03:06:21 GMT  
		Size: 18.3 KB (18339 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:3e3168f6c41907775547e0272732756a9617368e01f0eb7d44bd82cd76cfb3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49198434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494a03e260c3afcea70e8537d04e62c6d112ce7d73c8eb3c10b5d063ffa09ff0`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:39:35 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 03:45:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 03:45:17 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 03:45:17 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:ddab8730b1df461111046cd88b7848f70955e854e29bbbfa3ae304f7ec801442`  
		Last Modified: Tue, 13 Jan 2026 00:42:31 GMT  
		Size: 25.5 MB (25546235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fffb91a2a42cbde13f82898cd1bae68291e1d0f1b1b989c5689ce5d9b5f245b`  
		Last Modified: Tue, 13 Jan 2026 03:45:27 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce57942866d3f30e95ff3c5d0a790e229e368762a9d8979eee2f368221cfd46`  
		Last Modified: Tue, 13 Jan 2026 03:45:28 GMT  
		Size: 23.7 MB (23651932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce82e39a4147f410be921f7fce9133b71b50949c6d1c2792f50ea05d7449a84b`  
		Last Modified: Tue, 13 Jan 2026 03:45:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f050a6e52344b5f765719b2554f60caa9e18f9455d4cb926ab2e5d601f76bd42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8ec0e2ac53e3f0085726dbc302aef82e43138d693773beb294d4fe39adf7c2`

```dockerfile
```

-	Layers:
	-	`sha256:05a3f10738f609f40667812d20ce74e056968eb1f04f2df212787c22dd530a31`  
		Last Modified: Tue, 13 Jan 2026 03:45:27 GMT  
		Size: 4.1 MB (4094686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe27341cb1432779511f2341b06a9bd9e18c00ca3d53265423888023c7168c0`  
		Last Modified: Tue, 13 Jan 2026 03:45:27 GMT  
		Size: 18.4 KB (18411 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:0315c871e5eaaaead09b74606bf1678f98486a6c5bb8fdce57f112171781a410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54280796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347c574ed7e18bcccfd682238855ba8a38da3bf88b0e9d7a0f9b788156ee61ab`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:06:32 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 03:11:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 03:11:26 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 03:11:26 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af53051f7c0168e18e9495b3b3f7b5b29edc212692b12c9f1f220600a3b9045`  
		Last Modified: Tue, 13 Jan 2026 03:11:37 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9783a4f879cc8cf2e3663a489391b99e42e27d42065033cce69a185015a5c163`  
		Last Modified: Tue, 13 Jan 2026 03:11:37 GMT  
		Size: 25.5 MB (25532012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec799bcf5183a0081b24c50f91fc1f5d05cfc21f44bdd483c2bf36b585b05a70`  
		Last Modified: Tue, 13 Jan 2026 03:11:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:41e067705f0317dba59b6b18b00d2fe32d0670dca42edc27b3ea105182088274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147d891cd4f220ed139162abab1fa1e4fb7942d50b1912b779ea75544af9e097`

```dockerfile
```

-	Layers:
	-	`sha256:968a5072d48de973f02bbd5a5de07b12d3642528c7dcafddb94f41f1ab287fee`  
		Last Modified: Tue, 13 Jan 2026 03:11:37 GMT  
		Size: 4.1 MB (4095092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a7f79e019ceb4a59e1d6562a8a6ece237823c929e93915eafdda3ef2f176305`  
		Last Modified: Tue, 13 Jan 2026 05:50:39 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:b1a4fe965134130c11ab1542621d39ef30231f1e58aee15b2cc81a3374ae0962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59166853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5e6a2d84f97a6e87790bc5e6ebb8edcb912578139e687def3fedbc19b7db54`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:30:42 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 02:36:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 02:36:03 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 02:36:03 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:fc7e12eb54e533b7d72a8c4004d7a3b7d895d07802f534ae9aa75ea08b0d8bfa`  
		Last Modified: Tue, 13 Jan 2026 00:42:38 GMT  
		Size: 31.2 MB (31191589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f144fb3ad9775e0d4e06de772ee0dae456bc8a7d6d5d0e7ab2ecf9bac8efd0`  
		Last Modified: Tue, 13 Jan 2026 02:36:14 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e894eddba9abc1c031e794eaaa0a97cd61daf63984d293ad614185de641aca40`  
		Last Modified: Tue, 13 Jan 2026 02:36:25 GMT  
		Size: 28.0 MB (27974996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca3f4b0f30b3f90063bacbad12dd2726586d8a542e6cf601ee99e67b8d3e974`  
		Last Modified: Tue, 13 Jan 2026 02:36:14 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:6bbca1eff52a5bf104cb8ff6b443f34fe002f2884cdf19b891f5589cc66b583f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f320ddfa7637c2cacd64d4d61e518e6b49fe8960c7e47b15199864dd9f6bfd`

```dockerfile
```

-	Layers:
	-	`sha256:b5e14ebf297c18a68b8b643f9fca126a19c5c11c5c68e68671fcf7c5da251cb1`  
		Last Modified: Tue, 13 Jan 2026 05:50:43 GMT  
		Size: 4.1 MB (4124979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d1f536278a4243730da6d247d81b32718d5d7df79dad1fa1cc65e8e1735a4e`  
		Last Modified: Tue, 13 Jan 2026 05:50:44 GMT  
		Size: 18.3 KB (18312 bytes)  
		MIME: application/vnd.in-toto+json
