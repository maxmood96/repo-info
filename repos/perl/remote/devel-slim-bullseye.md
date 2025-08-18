## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:c42bd5ed52712e4fd4f863f684eef3e380f73066d4808bfe94fc7ebddb0f1016
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

### `perl:devel-slim-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:3acbccfec3913cb6c88c7e5cf75ce8114c09c104716b21380aae6f04bc982346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56429105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfe66e7fb518750d5ff2ca0b6a8ae7a05fc65d678965858cb5285c22a13c63f`
-	Default Command: `["perl5.43.1","-de0"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.1.tar.gz -o perl-5.43.1.tar.gz     && echo '5221ebf5badfbb943d168ff589ce93456a11f219105c930cc01e8a82a62adb65 *perl-5.43.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.1.tar.gz -C /usr/src/perl     && rm perl-5.43.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.43.1" "-de0"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2034e250ae0b455bd14768ca3e15370b13d0205256decd14ddb10e636bc244f8`  
		Last Modified: Mon, 18 Aug 2025 18:10:12 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c7aaeb80c626d03ce7a09ae316caecf682fcd282e1d46910ef778dafa0e2e`  
		Last Modified: Mon, 18 Aug 2025 18:10:14 GMT  
		Size: 26.2 MB (26172720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d1a11acdaff99bdad78d57ce7d67cff4614e75984b5cdb36c95305d01a3d4b`  
		Last Modified: Mon, 18 Aug 2025 18:10:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:73d87257d97c6aeab5a067a6ed9342dc72299e5fc4fc33f2c38024ae89bc5fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4138929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc84a29959b85d83d9520a4a5b3f416b4a6adcbdee58e31d8ef089108b5d42a`

```dockerfile
```

-	Layers:
	-	`sha256:11f44d939a3de5ee9409625283a8cef0fc91a18619f7da7f5b8cba4062e69c64`  
		Last Modified: Mon, 18 Aug 2025 19:47:25 GMT  
		Size: 4.1 MB (4120643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2a8a79ce6f83d77740e52553e11e1ecd2b592048b668713031153224457a52f`  
		Last Modified: Mon, 18 Aug 2025 19:47:26 GMT  
		Size: 18.3 KB (18286 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:a85258333b679d8b55a45f1e2193713e67fb14ff234aa787ec16a89a1dc7f0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48952553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0274ad828012666d48c744fc278fe28872162cd863a9528f232c3e934d5c397`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 04 Jul 2025 18:45:50 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/perl
# Fri, 04 Jul 2025 18:45:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/app
# Fri, 04 Jul 2025 18:45:50 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:42c6883fd732cb484051b4fff6157db32a689c12264945da05c930608a6fe450`  
		Last Modified: Tue, 12 Aug 2025 20:47:00 GMT  
		Size: 25.5 MB (25544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a568f17d68fef20cfc16e6b4267d7001c878d2865df4b827c77fe731a47b2d4`  
		Last Modified: Wed, 13 Aug 2025 01:01:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cdbca46f53e380c3c25578981bcfa7b025b0a863ae07ce6eb572c229376a44`  
		Last Modified: Wed, 13 Aug 2025 02:19:38 GMT  
		Size: 23.4 MB (23408169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4176d42dd111be56e7972dae2b4c8d79aa30b796adba1a790edef22e7fb29ed`  
		Last Modified: Wed, 13 Aug 2025 02:19:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:4d37a41b11e2c3196197ee96dc8bd2dd9b3025a323b24806c4c284041cfd686a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d7ff4aeb183ce4838df65ca4f2e6341f4a7ee617a2f698c09d56110d288d33`

```dockerfile
```

-	Layers:
	-	`sha256:2d887ee58b3dbb21bc2347bda42ca5d66ad0d13d4f0d30fcc92b1a5bfad8f46c`  
		Last Modified: Wed, 13 Aug 2025 04:39:41 GMT  
		Size: 4.1 MB (4094636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:328e81297e168f6e760184115baba6d10ab8813dfcb921f9edb2f3f00df33b65`  
		Last Modified: Wed, 13 Aug 2025 04:39:42 GMT  
		Size: 18.3 KB (18343 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:76521b191c99132b9921c4a887d5ecdaaa3ed386daa825e8db75d9f9004200eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54041216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8019472d8dd6872e6384efccdc2c06a53f1cdc696f5eb032404b18ed1d9808bd`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 04 Jul 2025 18:45:50 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/perl
# Fri, 04 Jul 2025 18:45:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/app
# Fri, 04 Jul 2025 18:45:50 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a56dbc48e0123d72bad7b68c1fc64103b17ad47b4e53b1d689d01c8e8f6579`  
		Last Modified: Wed, 13 Aug 2025 07:55:52 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37d78e82d222d165cb8dd9bffbae93ffda5159ae5d689f7c54da7e59f1bfc5d`  
		Last Modified: Thu, 14 Aug 2025 08:07:49 GMT  
		Size: 25.3 MB (25290458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b783294813f327738b546c3f39613a8d649f4121c2e8d0da2ea6b5d480fbbe`  
		Last Modified: Thu, 14 Aug 2025 08:07:40 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:8b85487492b964e744bb484f18ae32f6a299107fa7e5dfa934df637597e02ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1d9aaf9e7515957d1b9b3122ca0013d141b1eefd7c2a1fbefabdd8ff24f755`

```dockerfile
```

-	Layers:
	-	`sha256:8ce46175c596aefb8cebde3fb18974767a6380c388e6c449ec5b8d1d3d267bc6`  
		Last Modified: Wed, 13 Aug 2025 10:40:05 GMT  
		Size: 4.1 MB (4095042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0d10b349279084c4c44fb7800a93cc098d82904b643ba6eee955440f0bd2be3`  
		Last Modified: Wed, 13 Aug 2025 10:40:06 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:99a67c0ee60191f0a1ee927f697cadeeb841de9bc1dcd800db7369b2c67e7703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58874997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbea9e3e65aeca51db94ec1d69fe1d7a2e482fe5223aba12d976af851d943b13`
-	Default Command: `["perl5.43.1","-de0"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1754870400'
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.1.tar.gz -o perl-5.43.1.tar.gz     && echo '5221ebf5badfbb943d168ff589ce93456a11f219105c930cc01e8a82a62adb65 *perl-5.43.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.1.tar.gz -C /usr/src/perl     && rm perl-5.43.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.43.1" "-de0"]
```

-	Layers:
	-	`sha256:f952d923c30616dd90d420b9958914d214065718a4cbc33bd4dbc7e5e35712c2`  
		Last Modified: Tue, 12 Aug 2025 20:44:50 GMT  
		Size: 31.2 MB (31189737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ef7e92021e577adf60c5cf4965a6969b4ac914f682e5ec64d3ad5d83a99582`  
		Last Modified: Mon, 18 Aug 2025 18:11:59 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f695355b45dded159666b6e25c62e67a3197a2a95d41ecbe6a7ab08e84b80707`  
		Last Modified: Mon, 18 Aug 2025 18:12:03 GMT  
		Size: 27.7 MB (27684991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a7aecb1db5a74d25994567a4be82bf8411b06631f62826f646ea37a932cb3d`  
		Last Modified: Mon, 18 Aug 2025 18:11:58 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:06fb1f5fd2714dd894305290754ebc326464badccf22508676715d87a9e58ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1975866d741191f8fb22e4d5f540628a5708e90fc95a9a482fbef59ea6248eef`

```dockerfile
```

-	Layers:
	-	`sha256:bb708708e673e0511983c6928b005eb986a6fe2cf1452be618a737f1d983df42`  
		Last Modified: Mon, 18 Aug 2025 19:47:32 GMT  
		Size: 4.1 MB (4124925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ccec514399654fe57b0f14a118936feb3b3363644c0e76965d39f7ab2332fa2`  
		Last Modified: Mon, 18 Aug 2025 19:47:33 GMT  
		Size: 18.3 KB (18260 bytes)  
		MIME: application/vnd.in-toto+json
