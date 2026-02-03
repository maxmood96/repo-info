## `perl:5-slim-threaded-bookworm`

```console
$ docker pull perl@sha256:324d7d11868e8d010e94654e81a6191b8f5af90e232be4fd3d37e7dcd6eb8aa5
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

### `perl:5-slim-threaded-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:417a7e15ae7a27da710eb5206ad9e0a024555a6104065f3e90cde2ed3595bb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58503982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082f10a0db3c62fc96b164c4ef119a449eafbd323ffeda46d81f0ebc339c4223`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:51:00 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 02:55:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 02:55:44 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 02:55:44 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2333ab9d07e25d7f3785536bfe835347af8bd83ca1cb0ff66db8f699edf85644`  
		Last Modified: Tue, 03 Feb 2026 02:55:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf63f9f2f6c7efdfca2676512c1c1fd72d232df692edb194c73cc942fd9bb794`  
		Last Modified: Tue, 03 Feb 2026 02:55:56 GMT  
		Size: 30.3 MB (30275227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3050477177047318af94511a3ad2f34bbcd907090f0e5ed96a33c61aa90b7b2`  
		Last Modified: Tue, 03 Feb 2026 02:55:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:447e98cc32fe30424faa4ee712601735188138711e61ebe0eac7a79d68220d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a754a00768f9023c576dc450e39cdf9d623e0b7cdf574ade083b681fe54210a4`

```dockerfile
```

-	Layers:
	-	`sha256:6f349247cdb82b09f3b1109056fbd745b520bdd7be58d36719d3631564703d79`  
		Last Modified: Tue, 03 Feb 2026 02:55:55 GMT  
		Size: 3.9 MB (3940052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97d88daa0a8368d97692630fb69eebef0e72f6063518736bc5b738332a56277f`  
		Last Modified: Tue, 03 Feb 2026 02:55:55 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:896f1eb38f962578bc00cedecf8b9b8c148ba691dd049aaab7630d7049da32f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53070467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8053462d938bd8e9130d3d6b617ec3c72279165d6cd1b7fef95bcb4d68fa8a9a`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:29:13 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 03:35:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 03:35:18 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:6036aff531a372e1e9da48952322760c8c052f6735e66afd3251a32e5baace8d`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 25.8 MB (25757618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340a0d535010f8105dc089831137c20cbd46655a47e4349d6c11d5f84a5173d0`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68033621962d1611361ffcba0d32ba01190cb175c361c0018907aed7dffe7e90`  
		Last Modified: Tue, 03 Feb 2026 03:35:29 GMT  
		Size: 27.3 MB (27312580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca8bf2df95d0561e07bf2cdd5d6a9a71d8c8dec50a031dc06e23a32860b195`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:86fd2b294a65fd56b6430ec10dc23ec5cb04279cf142abf01ae00cd17ff65abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f40a8ca831010f83274146a9b2067f21d5ec9e344e2892580b3ace584da569`

```dockerfile
```

-	Layers:
	-	`sha256:c57ca55f456ae0bfc1cc20d5f70a6f64b142366eb541be65619b6ff836ee273c`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 3.9 MB (3910919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a85ba5303b9e8105544dfd221667c63426786b522943173e8db8a8bb3dbb5856`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 19.0 KB (19015 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:520e4a17533765f12c6ee10500e58368016c06792b1a6204eac66b19b12ee88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50335526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bf4dc1c49ff8a9afe457c6772d9ccc8c677fc4979c6be80ef2633bf576a8f0`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:27:51 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 03:33:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 03:33:40 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 03:33:40 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef0c0e557be651119734d73b24d75356b281b302e65ab3cc8d629f0f2ef717b`  
		Last Modified: Tue, 13 Jan 2026 03:33:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ffa5a6ac2c70e65d70667ae6eddf24fdc651ff20632f1816394bd638403861`  
		Last Modified: Tue, 13 Jan 2026 03:33:51 GMT  
		Size: 26.4 MB (26401142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf4eb139b5cb2f8690878d162f8a61b729ade5523c6ad36ce94698ba2684fbc`  
		Last Modified: Tue, 13 Jan 2026 03:33:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:5d330db462733bbdc1c73768f2c9a69cc2c7e58dfa8c1eef3b85476804410d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438f097beb30d7f447617c236a2fb4a06f74dee50ce7ed46da1bef1cb00d5a3c`

```dockerfile
```

-	Layers:
	-	`sha256:b673e3fe2e84b60112b6b762068e0213887eb5d669108fcad3a933d654013df9`  
		Last Modified: Tue, 13 Jan 2026 03:33:51 GMT  
		Size: 3.9 MB (3910144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994468be38ab6efea0a1b81dd544f15032c1b41f29bd3a56db2d045c46bd3a5b`  
		Last Modified: Tue, 13 Jan 2026 03:33:50 GMT  
		Size: 19.0 KB (19015 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:10c46c55ba790ed18e8764ccda61556ae5712f3bc921c305cd2866a9037091d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57224879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676bb41d9c1114d767006597e6dba01c534672cf266fcd89902c34f9a98f6cd1`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:56:35 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 03:01:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 03:01:32 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 03:01:32 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129df85c43e402188198d1ecdd2c214a59c486a4de6050007afd16973c77a257`  
		Last Modified: Tue, 13 Jan 2026 03:01:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087ea77bb14aa3d157063aae73f5b220ae2495b373d2154125559e6e19320660`  
		Last Modified: Tue, 13 Jan 2026 03:01:45 GMT  
		Size: 29.1 MB (29116723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6baa9f6fc45c861aa3f4e401a3a97e5d63e0a888b85525dd4b17b8300377e3`  
		Last Modified: Tue, 13 Jan 2026 03:01:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:e5bd670700aad749f019741c9bce8eff258903a16d9d7d27f3028114a7b8d039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81211741941679a2ba91703cd39cb617093055beef1f7ffc6e7810451740ba2c`

```dockerfile
```

-	Layers:
	-	`sha256:53bea0aa32107f247b4a882ec9895c36bcc48f8069ac2801a6b6e7dbf5eae2c7`  
		Last Modified: Tue, 13 Jan 2026 03:01:44 GMT  
		Size: 3.9 MB (3911313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b24eee1322135bc9653f37dd63b8d846cee57df1804203de681b94389d3b3877`  
		Last Modified: Tue, 13 Jan 2026 03:01:44 GMT  
		Size: 19.0 KB (19043 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:72e560ed6a12dd7794263556f64aa3b379041ac0f50feb4c0abac1ef9246e363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58659378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c46d24785b61261beabc93ac214e1c4afe37ea1f35d08b01abc3292d812668`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:49 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 02:26:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 02:26:24 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 02:26:24 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:37 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb657fc477c0e758dba5ce8f2d709344367fa2c358dd64f6211107cae3ec14fb`  
		Last Modified: Tue, 13 Jan 2026 02:20:40 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b1e7b04b1e3bf060fbfb4c3eefbf8c30cb4f84705be70dee9ac448e82d68e8`  
		Last Modified: Tue, 13 Jan 2026 02:26:34 GMT  
		Size: 29.4 MB (29449046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e87049a9a0b39c2ee81fe959bd9cd5af74ffb8da238ae273af6172f54b2acb5`  
		Last Modified: Tue, 13 Jan 2026 02:26:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:0eb96dfa40b7436b353e51d4b65cea1bb87a70036a22435784dfdc981db7bc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87ab27d7ede070f99e73d01c83b9946faba1bfdf66d28deaa189aa39d7049de`

```dockerfile
```

-	Layers:
	-	`sha256:46742e5cba85f4d2ecad991641292214dcbc75dea83a6a2931ae1b35584cb92a`  
		Last Modified: Tue, 13 Jan 2026 02:26:34 GMT  
		Size: 3.9 MB (3933984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7c7ce359431bbdad4707af89297b5c52af5296121b387f6e06515a1aed211c`  
		Last Modified: Tue, 13 Jan 2026 02:26:34 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:269ad6de6a7ee60419cf20bfbb0d339dba118274c9104f016b615bf4d9ebbc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56947882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82309eb0c9d9a25d029ce55b62649f696ea881cbf5c64402100de49a018e294f`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 16:56:47 GMT
WORKDIR /usr/src/perl
# Tue, 13 Jan 2026 17:50:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 13 Jan 2026 17:50:22 GMT
WORKDIR /usr/src/app
# Tue, 13 Jan 2026 17:50:22 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:c063a3c188d3088513ac303ee5a03a6c0ddff0d68a1e46804a822134a25bf8e8`  
		Last Modified: Tue, 13 Jan 2026 00:40:54 GMT  
		Size: 28.5 MB (28513755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c538ce4879599b5ff715e79d55c510bcbc55404be84947cc500ebf09345570`  
		Last Modified: Tue, 13 Jan 2026 17:22:43 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3002c1791032da7b72a85612df913f500477940927453406bd7676ee0abc29d`  
		Last Modified: Tue, 13 Jan 2026 17:51:09 GMT  
		Size: 28.4 MB (28433860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5074d565bc7f15c5a9eb164c108ce605e79d45be8a7742b3a0e5dc96306dae`  
		Last Modified: Tue, 13 Jan 2026 17:51:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:5e2948c55f08616105ea4bfda2d6c5d7b968be7ba7fcc14c5085e4117003be0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390d0adeb08c7fa8375b238df98c9c00de2890d0749041a986149a2c23049155`

```dockerfile
```

-	Layers:
	-	`sha256:2b20406ddcedcd1ba28ce11d207f8f61523558122205636f3c335eee905e81ca`  
		Last Modified: Tue, 13 Jan 2026 17:51:06 GMT  
		Size: 18.8 KB (18786 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:c7b5efaf47aec967f3fe907715dcde398f6906eaed1d9bed74c3d97faf42b8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63173892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e75fe7518889ed1d730f7bf1a27e0a5add4ba77eba71fa0fe5ef73bf631ea2`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 01:06:09 GMT
WORKDIR /usr/src/perl
# Wed, 14 Jan 2026 01:15:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 14 Jan 2026 01:15:27 GMT
WORKDIR /usr/src/app
# Wed, 14 Jan 2026 01:15:27 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c38a9956229e5051f1d435e1e733871adb8f1d0fa3cbffb1d3dc485e778a577`  
		Last Modified: Wed, 14 Jan 2026 01:14:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e3dcb28fb32c20cf2506673dd27bb8a22fe61e2f70d7823dd04f997e25c77`  
		Last Modified: Wed, 14 Jan 2026 01:15:50 GMT  
		Size: 31.1 MB (31104918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a265c7d2426439d2f062a02a2db3f4eee0cd43a6b4f5c6ff53762fd7b8614dd5`  
		Last Modified: Wed, 14 Jan 2026 01:15:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:bebbba2792497e9d81dc09412cbd12526a684a0cead62a372ff7c83bbe31a4bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbc0bd6d06c13555846e01d59afe18b485b9895ce4c9c52c5d6adbcd9fb516d`

```dockerfile
```

-	Layers:
	-	`sha256:80bc12ce79533ece66e9be81c6a7cb4a4616cc9da9cfbae6711d9c4c89fb4f47`  
		Last Modified: Wed, 14 Jan 2026 01:15:49 GMT  
		Size: 3.9 MB (3925992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4ee0d9c630af817b31c9027863c22484dc2d833a6e39c0548351b8b63e3bc85`  
		Last Modified: Wed, 14 Jan 2026 01:15:49 GMT  
		Size: 19.0 KB (18977 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:60fcbafc02dffabb802aedb4626257c60cbf6843bb5b6f778bffbb97bdafabaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55698415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908d2b0e1d9fe9c4a89b9db7d997ed5852cbb5b868b55c485e3207fcadab3b69`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:54:14 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 04:00:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 04:00:47 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 04:00:47 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1f62933055a52ff2753fc1dbb58ad222adb39a6a2135267ccb30557ea2cb2e`  
		Last Modified: Tue, 03 Feb 2026 04:01:03 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b8df988babd412b1286c260df47368563e9b5eaa894407452f4d438ac227fb`  
		Last Modified: Tue, 03 Feb 2026 04:01:04 GMT  
		Size: 28.8 MB (28813765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb611cb8dfc73ec36ffff1a208024da9073d8ea346d681ba5dcba61b16bae76`  
		Last Modified: Tue, 03 Feb 2026 04:01:04 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:35ade6b7547fb362a26f2c122c8d73a6779cb94a1d695ccc5015e6f4f126622b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffd596bd7c0d0b1e22cbedfd95510c2bbebc259748fbc6647a027da046935c6`

```dockerfile
```

-	Layers:
	-	`sha256:f5912168f5bb922fa6a4735f87ff9003d62cc0e4bacb5df8363a449fcf243db4`  
		Last Modified: Tue, 03 Feb 2026 04:01:04 GMT  
		Size: 3.9 MB (3925325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0754b501f28d78e5caadd80f2e2a55f30e9754ae9dd9a4c73b5ef8aefe06baf`  
		Last Modified: Tue, 03 Feb 2026 04:01:04 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.in-toto+json
