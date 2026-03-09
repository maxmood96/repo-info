## `perl:5-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:8ee5e6a6c0075f2f35e1a61b6d8c5caf511e638fcc3ab84ba5ad4d010b7de1d5
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

### `perl:5-slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:f61a6a44a1a9feb223e3992a677e1d8bec01bbbbe80e9a9ed1e94312e2884ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58205944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76a194fbbdc58047ab9e7dd37b4d32743f81b6d670c449e7286d1fc895fc652`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:28:41 GMT
WORKDIR /usr/src/perl
# Tue, 24 Feb 2026 19:33:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 24 Feb 2026 19:33:11 GMT
WORKDIR /usr/src/app
# Tue, 24 Feb 2026 19:33:11 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1c80ba4a5f6c292d4f5ba5968c2e86840ef1425fe2b8d0ec84877cbbaeda78`  
		Last Modified: Tue, 24 Feb 2026 19:33:21 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d71d73bc0cb1513caec428a256234b780595342ceeeddd06dc649bdabf5377`  
		Last Modified: Tue, 24 Feb 2026 19:33:23 GMT  
		Size: 27.9 MB (27947296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3c4d613353a7feb275c7770e03ea7510d849b6276ff4b90a28c0cf1321cf3b`  
		Last Modified: Tue, 24 Feb 2026 19:33:21 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e8c83ccc4907360764100ef8d7fc2dca4d39c67469f93bf304ca799beacdb11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d58a7c65fdb2989084ba8446e081422cff70f800f260160347b0d33d3787a38`

```dockerfile
```

-	Layers:
	-	`sha256:c394eebbc8aaf754c3e78c8ad5a5e9476334f9f15301be8b8ae39ed5dbfafffb`  
		Last Modified: Tue, 24 Feb 2026 19:33:22 GMT  
		Size: 4.1 MB (4129775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb5c7261fb30dc6b310ae5b29f5a3c0b0d0e0fc1978e325d53a4017aeae0614`  
		Last Modified: Tue, 24 Feb 2026 19:33:21 GMT  
		Size: 18.9 KB (18926 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:7398b21a71da6cff92b6690796c3c147a21001e156dab81b0454451ec88aa0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50342341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d69ca1a5649ca46763963c24a4ae661c4ed955e2cd0d260c6ee0a5216e941a`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:36:47 GMT
WORKDIR /usr/src/perl
# Tue, 24 Feb 2026 20:42:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 24 Feb 2026 20:42:26 GMT
WORKDIR /usr/src/app
# Tue, 24 Feb 2026 20:42:26 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:bb3e15331ea20fb55ac61096e3d658115aa008a224de61596add58765bac156c`  
		Last Modified: Tue, 24 Feb 2026 18:42:27 GMT  
		Size: 25.5 MB (25546149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0c69a03375389c288b9f9d40d06a2d4677186b34ec2ba5b3c38f2b773ba35b`  
		Last Modified: Tue, 24 Feb 2026 20:42:36 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f86d07925fbc7664038c85721cccb4e7e542bad06e50c2717b7dc273d39895`  
		Last Modified: Tue, 24 Feb 2026 20:42:36 GMT  
		Size: 24.8 MB (24795925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c743b43577f777ada736c57ee9ed3af3fad9df040653c4c0c36a2150672269`  
		Last Modified: Tue, 24 Feb 2026 20:42:36 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:860e510d0ec88aa6c6997e5092e3b434ad618e18234eb610c1d7ed4a2bd16225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1921f77d25ec7c9f0840ba453018d4acfa959879b9b2577771dbeed0b79267dd`

```dockerfile
```

-	Layers:
	-	`sha256:0cc62df23dc26fcda398f57827c01f2b74637c263dd11be58b9377fdb48c67c6`  
		Last Modified: Tue, 24 Feb 2026 20:42:36 GMT  
		Size: 4.1 MB (4103780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b089fa7362d51f03b4b6fb9383ad4d57532c501529bbb6976fa31ef74627ff02`  
		Last Modified: Tue, 24 Feb 2026 20:42:36 GMT  
		Size: 19.0 KB (19014 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:712aeecb217ab5c533b804ce1d297bd7c3f4b444bebebef7165421d73639e32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55662357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6258afd3eabe402def85b1017055d0a7b06ae92cc74a319cbf9d70c8ebea152`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:33:27 GMT
WORKDIR /usr/src/perl
# Tue, 24 Feb 2026 19:38:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 24 Feb 2026 19:38:11 GMT
WORKDIR /usr/src/app
# Tue, 24 Feb 2026 19:38:11 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0e85db6a93ab4e84a46aab680370b6cd7f255cb546e8a47560a308d680fade`  
		Last Modified: Tue, 24 Feb 2026 19:38:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad76e72eb9542ff1c1818c90a16d2bdb04219d7d60e88d1aab4f3cca434e3776`  
		Last Modified: Tue, 24 Feb 2026 19:38:23 GMT  
		Size: 26.9 MB (26917619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a44c0a482945039bef0b67a77faee5fd1243c0a9860a8b4a370cd7f3072917`  
		Last Modified: Tue, 24 Feb 2026 19:38:22 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c822c9f376b2a8343ccc43f64a5547d1b179baaf3c5789c29b8ce8be5429a611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b43bb149d29f3f16ce8207ee706b58912231a29bbb876e6a3866dc8fc90df08`

```dockerfile
```

-	Layers:
	-	`sha256:849efd1393557f7343a89394f320aecfd004e83e669e2e503a5a6055a6e6b3af`  
		Last Modified: Tue, 24 Feb 2026 19:38:22 GMT  
		Size: 4.1 MB (4104194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91d4c06d31308ba8ed76a3780fd0e9f5d6d6045d7fbf4f893df1835c7828633e`  
		Last Modified: Tue, 24 Feb 2026 19:38:22 GMT  
		Size: 19.0 KB (19043 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:a70538ed17f7eb55293ce779f396eceab2eaebd72b11cd0fca6cc1a02f2c615b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60697873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ded1d9c2cb4f14c3004fd0b68d4cc3ee25dcdd803d39825a1e2ad80f828a6e3`
-	Default Command: `["perl5.42.1","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 18:00:56 GMT
WORKDIR /usr/src/perl
# Mon, 09 Mar 2026 18:06:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.1.tar.gz -o perl-5.42.1.tar.gz     && echo '6f84e6dc8cce97181d1c6aeeb552c13775c91ded3c6c73743c9211af87b16bf8 *perl-5.42.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.1.tar.gz -C /usr/src/perl     && rm perl-5.42.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Mar 2026 18:06:20 GMT
WORKDIR /usr/src/app
# Mon, 09 Mar 2026 18:06:20 GMT
CMD ["perl5.42.1" "-de0"]
```

-	Layers:
	-	`sha256:e7fe90a9de0c5a23218f44ca664fcfd8e0326759af345f47445cdd5f305f3e6e`  
		Last Modified: Tue, 24 Feb 2026 18:42:18 GMT  
		Size: 31.2 MB (31191566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832bba967615f35b7a9f1255e0811096cdf969a168a290dcfb2df3d650278142`  
		Last Modified: Mon, 09 Mar 2026 18:06:30 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d703348a8ce44f58c3591e76b9ae84d16d5e0a891b90ee95aee34d62cce4c41`  
		Last Modified: Mon, 09 Mar 2026 18:06:31 GMT  
		Size: 29.5 MB (29506039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c6d6616f418ca584ec3f11113d31070a552d40120e0b8e6b0c8d3439d2be20`  
		Last Modified: Mon, 09 Mar 2026 18:06:30 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ed5c084b637dce49218b78c7541f28ee040d020b753c7c23f0de3a7523a91951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f45626b11474c2c211519e176a78d4761fd298867d8e3f37eb235650fb735c4`

```dockerfile
```

-	Layers:
	-	`sha256:ce2ae5662baeea00048734cd0977b6b51e952c5db61d42f991e4a150403b41b7`  
		Last Modified: Mon, 09 Mar 2026 18:06:31 GMT  
		Size: 4.1 MB (4134047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37dcefaa26d806a73a938fad053c3138f0436c4bdbae077582ea576f10b02997`  
		Last Modified: Mon, 09 Mar 2026 18:06:30 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json
