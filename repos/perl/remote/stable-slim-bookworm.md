## `perl:stable-slim-bookworm`

```console
$ docker pull perl@sha256:453997e9206d6c8fc6ffbb312167935aaa0abe8f658882a5a9e60efbd54f9bc6
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

### `perl:stable-slim-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:8c2066b142570609bee2819d78643fc93f55bd6c4f3bdeb4d6accc6a9314d0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58356976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226873daf2de29c99388199ece616dd069bcee8802015228ef0eac9ed5773e45`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Fri, 13 Jun 2025 11:40:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67755a24dc2bda98db47e0a35e781d9ee3f2bd53d72b3bdae8f57f2baf4023be`  
		Last Modified: Tue, 01 Jul 2025 02:39:40 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419c8e56b0e22efd8f3ba88caf38dd334a840cb1cb802992b808ceb3b647aa3a`  
		Last Modified: Tue, 01 Jul 2025 02:39:43 GMT  
		Size: 30.1 MB (30126566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f657611e11ddf9381fe88fb24cc2f412cb2f8a1f1911140ae623bbf09ef78c`  
		Last Modified: Tue, 01 Jul 2025 02:39:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:f405c7dc91da02e68354970a826de10d9dee46d5660e88138776eb38608aa94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3959632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76902808e3382361f068493791755567c3698244b6b009dc78b3ef382c20b3d`

```dockerfile
```

-	Layers:
	-	`sha256:cb6c1b8f2dea785386ad88c9b141638db98443f67bd754108c8cb6ce807ecc58`  
		Last Modified: Tue, 01 Jul 2025 04:37:29 GMT  
		Size: 3.9 MB (3939329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf2e9625211dd2cf29e84ef0588a4c8daa430a4be3d32bea0310a03b514c12bd`  
		Last Modified: Tue, 01 Jul 2025 04:37:30 GMT  
		Size: 20.3 KB (20303 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:cfd58ef720ac264a276627e2cfbcbdc4eae065d73f8197a7afaf447a52606153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52957935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f116c2d6317865c26294b6f2035c0de246326368091dd613947dcc66214278`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Fri, 13 Jun 2025 11:40:07 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4511ee95dfee2f66b1ff93d9d5d4a6f1954fb095a97c5630de00b520815e8064`  
		Last Modified: Tue, 01 Jul 2025 06:32:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd318808786c37443b30e56075101a80590ce5dbdf41da5d455d8ff65844450`  
		Last Modified: Tue, 01 Jul 2025 07:10:30 GMT  
		Size: 27.2 MB (27195209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a423e3068d43c4b57989bd5e24e05ca11ce016ce3c592873f5e55ee80af8709`  
		Last Modified: Tue, 01 Jul 2025 06:32:20 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:383262565403821fc0ed43e584e162de1a3c32ff6fbc370181a4928988949487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da554d88f4e03c1981b19ec86d003fc85f6b72ac70cc0dda6651d89768b79cf`

```dockerfile
```

-	Layers:
	-	`sha256:2240494aad4071bcc110d089c1d6f1c635821ef3aa11b6e076cfc8f083c96596`  
		Last Modified: Tue, 01 Jul 2025 07:37:52 GMT  
		Size: 3.9 MB (3910236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8023c0b16898258006b1d65d9bbe07546adf3a0e359ac536fd73f75327cca645`  
		Last Modified: Tue, 01 Jul 2025 07:37:53 GMT  
		Size: 20.4 KB (20427 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:1471140fece9788754a7a2687fe195698a0b273e8cda1ce02d32f407a636d92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50221153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eea730dbf6a6a5afbfda650c66791bc144d8354908b7b8bbcddaf39cc670b2d`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Fri, 13 Jun 2025 11:40:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5e8e7b506cbf60b04a8861bfbbe1b389cbc01b7565ba1452a7ace7f52b27f0`  
		Last Modified: Tue, 01 Jul 2025 09:33:58 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3c7e63da672289547dca4bf6f5f20674a00d3ce24a8e38b78524c810be39e7`  
		Last Modified: Tue, 01 Jul 2025 09:34:02 GMT  
		Size: 26.3 MB (26282144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad6ab4edf2969d7c953fde0d9db6d47c41716063550d6cb7f507cfb3e47d862`  
		Last Modified: Tue, 01 Jul 2025 09:33:59 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:facb7eea85f702fcb2470b195b83f3062fb0ff9c8acb8ca2994c481d13944904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d732c65e739fc5452f3de2be8874e42916488d56c3912d04fa2e778a0b395ba3`

```dockerfile
```

-	Layers:
	-	`sha256:24de79b85f21f334454ffe609839678a7e511398a84a2ebe9a8aefa01cd59695`  
		Last Modified: Tue, 01 Jul 2025 13:37:33 GMT  
		Size: 3.9 MB (3909461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44d68cbe066525dde78e1d043b65e2e29b19aa20cfd010e3c0c77ee58df4ff1`  
		Last Modified: Tue, 01 Jul 2025 13:37:34 GMT  
		Size: 20.4 KB (20428 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:43f9a8d24f8d41c936016d66f76b35521fe11a8917222b2aa66d1b53be0cef5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57023544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbceadd6208430da8b336012669e9d66ab110f5c947394d068c878e612ab6fe`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Fri, 13 Jun 2025 11:40:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8095aba573b9b6bbc07db9c7b14e44fa79c1ef3311ff4340492eb85307ef4519`  
		Last Modified: Tue, 01 Jul 2025 07:42:08 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4da45d60a8806272ad71b51f14b688eee6d9ad549c536db3319665c6c0d77e7`  
		Last Modified: Tue, 01 Jul 2025 07:42:12 GMT  
		Size: 28.9 MB (28945600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5adb6074509c09fe8aaee3f12bb16f29ac691e0cf4f1d41967e327aaa22dca8`  
		Last Modified: Tue, 01 Jul 2025 07:42:09 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:36e2f93b1826233eef3d8611040bb4d662e05c4a02554629c6eb972534ea7e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53cb5f419feba635609e0b39b79b13f3834edea19f10d63f4a6f01c88c12864`

```dockerfile
```

-	Layers:
	-	`sha256:0d5de44ca091cf6a0d9b75196166c92080a4ae4e7952ab2a21af6659a934b633`  
		Last Modified: Tue, 01 Jul 2025 10:37:35 GMT  
		Size: 3.9 MB (3910650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:058d8e3ff76a759055b723483e2d542bc63a143a1872c9224feafe2b8cb3e2e3`  
		Last Modified: Tue, 01 Jul 2025 10:37:36 GMT  
		Size: 20.5 KB (20480 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; 386

```console
$ docker pull perl@sha256:2071f18cd33dadad2b8bf80bb10f2ce9f6cd3ed4256c07001807bbd572d480a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d23c0ecaea1445da9084e41056bfe1fab9c3030fffb573dc3d68f997a126a9f`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Fri, 13 Jun 2025 11:40:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7a4f3d2ea523dee7fa7aba5d99bd8a1d831b6300d15f7e2e54fdaf35d41540`  
		Last Modified: Tue, 01 Jul 2025 02:33:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3e15f35788417d7ac622f8418ba7e381238508fe25bb1b38bb1a63e4943345`  
		Last Modified: Tue, 01 Jul 2025 02:33:57 GMT  
		Size: 29.2 MB (29245998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82699d4ddc6c27540ac4145a5f8f17d0a997e84e84c3c824d7f2de50780768ad`  
		Last Modified: Tue, 01 Jul 2025 02:33:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a874cf096ed2c3d56542a660654919f6e549d535980d895be990b431b80331c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07a3dd199410de6178d4bcf5ba29d728c20b23ad2cde780c11a11a1f30e1a3b`

```dockerfile
```

-	Layers:
	-	`sha256:e4463ef06dc78e8d0c5ba4d36bc2aea9924562ee4ffb0634551bbefdf262a307`  
		Last Modified: Tue, 01 Jul 2025 04:37:50 GMT  
		Size: 3.9 MB (3933236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6093c3692db96b94efb094d7af261267d8b5c3f9e11bf15f996851ffebe555b8`  
		Last Modified: Tue, 01 Jul 2025 04:37:50 GMT  
		Size: 20.2 KB (20242 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:8d8c2d1b59cf9776d5ab097594575418d27528100888b7468c3b6fa416c1f803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56805543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea22ee00a35ed5712f890a960fdb1d11518ba200cf9c4bdcfd5881b1b5d5bbec`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Fri, 13 Jun 2025 11:40:07 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:fcacdf0767dbc0b08ad73fb46ff36dc2ec6b87367debc1e5018464dc1d3d7035`  
		Last Modified: Tue, 01 Jul 2025 01:15:02 GMT  
		Size: 28.5 MB (28516734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f323c54b98bc377b877eb263c1272243cc436f8a9efcebce96c7ff81a528d2`  
		Last Modified: Tue, 01 Jul 2025 20:09:54 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4391b3840e74fd883c3f98e76ef8acc0bd164973e031968845962e63eca47cdc`  
		Last Modified: Tue, 01 Jul 2025 20:09:57 GMT  
		Size: 28.3 MB (28288545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc26e1bfa2da17085bdef2bdaec7ec322892b427e0f0fcb901ee732312c62bd`  
		Last Modified: Tue, 01 Jul 2025 20:09:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a835516236700b5d6fd9d26fc81b1482d663ea2fead84ffb2ee06ca6a802939d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a45f54ea857f339db619dd5221cfd1ea40e7625b68a0fbb2da5531219147b2`

```dockerfile
```

-	Layers:
	-	`sha256:bba71b42ee31bc71f47a0d9790ccfb64de81ca50c3bce4b09ae5bcbbb842e9c2`  
		Last Modified: Tue, 01 Jul 2025 22:37:45 GMT  
		Size: 20.2 KB (20209 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:c60d8439aa7eee4eb0c59b3999f0a94f2b10b2c5241c1373f846cae30a643864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62995874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1de42c3c8700640128217c30a4632062b7faaf02956fc4538670adb011688fe`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Fri, 13 Jun 2025 11:40:07 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e7ff39486a88d583ebdeef332f4f2d635e6d6cd422f17bd6ed0390499dde6d`  
		Last Modified: Tue, 01 Jul 2025 05:34:45 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5360da8031a4e73eb407a2146d199d4711c90a95e8347369b8b5e5a854c3c56`  
		Last Modified: Tue, 01 Jul 2025 05:34:46 GMT  
		Size: 30.9 MB (30922790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c01bad3b1c6e0ba717de9db787d0a7207bfb794dcdec29c2865b4d167f420fd`  
		Last Modified: Tue, 01 Jul 2025 05:34:53 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2bb05c4135d8dfe2d6e59095e970879a36a8b95d283f3e3b55d259875439654a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc10098c7cceaa70bc7b3a60930012ce9391bc6a1cb4cdb8dd0c775dcdc07af`

```dockerfile
```

-	Layers:
	-	`sha256:b4236b4cc90c6936956dfd95c434477dcea9ef3342f9bbb59de19dd3d530a654`  
		Last Modified: Tue, 01 Jul 2025 07:38:08 GMT  
		Size: 3.9 MB (3925299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5779d0a639c51cc79145ee354457ae917ae0322235d41a7f78d0d0494c20a54`  
		Last Modified: Tue, 01 Jul 2025 07:38:09 GMT  
		Size: 20.4 KB (20384 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:eb59d7bd9562a797e58e59e1c4afff7a6e69367c5b01d09bd0122adede405848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55554269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b47e8960a04a2dc509863e2a8e804223fc282919a14c78900d7e6c6c9b9b05`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Fri, 13 Jun 2025 11:40:07 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7022c2a575cc3a4d77de9e30c953c17d2779132b4e4d4b1f45bfa0cdc946079a`  
		Last Modified: Tue, 01 Jul 2025 06:00:04 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e433957f5a4dd6f6ee20fd14738e2866f1a1a0512ee90164464b6fbeb0ec05b8`  
		Last Modified: Tue, 01 Jul 2025 11:16:02 GMT  
		Size: 28.7 MB (28666193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7da6f30c479f97a974218fd03dba7f783f276d7e9a8e8761cadf5ee70575e7`  
		Last Modified: Tue, 01 Jul 2025 06:00:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:45334b628681b6286fff57e1115a40512252cccf02d0dabb41fa8b3f5bde6d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc4f163c4b2a36c4164f62ac0a8dd14c53f89430fa63dece25b399deeb2a178`

```dockerfile
```

-	Layers:
	-	`sha256:9d2b1645a6bc540070c5cad5903d776894f4f640404874a504c34f143cff4b9b`  
		Last Modified: Tue, 01 Jul 2025 07:38:13 GMT  
		Size: 3.9 MB (3924602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb220d15117af45cf2492bcf23b8928f1d6ac245cdc93ab0a395e207a68252e`  
		Last Modified: Tue, 01 Jul 2025 07:38:14 GMT  
		Size: 20.3 KB (20304 bytes)  
		MIME: application/vnd.in-toto+json
