## `perl:stable-slim-trixie`

```console
$ docker pull perl@sha256:8162d556f87da9ffcf9748c420f28b6d7ddb0b62a3011c73e7c3d5f186a03a7f
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

### `perl:stable-slim-trixie` - linux; amd64

```console
$ docker pull perl@sha256:950a0d98c65279ec9be29f50b212f7d2046662def3244c4f91f494ed9eacb6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61731600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1d0a432627c236b44da76b7f46d9dec6ba54c0d6e9d081be471ceac3a4a96c`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:14:05 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 00:18:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 00:18:30 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 00:18:30 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef18e2cbdb2df8d065a14cd358c4d1d41a924c03ad8d905163fdb970a4fa2950`  
		Last Modified: Tue, 30 Dec 2025 00:18:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629f5778b5cb2eda876405827931cb6a37fd31ca48ef89ad49f44486e8c9c72f`  
		Last Modified: Tue, 30 Dec 2025 00:18:56 GMT  
		Size: 32.0 MB (31954802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f37dfd34c0ad3c4124b3b0d572fb5e69a4861690b55f438ae3436f7a544932b`  
		Last Modified: Tue, 30 Dec 2025 00:18:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:8a70ec98726cac787515480bb67bb529e2b31b32199047c5e1678809c960fa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4030730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa7a03602c4f3b6206725fa73fac11d843ef8a095cdcbf5206d1df2c409ed01`

```dockerfile
```

-	Layers:
	-	`sha256:4408539d2d4d6a888374c2dc41337f427a4822742e56d4f9e36406ca8c9569e8`  
		Last Modified: Tue, 30 Dec 2025 02:38:29 GMT  
		Size: 4.0 MB (4010478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:334d00402c99121ef70338104b2d820922c01f5972107697f703170975433924`  
		Last Modified: Tue, 30 Dec 2025 02:38:30 GMT  
		Size: 20.3 KB (20252 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-trixie` - linux; arm variant v5

```console
$ docker pull perl@sha256:5d60068c288ec12ef6603cbf71a7e0799aec790fd6acf85231bc40b68edcf22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57144050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b683335f2776adce3458e0c2744136c339a39481fec34f32b5501e2861fb102`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:30:08 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 00:35:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 00:35:41 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 00:35:41 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0b89bac87450bc58e54f596ded9b5a0c7b161e017d131156c0dedbc0549769`  
		Last Modified: Tue, 30 Dec 2025 00:35:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe18c2d236c3347e93e8c60219e35adc7cdd575fd57e49bb7e9eb3d3a5aea48`  
		Last Modified: Tue, 30 Dec 2025 00:36:00 GMT  
		Size: 29.2 MB (29199637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67906ab015bb2f4974cbe236c5117cb517844fed9bf8b23309f153449a2d3bf`  
		Last Modified: Tue, 30 Dec 2025 00:35:57 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:74e3f6c6a54f1a1e619c58bc14a22882806c09d0b2bfce4735dbb89fff2f56d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c091d77e66c35d794c6a38e99e7822b43ea84097d3268a0bf74241c6cfc70f05`

```dockerfile
```

-	Layers:
	-	`sha256:e8973b3cc48efa896499202228c9ea3ce096beed71aa11ae0a80bdc22f78125b`  
		Last Modified: Tue, 30 Dec 2025 02:38:35 GMT  
		Size: 4.0 MB (4003555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa70022727110fe3ad698a265cc8db67643c9209c4adbd82328b8465c4201b3c`  
		Last Modified: Tue, 30 Dec 2025 02:38:36 GMT  
		Size: 20.4 KB (20380 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-trixie` - linux; arm variant v7

```console
$ docker pull perl@sha256:160948d25c5eb962e20274c163825d89c70c2c0187711a1cf6f52ee82bb02788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54486554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e004f9a8f16e8a2f554a3ea6debd974e07ec9815dbbf4b66baa563ae40aea27`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:50:11 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 00:55:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 00:55:36 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 00:55:36 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8783e4a657ab8f85933153c6e9a0da6ceed83263ca82847f235506000588522b`  
		Last Modified: Tue, 30 Dec 2025 00:55:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f76183263f4ffcdc348ba245fe95d150b9a6af3d59c61cc24f9ea97d1c0857`  
		Last Modified: Tue, 30 Dec 2025 00:55:57 GMT  
		Size: 28.3 MB (28276287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa494bc33acc56dcce9c6ab3cd891cd4675a9bea3749ab0c49af4f83b46c7a3f`  
		Last Modified: Tue, 30 Dec 2025 00:55:53 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:9f3838bd88e07bac1787e08664771ccd2d9a34d4510190f000564f36181a4f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9d17e741f253ca4e322cb231e222b6f6cd185278d36e579510047e056986f5`

```dockerfile
```

-	Layers:
	-	`sha256:3d8297b472198dd256107379385658ffb3c9039fd9045920020113de7bc33640`  
		Last Modified: Tue, 30 Dec 2025 02:38:43 GMT  
		Size: 4.0 MB (4002746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:435e96ec5986f1726d65030e496f92afd02ac2d754433f9d0a7242c7208b295e`  
		Last Modified: Tue, 30 Dec 2025 02:38:44 GMT  
		Size: 20.4 KB (20380 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:a6d0daba54c0ec0b0536167b862ee1939572d8911a9eb5c8c98a9be1b3777583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61759438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28391afed2b8ae52baa73250d72dc0cbb665f4e807788e4f359cde63080ad1e2`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:15:09 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 00:19:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 00:19:51 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 00:19:51 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25be679c04ae322a96be7b386ca482cf5624a34fa1188093776a64d3a314d891`  
		Last Modified: Tue, 30 Dec 2025 00:20:17 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b56cd2022a4b28073fb41c62a626890b9e60f014c55e2589cbf7ac768b2cd25`  
		Last Modified: Tue, 30 Dec 2025 00:20:12 GMT  
		Size: 31.6 MB (31620535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84187339e844af07ccbe704a1d3e14e5f059436fc5cbd21cb31ff8e275c157bf`  
		Last Modified: Tue, 30 Dec 2025 00:20:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:5d642061e5cd8f14635b6e32f8aa26d2b9e226cd2a9daeaf4b21b0be08389f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bad1397abce0ee09a56d83cddd6109e3b640cf3358fee75c65c1cd8af1d585`

```dockerfile
```

-	Layers:
	-	`sha256:1da4f8c69da08354dd6718f259f8d66334136e29480d2ba18cf4fec1a830b6b1`  
		Last Modified: Tue, 30 Dec 2025 02:38:49 GMT  
		Size: 4.0 MB (4005621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2050944316fde4ac5e70ae3864264d77c30a3cc54d1795a5963ff4349f86d3a8`  
		Last Modified: Tue, 30 Dec 2025 02:38:50 GMT  
		Size: 20.4 KB (20428 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-trixie` - linux; ppc64le

```console
$ docker pull perl@sha256:c49f7bcb37ec690d500f40fa85b48eb70a9730499c7db9039001af985f01dfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66269083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6940d98689c0a2a8fcb157d931d9f9144273e573e4f3e1528ed1b2255026e4`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 02:19:01 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 02:26:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 02:26:44 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 02:26:44 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45f3fb23bd4730cdc9b834427bff94aa0ea5ffb0d70e8e92d1745e0a72971b9`  
		Last Modified: Tue, 09 Dec 2025 02:27:24 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a82c6ea5c5c9cc8342ef5c935789d90c66dab2a0f860133937857165f82ca3b`  
		Last Modified: Tue, 09 Dec 2025 02:27:27 GMT  
		Size: 32.7 MB (32671928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ad6f89a69ee56038a528801a49f6908da1a9429f1518727a99b946eb4c5504`  
		Last Modified: Tue, 09 Dec 2025 02:27:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:a7f0eb7d4281a87dd3ba1dbbe1b6e6d6a2689ab8a4bb03af437c2339322dc106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48d01c0e0ef56e5ad14b1d1cef13d547d1ad1c649bc7af5a415089fcfeca44d`

```dockerfile
```

-	Layers:
	-	`sha256:2c8670843c0116420820bc44184ce498bde86312c661f62d26afa92847b29260`  
		Last Modified: Tue, 09 Dec 2025 05:38:11 GMT  
		Size: 4.0 MB (4006514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aa7e398b54fae580731736bf60a2a89548d0f22cb6c8eaa7e47ede08a3fa555`  
		Last Modified: Tue, 09 Dec 2025 05:38:12 GMT  
		Size: 20.3 KB (20332 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-trixie` - linux; riscv64

```console
$ docker pull perl@sha256:5753f719f4923d71cf13e19b8771ac14f55bf1ae77c0d9ad9485935f70b9ab66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68050224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040415080cb153b751b01e9dd6a1f282396e4db12cc3e8f20202be406f19e993`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 17:47:50 GMT
WORKDIR /usr/src/perl
# Thu, 11 Dec 2025 18:55:05 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 11 Dec 2025 18:55:06 GMT
WORKDIR /usr/src/app
# Thu, 11 Dec 2025 18:55:06 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c559b49aac752b97f67651f6dfca0a26342e00e2ebceb43c6d6d8408b58dda6`  
		Last Modified: Thu, 11 Dec 2025 18:57:58 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c195c8cef3c43d51b8db3cfada0f7b3c81bb7f9165bc7aa968d08ceee8068f0`  
		Last Modified: Thu, 11 Dec 2025 18:58:01 GMT  
		Size: 39.8 MB (39776802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7ad718ca294da2a3c098cd22935ef1e3655323afe77ab2c817ce268be0ec85`  
		Last Modified: Thu, 11 Dec 2025 18:57:58 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:e2ed8033bde14b72148639e5196796b6f105987060e89f3b6a037fe5b309cf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4018111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044d59f602cef02c11e005341fba61bd982a0067719462067397d3a5d3849b5f`

```dockerfile
```

-	Layers:
	-	`sha256:fb6a944e9e3bd8fa0b8770d2e8ee388d20f868b01f27f92dabd780a6a2855b54`  
		Last Modified: Thu, 11 Dec 2025 20:39:27 GMT  
		Size: 4.0 MB (3997780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38340c403d84930d910298c261ed173b17d733d6c5765fd9eb1ec7eaf391415e`  
		Last Modified: Thu, 11 Dec 2025 20:39:28 GMT  
		Size: 20.3 KB (20331 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-trixie` - linux; s390x

```console
$ docker pull perl@sha256:edc4e500c75520cec9b0a0d789f1a7115b9506cf82f9cf5952553ea0b44ac5bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61143042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8a66bd7343c548ecf998b48d2323db6df80eb08814696f1305c73d32339cae`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:49:47 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 00:55:14 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 00:55:14 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 00:55:14 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9c44a7d7e5d0a1b3c603d5ffdbacdf1be3895539cf7fcdb0b679c6b3100ae0`  
		Last Modified: Tue, 30 Dec 2025 00:55:36 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da91ddc9cf6fbbac81964d80e808c3dc643b9bd37618752c938c080a7769a0b`  
		Last Modified: Tue, 30 Dec 2025 00:55:41 GMT  
		Size: 31.3 MB (31308358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b06cc14611c0afa5932ce972adf2d82c1739379b39d9d31c5d5550028f22ba0`  
		Last Modified: Tue, 30 Dec 2025 00:55:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:10f07ca0b637a4ae2c53111134922f487f2cb79bae5109fbe9f97901e7babb15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607e35007be9da6dd8c9a003ed0783b93331d46e4ea8a6d19e5085ceb4bdb4c0`

```dockerfile
```

-	Layers:
	-	`sha256:788f342be790a7276aeecf8cd77836ea9f062c57aa40084f948a128f01a40ed8`  
		Last Modified: Tue, 30 Dec 2025 02:39:02 GMT  
		Size: 4.0 MB (4002806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af90625a625e9ff43834d9dcf6ccd02f71926be4040761a946c5449128d2f9a9`  
		Last Modified: Tue, 30 Dec 2025 02:39:02 GMT  
		Size: 20.3 KB (20252 bytes)  
		MIME: application/vnd.in-toto+json
