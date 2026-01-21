## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:6b0476900b8012c5ead698b0cdce1e985a03e464a1dd4bd6668af36a9386d264
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
$ docker pull perl@sha256:3c4035aa7818bd44dbc111c486e95f3fd43b795c07dfb1b92b1d13eb7f322b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56626346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a041b79113f3ad4b125beb63becf5486eadf6d142ce7678625a4bf7e49412d90`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:58:00 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 03:02:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 03:02:03 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 03:02:03 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d2f3f3d2b40d4e446ac2ff2c9deba45eb958ee5778ac53219e6d015a63a90d`  
		Last Modified: Tue, 13 Jan 2026 03:02:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71cef92a1b99924fa4699757fbe1121a9de4ee50cbfb671bb23a20edc00799b`  
		Last Modified: Tue, 13 Jan 2026 03:02:22 GMT  
		Size: 26.4 MB (26367583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c9f390a73cd16344001cbf66ddbc8c530887794a65dd9378170c53d9123f75`  
		Last Modified: Tue, 13 Jan 2026 03:02:20 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:fb7090754b45724462453ca8211ad344bf9642d519b1717595978736de0507f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4138878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d133342377718e6b0f29034092783f00a9a8f7e6b805b970d512e6468bb144de`

```dockerfile
```

-	Layers:
	-	`sha256:c58077fd58d3fca6e2640af0c7ab2c6bd0e8b96846156dd3d197b7ac75b221fd`  
		Last Modified: Tue, 13 Jan 2026 05:49:04 GMT  
		Size: 4.1 MB (4120643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7339e2f166db2beb1a563fd1fc0127f9e13efafb3a9247fec74b5ed5ec60704a`  
		Last Modified: Tue, 13 Jan 2026 03:02:13 GMT  
		Size: 18.2 KB (18235 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:35363e07d68c313ff2a842a2ee09e5e86bad9b243de0719dab554d752d3be24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49165320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30453234e13f52690baf76e71f76dbc35f9312edb6173449c091c14b4a08cf6b`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:26:28 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 03:43:29 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 03:43:29 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 03:43:29 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:ddab8730b1df461111046cd88b7848f70955e854e29bbbfa3ae304f7ec801442`  
		Last Modified: Tue, 13 Jan 2026 00:42:24 GMT  
		Size: 25.5 MB (25546235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d160422cfc3436f13c67841364f339557a862f1611d72acacf42eed98ce27816`  
		Last Modified: Tue, 13 Jan 2026 03:32:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8320441a9b9d3ebec3e3ed51da9375545b7ba1705526750c87ccd01c822736f2`  
		Last Modified: Tue, 13 Jan 2026 03:43:40 GMT  
		Size: 23.6 MB (23618818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4bfeae9ba74815cc9f3bfc843c2c878e0e517bd05333d5265795a4fbd92578`  
		Last Modified: Tue, 13 Jan 2026 03:43:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:8d43152ba4398b94916f97c6a4652e4fdf7fccb230e66793c47c94bea34a80c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1ca7f2d4d4dea5c257aa561ff35afcc194ea4400b66505a6887e7e0e0d51b1`

```dockerfile
```

-	Layers:
	-	`sha256:dab1579db199588c5c95b995107be9131f469afa803237205be359e20b4ea60e`  
		Last Modified: Tue, 13 Jan 2026 05:49:16 GMT  
		Size: 4.1 MB (4094632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb8b886961ab64bd1c629f466747d8fbb64247fc75be6c7c6c0e2b8d1a0937f`  
		Last Modified: Tue, 13 Jan 2026 03:43:40 GMT  
		Size: 18.3 KB (18308 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:4f099d7be6a02ae94994dbe64b7c4b30b5831169bf6bb3cf0d3a3db0fc548e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54249928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e0b65dd5eb05bfb8402f3123f16c98db06416eef8e48aee0a7bcb0fc9cc6f5`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:03:32 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 03:07:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 03:07:56 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 03:07:56 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f405a79a168a67e757ee5755efed1e5770d313e19fb515242c33da3a7f42eaf`  
		Last Modified: Tue, 13 Jan 2026 03:08:14 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df1d78709e8922a3b0d42dec077941600ce0f18efb91474cdf144182cb61143`  
		Last Modified: Tue, 13 Jan 2026 03:08:16 GMT  
		Size: 25.5 MB (25501144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3869e27c7dab6be562d5c4f1c83c377259c2e828015b16f89e2bd99d9d44b8aa`  
		Last Modified: Tue, 13 Jan 2026 03:08:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:49d0696a64433a51ea2ca32a69a10e84c04e7b294db822091db7d0f4704e3666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558cb5b07f506288237caea2a8cc398278c4129ebd41010f80c166f562963a6b`

```dockerfile
```

-	Layers:
	-	`sha256:5ab6be1d00ae922a3d3fccd832ca81a3e779882b952569665c2b29d6bbc84d33`  
		Last Modified: Tue, 13 Jan 2026 05:49:22 GMT  
		Size: 4.1 MB (4095038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af81978d0f0e217dfaadf86abf4370025ac8aba37b574e9943105140db51d439`  
		Last Modified: Tue, 13 Jan 2026 03:08:07 GMT  
		Size: 18.3 KB (18329 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:516702c5232426a2e9a0c472f0b0febbfb1dccd518d613b7a6dad8663095eea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59064154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ec5260415d168cdee85dfd3d888ec59af14dba67a0e5f992d6ac2895c7ab0b`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:16:24 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 02:33:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 02:33:07 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 02:33:07 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:fc7e12eb54e533b7d72a8c4004d7a3b7d895d07802f534ae9aa75ea08b0d8bfa`  
		Last Modified: Tue, 13 Jan 2026 00:42:38 GMT  
		Size: 31.2 MB (31191589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955635ae63c78365a037bb70ce0f0cf4324bcbf3fa5c65d66ee78d91592128b`  
		Last Modified: Tue, 13 Jan 2026 02:21:28 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f8ca3aa6489fd375166343f82fb67c0ea741f5cf4d0321b7bf4881be52fdc3`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
		Size: 27.9 MB (27872299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eab419f3e5f56031312409a7d35034f36518fba146f14e6421e997a9576bc76`  
		Last Modified: Tue, 13 Jan 2026 02:33:23 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ffd355284d688b08eecf70f46f7a620852c6fe3e4e0fb47a50c46742a2917b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ae9fbf4ee2a2bccb26317f832e6bb4b0b108ed6adce40343e17d41b1d80034`

```dockerfile
```

-	Layers:
	-	`sha256:6919a771dcbaa5a077fdcd8430a853ea92b37fd0963c3a176d8a343bc8ace020`  
		Last Modified: Tue, 13 Jan 2026 05:49:27 GMT  
		Size: 4.1 MB (4124925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65ec0d76a05001cb10b25eb033c6e470a8971df4c83b76aeb4456f9638d6f9ea`  
		Last Modified: Tue, 13 Jan 2026 02:33:17 GMT  
		Size: 18.2 KB (18211 bytes)  
		MIME: application/vnd.in-toto+json
