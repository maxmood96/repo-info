## `perl:slim-threaded-bookworm`

```console
$ docker pull perl@sha256:90be6594abce334669fcfc5612cd1620984d2a59615c4af931beda93c3701e35
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
$ docker pull perl@sha256:79e4a6faa07113cadb22feee3a01887eb2e1903bdb175653267c547f13dcb90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58494759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7388f8fb4552da3a3d83b0ea7ff6574b6aef4aeea3fd04195968f327936cfefb`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:18:32 GMT
WORKDIR /usr/src/perl
# Mon, 08 Dec 2025 23:23:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 08 Dec 2025 23:23:39 GMT
WORKDIR /usr/src/app
# Mon, 08 Dec 2025 23:23:39 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a601d43042d8b1f15885db054127a18dabf966544f561ed0d04730aad440d5`  
		Last Modified: Mon, 08 Dec 2025 23:23:55 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3400ed69c40b4fe4920c349f080f369acb6625bc2d6fbf3933d7fb5caeac5aa`  
		Last Modified: Mon, 08 Dec 2025 23:23:58 GMT  
		Size: 30.3 MB (30266075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bda4a57639b389091f3973b16221239409f4656ef7915a85ca8d3e5df5f7cb`  
		Last Modified: Mon, 08 Dec 2025 23:23:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:e063c519a37af6590e9e0c57faad7bd5ba2268f4fababbda97915f00dcf272b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d6fa8afc81acbc968d47d2a032e95a7ffabc5f4001683bac798869bb066b9a`

```dockerfile
```

-	Layers:
	-	`sha256:3d1e92adc9c017a7727afac7fa7f14f85bc9842851ab5abbd73735aefaa02767`  
		Last Modified: Tue, 09 Dec 2025 02:38:55 GMT  
		Size: 3.9 MB (3940042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:950c7997e8f608357d1adeeb6c56c1ee01eeed1212d5bfc64453f93cb7b2c365`  
		Last Modified: Tue, 09 Dec 2025 02:38:56 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:93e9b0de90f7647c451341d0c0d52d7875635c9633ab42a0b8238f39556eb58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53062832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b6eb5939e618cf46b4605d6f02921b733a6a8d05993347db151507cf1f7ba5`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:01:45 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 00:07:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 00:07:56 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 00:07:56 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:20ca79728ab9e4eb574872cf271bd965c51cf4e8ac84660ef17b281a3aeb750e`  
		Last Modified: Mon, 08 Dec 2025 22:16:26 GMT  
		Size: 25.8 MB (25757588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e53926c7b950f1df8f450c2f3a1fe32cba0dffc7feecf427d4479fac59674c`  
		Last Modified: Tue, 09 Dec 2025 00:08:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233fb15a59020dbb194cd68218e9eefbdb8d385a329ae412b7c4d2b9861a9276`  
		Last Modified: Tue, 09 Dec 2025 00:08:16 GMT  
		Size: 27.3 MB (27304977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cd2a2622b4354a43ded30da81c8858c247e84fbdd194d0f00047ba387df145`  
		Last Modified: Tue, 09 Dec 2025 00:08:13 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2c00646d6eb90f3ed8af54415b469ed887828e2d4ce7ba30c378be70bbf4facc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450b8ea48b344ad4183bb1c1ef8a2ef42d3803c62048c34aba1667f403b84fd1`

```dockerfile
```

-	Layers:
	-	`sha256:0087cf2540b0aa61194cb6a2397cb3c448102308975badb980d8c93770d88b72`  
		Last Modified: Tue, 09 Dec 2025 02:39:00 GMT  
		Size: 3.9 MB (3910909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e0ff136aef3e4e785aa776338fe4ba9bc20cd2be0d1051b98b202fada68a400`  
		Last Modified: Tue, 09 Dec 2025 02:39:01 GMT  
		Size: 19.0 KB (19015 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:760b7943f3b7b4041576b3df1a0f5d17f8e1be832dd2d20545660dee46fb64d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50337460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c859b5226ef827a9304433bf0457093d206e792a5449e9004e982a272ae9aaa`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:37:38 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 00:43:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 00:43:30 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 00:43:30 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b70368822accd52ad083847121c8f8c4d60d6c6f16d3ac27f1663e9442ec64`  
		Last Modified: Tue, 09 Dec 2025 00:43:48 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17e1937c35411880145ac4366a610c0baf83a1ea4b34a050bc3487d936a8ce0`  
		Last Modified: Tue, 09 Dec 2025 00:43:49 GMT  
		Size: 26.4 MB (26403174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2225d50441e8dc79976c82f042083d3e3e4fca030196550acf54108e0a83b1fa`  
		Last Modified: Tue, 09 Dec 2025 00:43:48 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:7bd0919b85f9c984c97852a32117be8af4e4fdaa03a6e2efc95dc0374b00bbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee681114c6e2ec2689d9bd6ef2374bf2b260508c72451369ec0f3b965e08ca9a`

```dockerfile
```

-	Layers:
	-	`sha256:54d2fd5a8195e3e2340258bf359fa07d21619ba27b8294a38c4e57cd1ff3430a`  
		Last Modified: Tue, 09 Dec 2025 02:39:05 GMT  
		Size: 3.9 MB (3910134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d356cfa02bc2e8751a2b7019ca57beb987c09e3e77b41ac75ff615f421bbb62`  
		Last Modified: Tue, 09 Dec 2025 02:39:06 GMT  
		Size: 19.0 KB (19015 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:9cbe4fd2209e2bee0579613b6fc7db1c6a728863f0e6631090e76f03f5bb5563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57215606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b644ab2dbf85aeb755a92b3b1b0ce34f631e968c949d99607218b01b3e5f270c`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:22:22 GMT
WORKDIR /usr/src/perl
# Mon, 08 Dec 2025 23:27:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 08 Dec 2025 23:27:26 GMT
WORKDIR /usr/src/app
# Mon, 08 Dec 2025 23:27:26 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bc4c24e58f0ce84605c61713758bef980c2afdcb5f539fa929737a25b98933`  
		Last Modified: Mon, 08 Dec 2025 23:27:45 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd00915a2da4de1d2769bbf3cf96171b6380802e4ae26ffea004df20f7f8375`  
		Last Modified: Mon, 08 Dec 2025 23:27:46 GMT  
		Size: 29.1 MB (29113112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc4f591a71980630a7c312870f2483cb8a7c9a850ed693e4c7a7a1fbdb578e`  
		Last Modified: Mon, 08 Dec 2025 23:27:45 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:9a39322c840e5f56261405f254ed299e4b0264c43aafba5a85d093e89e6942fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84df4cad892dbe13f2a783fdf9d8a0518f6976236cf96c94fe998d479c76dbcc`

```dockerfile
```

-	Layers:
	-	`sha256:8f78c2f9cef50c14d277e4ed5a184c5db27a39d766692d2123d8bd7e02515679`  
		Last Modified: Tue, 09 Dec 2025 02:52:28 GMT  
		Size: 3.9 MB (3911303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8304da6d345fb966ba3b2d21cb13a26141cd010cdb393267f9ef3167e81c367a`  
		Last Modified: Tue, 09 Dec 2025 02:52:29 GMT  
		Size: 19.0 KB (19043 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:0b55c759842ee40e4bad3c3fd5573a5ddd4bc5e668177af29111314776d97581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58650152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac441e4e77bf9788dc201a62eefa49a3b1cca681aa34aed6dd76dadb4614370d`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:16:23 GMT
WORKDIR /usr/src/perl
# Mon, 08 Dec 2025 23:21:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 08 Dec 2025 23:21:39 GMT
WORKDIR /usr/src/app
# Mon, 08 Dec 2025 23:21:39 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35f3e9969c68b84eac31e19abdd45f0fcacbef7630d6f23b5034a6b8a3e4efa`  
		Last Modified: Mon, 08 Dec 2025 23:21:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f85efc8ddc79568b55e2bb50436440ab4fd18573906fafd89b3153714a22fa`  
		Last Modified: Mon, 08 Dec 2025 23:21:56 GMT  
		Size: 29.4 MB (29440156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f65dbcc592cf737a90a3b147b15c1973e83a060fdd4093a2c595e4306630b85`  
		Last Modified: Mon, 08 Dec 2025 23:21:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:cfbe11e9a88a5ea70cd58f66e6a5cee9d242b25120b0ddb58e33027baab0772b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f662181c9e040e282620753877139ff15867e695ade6e00e7f4301ae45f491ad`

```dockerfile
```

-	Layers:
	-	`sha256:5da4eaeee0ebf7e236d38eef445d08bd6cb99850c7ac4fac308cb1f9f7275c33`  
		Last Modified: Tue, 09 Dec 2025 02:39:14 GMT  
		Size: 3.9 MB (3933974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c141a232f5adf36f241bf5d844522e7f90a79575d6426d790e09683aab77d2d2`  
		Last Modified: Tue, 09 Dec 2025 02:39:15 GMT  
		Size: 18.9 KB (18889 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:426f887347b8f032c9785ea7f2cf906bdffd1353d00c265ee149fb9b574e6af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56946838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32818525fc74c2d7d112d5e26c1612be4dc51b9e3521335e7865da815169d551`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:03:03 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 16:56:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 16:56:32 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 16:56:32 GMT
CMD ["perl5.42.0" "-de0"]
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
	-	`sha256:4f5887094d718c65aec70f616c78fd64d5ed798888a47f9e97fcda423b8d41f4`  
		Last Modified: Tue, 09 Dec 2025 16:57:26 GMT  
		Size: 28.4 MB (28432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f83a840e51f5ac33d5871bd596416994c45a1156961b674f9d07aae8b502b9`  
		Last Modified: Tue, 09 Dec 2025 16:57:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:88b2a5db4ccd62eb8d47d6c587269b188de2fe03ba85ab83e98724b0d6c41f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dbab9e50ef8af71475d3cdd364ca27ad0812088af825eaaa75e5b749047edda`

```dockerfile
```

-	Layers:
	-	`sha256:965425a0c85ca7675251c75ac11758664e5b19222d9fa55b57f122e9cd738d00`  
		Last Modified: Tue, 09 Dec 2025 17:38:05 GMT  
		Size: 18.8 KB (18787 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:94e80d33f5b94a2ead52a988c169fb0a98945ca119c8c94d18743bf4813071d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63172682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d2bdc9c3a4f607a473ee4d881e4383705c47d3f4aa36423d1ece5bae8d7e17`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 14:26:45 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 14:34:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 14:35:02 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 14:35:02 GMT
CMD ["perl5.42.0" "-de0"]
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
	-	`sha256:849cdb50bae6da6d4afe1a49ed8ac81487584c81b69602832830cdd808697d1e`  
		Last Modified: Tue, 09 Dec 2025 14:35:34 GMT  
		Size: 31.1 MB (31103570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dec003263ba1af00078f7566b17b250d4f7de73a013a4d1c69a1d42e26b3a01`  
		Last Modified: Tue, 09 Dec 2025 14:35:32 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:9fd24132d912b4639a24a39f4a25127dad2c0c746b9e134c6f7a4df6b9ad823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558c06d00b26fba595c3fc4add5bd3e55f88f1047198672abdc366d7ff42d717`

```dockerfile
```

-	Layers:
	-	`sha256:c2935124c0158e4f2c4f31fa8e6b643f6823cf9fc69cb4fe7b1e35f1f5c392dd`  
		Last Modified: Tue, 09 Dec 2025 17:38:08 GMT  
		Size: 3.9 MB (3925982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0607d7cc4829b15d9a044c29c4f7913de79d2fd2c3daf4ed56d19da1dee4f33b`  
		Last Modified: Tue, 09 Dec 2025 17:38:09 GMT  
		Size: 19.0 KB (18977 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:17d32e57fe30a8bfcc708f8454d2355f7c44af91bff0c65eea295e14f07dbf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55692855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30770b35dce62467c9c5505a76e643a1dcb60d5364bcff7ebd577564aaff46b3`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:20:37 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 00:27:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 00:27:00 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 00:27:00 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e16ac4c1075ae8dc1990241a3df62b547b0bd06a44b575186ddca25a6429cba`  
		Last Modified: Tue, 09 Dec 2025 00:27:22 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb81ac61fcda400739db86da69cf267afb4fb20f84ef1d427235b2648f06fdb`  
		Last Modified: Tue, 09 Dec 2025 00:27:25 GMT  
		Size: 28.8 MB (28808160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e01ccc6b17ecb6bf8153a7ebf23ca89f4715771a0495587027e7fa365e8ea5`  
		Last Modified: Tue, 09 Dec 2025 00:27:22 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:39e08eb698121740297f1c6bc77ca8bcee7b1b1c1a0c8aec0007f55f2f26744e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc474565a6fb04599fd649844f157bde240bb61d0f72e498536a0c5c9cbd82bb`

```dockerfile
```

-	Layers:
	-	`sha256:103ed802bb12710441bd4e5bba67d021eb12788669044255b3f2821f3c126fd6`  
		Last Modified: Tue, 09 Dec 2025 02:39:31 GMT  
		Size: 3.9 MB (3925315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e193543dbe71cd7b66ed7ac30284b13c594094ec74d401d98c8b9ec66e608d1c`  
		Last Modified: Tue, 09 Dec 2025 02:39:32 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.in-toto+json
