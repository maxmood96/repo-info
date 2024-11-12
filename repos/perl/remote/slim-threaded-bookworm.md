## `perl:slim-threaded-bookworm`

```console
$ docker pull perl@sha256:6b58f53a101a93551c4ea6f9a5deb6da64f27f5b98560b0c585f5ebeceb560bd
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

### `perl:slim-threaded-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:5970097f5a55534e08d0a7f574eeb1892260dfd2b91832fffc640ee79a710f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59331464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adebfcba3638fb7350c5c597e1e93740f08023aa85cdbd1dd6008e86afa2e0c4`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8281ea78d717eb092c72dd268ee2ecc358035ece34a5db0b6aef402a470945f5`  
		Last Modified: Tue, 12 Nov 2024 02:47:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766f56d614dbdfd857ba652f9984fafcc399c212431aeafc861bf7c0ab8e5cf7`  
		Last Modified: Tue, 12 Nov 2024 02:48:43 GMT  
		Size: 30.2 MB (30203204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a81b4b6060b587472be325fb18f01494fe7f94033bfcfbd94508a664cdde4e`  
		Last Modified: Tue, 12 Nov 2024 02:48:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:0af71c09b598611504950571158ce22b17dab4fc16a2512e8811215b4889651f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4a5ede2145b9c773900255baf3183d2869949a46211c9e31872cdad4306d3e`

```dockerfile
```

-	Layers:
	-	`sha256:9ba3e23510d7f21a40ff1424b7c6d069c3c4cb7a41031c97669a15ad0110cd6f`  
		Last Modified: Tue, 12 Nov 2024 02:48:42 GMT  
		Size: 3.8 MB (3815361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20ce58e5f48e35b5226f6760572a33446fbc5a92632bf73624bf6b171b3f4a4`  
		Last Modified: Tue, 12 Nov 2024 02:48:42 GMT  
		Size: 20.5 KB (20536 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:fcfcbea4dfcfc75dff6f1d3b7ae620f870ea368e662699eb787176ab5899ad7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54114338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4460aa5c74c4dea0669239ab59918698179f807ea5d7b67a05bee58a2db04444`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04209475e978f93a62a76f714523f214b85f644ce8192912158891b495d96f3`  
		Last Modified: Tue, 12 Nov 2024 06:57:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0780224adebebf775ee91b43e26bbe224ba7c38798dffbac1b5fd74548b43abf`  
		Last Modified: Tue, 12 Nov 2024 07:09:13 GMT  
		Size: 27.2 MB (27224013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919613a40754719c18633ff0b95b50dd6d60f3d57cbb89170dcd20f491389871`  
		Last Modified: Tue, 12 Nov 2024 07:09:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:4bc05d5411f24a07fdd484ade536126bb13be1cd44e60905d160195b93aba032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3806577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a180a9f75de612aa42f004c626fa2e76a4615a0cae2abfd6e610a4bacbdf4c`

```dockerfile
```

-	Layers:
	-	`sha256:3c1873daf564bda05bf173a5107897306828420a5c093600f120b7f49fcba0d2`  
		Last Modified: Tue, 12 Nov 2024 07:09:12 GMT  
		Size: 3.8 MB (3785917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:680abcd35fd3172fd1de3ca406db5db16f584e08a793172536edd1a91d3a00f2`  
		Last Modified: Tue, 12 Nov 2024 07:09:12 GMT  
		Size: 20.7 KB (20660 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:2a82584022bfc5b4697ee8541da9efdf4ba4279c972452005779cbd98e11806d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51023370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a710ea54328f61a080ad5f88a16dfee69c30063bfb668b181cec1f5075f2bcd0`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 20 Sep 2024 18:57:44 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["bash"]
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb9475168dc9ca57175b1b4be56751886989d3eb029c21f9fb85f4ed1751650`  
		Last Modified: Thu, 17 Oct 2024 15:06:29 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6434b940d0b05e1904a3ffd71180329a678ed7baab9f787bf13e3d90ca1d7229`  
		Last Modified: Thu, 17 Oct 2024 15:26:59 GMT  
		Size: 26.3 MB (26304906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f27272b091d9cc1943695cd28f82aaec9a100d185dcd02a032bb60702858ca`  
		Last Modified: Thu, 17 Oct 2024 15:26:58 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:fcaa4f6d952596a389e6b70fe8946f1f89d247677b9e7574cbb3b369f7145be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f485b893345974d07fdb7cf49fdd4697aa1ea76d20fd7dbb65c846ae8eaad8f`

```dockerfile
```

-	Layers:
	-	`sha256:ba7d1519647767c493dd07c56682fb36820f5e914ef038efdfb9809dcbec3907`  
		Last Modified: Thu, 17 Oct 2024 15:26:58 GMT  
		Size: 3.8 MB (3770093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a87181d36c79a067650a4c6a04f280fce98e1d1c19b2fcff2591e83ad47447`  
		Last Modified: Thu, 17 Oct 2024 15:26:58 GMT  
		Size: 20.5 KB (20486 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:6aa272cb3aa40fbeacfcb62c2480ceac088cf67f02e87063c7647d4e191182df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58145765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf673278fe403fef660db4700a24b0f40b8ae50c02e7d00eb4e6362711bec53`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 20 Sep 2024 18:57:44 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["bash"]
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e0438a6dc8ce9271e707806179b7fc30232d02cfdc0006118b01bfcc8088cf`  
		Last Modified: Thu, 17 Oct 2024 14:10:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df08753dfaa9492cbdebb2132fa75db0339eae43efa251b4de37325cfd94f46d`  
		Last Modified: Thu, 17 Oct 2024 14:33:40 GMT  
		Size: 29.0 MB (28989159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79481e25931a29f37a36b388c05d515d547aec10db0edda592f72aba09ba1a4f`  
		Last Modified: Thu, 17 Oct 2024 14:33:39 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:16d12a6bd71f23729cafd87fae314ca1042d2402cc2fcef1f8178bf14e7c2a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3791825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dfc680d416b85918fa2a78160bf3c23c02cbcaf2e9ee96c8183b1133bc2806`

```dockerfile
```

-	Layers:
	-	`sha256:0917a210b034b0c6cc5c176b73f9107aa4017bdae22d07c571d17e877ff1bb67`  
		Last Modified: Thu, 17 Oct 2024 14:33:39 GMT  
		Size: 3.8 MB (3771287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9cf8b8505da63ab715ff8f0602c14c4a3eb6be3c01d06914990315f37c6679e`  
		Last Modified: Thu, 17 Oct 2024 14:33:39 GMT  
		Size: 20.5 KB (20538 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:b5d0cc69326804e11cfaeb2063ed38ed91a8b728fab0f2ed45645aa73a07d613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59497890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3044ce198ec8e7855f8cb42545d9484e9f778f9ab663eb18a77d9e82d9d2b87`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e256f9e231d50976241dc312aab6bd77c3043181020ba9db6eb6623203fa3853`  
		Last Modified: Tue, 12 Nov 2024 02:49:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f179a9705c34ae132612af8a261c7cf5edc92093775e7fcbe41e29e2117b127`  
		Last Modified: Tue, 12 Nov 2024 02:49:49 GMT  
		Size: 29.4 MB (29352172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8e739a99743cff04769c5af055a8a760945750c5fec31055394088b131fb8e`  
		Last Modified: Tue, 12 Nov 2024 02:49:48 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:b197c0cea5e1b0186dcdc2a480dd75a33753c083609a39b1cede09d135040685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3829675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d847681714def3b53d1210c78c45e0e086db07b68dedd1f54c1ab9e755ef8ca5`

```dockerfile
```

-	Layers:
	-	`sha256:b69ac81f0ebe3a1d96bd17f348f8cf128ea7da524e8f91dd6fe2d2963142d4c1`  
		Last Modified: Tue, 12 Nov 2024 02:49:48 GMT  
		Size: 3.8 MB (3809201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a543ef24b6ea52761485d4dcb83e5b7dca9cc9560ad9e32823eead90e69bd0db`  
		Last Modified: Tue, 12 Nov 2024 02:49:48 GMT  
		Size: 20.5 KB (20474 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:e138f0eeae642d1d02f36ae382d8319b4b25e891abc901fb3f6e0e7f75c6d204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57468266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20514f09189ec2b20390019785d61ecbbe7e4e679447a20745f32a5fa8b1b17`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 20 Sep 2024 18:57:44 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["bash"]
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bc152ccb63abe4a025a92e16e303ad6eb5e2e6cd356d2ee0539ed4d80f7933`  
		Last Modified: Thu, 17 Oct 2024 19:27:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1d0e16e90f634d77dcf5c1930f85105be7e3b30066c1a6fe02e28af8436fe9`  
		Last Modified: Thu, 17 Oct 2024 20:24:42 GMT  
		Size: 28.3 MB (28343221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb96521bb97c780d72bba3944e314de8e5e0c6dfe25f4d4f0815a08f03677e`  
		Last Modified: Thu, 17 Oct 2024 20:24:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:667f39b017f0997d8b142218fdbaee5a7997ef81e8de4abd6fd2b686c8163b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 KB (20259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c036b5c19b0ae51ddc3de651fd7181fa2682a3003d05cc72e6f93f53750909c9`

```dockerfile
```

-	Layers:
	-	`sha256:2178b360edeb4c0de69322e69517bb94db35211fc47b76a61e9441c7a99ac067`  
		Last Modified: Thu, 17 Oct 2024 20:24:39 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:b7e2ca290810c5994c6394a480c8a1adcf50a5f092cdc1b23d43d9ca856c2bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64136617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c179ddf65bf1d07cda08f49fd927ca69c1d260d8a0a958c631b0d7aa222288c`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 20 Sep 2024 18:57:44 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["bash"]
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07382dc16102e0d5ea7e6b5fa161a31a09b5e83ccdfe717585454dda12b7c438`  
		Last Modified: Thu, 17 Oct 2024 09:28:31 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a5fd618422be8e3da55d699018d7be2e3147cfa216efcfc0d4873ea5c7674`  
		Last Modified: Thu, 17 Oct 2024 09:42:26 GMT  
		Size: 31.0 MB (31014152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd342a53d7841503b372384b87d51cfc69775090a3f92147dc4dee7ac751b26`  
		Last Modified: Thu, 17 Oct 2024 09:42:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:ba4f73745099eb3a2e7a3286786137e6ace05faae9886a89a592d40cd75a5b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3806251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91e366c5b8238d2e43b7d997bf60ca54fd3ae91726bb102d50927d92c58de34`

```dockerfile
```

-	Layers:
	-	`sha256:54d701fc994ee70ab18f26c9a4e017658002efc6c1e80b01e74bd95bc3c37bd2`  
		Last Modified: Thu, 17 Oct 2024 09:42:25 GMT  
		Size: 3.8 MB (3785809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973d7a8d028f099af2d10ed3b0db14bd02b6e0b6ebed7473bbb2cc4142376732`  
		Last Modified: Thu, 17 Oct 2024 09:42:24 GMT  
		Size: 20.4 KB (20442 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:a8e0e06870a8a50a4751feedba6a85dabf9350243e379f5b201df3cdd4d3cc0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56204640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97a94a1f4c2a844947eda7de9859fc050636d279a22259ab9e94636e9ab972f`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 20 Sep 2024 18:57:44 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["bash"]
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0be519b34739c08c1547bd26ec85569d26132ac024a4d7c779a15464407e321`  
		Last Modified: Thu, 17 Oct 2024 13:58:02 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c66441f96552ae3dbf1758127972372919f4729629676e0f87acfb07680626`  
		Last Modified: Thu, 17 Oct 2024 14:17:15 GMT  
		Size: 28.7 MB (28714291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08de650f46b713399d6a7ebf870a30b36b3f8a4ba1d5ab81967720212de7bc7d`  
		Last Modified: Thu, 17 Oct 2024 14:17:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:ed8e7b742e86983faea54fc7f7880a49c9fc9ccc6b87ae0e489754a85edad998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3808630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3861db2b711e3efa54c3b0530a68dca1e56897b61c9d33875387ec1b5f96016`

```dockerfile
```

-	Layers:
	-	`sha256:5afcc23282a1a501e1c3a488acf117a21baea7be0fc096357f4227d1d21e82f9`  
		Last Modified: Thu, 17 Oct 2024 14:17:15 GMT  
		Size: 3.8 MB (3788262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56620f58cd9c202b285950cd0c6feabc6f1de8475f31c06eb7b426cf2dc1d05f`  
		Last Modified: Thu, 17 Oct 2024 14:17:15 GMT  
		Size: 20.4 KB (20368 bytes)  
		MIME: application/vnd.in-toto+json
