## `perl:devel-slim-threaded`

```console
$ docker pull perl@sha256:dfbfd148a4e2c68e4252aba7c3c5ae5bd143643991d78985de257a4e7a50bd33
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

### `perl:devel-slim-threaded` - linux; amd64

```console
$ docker pull perl@sha256:bee240c458efcab987a975305f7ee4710e207bb8ef739acfedbeb43015c263ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57840693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196c2b2fbc7d475dc2abaab391af4d68ebfc41debcd2538dce96dff972e61108`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03949bfe3a9431f88b8166859da28da2774e3ac3a7f6238f0c35744f124f750`  
		Last Modified: Mon, 22 Jul 2024 20:15:07 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f83349436e620cc54d4d81d90acb377f39a425d270804f43fd319b44de79b5`  
		Last Modified: Mon, 22 Jul 2024 20:15:07 GMT  
		Size: 28.7 MB (28714148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16973c477f756161c88ec29badcbaa894887bca1ac6d210bfbd83bdd15f5df96`  
		Last Modified: Mon, 22 Jul 2024 20:15:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:7e0359a3f46983567199389182b3b7d7aba0995f0345c26ca4a590bcb0d97417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa3d9a6f638f9e9842c80f072ca15e8b3330a875c4d0890fc6e46473b66902f`

```dockerfile
```

-	Layers:
	-	`sha256:e50144daf8cec946e868f3b5ae552d815f2e2b1754ce067c4cd43c7dc32e1e91`  
		Last Modified: Mon, 22 Jul 2024 20:15:07 GMT  
		Size: 3.7 MB (3741632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9df12ba37288b82763d52bc450693bf318c0df0b4603ef90f6d96003adc65a11`  
		Last Modified: Mon, 22 Jul 2024 20:15:07 GMT  
		Size: 18.4 KB (18421 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:565525e22bcce966b5116f935e6c6b3fadea14bd233f080e0e0eff905d02636e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53603935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a131babec711f384367ba2919f3040fc138d6b3621c5f94582f1dfbae8acecb`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:27 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
# Tue, 02 Jul 2024 00:48:27 GMT
CMD ["bash"]
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/perl
# Wed, 03 Jul 2024 14:39:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.1.tar.gz -o perl-5.41.1.tar.gz     && echo '7dee38af601b0ba3f3730cb812cdbc799c921da440cb0ce96dd7a4f508b1a6f8 *perl-5.41.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.1.tar.gz -C /usr/src/perl     && rm perl-5.41.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/app
# Wed, 03 Jul 2024 14:39:46 GMT
CMD ["perl5.41.1" "-de0"]
```

-	Layers:
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054f72d1b17de4aefa57a2b686eda3cd69fc6b62c160ac750a6f4bd6f2ae0d1d`  
		Last Modified: Wed, 03 Jul 2024 16:23:31 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410372e6f97a4a38ee89a2c46e7e43e329b1c52e438e02d1b8db4959d1148ac1`  
		Last Modified: Wed, 03 Jul 2024 19:40:04 GMT  
		Size: 26.7 MB (26716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95c272c1da596a9dbc71ef4c652c8221ef0d4a8aae51df5edc54b3f41d58406`  
		Last Modified: Wed, 03 Jul 2024 19:40:02 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:8c85b861cce054393b849dbebb572b21a44f4e27ecd04c6647a4fdb5548c4043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3708033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a41afd7ba69acbe12fb600caf1b8ece0f445f2245e8c3c6a752623d5a79157`

```dockerfile
```

-	Layers:
	-	`sha256:836521e44a1edc38920529e07e02c956ecc916a68b4505c6c0c621407fc07429`  
		Last Modified: Wed, 03 Jul 2024 19:40:03 GMT  
		Size: 3.7 MB (3689645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f529f19dbef6f34ec89a2c049ce5ebd975e69d9a00827c76efbc2b03858ecdbb`  
		Last Modified: Wed, 03 Jul 2024 19:40:02 GMT  
		Size: 18.4 KB (18388 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:7969053e7146e85f5f474bb802019a227330cf78bd2200ab846b3bfd2400d23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50650234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1b14086fb10fb26333067667c4e7bc001cd6739c60a08ed6940c8242834ce3`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/perl
# Wed, 03 Jul 2024 14:39:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.1.tar.gz -o perl-5.41.1.tar.gz     && echo '7dee38af601b0ba3f3730cb812cdbc799c921da440cb0ce96dd7a4f508b1a6f8 *perl-5.41.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.1.tar.gz -C /usr/src/perl     && rm perl-5.41.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/app
# Wed, 03 Jul 2024 14:39:46 GMT
CMD ["perl5.41.1" "-de0"]
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af963df78e4082e2f93e40fcc3ef5501fd998fbf9f6ef837fe9e4eef08d83de`  
		Last Modified: Wed, 03 Jul 2024 16:29:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ecfc00f4d7507362545d50d5e4f11c0384ee61bf40e6dcbd003e2830467313`  
		Last Modified: Wed, 03 Jul 2024 19:40:31 GMT  
		Size: 25.9 MB (25931797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb08b5c582cdd5ecfc6c911ac2caf97e60d72ff06c526a74143b3b290c18365`  
		Last Modified: Wed, 03 Jul 2024 19:40:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:15180a5b577ed3292d463e086655abecc61bd1405a194b4ce21c85796593b77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3707791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fbb582ed40840698bd0f7ab2c58873fc83f554c2a49aa36fca4b6ffe382ae0`

```dockerfile
```

-	Layers:
	-	`sha256:699972ce3c29c00604ca9167cb9bb63748f660e2477eff24a077367e57f64cc2`  
		Last Modified: Wed, 03 Jul 2024 19:40:30 GMT  
		Size: 3.7 MB (3689403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f37150b8547c6992a6d4eb23d4565e977b8bf36bfd89482aa1fdd9a4f197feb2`  
		Last Modified: Wed, 03 Jul 2024 19:40:30 GMT  
		Size: 18.4 KB (18388 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:d14a6d1efd045600b0946852bfeca989eeedc05f0ccb661f4c51f491769a30e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57580754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4fb54f3cf114fb1eb4ade93b0a319a6ff8dda5fbc222cf8e1e9bfd3f3aa287`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/perl
# Wed, 03 Jul 2024 14:39:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.1.tar.gz -o perl-5.41.1.tar.gz     && echo '7dee38af601b0ba3f3730cb812cdbc799c921da440cb0ce96dd7a4f508b1a6f8 *perl-5.41.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.1.tar.gz -C /usr/src/perl     && rm perl-5.41.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/app
# Wed, 03 Jul 2024 14:39:46 GMT
CMD ["perl5.41.1" "-de0"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18714cb77e8c769ffeb0ac4068ac412f0df8af172eb0c6ee57017dd29f1fa130`  
		Last Modified: Wed, 03 Jul 2024 16:18:14 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562ed8c12964f842c846fe5febf52cbebbe69fc266f9caac2f361c7622ceff93`  
		Last Modified: Wed, 03 Jul 2024 19:03:52 GMT  
		Size: 28.4 MB (28423924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dda3909478cd736cdda9af77a81a2225fc8000d3ea5bb90b3aa7da0aa1d132`  
		Last Modified: Wed, 03 Jul 2024 19:03:51 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:d0599f647ddb707cf9f46cd3326d455cc95e3b3eefabd105ec415087222e4c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a14dbe2ceb3a89cdfbea15e30f91c6d959673f524d1a023f93e0c201dca87f`

```dockerfile
```

-	Layers:
	-	`sha256:503f04e4127b11d6743abcbe2ebc7126447ac0d341cc6382fdf949a5de421de4`  
		Last Modified: Wed, 03 Jul 2024 19:03:52 GMT  
		Size: 3.7 MB (3690605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:404c354fcf421faabcde1ef084c35eef6adc6a38b1a5022c226c3a75c3b0de8d`  
		Last Modified: Wed, 03 Jul 2024 19:03:51 GMT  
		Size: 18.6 KB (18634 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; 386

```console
$ docker pull perl@sha256:565624b2b1cd110dc64550fa00b43ba2e6cadff7823cd38bb68adb77741afeca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57916019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85c46e57ba2257dbc65b9f62d0b263f620e83f6e4cf99b8c2d1268883b66250`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 00:38:54 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 02 Jul 2024 00:38:55 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e135bff641927bc5c8aa3872f9c5c7a52c1ee2fd49a2ddb7f13c5db0ead8987`  
		Last Modified: Mon, 22 Jul 2024 20:15:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4237c79c4c6e95a162a941e597caca5a5844d9d1dabe1285d3085d9378b4e9cf`  
		Last Modified: Mon, 22 Jul 2024 20:16:11 GMT  
		Size: 27.8 MB (27771479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9779396592b13f2366fa6dc7a6ba002f25284a20bad4c50400cefe1b14649bdb`  
		Last Modified: Mon, 22 Jul 2024 20:16:10 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:48dfd01346201dde8bdc9e8a1db04522643d0bf18bf75ce3292048694f175de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3753907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babf281865491459a627e9105ece121451beff8c5bfaff1049418cef4bfd1c67`

```dockerfile
```

-	Layers:
	-	`sha256:eb23e3f677feb5ea35b094fc29f9ea82e4b863948f7961a55a8db13ac5233ee6`  
		Last Modified: Mon, 22 Jul 2024 20:16:08 GMT  
		Size: 3.7 MB (3735525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50fd454aada7a015ba84098ee8923b2e3e693d9ee5d5ea7d709874db039f1aba`  
		Last Modified: Mon, 22 Jul 2024 20:16:08 GMT  
		Size: 18.4 KB (18382 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; mips64le

```console
$ docker pull perl@sha256:5defa51517d4873150e176f0332012454e028746a2de90d75b12b4a2b3e48a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56931406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682af580556b2e8060958f89be1535de9ddbe63db7f1c68ffe7a59a5f6f0f61f`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:23 GMT
ADD file:9a0f0c8ed27f6f2bb89272036da4d44a63dcaf43fb03528dd2d970fbe64ccc92 in / 
# Tue, 02 Jul 2024 01:18:27 GMT
CMD ["bash"]
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/perl
# Wed, 03 Jul 2024 14:39:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.1.tar.gz -o perl-5.41.1.tar.gz     && echo '7dee38af601b0ba3f3730cb812cdbc799c921da440cb0ce96dd7a4f508b1a6f8 *perl-5.41.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.1.tar.gz -C /usr/src/perl     && rm perl-5.41.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/app
# Wed, 03 Jul 2024 14:39:46 GMT
CMD ["perl5.41.1" "-de0"]
```

-	Layers:
	-	`sha256:cbefe199012545da86e0f461f1964dea0c9bab400e37766ee5f32b967423cf0b`  
		Last Modified: Tue, 02 Jul 2024 01:29:29 GMT  
		Size: 29.1 MB (29124929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e98d895105e0bd56275cb11711f34b173ed76fc0e049d6f426643b28e1932ea`  
		Last Modified: Thu, 04 Jul 2024 11:47:01 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934aea54ccca605b1bb716c3109b31b5cf6e2e4a1fad4884aaf8052a191b4fa9`  
		Last Modified: Thu, 04 Jul 2024 13:37:04 GMT  
		Size: 27.8 MB (27806210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3de05d34a38f7271705fbe39ec3235e1a3bb28ef55ce350f7b929faf576021`  
		Last Modified: Thu, 04 Jul 2024 13:37:02 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:fdd52cc0c6ee2289b2353711acb31ace8a8f0f51180f9d7fee2404bb6b1ce551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b26bf5c95781ea95565e12eb004ba27ed56d1f77bd2567acce753db33d72088`

```dockerfile
```

-	Layers:
	-	`sha256:eabf9fb1fb6b6859442108029a16c71a1b6ffded406d44b65b8a278fca7b70b5`  
		Last Modified: Thu, 04 Jul 2024 13:37:02 GMT  
		Size: 18.2 KB (18158 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:3987f37307122881fd6ffb910daa0f8d9e11cd8c8d118fd4c01b60e3b48bf606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63363926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b568e0c073eca171521fe18d6afc2f9defe981085f875ed461912eca991885`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:35 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
# Tue, 02 Jul 2024 01:17:37 GMT
CMD ["bash"]
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/perl
# Wed, 03 Jul 2024 14:39:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.1.tar.gz -o perl-5.41.1.tar.gz     && echo '7dee38af601b0ba3f3730cb812cdbc799c921da440cb0ce96dd7a4f508b1a6f8 *perl-5.41.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.1.tar.gz -C /usr/src/perl     && rm perl-5.41.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/app
# Wed, 03 Jul 2024 14:39:46 GMT
CMD ["perl5.41.1" "-de0"]
```

-	Layers:
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df76523bde538f7071bdb8b97ea71a72675926ffd79099660fdd48c1c2fd0126`  
		Last Modified: Wed, 03 Jul 2024 19:26:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e648b8f4a528bec1617e547657e193fc5d29f69fe81405567ed96df59c493b6a`  
		Last Modified: Wed, 03 Jul 2024 22:30:27 GMT  
		Size: 30.2 MB (30241382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee7d617b40aa5412507a4904f0caea1c7675f56681acb5fa04f0b5cd30aebb6`  
		Last Modified: Wed, 03 Jul 2024 22:30:26 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:c81fc48831ac63d327f5a181f20065afc3bda47308733a6168d3f6c1dd26738c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127901393d9ccca5ebb88be495f8251c18ebf87d2e9d263ca7d20b26d0d2822c`

```dockerfile
```

-	Layers:
	-	`sha256:5a0a066996fd8d116d86393e7e8ab8a8c914957fa90219517ab7dabfde2a7c7c`  
		Last Modified: Wed, 03 Jul 2024 22:30:26 GMT  
		Size: 3.7 MB (3705085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2e43944b547351c6db5f34ed6457ee9076247c0d631079bbb8b79a44f005db2`  
		Last Modified: Wed, 03 Jul 2024 22:30:26 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; s390x

```console
$ docker pull perl@sha256:fc30523ee9bc1a8b9e2e1c20ad56d69eea6f99261039c3cfbf71365261c6b199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55661771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a846417a2c9477d4f0f52070b1af8105504fe7791f03bf5b37bca3ebe1877aca`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:46 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 02 Jul 2024 00:43:47 GMT
CMD ["bash"]
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/perl
# Wed, 03 Jul 2024 14:39:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.1.tar.gz -o perl-5.41.1.tar.gz     && echo '7dee38af601b0ba3f3730cb812cdbc799c921da440cb0ce96dd7a4f508b1a6f8 *perl-5.41.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.1.tar.gz -C /usr/src/perl     && rm perl-5.41.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/app
# Wed, 03 Jul 2024 14:39:46 GMT
CMD ["perl5.41.1" "-de0"]
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95572dffeeb27b417d1030f4bdb3d7561b01ba80cb3180b3cfee6e3e589086f`  
		Last Modified: Wed, 03 Jul 2024 16:29:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627155562b80d308edf78ff8698608df94f3cf3d4fead3c3fef4882f54f0ba53`  
		Last Modified: Wed, 03 Jul 2024 22:05:03 GMT  
		Size: 28.2 MB (28171414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67d1201e4a089e62303e363bc5f524495628fba687d14e5ae1261fe50bfe2f7`  
		Last Modified: Wed, 03 Jul 2024 22:05:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:0e232caae5c3b6dc9a7780b224e7f288fec6baaaffdcee0669e2fa3fcd45499d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c341af07ff4af8c7cfcc1ee3fb2ee871804c65194f2ca24b20672d211e7de8`

```dockerfile
```

-	Layers:
	-	`sha256:7ddd0ca59977a66620370fc18770ff9d57426ed624a60beb68940db358835beb`  
		Last Modified: Wed, 03 Jul 2024 22:05:01 GMT  
		Size: 3.7 MB (3707652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c77c462c3f638808a8e039e1eaf5e1b11cc3a6553c73169586034b116f199be3`  
		Last Modified: Wed, 03 Jul 2024 22:05:01 GMT  
		Size: 18.3 KB (18302 bytes)  
		MIME: application/vnd.in-toto+json
