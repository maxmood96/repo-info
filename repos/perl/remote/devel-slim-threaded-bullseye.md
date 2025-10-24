## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:cb17739c4bd3da24f3198f258157731162a7b850a4dd296ba2b5e3d36e6c214c
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
$ docker pull perl@sha256:8d7894f98081fb7491be468dd364d8213cca1e1464abf3a70553de5a4b1d5cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56506494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbb960f8d61bd07e2007f61fd6b3d997ad7aa674b32da882f438cf1b15672ab`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d648ca2b84e96fa8195965687cf75efea0fb77bde1d241ba2317d3d184d252`  
		Last Modified: Tue, 21 Oct 2025 01:54:18 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7060ba773c75ec6ac7fa2ffe201177aef6700773083066c7f723129f62f31c`  
		Last Modified: Tue, 21 Oct 2025 02:04:17 GMT  
		Size: 26.2 MB (26247862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb76844b17af71ef5e21662e637b366c25a36b2850ba1a6f8ca7a387a6255cc`  
		Last Modified: Tue, 21 Oct 2025 02:04:15 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b4fc3619aa0b0235ca552ed6ce1173e7d3a493bf1fa0da3b8e1adbf6d7679235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4139084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b5e9f81f36eca9a4b166092333f870b153a7c6cb9751748e9938ebd01e7c77`

```dockerfile
```

-	Layers:
	-	`sha256:9ea1b0b57fd25988ef9aa815c488c6ae286890ece384a1092ddfa263392bd1dd`  
		Last Modified: Tue, 21 Oct 2025 10:49:43 GMT  
		Size: 4.1 MB (4120697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a26a0bf02416e23724443e73ef2f7b294d06e5b632168ebbf65f2d079e4cfbf`  
		Last Modified: Tue, 21 Oct 2025 10:49:44 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:64d3b35362aade35bc4d3c38bd8d56eef394fbf14bd0fde346452243c6fb0d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49015923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc48287b94fb9a17f30475069d0e58681e20758c0fa1c5f4caf085c563ff9b99`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:4b897c04dec26603bcc1b01b4283220cd1ffb208f0ec4c0db9e08dab58fcfb5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 25.5 MB (25546187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15d37363d7062a7e75d13d0879b9edaf5f96dfd2c89980c923f82053c5359bc`  
		Last Modified: Tue, 21 Oct 2025 03:22:14 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f0670e4313212a4f8ec17595d46cbdc55cb774440e15928571f0bd1d876f78`  
		Last Modified: Tue, 21 Oct 2025 03:33:42 GMT  
		Size: 23.5 MB (23469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7835c600edd18e1e96752cf08664094a0b49e583ee4d0d0cad80f726dcde6f`  
		Last Modified: Tue, 21 Oct 2025 03:33:40 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:0b1fb50138ae66c40ce956f8a3ebce68a1d60169d1107aebdaad2b2f202ab7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4abd765baa85618e63ff69a813a95019e35c48847f01beae548f2977e766583`

```dockerfile
```

-	Layers:
	-	`sha256:6ff6c5bee39a3c35787539d2c5343c4c75d997d974ca775d2ffa4bc4c9f90238`  
		Last Modified: Tue, 21 Oct 2025 07:44:49 GMT  
		Size: 4.1 MB (4094686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9606c62b10a8cb0fda21309c285cdb5a5d2fc1742569213a7e9e98ae220b6f3`  
		Last Modified: Tue, 21 Oct 2025 07:44:50 GMT  
		Size: 18.5 KB (18459 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:0b02837e29e4c10c70749aa34c01682c4ff9fb78ba6644bf545b4d447fd5e030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54103800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d42acd638502b4b6ea513381c71ac82fa03854d13be61b1076b0ca9c16e5c85`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9890b57c601c9f317d759561bc639841f8bf153c1e15008be41bf0633c2fc88`  
		Last Modified: Tue, 21 Oct 2025 01:58:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d178bd7576002e1cf4b0edb53471ba13d8b788abcc9d4b2607157c1e1b35aa4`  
		Last Modified: Tue, 21 Oct 2025 02:08:59 GMT  
		Size: 25.4 MB (25355134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca72185104b50c747f6f204fbe6ed89e83e7fb03c13e065e321185903e0f6a8`  
		Last Modified: Tue, 21 Oct 2025 02:08:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:44368144b0a3960ab5e2eb2710c5f2f7f0aaf6a89776b00b0a07ce0f1ffd74c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42feaeadfe304ee141c10ae742ae1f683379c8e0dce004fa0ace9fc989934a9b`

```dockerfile
```

-	Layers:
	-	`sha256:50d3e1958a11dcf9257aaa5ad123d38b3ae8fb7b0af9b39a65ab719eaceb0abb`  
		Last Modified: Tue, 21 Oct 2025 10:49:51 GMT  
		Size: 4.1 MB (4095092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84d38b13c911175d6a26e4a2c51b37bf5e311128e6ab7b6837061ac471e325a6`  
		Last Modified: Tue, 21 Oct 2025 10:49:51 GMT  
		Size: 18.5 KB (18479 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:af8f6792ff96e24dba706d16ddb391477c99e283169d9e56ba0af2c4a9145786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59099305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52930b69d773c6ab881ec7423bf9073843bc479ec47e6b5567be19bc91f0644`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/perl
# Fri, 24 Oct 2025 07:13:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.4.tar.gz -o perl-5.43.4.tar.gz     && echo '75676cc02c1d4d6f4577f7fd953e07ab5d06f71cf4201753ab6e2b0ddb5a4931 *perl-5.43.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.4.tar.gz -C /usr/src/perl     && rm perl-5.43.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/app
# Fri, 24 Oct 2025 07:13:41 GMT
CMD ["perl5.43.4" "-de0"]
```

-	Layers:
	-	`sha256:ed9b7a4c5998c0d248e37f414fa0883c2b695df7b879c0ba096280f29fcb2660`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 31.2 MB (31191494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbe51fb9f28a5e587d9971c18545f0c76295e5e6f98c90016fb95caeba15613`  
		Last Modified: Fri, 24 Oct 2025 19:02:15 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d56a320e849dbf1497df4ed31b06510b56c3686ee1462b8a048c3af34319a2`  
		Last Modified: Fri, 24 Oct 2025 19:02:18 GMT  
		Size: 27.9 MB (27907544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87492f49085912ba3fcf2243b984f2d73f487d9ea06fd4357ec67635824b7d54`  
		Last Modified: Fri, 24 Oct 2025 19:02:15 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:3fd0d9b5854b65e74323d99a113e1e4e53b2e89df450b0df3bd252ba6802ce57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655c184f6bcec446ea368a539718080f4fb0ee1598458797cc382d233499b2a4`

```dockerfile
```

-	Layers:
	-	`sha256:337ba3fc345cb431d2e13c7b5f023503f40ea6c7cda3287b8ad5bba23c3963ad`  
		Last Modified: Fri, 24 Oct 2025 19:42:40 GMT  
		Size: 4.1 MB (4124979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94c394cb4bd7f9db5db5aa51edd9266d35f763e62c968378263e206e5a516b7e`  
		Last Modified: Fri, 24 Oct 2025 19:42:41 GMT  
		Size: 18.4 KB (18362 bytes)  
		MIME: application/vnd.in-toto+json
