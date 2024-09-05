## `perl:slim-threaded-bookworm`

```console
$ docker pull perl@sha256:1e1a033af50597a515c5bdb0031680ed87defcefc90708f4add14a09e08c6265
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
$ docker pull perl@sha256:20a61317b823dad6c321c186aa4026e1be838349cdf541cbec04935a73142256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57849559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93539fc05ae90d1d22e12fc7e6853dc1f22753c8f71ee2757d78bc4d9ac7c894`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f14495fefcef85466d64e83a33e76929784189fd7df35c153df4cececbdc980`  
		Last Modified: Wed, 04 Sep 2024 23:16:25 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ee40c4a67cf9e455f333603d73fc9df81785ac88b47fa518a00d14af2873ab`  
		Last Modified: Wed, 04 Sep 2024 23:16:48 GMT  
		Size: 28.7 MB (28722812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38072d92e6e59d002cb6f7e42ded801eb55062f8ec9c577ea3b2ad50c9b93670`  
		Last Modified: Wed, 04 Sep 2024 23:16:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:e43a3d8881f3fafdb150be110c9c7dd667ff75551d7617dccbef14b31252b86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3763035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea124e2c908a72b1c26af988eef0f5e9acc40fd303df1f2c26f3a44ebe10491`

```dockerfile
```

-	Layers:
	-	`sha256:9b068046bbbc025c577da432209b8a1bc429e873c96360bca53ba7cd24dee09e`  
		Last Modified: Wed, 04 Sep 2024 23:16:47 GMT  
		Size: 3.7 MB (3742916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c2a38373a283c4ec57bd75e13bfa983bcfc02075a480ddbe72f5854d358b817`  
		Last Modified: Wed, 04 Sep 2024 23:16:47 GMT  
		Size: 20.1 KB (20119 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:d5bddfc2ef9b5035106323fb643851cce90566c8827ed0a3b6c62e686860b62d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52698360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e7d81b9296f7657d239b7a7a9db9a1f3cf586a3b8da80a770513b3e90299ee`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83e3763c3015113b5770ffa9e9254b4751b03fbbd833e55608804eef4fdf7d5`  
		Last Modified: Thu, 05 Sep 2024 03:41:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f12624bb23248cd8dc7234eaf8b37d682114c7e4b066b3b1800aa1548bb2a`  
		Last Modified: Thu, 05 Sep 2024 03:55:11 GMT  
		Size: 25.8 MB (25810685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03033603a757ff9d6491daa7d418b3f84ba2b425f6f59d857961fdfe4a7ee758`  
		Last Modified: Thu, 05 Sep 2024 03:55:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:6f1d0efe077eace5d0a3bfd283d244308124cf76562e91eb48d4677653161d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2ff50a3a49b14bec771916acd94402939465e65a3b891ae4cb71ee2f523f41`

```dockerfile
```

-	Layers:
	-	`sha256:7b4af4d2a541a50445faf939e82e5ab12566dfbcf39b3a0183dc5043d6cc54cd`  
		Last Modified: Thu, 05 Sep 2024 03:55:11 GMT  
		Size: 3.7 MB (3713354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:670949bae9b9e2cab4ad1dcdd57b040571fbe283ad9d9d61f730d0e38284fe52`  
		Last Modified: Thu, 05 Sep 2024 03:55:10 GMT  
		Size: 20.2 KB (20237 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:d2b20ed4d7b086b95d269934131fd7120975d267685741dc0f480a9d2a4c1afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49727988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98194800d68c2f905ab08a55e21f8c6b1a1519be81baa434e610a4c5de7dc61`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286f85eaac31ce80d7f89c91985374093e44d6e26b6a84dc28cda35148727505`  
		Last Modified: Tue, 13 Aug 2024 12:45:56 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e706fbc53cab12a03a6ab1f8d0b291d71aeb45acc3778b24ce28c3ac2314f060`  
		Last Modified: Fri, 30 Aug 2024 18:47:59 GMT  
		Size: 25.0 MB (25009580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be88e9017965c2fd6f3a0640080c260b69d1218052bd7007004ac845a41c6eb9`  
		Last Modified: Fri, 30 Aug 2024 18:47:58 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:7c192fda36eb47937341ed8d9e8bc8a68c2e4fd6af0338f878db287d96cf6930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b4a70ec8575fdd3e15256edce27e8315da4e867397e35e7eb5df5435164c95`

```dockerfile
```

-	Layers:
	-	`sha256:97ee29eeba5d434b857186a9f29cf674cb307594153b14023494755591faffb4`  
		Last Modified: Fri, 30 Aug 2024 18:47:59 GMT  
		Size: 3.7 MB (3712965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3ed39ac47b75f4786b33963698ce43c931fdcaf6e89fceed7ce492ed08646e`  
		Last Modified: Fri, 30 Aug 2024 18:47:58 GMT  
		Size: 20.2 KB (20237 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:f77f0e82443e7f482f166296221193192f6119e40a0dbd7007ffe9fc05d5b153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56657893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d1d887fd27eb2e13d0d5791f35af63317de51cd4cf4329537349d0a6bfddf0`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab597e8392b11fe7ca4a47cf01a5b0a45a3b02007f73ee9ff0b6caaca32b7fb`  
		Last Modified: Fri, 30 Aug 2024 18:14:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a103ebfd890006d7ac4f74746996758a7c87ed285de1401e3db143cc025be1`  
		Last Modified: Fri, 30 Aug 2024 18:38:31 GMT  
		Size: 27.5 MB (27501096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36cc23095564be2d41b750e84d7e8a17df9d2ba4ae77b620a13d66d52188661`  
		Last Modified: Fri, 30 Aug 2024 18:38:29 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:36da8dc74cbfd1f6e71dd0ccf69898345ea6d487ad807d966ac4aae819a144ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3734683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86bc825a382a1fe60ca3a1c18984dacb096f77b9f049663a469bd55f3220fe2e`

```dockerfile
```

-	Layers:
	-	`sha256:9c7fb3367b7426ddfcfb34fd95f3d6c8a59aedda6a40329bbf15a1a3f84c5bd4`  
		Last Modified: Fri, 30 Aug 2024 18:38:30 GMT  
		Size: 3.7 MB (3714183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6aab22ffc7ff509fe8e95fafcb55da3ebf0784d1328a39d2aad312e3365dd57`  
		Last Modified: Fri, 30 Aug 2024 18:38:29 GMT  
		Size: 20.5 KB (20500 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:b326c4e8b8e85ef8a5f5700324609b8851d04cd6de8bb13ec1d4233de0a9eb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57919758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aad06fdb2a592ff01c415de1110b08e6760ba8fbd3cde77f657caaeb1e8ee3`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf74852a23e6321533ae200c2cd9bcd7a09175c98a9e0679cdc282050c615554`  
		Last Modified: Thu, 05 Sep 2024 00:27:01 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a426183f3964d63e5701d3738fe09dbc1e6a313e284578c09643f7c9591fcd9`  
		Last Modified: Thu, 05 Sep 2024 00:27:02 GMT  
		Size: 27.8 MB (27775199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe6c8697ed37e5575e2e6c15f5a51093462676942bf2b486942e2cc5f65bbd6`  
		Last Modified: Thu, 05 Sep 2024 00:27:01 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:408cad4e830d8aa244508346acc343e3346373139e945d36c015a0bd9fe850ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b917e3ab7484c1ef5e19da8208e35d385e228b1ef3b55313e6f1fe5a508e8413`

```dockerfile
```

-	Layers:
	-	`sha256:a56724203ffd6f1bf9ea05eff64a3249bda2d15957df5593b5e0b8a230cf3e34`  
		Last Modified: Thu, 05 Sep 2024 00:27:01 GMT  
		Size: 3.7 MB (3736789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:447ae6e9f0b8c2374fbbee0eb0407fb430b16663dedcae23b96b050e388ad987`  
		Last Modified: Thu, 05 Sep 2024 00:27:01 GMT  
		Size: 20.1 KB (20060 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:fbbd137680bfd8b5167d187f7e299e71c3bdc39e3a34808a93541b0c8bc29fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56014193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28768e114d310db7abe4cd86d2a1a61e9e07f3ccc8f1b52b1e13671582aa01ec`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:09 GMT
ADD file:2fad80cfc89f7b624d81eb445f9c64e4cd3f190b85d89f40c33eb7e4bc562c6d in / 
# Tue, 13 Aug 2024 00:11:14 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:e8ebfef8c6b7f6250b54eec0d5d1ae5d66f60f418704f4094cb9291dc214be0f`  
		Last Modified: Tue, 13 Aug 2024 00:22:29 GMT  
		Size: 29.1 MB (29124941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbba02a877500d4e9aac9fe733acdfaa6eabbd68deb911fde6ed7063aacaf7e`  
		Last Modified: Tue, 13 Aug 2024 20:56:23 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdb422328ece0a06fbf0afc9f816fc75daf6665aa8f7e84aae31650357623b7`  
		Last Modified: Sat, 31 Aug 2024 08:16:18 GMT  
		Size: 26.9 MB (26888984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7053db84a8b98848c7d67369d8f911515a529b700827010041f52473d6e60649`  
		Last Modified: Sat, 31 Aug 2024 08:16:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:25980a2c0f0ab5b94384d39403a9f1f9233be9bafef93a79bb20947fc09ed21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d20f6707621bad4b3050460c3e65fd6bf2f1f65b8d40f301ddecb99d72b76a`

```dockerfile
```

-	Layers:
	-	`sha256:cff0427b39dc61a6e6b3185b71c75d3d74d5f110efc1378b29cf3759cda9326b`  
		Last Modified: Sat, 31 Aug 2024 08:16:15 GMT  
		Size: 20.0 KB (20011 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:0f0a194f070aa521d649c70cc5ce28af24740cd53260dec0e4df13145310225c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62454304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec990faffda25aa35829c3af0c4a6c1228e15db04915d63e9db45806c1689cc`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e077182d775e08c3d4709ad38c4d0dfddf9316046cfbdc0c6ec9550cc2b8b0a`  
		Last Modified: Thu, 05 Sep 2024 01:21:57 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f910fbcda431e4c4b5a9cc42824e162df29cae773b8b32e543aa637e7a3eabb`  
		Last Modified: Thu, 05 Sep 2024 01:36:03 GMT  
		Size: 29.3 MB (29331681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c750069ca03c410d2b21c053cee08f23c1596e58d19a70b6b45b96b68a0be4`  
		Last Modified: Thu, 05 Sep 2024 01:36:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:1cb91e89b87e811c098db021247225bd72261cbd8f417be12b1b91f3297c7b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f15d685d3f206ae8bb776883f5b6b19cb8ef27cddd6418d835f878b09f83c4d`

```dockerfile
```

-	Layers:
	-	`sha256:08cf361223aeb528928dc0f30681663c0054654f476fd4d7e17be3c0142f00c1`  
		Last Modified: Thu, 05 Sep 2024 01:36:02 GMT  
		Size: 3.7 MB (3728643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f34780e110adcb7e82affe1c7211e9d1c1d424fd3d347643595cd9097e88ba61`  
		Last Modified: Thu, 05 Sep 2024 01:36:02 GMT  
		Size: 20.2 KB (20193 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:bc6f73f7f2ff91d5cca398e506132ea0e408fa2959b3889d31883570ae9009c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54749985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d948d08ad43e48602f343e9cf2849cd5bb6c36f872c034604706d3c766f9a05e`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5b4928b2a810fcd721fc12f54789a0998cd9ed5bcf75e1459afaa9c8100ea7`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d5f4a5c4b3e8c5c6f4fef12734ec96d0842f7921ce7741a5252a9c4e299203`  
		Last Modified: Thu, 05 Sep 2024 03:24:01 GMT  
		Size: 27.3 MB (27259400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516aff72a4e06081a3181007b75da43a00a75d73d5026d700f42fc844ece5980`  
		Last Modified: Thu, 05 Sep 2024 03:24:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:4a93f18ca2f8404ee09649948a471339b384bc429ac7a7709b38f2cd0042c1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3751305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbbe451c17caaa245937aac1563714b34c3dc430f79e872fb7cb9059f409d89`

```dockerfile
```

-	Layers:
	-	`sha256:fc07f21d2b6dc089c395633c80128d5d9b9739f7b8833474e640fb869eeb900e`  
		Last Modified: Thu, 05 Sep 2024 03:24:00 GMT  
		Size: 3.7 MB (3731186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61326fb2603bd91fa77763829bbd775f2f9de0613f9e17c2fb2159c5f3be3469`  
		Last Modified: Thu, 05 Sep 2024 03:24:00 GMT  
		Size: 20.1 KB (20119 bytes)  
		MIME: application/vnd.in-toto+json
