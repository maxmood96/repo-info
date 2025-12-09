## `perl:devel-slim-bookworm`

```console
$ docker pull perl@sha256:1541ffd6d1c9408ae046abdff0de94b95c9a55b7ff2d9e99150053649215a280
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
$ docker pull perl@sha256:c9862e18ff05453b14c87240a84261dc824c592fb2384528a6f692a90660cf1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58586680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba16e7c1565c0fc6a87b6c0e7b0ab5ab7b949a8f1348f9c84ae594c082b206d9`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:24:47 GMT
WORKDIR /usr/src/perl
# Mon, 08 Dec 2025 23:29:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 08 Dec 2025 23:29:17 GMT
WORKDIR /usr/src/app
# Mon, 08 Dec 2025 23:29:17 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb910aba604b1020f4778412728bedfcde5fed1b7c39e9ae7d87fab1bb169db`  
		Last Modified: Mon, 08 Dec 2025 23:29:34 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d8f76d48440eb37f7d7e1a37d5b92ad7c1bec611a7c0ddc2fa476c6c046193`  
		Last Modified: Mon, 08 Dec 2025 23:29:37 GMT  
		Size: 30.4 MB (30357996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25451e0e9dbf72c444f76cff30f5a9e3524ab8bec10400b963db769f9b90520`  
		Last Modified: Mon, 08 Dec 2025 23:29:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:0d889c98dddb9422feebb58cac8eb36609bc26b2ee1b2d47143d54d829be39e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3957573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffca4378d0c2c76aa9c9738666b4591db5c9ffe2e800efb6711ed80f6c6f81a`

```dockerfile
```

-	Layers:
	-	`sha256:231040376c498f65c96fb32bce3055a3dfaaa7740f99921fce57130fedbf20e3`  
		Last Modified: Tue, 09 Dec 2025 02:48:39 GMT  
		Size: 3.9 MB (3939330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11062b25ed30f3edd8371d642febe5d37b1c95f9dd91d6e5489ebb5a22940f1a`  
		Last Modified: Tue, 09 Dec 2025 02:48:40 GMT  
		Size: 18.2 KB (18243 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:29d68a91f2760b429b4f2460d57cdf53630651b0c1ae5730d24db9466f3b7934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53181676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b54a33e70cbff2787950123b9fe9a2e4e61d156fe3e94342f0be90f77bc93a`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:08:34 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 00:14:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 00:14:21 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 00:14:21 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:20ca79728ab9e4eb574872cf271bd965c51cf4e8ac84660ef17b281a3aeb750e`  
		Last Modified: Mon, 08 Dec 2025 22:16:26 GMT  
		Size: 25.8 MB (25757588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98740e04ac46d2d56b0ef8792b70cb63695c862923c116086a70a9da193ee5cd`  
		Last Modified: Tue, 09 Dec 2025 00:14:37 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1222b5743a589beb55530c5a0144e0efb1d8d91792c3bfc1bed3c863bc46ec6`  
		Last Modified: Tue, 09 Dec 2025 00:14:41 GMT  
		Size: 27.4 MB (27423823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717d344c3cf7037f87ecaacc4c29c55a4baf4dd7c99c580f823ad4ad9ed66b69`  
		Last Modified: Tue, 09 Dec 2025 00:14:38 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:393e7d76f28a8fb82474a2db1e7c2e73c9a203e5176e1e9ba7719eddbe1e57ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc548b35faada9bc4c506a53bb37c8a458e844cb288a206d49074342eb838958`

```dockerfile
```

-	Layers:
	-	`sha256:8acc1d8c962d60f8d51bf410796dde0d24d8d3dee312e09bd6344b34b2a9d8de`  
		Last Modified: Tue, 09 Dec 2025 02:48:46 GMT  
		Size: 3.9 MB (3910181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d52595e19970b70ba41c860f247a4913d76ccc37034723757e3b635ec3848c0`  
		Last Modified: Tue, 09 Dec 2025 02:48:47 GMT  
		Size: 18.3 KB (18316 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:9f9348666302db4376ff39493141e0ff71ade4064b89a012c83adcd4e76cbd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50444774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2c77c4d89e47b60fd0066c824a9126b87f5330bf2a97a8668ad8f90d5a0a1f`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:47:31 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 00:53:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 00:53:02 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 00:53:02 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe2a43b9f8ec2f051ec3eeda8fba04c3adf41075c145220531c75e5386d234`  
		Last Modified: Tue, 09 Dec 2025 00:53:19 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c0c676f4d8dab7c630700150d330bbf4c311c17a0fec04730f81c63e70af43`  
		Last Modified: Tue, 09 Dec 2025 00:53:20 GMT  
		Size: 26.5 MB (26510487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d419277f3e3d206c7064ff9304a2d778bcb151184fad8631f0aeb6560886b`  
		Last Modified: Tue, 09 Dec 2025 00:53:19 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:4ab830a00c720cfa1aef23f841fc3f0426082b98cba389346c9519c7cde71c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c123fddc5fcdde133c0c3f7b3059fdb7a8cdcfd234089e2c923f1153e09491`

```dockerfile
```

-	Layers:
	-	`sha256:8c618921a9d3d63af19a9dcd73b7024bf4c5c53eb1992ad60c784e987dfe6b88`  
		Last Modified: Tue, 09 Dec 2025 02:48:51 GMT  
		Size: 3.9 MB (3909406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c198a2a9071b6316b305f2b90c293ae920d82b8f357c89b064e435a9dafc85f8`  
		Last Modified: Tue, 09 Dec 2025 02:48:52 GMT  
		Size: 18.3 KB (18316 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:fbde70c2f801dbe37f8a7bdec583953aff252d4698b0fe25abff7832cec23b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57310220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff812f67e6ca9bd8f6606d82ab88ddde5d475126be2b3cbc188a27b597f116d3`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:21:26 GMT
WORKDIR /usr/src/perl
# Mon, 08 Dec 2025 23:36:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 08 Dec 2025 23:36:34 GMT
WORKDIR /usr/src/app
# Mon, 08 Dec 2025 23:36:34 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57925dd307bf32b83800dc2194f86c8d4ca01ae2ada8782acbd23c3b6294a360`  
		Last Modified: Mon, 08 Dec 2025 23:26:18 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb37b38b30b32b33d75f3430b192a1b253726f168172cfddf911fd44b84f7f8`  
		Last Modified: Mon, 08 Dec 2025 23:36:52 GMT  
		Size: 29.2 MB (29207726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09692b6f42ba0bd0ac6bb1bc698fd5a7c98952ef1da158fce265e686777209b1`  
		Last Modified: Mon, 08 Dec 2025 23:36:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:1ad19bfdacb2b51c76491063d7b4c14fa4f8880ffeb20befd8ab41d4de028cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a3d2d888593caf1e0da053f0a314d318107a40eb51aa51107bbbe3577d93a`

```dockerfile
```

-	Layers:
	-	`sha256:96e3974a38089d099f927d532c84ab816e7316363084cb61707e2c7eb9786d93`  
		Last Modified: Tue, 09 Dec 2025 02:50:37 GMT  
		Size: 3.9 MB (3910567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c8c4517a54aa1886ff75aca41fd41ebbca379a7efd5064fd42f93e6618c6b8a`  
		Last Modified: Tue, 09 Dec 2025 02:50:38 GMT  
		Size: 18.3 KB (18336 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; 386

```console
$ docker pull perl@sha256:261c6c6564566ae316f33d92f79b388c317a748420db0d6fa9ecce4255cb0a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58684136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14a3b0ddc0abcbd8baa63dbf26e81bd8085b7340ee988ae9cf2497680318676`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:22:04 GMT
WORKDIR /usr/src/perl
# Mon, 08 Dec 2025 23:27:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 08 Dec 2025 23:27:01 GMT
WORKDIR /usr/src/app
# Mon, 08 Dec 2025 23:27:01 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f0264dad838f16cb9685d6359734c8de8e2dad650c7d5f6cdc3bb4bafb746f`  
		Last Modified: Mon, 08 Dec 2025 23:27:17 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efebe7a384bccccf1024cedb0a36f3247dc18d7cad8be18f1305efcedf86781`  
		Last Modified: Mon, 08 Dec 2025 23:27:20 GMT  
		Size: 29.5 MB (29474140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e97a410d93f208b94270a937bbc19479de125d52529dc07cb929f552ab41ee1`  
		Last Modified: Mon, 08 Dec 2025 23:27:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:dfbcd907006e24e02558718af04e74864606cee9f9be6f16739841e76c0113aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befbdfb70a3a10ecbd3102c7f4427a2d7a2b7ad56fd32c28960ac4686733be04`

```dockerfile
```

-	Layers:
	-	`sha256:b3f00a9a6aa7cf7899fd0a2e770ffc9c5c86915713cfbdff5dfaf85ae2cec0b3`  
		Last Modified: Tue, 09 Dec 2025 02:49:02 GMT  
		Size: 3.9 MB (3933272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8954309b52aca9aa3f30c9f26ea83c89e39331725012c6faa77bfbe171e97ec`  
		Last Modified: Tue, 09 Dec 2025 02:49:03 GMT  
		Size: 18.2 KB (18216 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:d793fe50eced47444b741b12689e1e998754f8a491aae712479fbb72be35d3f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57026818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e488e5bdb332c10a7498d7a66fdbb46fbae792088eb28f961cc628cd0c7183`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:03:03 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 19:10:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 19:10:40 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 19:10:40 GMT
CMD ["perl5.43.5" "-de0"]
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
	-	`sha256:72866e471c72346f2726f19a6ebe8ce764950ae10e6b9f322827916bf4065dd2`  
		Last Modified: Tue, 09 Dec 2025 19:11:36 GMT  
		Size: 28.5 MB (28512749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7f1d2db31ba828b5361a373e2522787c975f5e8d01a88513bf3f4f03e87cf`  
		Last Modified: Tue, 09 Dec 2025 19:11:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:359ae118d3bc473b3627de4391ed6b93fd0188cee14a14e0b1fa3de92a8d7516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 KB (18086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261657e92378f4144dcec1ca7c78e66bef03dcc8b321c196c1c08a7bd5bb8192`

```dockerfile
```

-	Layers:
	-	`sha256:1c78b25bce499af374f95e4fd32174912e7e71b21fe8e28c0cd8e3252ffb979a`  
		Last Modified: Tue, 09 Dec 2025 20:40:05 GMT  
		Size: 18.1 KB (18086 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:9bedb7608cb28b5a1ec1d5da6f3f3c1bcf9ed4e741a5c619b8d4f8c339fab5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63213926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6222b68730f5c1afffa63d2c13963849f382136a2e0e45d41d270dd2e2b45109`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 14:26:45 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 14:58:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 14:58:43 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 14:58:43 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d408681ffbf8714eb9d0b7cb46b1ab1421ad6bcb6c6d4bed823f2b87ff6b9e`  
		Last Modified: Tue, 09 Dec 2025 14:35:07 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ec3b027c0c88a3cfab325ad1a17c31fb29876787318cb3c92ecb9733f47310`  
		Last Modified: Tue, 09 Dec 2025 14:59:33 GMT  
		Size: 31.1 MB (31144815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433322e18729da5f95fd5ee0c2bf3607a3d087341603baf0980c1493371478de`  
		Last Modified: Tue, 09 Dec 2025 14:59:30 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:86026ee9da1663849c80cb389348eb5cdf2546ee7593ce5496b477b7e064c4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3943540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f2a19a310d8df028cccc04fe833c5141bb24d9356a2b47d9a2b57fd020314a`

```dockerfile
```

-	Layers:
	-	`sha256:b51aff086e7543998259c3a55e94346b1ba5df34e5fea4f0c78cb93141b9181e`  
		Last Modified: Tue, 09 Dec 2025 17:40:52 GMT  
		Size: 3.9 MB (3925258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea71a2e7aa2cefe0c93f4c8566a46b875ec85e4bc0e0651128b6299c7bd59ca6`  
		Last Modified: Tue, 09 Dec 2025 17:40:53 GMT  
		Size: 18.3 KB (18282 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:882198439b1c352c076ef94db8213490edb5d572cd6d8fe833c6813efb536995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55792140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd1a6c7f17678dca7dcb61e7e281cee3d336d0c56de1d5c0d4d4a407d7b6fff`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:20:06 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 00:42:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 00:42:34 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 00:42:34 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab0af3556c89b1de205bf1fb947bbd5199d2fcca38b366b34b8af6975fcf29a`  
		Last Modified: Tue, 09 Dec 2025 00:26:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c3e5f883532b3549e928a2fd61d4fbae2ace14d5fc8523657a57eac39262f2`  
		Last Modified: Tue, 09 Dec 2025 00:42:59 GMT  
		Size: 28.9 MB (28907444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e62ad2b5ac90004d006a673c33274bb7fde2e8367e8c1ed22dc1265dd3cb16`  
		Last Modified: Tue, 09 Dec 2025 00:42:57 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d85ecfe6aa607148fba3202ba0685e1e3ea191d9aa5867b4201efcfa8368e07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11048d7ca6d62d6b482751d118dec3e1e0e0b98cfadc4641f82bed3fe2dc57f1`

```dockerfile
```

-	Layers:
	-	`sha256:3f64b0a8f2c42ad6bec3e5f6423028352615c3a3a68f6f85d17ccd4c71f12575`  
		Last Modified: Tue, 09 Dec 2025 02:49:13 GMT  
		Size: 3.9 MB (3924603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc627fce7ad1a94f9505b19f348509f10e2633c42a4492db2970e80494daf01b`  
		Last Modified: Tue, 09 Dec 2025 02:49:14 GMT  
		Size: 18.2 KB (18243 bytes)  
		MIME: application/vnd.in-toto+json
