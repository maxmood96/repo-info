## `perl:devel-slim-trixie`

```console
$ docker pull perl@sha256:3158e012c39700f8828bc40384073a11b5d2b446750027b0e7c96c6de7f5b45f
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

### `perl:devel-slim-trixie` - linux; amd64

```console
$ docker pull perl@sha256:4a87ce5ee6946c203bf00646b196258e26612e65773bbd9034137bb573dfec7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61942158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de9d242c0dc15c5f4119912cd88c65b048cb5ca68c4ea55902316c481b29988`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:56:19 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 03:00:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 03:00:47 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 03:00:47 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f905e955a52ec62518db071369823fb02d781903bfdedce550842cd238ccbd9`  
		Last Modified: Tue, 03 Feb 2026 03:01:01 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2126ae00a4ecc519b3389b00fbcf2cb350f45bd72debaff82d8bd7d84fea97b`  
		Last Modified: Tue, 03 Feb 2026 03:01:05 GMT  
		Size: 32.2 MB (32163292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1b40d50fdcaa967adb9744c85ec9f7a66e1cf20c0070cd39c415861a92e36d`  
		Last Modified: Tue, 03 Feb 2026 03:01:00 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:d003138c250007e644196db9a0fb0cc9593c58bc181369f201874c22b3bf1c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0b22df9f58bbc69f3938a7ec964a7db07dcdc8e482039038da6a47e825f4be`

```dockerfile
```

-	Layers:
	-	`sha256:2ddcb101bf0d77e41b198e8a95925b1497aa059516ac09432bd0b60af6d8f770`  
		Last Modified: Tue, 03 Feb 2026 03:01:01 GMT  
		Size: 4.0 MB (4009412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4093f3ded969dedf2213aee1b2f03771963274a59ee1cf35e7a45f87bccc308d`  
		Last Modified: Tue, 03 Feb 2026 03:01:01 GMT  
		Size: 19.1 KB (19127 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; arm variant v5

```console
$ docker pull perl@sha256:408043fe8504d92d878e7bf8a4b8288628ac9f2963ccd6bbb8644180524d416d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57357983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72cd5106a012ea8ed12027604566bb103c89e6fbf209e292ae9ef47ab12593f9`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:35:35 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 03:41:14 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 03:41:14 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 03:41:14 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66214ea598f46aa7067a4f707cd3bd5e6619993c5caa11704ba8310857c44684`  
		Last Modified: Tue, 03 Feb 2026 03:41:24 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8a908f11bcd2c8a2abe8a8bc304c5f61057b11d08890b236fcef331dd21304`  
		Last Modified: Tue, 03 Feb 2026 03:41:25 GMT  
		Size: 29.4 MB (29410159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cd4cfb9d34394d34880ea4079dc0ee806f5073d2018bb1cfd0cfacbe89b7b6`  
		Last Modified: Tue, 03 Feb 2026 03:41:24 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:b88ae23a81b099f23ebe78cf44696bb16bfa65523ad54a80de205167555f9701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4021681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eced0f88c31605742b23a83bb159732858426d77543b3b2395ceda27f60dfb54`

```dockerfile
```

-	Layers:
	-	`sha256:444b8189c287521bf552d06b1e09b8919a633fcc9434c6684bb9afe5e0194740`  
		Last Modified: Tue, 03 Feb 2026 03:41:25 GMT  
		Size: 4.0 MB (4002457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afbd701f7999d4c6cf62b059a0d913f1af13a62689b3eb5cca287880b8f84068`  
		Last Modified: Tue, 03 Feb 2026 03:41:24 GMT  
		Size: 19.2 KB (19224 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; arm variant v7

```console
$ docker pull perl@sha256:8e3fb9d56181deaedcb09e7abd43a497271acf88c22750e567d8eeb2f055ab44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54684263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aea8b2c9cf1215b9b84d8e1a2d6be9852c454baa6871b2fe8052138ae5b8f4`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Mon, 26 Jan 2026 21:58:54 GMT
WORKDIR /usr/src/perl
# Mon, 26 Jan 2026 22:04:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 26 Jan 2026 22:04:15 GMT
WORKDIR /usr/src/app
# Mon, 26 Jan 2026 22:04:15 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4804ae389d99a06786030d8ab0e2e79866f094525bde7d0cb5fa7bbac10688a`  
		Last Modified: Mon, 26 Jan 2026 22:04:25 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10914e0f7badcceaae482f829589f0f137d513d60bcf980c7e4ea7830b63b4a0`  
		Last Modified: Mon, 26 Jan 2026 22:04:26 GMT  
		Size: 28.5 MB (28475418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c0eed856c7b2c76abbc6453e275566a252c7e94f223435945a2cd3f6f4eae6`  
		Last Modified: Mon, 26 Jan 2026 22:04:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:4bd67bd8521280aa217130599bc064b83e92c03af1173a888ef162f1066a5f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07467c32d931dc95c744bde5860e2d1c0d7e33a9f1295b82917ece374593bff0`

```dockerfile
```

-	Layers:
	-	`sha256:5fd55c7e8be63b3f36975250c8cd13f90b99a21a7f6092f68be6476c0faed4f9`  
		Last Modified: Mon, 26 Jan 2026 22:04:25 GMT  
		Size: 4.0 MB (4001648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff640267a3127dc09fd5ab00014997107421a163d69ab0e11061638e91b1a9d2`  
		Last Modified: Mon, 26 Jan 2026 22:04:25 GMT  
		Size: 19.2 KB (19224 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:c9915544868724fea5ac5c1bf5bedaa572bf85d9bc14ca61f19e63bc5e348de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61961625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b18af924d0a351b9c2744b3145e36098562cd550c4750373ead4b547fd2bc7`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Mon, 26 Jan 2026 21:54:27 GMT
WORKDIR /usr/src/perl
# Mon, 26 Jan 2026 21:59:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 26 Jan 2026 21:59:07 GMT
WORKDIR /usr/src/app
# Mon, 26 Jan 2026 21:59:07 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08eb7cddbec1b7c31d07c691070542943b5311e0f08e74e83657b9f20e9bbb2f`  
		Last Modified: Mon, 26 Jan 2026 21:59:18 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fafeed1ee95713e1bf100d19dbe0786ebb64829b1daa68f3796772e724ab0e7`  
		Last Modified: Mon, 26 Jan 2026 21:59:19 GMT  
		Size: 31.8 MB (31827315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f2ac2ad9148f66d120db24b1fc168a85382e9471c10b913e5fc6d31cebba3d`  
		Last Modified: Mon, 26 Jan 2026 21:59:18 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:2144b1a969ede4ba02da405e37fcd14deb0b02b38e47d3d6563705e4f8422895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678208341248997fcbffd7e2e87429013e384750960b1a9e18960a04a62568ab`

```dockerfile
```

-	Layers:
	-	`sha256:f0b39763030d447f1033247aaf941cc940a8be0a13c947c015e90d28b126182b`  
		Last Modified: Mon, 26 Jan 2026 21:59:18 GMT  
		Size: 4.0 MB (4004507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2380bc1715827c7312f33fd318bd5041502618ec13d65e84348ba8038bc584`  
		Last Modified: Mon, 26 Jan 2026 21:59:18 GMT  
		Size: 19.3 KB (19256 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; ppc64le

```console
$ docker pull perl@sha256:05f726cc2ae860698068b43f7885ed1bfaf4b7ad8e4119b9cb072004ad989308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66477944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f837b744b6cd6a2d6d49275e773eb583b8b0adecdfb442036b9e78087764ed`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Mon, 26 Jan 2026 22:01:40 GMT
WORKDIR /usr/src/perl
# Mon, 26 Jan 2026 22:09:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 26 Jan 2026 22:09:20 GMT
WORKDIR /usr/src/app
# Mon, 26 Jan 2026 22:09:20 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4892f68912311db4d8a6f760096ce92822b53c261e1013ca20369a6ba601ebeb`  
		Last Modified: Mon, 26 Jan 2026 22:09:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bc9168d65e3ea0a99a50837f0e3e3bad37e2c0508d50e89460369cf7d22261`  
		Last Modified: Mon, 26 Jan 2026 22:09:50 GMT  
		Size: 32.9 MB (32882078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d131f2e50d267044fb1f39d78e00673ee888b9b0f0b9c2f4d39042c9502642`  
		Last Modified: Mon, 26 Jan 2026 22:09:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:79c26afe013ba74386756bda9fa3a7fc54949eba1c3b6988f51fd7c35ac40e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9893ee8f965aeb55750e8f0d9cc0a0471278fd46adc75dfbe16e419d0ab7aef8`

```dockerfile
```

-	Layers:
	-	`sha256:66eace378db10f8139684a3884822828eb278369ab95f1099683ca51f460d66a`  
		Last Modified: Mon, 26 Jan 2026 22:09:49 GMT  
		Size: 4.0 MB (4005424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9034fefdfa95efafa1ba161678e59d62c37df4bd749411c8ace235b3bb81ce0`  
		Last Modified: Mon, 26 Jan 2026 22:09:49 GMT  
		Size: 19.2 KB (19184 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; riscv64

```console
$ docker pull perl@sha256:72826962329a563e750c496773541125fb36c20866e70a213b9a5a6a624ee669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68260651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c115eba94284f2d1832fb71d3c1f1ed41da776aa7a3cbadf526bf234cc712c`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Mon, 26 Jan 2026 23:12:46 GMT
WORKDIR /usr/src/perl
# Tue, 27 Jan 2026 00:24:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 27 Jan 2026 00:24:22 GMT
WORKDIR /usr/src/app
# Tue, 27 Jan 2026 00:24:22 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f463bcabea6380292fff0222d6ead71b152d6fe11ea738a6f6629bd014d987`  
		Last Modified: Tue, 27 Jan 2026 00:26:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6751ffe2b8817d9db8a59a9929fad75ffea8b579afe9407013ad60691438232e`  
		Last Modified: Tue, 27 Jan 2026 00:27:05 GMT  
		Size: 40.0 MB (39988696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daca8b393e231e32519e93db31fd4c15df88fb297ebc0c371e991af029ae47f6`  
		Last Modified: Tue, 27 Jan 2026 00:26:58 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:d268e1f5336f25c916ef1e7d4bce934b716a260687949cf358db6c9c3e9db88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2842545b49587cfb18bf122f604a66d8d24010edeb5f8365d0f5013057a654f7`

```dockerfile
```

-	Layers:
	-	`sha256:aa97552ee752ddfa74ddeb4f89ee43ce70ae98ec9b5468357be048c4c92c2afe`  
		Last Modified: Tue, 27 Jan 2026 00:26:59 GMT  
		Size: 4.0 MB (3996690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:461b864ed6d55a1b93ceee1ec95b0cc58a3091192fa5d5c5f32137a530254264`  
		Last Modified: Tue, 27 Jan 2026 00:26:58 GMT  
		Size: 19.2 KB (19184 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; s390x

```console
$ docker pull perl@sha256:76cb3fd046781af8eb31ec73aba0681e3a65c06c64300d210e4e21e239bc3552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61364085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a7d8d9443849d3549245b49410fd4922c65966f204319376ef54f46f74e809`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:52:43 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 04:17:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 04:17:20 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 04:17:20 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e546a7529553e82150e83c720e4c7894370af6f94f06ad4cc06f47a36d3b4d1`  
		Last Modified: Tue, 03 Feb 2026 03:59:10 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8a9697e41736a4b6a79652321a2a236a9b6bf8a22a3324ee4a77be4d40779c`  
		Last Modified: Tue, 03 Feb 2026 04:17:37 GMT  
		Size: 31.5 MB (31525668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0820ca68ae6f4829fa31267a5a206c72787cda832a357e89748b4a946ae3fc`  
		Last Modified: Tue, 03 Feb 2026 04:17:30 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:5b97a2f1b6b2c4db39403f55c7b1fe5026be60ddfa431e3191474d0de17f6540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69599cd9593a07a6105dae321bd29450e6fde53bd28d7f8d9aa99815ed72ca7f`

```dockerfile
```

-	Layers:
	-	`sha256:4f8d0bedbb3b46bdd5c7b72f8504d8120e4a906e93d5198db258221ef82813c9`  
		Last Modified: Tue, 03 Feb 2026 04:17:36 GMT  
		Size: 4.0 MB (4001740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10dbf10b0b6150f0386c5ab22155272270ea0d612b712b1bacef2b201f3cfe09`  
		Last Modified: Tue, 03 Feb 2026 04:17:36 GMT  
		Size: 19.1 KB (19128 bytes)  
		MIME: application/vnd.in-toto+json
