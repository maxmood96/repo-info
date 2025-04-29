## `perl:slim`

```console
$ docker pull perl@sha256:5488d86b19620bf67e325240c511cffe2ab10e029f9931c8f0139c06c698afe7
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

### `perl:slim` - linux; amd64

```console
$ docker pull perl@sha256:d290a84726f5b34ed4fbd107b20dfaa0f72b5b0cb7b22ae162242a29141ff694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58332723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85dc3824ae82f35a71d59e2f7aabdb388f47163d41a1aa8ec871125edb114710`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Mon, 14 Apr 2025 09:33:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e731922d9487406a545f0d65a12c29fcdfd23ac038e39ca422987d96c06f2b`  
		Last Modified: Mon, 28 Apr 2025 22:06:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9d2310d380aef6c091b26f8201b7f24bef6bcdc5695ae26053980513e40fdb`  
		Last Modified: Mon, 28 Apr 2025 22:06:22 GMT  
		Size: 30.1 MB (30104815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2005631286a01a425797dbd9cfe2cfe0e09b8f9abd436854956df50b67c0634`  
		Last Modified: Mon, 28 Apr 2025 22:06:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:a1e39c17acd8919ca5bb6b2d0a9c68cda367c3202846aa385e833b2e8fe88960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec49901317aacbf6cf1de4be0b841526ccdbdef5761d60068f040f8b1ca4076f`

```dockerfile
```

-	Layers:
	-	`sha256:41842c0ba551516b71f268228690d344f70687c21fd373d7adefe98d72ac87c6`  
		Last Modified: Mon, 28 Apr 2025 22:06:22 GMT  
		Size: 3.8 MB (3810574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58e592ec5c710be01e49577dfa3b0c74c6f6cebb6a20575f8ac895bd92eace53`  
		Last Modified: Mon, 28 Apr 2025 22:06:21 GMT  
		Size: 20.3 KB (20304 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:e7b72851803d7ac5cfcf21cecc9692e81b6f5006cb78f9ef82bae8534c5d66fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52939213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e01ab20d771a66cfb14bee7d855ff79d004ddeb41630e8cd7a1fd57cb506d5`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Mon, 14 Apr 2025 09:33:51 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:3bc532ff9d2a2a12c6cfc746359843257a240960865aea7ecb10c71e0b93ec78`  
		Last Modified: Mon, 28 Apr 2025 21:07:56 GMT  
		Size: 25.8 MB (25757836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16ba8d6a09db44d1970c26cae525ced899f77cbf99e63167d106d6fd49c60ae`  
		Last Modified: Tue, 29 Apr 2025 00:56:30 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955d4bce4b92eda1cef8420b595d59d0f703de106a86d1d1ad6b2d649e4e23c6`  
		Last Modified: Tue, 29 Apr 2025 00:56:31 GMT  
		Size: 27.2 MB (27181110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cdf900bc9f8de9fa31a1bca1671e43a05b288abc5dbf40d03d25240ea9bc5d`  
		Last Modified: Tue, 29 Apr 2025 00:56:30 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:fafe296e9578a057dc02fdfca04279b37db2c5694eed6590af8968bca9174632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98237ec62edd313605176dfc1eccb9b114b6ce8452a605983aab5f4ec7e72812`

```dockerfile
```

-	Layers:
	-	`sha256:65ffc246103ecd3f5e907a07d02cbd7dcf182976bfec7dc84c69e7dfd8b9bcb9`  
		Last Modified: Tue, 29 Apr 2025 00:56:30 GMT  
		Size: 3.8 MB (3781173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530ed5c8f0158243a7f995311ee21c5a60c9f2f0c8684d1d671b49f2659c879b`  
		Last Modified: Tue, 29 Apr 2025 00:56:30 GMT  
		Size: 20.4 KB (20428 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:5f14b9204123e458ac6ee194252f2f3b7a11bc4546ecb6b6046da21ea5563d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52322735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b13c9cbb6b9562cd09bc285e5ebee9b2d512d6a36a3fe6f931b2137e4629a97`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51325a5a56bacbfd755f949f8154053778cdbedbae006a44a4435af077d8cda8`  
		Last Modified: Mon, 14 Apr 2025 18:00:31 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d36eef66bbf5b7c53a589a62e9c55734a92505c7c83d3980cf4c79b5f4a72a`  
		Last Modified: Mon, 14 Apr 2025 18:00:32 GMT  
		Size: 28.4 MB (28384602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46db1b44c52e23a7a8a59284ff9f836026f68de6f373ccb25b06890d18566a7`  
		Last Modified: Mon, 14 Apr 2025 18:00:31 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:c1b4f198fb6705e8c5e0ff3495aa9eaf29339e132b57c80b08f1a4adb5c298c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9d45066025d7a59b4dcacecaaf0a6ec5582448c14a8770ca887fa3a747ec7f`

```dockerfile
```

-	Layers:
	-	`sha256:51064b6bf3d072d4ca2c78bfa624fc64a7057f5c635edc675a6c6144f52c2a88`  
		Last Modified: Mon, 14 Apr 2025 18:00:31 GMT  
		Size: 3.8 MB (3780706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b08231a1ee9b0009c26ddc1b93768f46a770ac6aab21ff43c01e1dd968eff224`  
		Last Modified: Mon, 14 Apr 2025 18:00:31 GMT  
		Size: 20.4 KB (20428 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:45443a920534847f4ce91a2afec69b558c476ae03a5d1b6d5e2f7aa6c1918aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59261586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744f3b260a2876d7831aa96988747826e116b123679125da488acdafce775401`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109af97fc9ba3f4cfc1ca6280c2b9d8d1a4adfdbc26e9e601249458a02d5eb6c`  
		Last Modified: Mon, 14 Apr 2025 17:55:17 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b26b3ccc13d25d65c0623cf797a84d2f579bece04d1ee2928934bee5cca4cde`  
		Last Modified: Mon, 14 Apr 2025 17:55:18 GMT  
		Size: 31.2 MB (31194998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74613b2a95c139a5784711a21a11a47db808a288f984f6ef4735540009e26851`  
		Last Modified: Mon, 14 Apr 2025 17:55:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:1abb4ad35d0968a6eb4f3c1a3c894dcb29532c4a5110b105262ef1b52bdea878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de65f5d3a2af59a4e707450088d931cf70eb35562f3cf9d7531c2247d3c8401`

```dockerfile
```

-	Layers:
	-	`sha256:fe288eb66c5f2aa450a24ae002305200097fa2d8f8d4250c1c009a73084a70d0`  
		Last Modified: Mon, 14 Apr 2025 17:55:17 GMT  
		Size: 3.8 MB (3781895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d0466469f3c1aec8067d0a49f6c1e398792a93ca590e9dfe5500136b48e983`  
		Last Modified: Mon, 14 Apr 2025 17:55:17 GMT  
		Size: 20.5 KB (20479 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; 386

```console
$ docker pull perl@sha256:202685d6cce60bbed3e8f65eff2c81f82013c3a08b0e2057a816c2521e2e1234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58449319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36db8b257159408287664ad61573ddb6c37299fb98ea8ebea63e3b8a3aaf6129`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Mon, 14 Apr 2025 09:33:51 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d38a8e839473141de91a6dff0573722f415dc1263e74806e9d20c51ad3fcaa4`  
		Last Modified: Mon, 28 Apr 2025 22:03:05 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae398473f83fdcec899167e0ff69486373e0747f30a0c69cfad4de95d9c6648`  
		Last Modified: Mon, 28 Apr 2025 22:03:58 GMT  
		Size: 29.2 MB (29238189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6e320ef1a235a2a037ed36b1bb3ac1c89225029f8f4380fa4af7e8c347f61c`  
		Last Modified: Mon, 28 Apr 2025 22:03:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:e9f768c522a07fe941fbf971a31c3f921bccf660cc7babb65d8f33238b297fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3824660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d64eb824b4c5c4c0c5c9d8dfc94e7b6e1f6629d059a55680bc36da62cf54c5`

```dockerfile
```

-	Layers:
	-	`sha256:4fba2974bf4a724dcc903307d13c02a95ab81d957c9234c639ea1ac7585e1f8a`  
		Last Modified: Mon, 28 Apr 2025 22:03:58 GMT  
		Size: 3.8 MB (3804418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d125f3f9a23da20e1e353274edae12267faf5a56769372ce74242b4e5a5717e9`  
		Last Modified: Mon, 28 Apr 2025 22:03:54 GMT  
		Size: 20.2 KB (20242 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; mips64le

```console
$ docker pull perl@sha256:e3203129224e6d02b768d5de1260ede31af7599644c8767b0968f0faae83b104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59067428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40551076d7f161e4bf9401be60d9e448ac2f27c90d3f6d35032e426b73f0e3c2`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777ba5f6d3a13ae7621a610c637637b53eb659b3c56bcf2d87e3c19228c408ee`  
		Last Modified: Mon, 14 Apr 2025 18:32:07 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fde749f7e5382dc6c4b7e0427ea4c7e98c12e79fe388f31c1ac4494911c494`  
		Last Modified: Mon, 14 Apr 2025 18:32:11 GMT  
		Size: 30.6 MB (30553207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42424118086ed01cfcfeafb36d692eff6dba58994eaebdf95b352374425cf555`  
		Last Modified: Mon, 14 Apr 2025 18:32:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:5099aab8f19a9601e2d59192244fbcd23cc3f4484b12b8b5789e0393bd3818fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22de66ba4c0ff92c88dfb7bbe0f07429b7b2d1ed2142d44b01ffe079a0923db`

```dockerfile
```

-	Layers:
	-	`sha256:451c89a3a5c837992780f7f8a44d51c80e01061a47e0da3ec7a51c836f6ef00c`  
		Last Modified: Mon, 14 Apr 2025 18:32:07 GMT  
		Size: 20.2 KB (20209 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; ppc64le

```console
$ docker pull perl@sha256:964ae55c657be62321d7b3687f5f24a37a25d2d965d5e6c8c5bdb9e2bb8a082e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62975531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99872e54eb89aef0af236ed155dc50ef97ae2ecdf45078fbff41ff0b08e50f8f`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Mon, 14 Apr 2025 09:33:51 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cff34e84d2038755e1b2fbc21dc92e9e054557c7719c28478835e47865eb292`  
		Last Modified: Tue, 29 Apr 2025 01:00:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc22e42bed7977e4eee0fc42dd927b09721070e64c6c403913739c6dcf24285d`  
		Last Modified: Tue, 29 Apr 2025 01:00:57 GMT  
		Size: 30.9 MB (30906820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9de67dd4f65b815302e9bd053fec7ad71ef6b7eef261aae727a94bf0a06bad`  
		Last Modified: Tue, 29 Apr 2025 01:00:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:7d2fe4d38e95af14e94ab40e11c64f7f4831948817338d44076848eb4b9c1751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7afd4fd7aee70faf607d5ae4f204c50bdb0f226e3c659347bd30aec79f7425`

```dockerfile
```

-	Layers:
	-	`sha256:a14aff63eb729226dca8cbba30bbcdeffe97505def18fd7e0363bda57b5ed4ec`  
		Last Modified: Tue, 29 Apr 2025 01:00:56 GMT  
		Size: 3.8 MB (3796406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade1fc9f62ddfcc68eef6cd8e2dd893c936e96547f391c4eef33781c644bb61e`  
		Last Modified: Tue, 29 Apr 2025 01:00:55 GMT  
		Size: 20.4 KB (20384 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; s390x

```console
$ docker pull perl@sha256:da872c460f61fdcfc90601858c24a4ac7a3ca3b2e68e0538f333824960eed0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55536557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1aba89f0057077d6a62711d4249050d281bf8fa18582873f20f2ff042384001`
-	Default Command: `["perl5.40.2","-de0"]`

```dockerfile
# Mon, 14 Apr 2025 09:33:51 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/perl
# Mon, 14 Apr 2025 09:33:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.2.tar.gz -o perl-5.40.2.tar.gz     && echo '10d4647cfbb543a7f9ae3e5f6851ec49305232ea7621aed24c7cfbb0bef4b70d *perl-5.40.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.2.tar.gz -C /usr/src/perl     && rm perl-5.40.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 14 Apr 2025 09:33:51 GMT
WORKDIR /usr/src/app
# Mon, 14 Apr 2025 09:33:51 GMT
CMD ["perl5.40.2" "-de0"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e638ad9f39cf96377e2826915a1963ba78670aca7c9fe652687639dac8b3d38`  
		Last Modified: Tue, 29 Apr 2025 00:25:18 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc143e6bbd55ed75f4f496367efe515328046b6812e42e4fd09bc083a1d7c91c`  
		Last Modified: Tue, 29 Apr 2025 00:25:19 GMT  
		Size: 28.7 MB (28651424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173b2b68615edc6f5d9a5344b8d8b276a649d1ecba7681a759b368eabb22c625`  
		Last Modified: Tue, 29 Apr 2025 00:25:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:21157277124f1867059d7381cfabbe0df56a0010d4f12a70d5ad6458bdfe2263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3819043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349de95fa27ca5a8a7ef562463f9a63f6c8ef35b22a52d92c851fa930b451af3`

```dockerfile
```

-	Layers:
	-	`sha256:a62a5d71e22bf4d6b529413e763c157ef7b00a7cf05f1b3b13198cdf65c635ec`  
		Last Modified: Tue, 29 Apr 2025 00:25:18 GMT  
		Size: 3.8 MB (3798739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dccb250479f2d5c607adbc41a06cdfcb31e28469774a9836f79ebf1b6778f1da`  
		Last Modified: Tue, 29 Apr 2025 00:25:18 GMT  
		Size: 20.3 KB (20304 bytes)  
		MIME: application/vnd.in-toto+json
