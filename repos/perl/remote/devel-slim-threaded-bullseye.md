## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:915cc0951574dc0cd09bd732dff9efd1573653b7c7fc4946eb74042da4e29f7b
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
$ docker pull perl@sha256:be346783bb7b4a9f421d232bc0ba3c4327ca5c2b54469c9613a2d4ff6b372dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56250232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95160008b65ba292d24ca7790e26cb3457832fb4a69cc33b4db4c1ab83208ff`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Thu, 21 Nov 2024 11:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c68b0611a3d51caeb0e45f8fe5c217cc8b2d3201c7040ddc6f38949e858a88`  
		Last Modified: Wed, 15 Jan 2025 11:05:55 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fe1cdd98cd1e1bca8052e9394805d94d31efa3169e4a9e8af81c3445bda4fa`  
		Last Modified: Wed, 15 Jan 2025 11:05:59 GMT  
		Size: 26.0 MB (25997300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710d25fa65d42f37fd8c3063899ea90eeef6215f400aa1c1d50633021ec17460`  
		Last Modified: Tue, 14 Jan 2025 02:48:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:d5faa9037b7601d668fdd059fab36e495ec5963c4409c7fabc763f7b6864da0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584011d418279661e23eb3670245e216365f02e8fdf19009ba0d2e295d7af87a`

```dockerfile
```

-	Layers:
	-	`sha256:ac448b1f8f150466be59c5e83de08595d69955c511edba8b299708050eb1fa73`  
		Last Modified: Tue, 14 Jan 2025 02:48:28 GMT  
		Size: 4.0 MB (3998508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b6160f04951316a93b166401655f5ed9e747000202d5e6a62a11a147eb34bb`  
		Last Modified: Tue, 14 Jan 2025 02:48:28 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:9e2afd4895bdd4637b04751853a7e02fe6d0ee0397a861d7b9335052fd34d752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48749678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626f15bfbbb630a8d96d5c396297ee50e00d7f0d1ff97c72b131173efe053443`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Thu, 21 Nov 2024 11:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
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
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214065b4e5f9c95928990371dca71ed988f7f4c799cb8289e91a6fdca29943b1`  
		Last Modified: Tue, 14 Jan 2025 09:45:33 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df31c8a3ef3006894371729457a50294a48ca23e8ac2142580cae2aecd02fa54`  
		Last Modified: Tue, 14 Jan 2025 11:08:58 GMT  
		Size: 23.2 MB (23215453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfc8ed7a98f748feec2f877c276a2a380dc459def2e95bcaf888fadd9fbf1a2`  
		Last Modified: Tue, 14 Jan 2025 11:08:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c20c269ab7b5005d0b32df89f5a4c736cac9aee6862e1847eb895b030ab9523d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f0989638d3da7b781a65074015a561bbc907c846396d1747bbed773425957c`

```dockerfile
```

-	Layers:
	-	`sha256:b65a1ce45ff79d944d532568fde6475c5bad1898c9ba60f4c139476d89c8678d`  
		Last Modified: Tue, 14 Jan 2025 11:08:57 GMT  
		Size: 4.0 MB (3972497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d07552a513801e4f09df344432fbe536a5b4ef2d1da1de1392431269d0c7c116`  
		Last Modified: Tue, 14 Jan 2025 11:08:56 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:1bed658c512f435c1aeafb5c205d104a5592146cce26fc68e7f78200e8990dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53859163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953d436ac5444529120710814f675fe8fec1887c595dc9dc8d92474bacf61c28`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Thu, 21 Nov 2024 11:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 20:33:33 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8d077d4368be311435a6be03b331522adcaa3efcc3843cedf41fc616658945`  
		Last Modified: Wed, 15 Jan 2025 01:59:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f68c029f9a73efcf74c5a5b0421c5fb474ed150496ffb4f2338b046d7fdc97`  
		Last Modified: Tue, 14 Jan 2025 09:10:12 GMT  
		Size: 25.1 MB (25113983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3675854636b7db6a935b66b297c27e0dd753093645d26be98047fbd957579966`  
		Last Modified: Tue, 14 Jan 2025 09:10:11 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:fe6a4dd9f4be8147d8630c7829c9cd55e21284552bb21a252389895897fa006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c81891307004df9a346c32b55e4a94140f04732452dcf625f726aef7f8c989`

```dockerfile
```

-	Layers:
	-	`sha256:df4c1fd23bd18ebe5a77cd621598f07ea9f8f8348a87521b6f307b0b59fa09a7`  
		Last Modified: Tue, 14 Jan 2025 09:10:12 GMT  
		Size: 4.0 MB (3972903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25798a4a6311ee38a4fc5dec71eb09d3f82a571527fae87a46c9eee6138af58a`  
		Last Modified: Tue, 14 Jan 2025 09:10:11 GMT  
		Size: 18.5 KB (18459 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:e91d70c7d220558de4b2db00c14a39e00c1ec5099de2b0e7980ed1653554cc2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58716582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9268b6436857f9e20b26a929b0f81592b97192210a6afe7b9bb112b7c6cc75`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Thu, 21 Nov 2024 11:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
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
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 20:37:11 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9b409200ef5b07f501c6660e5697e7d58a3d33434d0a0da87e383a080baf63`  
		Last Modified: Tue, 14 Jan 2025 02:43:34 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d8dbaf41d7523eb6964ce6c11c10ec0e3c40be949732520c652f5199415e6d`  
		Last Modified: Tue, 14 Jan 2025 02:43:35 GMT  
		Size: 27.5 MB (27537287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805df5f45418d3f9ef2703d5d9d904c44ff0bf4c3c8010565a6734eafb7f83f1`  
		Last Modified: Tue, 14 Jan 2025 02:43:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:32e0e7eae7da5bc9545c25ac6078abc5a81d1146024050086e2c56aa4f73b88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4021066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214a15effc53ad5ff531a467d6036410bc7ce648956f4714d515903c6a14cb82`

```dockerfile
```

-	Layers:
	-	`sha256:7241afb539187150c1e425bb49434c50f268cc976e69f7083b01ffc1f40b8d63`  
		Last Modified: Tue, 14 Jan 2025 02:43:34 GMT  
		Size: 4.0 MB (4002727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e96d03a396bfcf3b1728a9642ce511dbd875fab6053584730d08d8d0a87f88e`  
		Last Modified: Tue, 14 Jan 2025 02:43:34 GMT  
		Size: 18.3 KB (18339 bytes)  
		MIME: application/vnd.in-toto+json
