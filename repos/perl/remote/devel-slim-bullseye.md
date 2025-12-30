## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:b8e06adbdedd24f59c2b3556f466f2fd563f4321176b3336bf49e169f7ce7d03
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
$ docker pull perl@sha256:250e14f547b77c31ce152d3b9dec40d405031c5ea87d1fdaa0d54be5058e7b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56627035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2acf593a6f8d0abdd605e1ff42ba36f1dcb3750e42c15d1cda56ffde6512976`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:27:37 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 00:31:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 00:31:52 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 00:31:52 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ab5ea82374eaf02095a1df012db4d665e031567e3f222c4e028046e8ed551`  
		Last Modified: Tue, 30 Dec 2025 00:32:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a3aff9da12f95e139dcb882d1ecb03ee66be3bb9344158980e04de1519557c`  
		Last Modified: Tue, 30 Dec 2025 00:32:12 GMT  
		Size: 26.4 MB (26368328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59e86022c4cfefa678214cd4c6da7e183bc86d196968cf3bb1ee11f4ca30706`  
		Last Modified: Tue, 30 Dec 2025 00:32:10 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:42c85f5ee18b97b0974f1780209ec5dc38e01b500c2ffef3f8fad63cabd499c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4138881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9403d96a3f68d3dbe0189f923233797b3cb8499036f74ac57596d89b2edbcbf5`

```dockerfile
```

-	Layers:
	-	`sha256:b25eae52ccc93a6dabdb07eac4955415634c751a46108c17530dfdea9e0ea664`  
		Last Modified: Tue, 30 Dec 2025 02:47:22 GMT  
		Size: 4.1 MB (4120643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35a0693803121d6c7875dcd118601735883b7c638f793fc6f23e9189ee7e643a`  
		Last Modified: Tue, 30 Dec 2025 02:47:22 GMT  
		Size: 18.2 KB (18238 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:afd8f56698a68262689a9ed2b6d2ab22ad51e25a5febc164596d79dd8f0d8cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49165321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3f55de316cf9b3be4b84849f023d2d5f755fba6a283afca9baf5d1870451eb`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 01:07:54 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 01:25:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 01:25:56 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 01:25:56 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:157cb1ae1e97b073d55fa44e5e4ce17ccecf29dcfee2e34ca09a7de19793cf95`  
		Last Modified: Mon, 29 Dec 2025 22:25:27 GMT  
		Size: 25.5 MB (25546225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f78b7939ed85c561a5262f5935c0632078cffc2d1fe42b8a5611b4a3ed787c`  
		Last Modified: Tue, 30 Dec 2025 01:13:51 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6475336ad59f154959025f41894e9845dbe6963900d5e4908c96ab02a96ce1b7`  
		Last Modified: Tue, 30 Dec 2025 01:26:14 GMT  
		Size: 23.6 MB (23618830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6a2f152c21cf45b2b924a3b04c378b18196131050cd97ea2ffbb9c031a8e33`  
		Last Modified: Tue, 30 Dec 2025 01:26:11 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:316443a8f037003143544f63b91b03c6c45acd964c1ade3dbd68898141d18e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7cfb42f1540277dde433756fffab3ea16253b763f7b880499f2057bf0ec795`

```dockerfile
```

-	Layers:
	-	`sha256:c794a20a62287da985bd0ff65ccc976abb87f7547f03329641bd9ae7f600c439`  
		Last Modified: Tue, 30 Dec 2025 02:47:27 GMT  
		Size: 4.1 MB (4094632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d580b4503a79c59e76cd2df21f0513a48a117097c882982daf7002b063d4b18c`  
		Last Modified: Tue, 30 Dec 2025 02:47:28 GMT  
		Size: 18.3 KB (18309 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:9d9e43610b459ec5c53a9fb73ee004707840eeec4385ccc737cbc77d64ead7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54249738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ac500ce06b4664d050745fc006182ea2fb655a8f6ed72234bdd052e6e365b2`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:16:55 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 00:33:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 00:33:31 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 00:33:31 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99480bbf23bf2665cc646874094c7ad3c77f2b8d1c557b7a9e7f343e0890967d`  
		Last Modified: Tue, 30 Dec 2025 00:21:39 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb3582cc5c9e757f2c09739236b1d1aaed4e6b4607ec2b2e9a019ad868eedea`  
		Last Modified: Tue, 30 Dec 2025 00:33:52 GMT  
		Size: 25.5 MB (25501007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3aa478c8bf84d3bf077880d33dea6b696765b1747ec50557ee4c9999353ef9e`  
		Last Modified: Tue, 30 Dec 2025 00:33:48 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a69f07836b983d35757d572c1dcc4cfc8069e4c38ef1b3b1ddda87ac67aa3e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096e68e1de2f3e0cfa4e0969d99dc4bf6037bf148298bb9e5750b0398bd1d7cd`

```dockerfile
```

-	Layers:
	-	`sha256:e8b1f1d6b3ff9a2eb1f66845503c16279435e964b976a05f734da8aaf713d5a3`  
		Last Modified: Tue, 30 Dec 2025 02:47:33 GMT  
		Size: 4.1 MB (4095038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cab03894abf78b45da4dcafa798641c598eaeae8874fdbcc163f8be18ddb16`  
		Last Modified: Tue, 30 Dec 2025 02:47:33 GMT  
		Size: 18.3 KB (18330 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:2119c842af7ca777ee98bbee15230642202640831075d6f6b2b0fdd94de30a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59064254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0bed152a06b13b73769a4f6bf32c288a7cba211b2e63d391535edc1d953eab`
-	Default Command: `["perl5.43.6","-de0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:56:04 GMT
WORKDIR /usr/src/perl
# Tue, 30 Dec 2025 00:01:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.43.6.tar.gz -o perl-5.43.6.tar.gz     && echo 'c93a24d245b9f8e2a5bee6bc17d670f556ba3e75a3e090728b2210ec3323f136 *perl-5.43.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.6.tar.gz -C /usr/src/perl     && rm perl-5.43.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 30 Dec 2025 00:01:03 GMT
WORKDIR /usr/src/app
# Tue, 30 Dec 2025 00:01:03 GMT
CMD ["perl5.43.6" "-de0"]
```

-	Layers:
	-	`sha256:fa566a3e7b480e5bbc6006ae0d5a282051a1a92c7b8994dd11343ec7ed054045`  
		Last Modified: Mon, 29 Dec 2025 22:25:08 GMT  
		Size: 31.2 MB (31191561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f16ff59b024740999fa1620b3c4cf0257eb629e46d941626d9bf1cb2575677`  
		Last Modified: Tue, 30 Dec 2025 00:01:07 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39494f0eb1775f0bdb30d4122de457398dd48923135d020f361f5fb1e28c9afa`  
		Last Modified: Tue, 30 Dec 2025 00:01:23 GMT  
		Size: 27.9 MB (27872427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11ba2eb79ca7fa7f8b2d8d2758e6eb90e07d9edc61386f712d281781bc539c1`  
		Last Modified: Tue, 30 Dec 2025 00:01:18 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:d3097c7ce12a9196b151fac7678f0035cc9eb408d930ead1e9aac22ca59f5f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447e490fb9da71c4428049d0a8c22fbfea3c50f9a446a5e9f8cd34fe572e76e0`

```dockerfile
```

-	Layers:
	-	`sha256:698aa08a48ffa8384abf98fbf187636fa1e7415ed1084f6ea81856d57d8fede4`  
		Last Modified: Tue, 30 Dec 2025 02:47:37 GMT  
		Size: 4.1 MB (4124925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46857d30f0020d36ba77365a7f6c30840122175f24591332217a2235c53deceb`  
		Last Modified: Tue, 30 Dec 2025 02:47:38 GMT  
		Size: 18.2 KB (18211 bytes)  
		MIME: application/vnd.in-toto+json
