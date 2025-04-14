## `perl:slim-threaded-bullseye`

```console
$ docker pull perl@sha256:f2602aa7a2679a6d867e95621ed1f982d1d3d09807e8f10c81b407c09d1a7090
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

### `perl:slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:09f1e6d6e08f1843830d3ce97375c139a2b497efdb5f7d9165506d45ad70dbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56389066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31c328472b61558396e5a0f837df3dd2550a07f18d325eb4e1e7b35dc4c25b3`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f7c1ba8ed5890ef19f3b024b212ce0c85b2f6b68924247475e7960cd67751a`  
		Last Modified: Mon, 14 Apr 2025 17:49:21 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4233702c97d6b13c0bff4f8427c52d34a7983ee4e1c0be418310177edd933ad1`  
		Last Modified: Mon, 14 Apr 2025 17:49:22 GMT  
		Size: 26.1 MB (26131379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2215a557ca1df1bf1eaee9b819516791ff43eb0d45c9f9d496bbc20f78d1a6f9`  
		Last Modified: Mon, 14 Apr 2025 17:49:21 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:d356fb7aaafcba8ec182475dd58d836db6215ef0d3b57dd9b80109cfcce96f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a07d05961a8b1dba9c09f7a82e089d23026725f4547ef3d34387c51bafe599`

```dockerfile
```

-	Layers:
	-	`sha256:e87eb54860548c01ceb6ec7719d09cb9cfb322b325e4bd9b4cea5c5613aa0775`  
		Last Modified: Mon, 14 Apr 2025 17:49:21 GMT  
		Size: 4.0 MB (4001084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:660102007152aa3d6d51b54a6e15ceafe73ab3f45cc8d0b3d4f44776cf3e6224`  
		Last Modified: Mon, 14 Apr 2025 17:49:21 GMT  
		Size: 18.9 KB (18949 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:472df51cd3b9151ad12ab25c061a1a8beee6e9d8c1e0d17a2435817648fb7eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48893966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c74cb65d5ad7ff4f3a7b6ce3d9a393bfd8e199daa8cd1b75ba28c2ab4f5b9bd`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde3ec66522e2a218029d1cc04e677a72d6bb051517600542282beb79f72b827`  
		Last Modified: Mon, 14 Apr 2025 18:06:55 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b1b49bac90998ad47d16ec10ac107ef79ed6174f20528d974843b552f3c539`  
		Last Modified: Mon, 14 Apr 2025 18:34:28 GMT  
		Size: 23.4 MB (23354563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cab8d018fd2fcd4f5e2f7c6283858b83b2035d904d344c3bf88c39b203432c`  
		Last Modified: Mon, 14 Apr 2025 18:34:27 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c5362c71dfa3c8642efd1e77b80e1a43ecfeea1e68bd064357e30217dae26860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9c17a229a8afd00fe84c87b695ce5a739e999a621089fe7c656b9e948d1bd9`

```dockerfile
```

-	Layers:
	-	`sha256:1951a883072a65ef933306142f39e31f77411c23fa2f58f61686b3865d416958`  
		Last Modified: Mon, 14 Apr 2025 18:34:27 GMT  
		Size: 4.0 MB (3975089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff920071ca51050a7e46c4d74e42a0de8cb170c1808cb417bc10a87e1ea1b645`  
		Last Modified: Mon, 14 Apr 2025 18:34:26 GMT  
		Size: 19.0 KB (19033 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:c01f838906390da1c211bb706be503e0f56c1678ac0046d6df9f2e7e7c7c19ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54002972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69289891eac9fe31c93e9bc32dbfc0ccad464eec39a877984f387911905f6a25`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006625dc836279637432b692810fe2538357c185cd7adcb3d1016591dfcd9b75`  
		Last Modified: Mon, 14 Apr 2025 18:00:07 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23facf8fddf4b134b5014e052a78142dc9272da1afef613548f21152948ddd0f`  
		Last Modified: Mon, 14 Apr 2025 18:21:36 GMT  
		Size: 25.3 MB (25253206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2b6b83c093844b60e72fbbd73222a6d0db33ec66361f521707456b33818397`  
		Last Modified: Mon, 14 Apr 2025 18:21:35 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:595853991d78659966304b96bf4c35bf8f576296677d32317977c6939af6cf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6126c40e2ae194cacbab3647af72a5287d866d0a46bf928167aba9261214212b`

```dockerfile
```

-	Layers:
	-	`sha256:38b66a17290fd83eeaffb587e19bf8c525efc1ae9039da5c8879f423b4f64f14`  
		Last Modified: Mon, 14 Apr 2025 18:21:35 GMT  
		Size: 4.0 MB (3975503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6ee5783c06f8e0272a49730a2a74d3808f9355ddf9019ad2966581cf78d41ae`  
		Last Modified: Mon, 14 Apr 2025 18:21:35 GMT  
		Size: 19.1 KB (19064 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:7e6042fec3ff477b990f22c5b03a5c20660d48c2e166ea58f25099479e3c19cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58874856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17d4ec77072218020dbd5feb5d7aa35dc2afff7e3d13e9395cd62301c2e7f3e`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:c7f226a3ed9e3a783e859dc8479e50da2694130147ffb4885645e02664eedbec`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 31.2 MB (31184573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04046937acca8cf0248f3d1b57ed2df45d41493838fa4bff97790bcfe56eebb0`  
		Last Modified: Mon, 14 Apr 2025 17:48:01 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d67681d104912561d197b244f1af363deaf99f3c959641da9440d6586f6eccf`  
		Last Modified: Mon, 14 Apr 2025 17:49:57 GMT  
		Size: 27.7 MB (27690016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4e510c7349523a01bfee82481479820bdb49cff400e7b1e1a49d60e0660ba1`  
		Last Modified: Mon, 14 Apr 2025 17:49:55 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:9389bda8bc36f7ed3dc3921d4b6336b1ce89ba1b5e4007d448834e5147e252f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc9fd9b79b50bf5125081689be46cbde9ede965817906e5b2d096a3b510efb6`

```dockerfile
```

-	Layers:
	-	`sha256:2aac70f822422ed7ba5d6d02e74e4246e56e4de1d0702f549b4d97ee6c10816c`  
		Last Modified: Mon, 14 Apr 2025 17:49:56 GMT  
		Size: 4.0 MB (4005293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24df4f8578c10a66a7f76807d8b6b323e1a00cef7ec32fe3428f7cabceaca2ba`  
		Last Modified: Mon, 14 Apr 2025 17:49:56 GMT  
		Size: 18.9 KB (18912 bytes)  
		MIME: application/vnd.in-toto+json
