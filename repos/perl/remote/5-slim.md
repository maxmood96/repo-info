## `perl:5-slim`

```console
$ docker pull perl@sha256:6cf6e501165712485697f8af6e287117ad79fc2eb4a5d318cfc447e03dfcab0c
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

### `perl:5-slim` - linux; amd64

```console
$ docker pull perl@sha256:59b90f85f257b752431c2002482dd20fb3aaf27031b4f9459e4b694e887be5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61738606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fde82787e2d84e1813bbe1919e8e872f2dbd64b41982624bca877d41b8482d8`
-	Default Command: `["perl5.42.1","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 18:04:14 GMT
WORKDIR /usr/src/perl
# Mon, 09 Mar 2026 18:08:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.1.tar.gz -o perl-5.42.1.tar.gz     && echo '6f84e6dc8cce97181d1c6aeeb552c13775c91ded3c6c73743c9211af87b16bf8 *perl-5.42.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.1.tar.gz -C /usr/src/perl     && rm perl-5.42.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Mar 2026 18:08:38 GMT
WORKDIR /usr/src/app
# Mon, 09 Mar 2026 18:08:38 GMT
CMD ["perl5.42.1" "-de0"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e5d5069cd54494ab8d65c5864b25105e1e204195590ae2bca02386303a6cd1`  
		Last Modified: Mon, 09 Mar 2026 18:08:48 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c790c00eeee2e56724d0e3e3340e78e348a1ef0975e0d48ea6b2ac6abdf5bec`  
		Last Modified: Mon, 09 Mar 2026 18:08:50 GMT  
		Size: 32.0 MB (31959704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fff2f0a3a85bcb8cba1ce3496fd94c7c3b5a109ed9d4fe82b7a70898a7439c6`  
		Last Modified: Mon, 09 Mar 2026 18:08:48 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:3606dda8f3ca49f762542d73fe6019daf60a007c47bb1ff68e7a942cbd1ad92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4030864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad51a4151d8fee58c9c4bbb80ea88fa5edaeb69a7fd6b73e740dfa35c3ff5e9d`

```dockerfile
```

-	Layers:
	-	`sha256:9b604bcf9c2dc061a33e4c43022e331a4b4ac4fa047c7e439283c1b48eb5fa42`  
		Last Modified: Mon, 09 Mar 2026 18:08:49 GMT  
		Size: 4.0 MB (4010612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06da26a9d44dc7d79bd4aae8aa79d0904906277b64bc97691ce9a5aafff769e5`  
		Last Modified: Mon, 09 Mar 2026 18:08:49 GMT  
		Size: 20.3 KB (20252 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:5f2895588cb60fd18f73ba42eb3eae782137a74823dee77046ad65d8a6446519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57143442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898acb94c199958315a21d039218714187017865a2122bd0d9dabe116f429215`
-	Default Command: `["perl5.42.1","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 17:59:59 GMT
WORKDIR /usr/src/perl
# Mon, 09 Mar 2026 18:05:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.1.tar.gz -o perl-5.42.1.tar.gz     && echo '6f84e6dc8cce97181d1c6aeeb552c13775c91ded3c6c73743c9211af87b16bf8 *perl-5.42.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.1.tar.gz -C /usr/src/perl     && rm perl-5.42.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Mar 2026 18:05:38 GMT
WORKDIR /usr/src/app
# Mon, 09 Mar 2026 18:05:38 GMT
CMD ["perl5.42.1" "-de0"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227a540b2af8c87158c6471469ef693569037e9e9af589017f28b33f30c9852b`  
		Last Modified: Mon, 09 Mar 2026 18:05:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508bbf661004df0fc9d69526b2b7bbb82097a36901e600056896b9a0c6ba73e2`  
		Last Modified: Mon, 09 Mar 2026 18:05:50 GMT  
		Size: 29.2 MB (29195565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2330a966b8f00a55f20417fbb2d3ce846960a996d53ce1ebc72c15fbdc220617`  
		Last Modified: Mon, 09 Mar 2026 18:05:49 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:1a074ff4998ad3cdd98bf554004c5b917ee74452c4876f53b77498639411a011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a60012611e78aee6e58092eacbda74a0963cf40a4d1bd0a29c1e84b32b1e258`

```dockerfile
```

-	Layers:
	-	`sha256:df37b710fa66b478693707d58b3782c036a5766f5582b18828a7b43d01517964`  
		Last Modified: Mon, 09 Mar 2026 18:05:49 GMT  
		Size: 4.0 MB (4003689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de51d214ed10bde82cafa7d19d4b108860861274a344bf7d8918b46f90f89f29`  
		Last Modified: Mon, 09 Mar 2026 18:05:49 GMT  
		Size: 20.4 KB (20380 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:c91652b9b598d19c739949ab62042afbcac7fb0c6bb9010efa5c531a0f5b7a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54488344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ad1803155d0c9a7f4c2422bfffa658d2fc5bded92707fc665e5c577aad5677`
-	Default Command: `["perl5.42.1","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 18:00:18 GMT
WORKDIR /usr/src/perl
# Mon, 09 Mar 2026 18:05:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.1.tar.gz -o perl-5.42.1.tar.gz     && echo '6f84e6dc8cce97181d1c6aeeb552c13775c91ded3c6c73743c9211af87b16bf8 *perl-5.42.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.1.tar.gz -C /usr/src/perl     && rm perl-5.42.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Mar 2026 18:05:54 GMT
WORKDIR /usr/src/app
# Mon, 09 Mar 2026 18:05:54 GMT
CMD ["perl5.42.1" "-de0"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18538e44f56b87cef6d97c3891cb542366901c1384e8d5a69d47ec178c432de1`  
		Last Modified: Mon, 09 Mar 2026 18:06:04 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6077e4688503a5407c519f84dd6f74d70b0987b99b90d3a7f95f290b99a8219`  
		Last Modified: Mon, 09 Mar 2026 18:06:05 GMT  
		Size: 28.3 MB (28274330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33128aab4f8840ff81f0a0e3520fbe71654f4d777565a596ac38bdcb3832a03`  
		Last Modified: Mon, 09 Mar 2026 18:06:04 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:aca08bed59d96cc368a9b2155884e1841e844c1e671026d5e6697ad5e02675c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c57c2bbf3c78f890c414a63126b227e113504b4312f84cfadbf89a3c23d7b1`

```dockerfile
```

-	Layers:
	-	`sha256:4c9228866704a5b1fe407d3cef0fed690bf4d7199f680d051f37817eb87b992c`  
		Last Modified: Mon, 09 Mar 2026 18:06:05 GMT  
		Size: 4.0 MB (4002880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c682d5f05bea86f1520dcdb725262743285840377be6541c899eff87d066dc9`  
		Last Modified: Mon, 09 Mar 2026 18:06:04 GMT  
		Size: 20.4 KB (20380 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:e99fd8c6ea746bd3d3e9ad30ed8d79712f7714fc77f86cd3aa0d91c8b944b8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61768953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88aefd17c61517968546c94ad6c4f0f06ef6a5e89fa839d31659ebf1900029c5`
-	Default Command: `["perl5.42.1","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 18:08:15 GMT
WORKDIR /usr/src/perl
# Mon, 09 Mar 2026 18:12:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.1.tar.gz -o perl-5.42.1.tar.gz     && echo '6f84e6dc8cce97181d1c6aeeb552c13775c91ded3c6c73743c9211af87b16bf8 *perl-5.42.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.1.tar.gz -C /usr/src/perl     && rm perl-5.42.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Mar 2026 18:12:54 GMT
WORKDIR /usr/src/app
# Mon, 09 Mar 2026 18:12:54 GMT
CMD ["perl5.42.1" "-de0"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33039b1e1cd34a58e86c768396574cc6bbe2580abca38c29222631dc48d80c5`  
		Last Modified: Mon, 09 Mar 2026 18:13:05 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5673081942ad1e9e5a6194f6e9257b1228f801ce04ed0732e6f4836f1cd6773c`  
		Last Modified: Mon, 09 Mar 2026 18:13:07 GMT  
		Size: 31.6 MB (31628586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebca25aa27ef90f5caaebb6abeeafc12a0076293f5373fe016637d0da2f98807`  
		Last Modified: Mon, 09 Mar 2026 18:13:04 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:33146866d56f88b513c481a1de99ee548ea5e86b1c38fc280fd1912f9c89af9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b551a3eb0728cbfd2233fce0a087f3389c57abdae02a302fc8d94ed119b68cc`

```dockerfile
```

-	Layers:
	-	`sha256:02dbc755c7c4b8b61a1f97b6d20fc30dd6ed2f762ec71e23ce01362038447464`  
		Last Modified: Mon, 09 Mar 2026 18:13:06 GMT  
		Size: 4.0 MB (4005755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc32d82974a8f0461b29d1a42f17063adf1a01360d5acc7d7f9938d50d218c21`  
		Last Modified: Mon, 09 Mar 2026 18:13:05 GMT  
		Size: 20.4 KB (20427 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; ppc64le

```console
$ docker pull perl@sha256:3ae3bc8e42e022943e6fc9e6108cf93516df1f463dc035223f23635747b0517d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66278083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64c57822453e66bda16e420ac659a900c1f1d4d213d4e226628c53a8d823fc6`
-	Default Command: `["perl5.42.1","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 18:06:58 GMT
WORKDIR /usr/src/perl
# Mon, 09 Mar 2026 18:15:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.1.tar.gz -o perl-5.42.1.tar.gz     && echo '6f84e6dc8cce97181d1c6aeeb552c13775c91ded3c6c73743c9211af87b16bf8 *perl-5.42.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.1.tar.gz -C /usr/src/perl     && rm perl-5.42.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Mar 2026 18:15:26 GMT
WORKDIR /usr/src/app
# Mon, 09 Mar 2026 18:15:26 GMT
CMD ["perl5.42.1" "-de0"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7961a979bb58e16352d85f99b1c6a52a1babd680ee95dee931f7da60f1978fdb`  
		Last Modified: Mon, 09 Mar 2026 18:15:48 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aeadccdf3a81810f6409e96cf1c1c30b67fea47cd1fc21beab756864cfdc6a3`  
		Last Modified: Mon, 09 Mar 2026 18:15:50 GMT  
		Size: 32.7 MB (32677598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0802003cb620e4e3f8097c531ab3096ba0bf35183d6a1caf702b9fb17e398625`  
		Last Modified: Mon, 09 Mar 2026 18:15:49 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:05a0f3e37e57726549680bd97a7c085adaf7ff48a06c618c5bc39bee410b2dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ea97314d8059b626888e0876f40b1bce0986fc9b27729a9db0087d693e024a`

```dockerfile
```

-	Layers:
	-	`sha256:20536bc1842ca286d935a9c2efee09199ebb0595aadde127977918ef47ffbbf9`  
		Last Modified: Mon, 09 Mar 2026 18:15:49 GMT  
		Size: 4.0 MB (4006648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c45fd4837677cc22b4795a87c7451c11549fa934c842467d812f88dcf593a6`  
		Last Modified: Mon, 09 Mar 2026 18:15:49 GMT  
		Size: 20.3 KB (20331 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; riscv64

```console
$ docker pull perl@sha256:a3efd97d30e55ca0b6c5d886f5f419292eada5b9d68957597e67a8088aaab391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68064615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baeb32ce38a0bc12953b480673629479716bcecb8c2d0cf2ef2dbcfcad2834e6`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:59:06 GMT
WORKDIR /usr/src/perl
# Thu, 26 Feb 2026 23:06:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 26 Feb 2026 23:06:34 GMT
WORKDIR /usr/src/app
# Thu, 26 Feb 2026 23:06:34 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195627fbbda9b60918f227dd345b9e530095bd286577d0139a8cb67387002a9a`  
		Last Modified: Thu, 26 Feb 2026 23:08:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3327f556f280c40b771efa74c8028c8dfd5b8070603a42abed8f948a72276821`  
		Last Modified: Thu, 26 Feb 2026 23:09:00 GMT  
		Size: 39.8 MB (39787930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babb6344233a4571edcc6af03222f7bb8bb5ab334e0aa8d7201d517edadc136e`  
		Last Modified: Thu, 26 Feb 2026 23:08:53 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:51e4979dbf400070e9f1e1125d143a6e80c1b46aed89ce64f330f126a6933a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4018246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2d16894ee24fddd16e7abdca95d9b5fa43c711d7344f0627b15b5477dc0fd3`

```dockerfile
```

-	Layers:
	-	`sha256:0290b3b5360f9531fd719bd900a2bfadcf5707cfc71d0bfced132030fef101ce`  
		Last Modified: Thu, 26 Feb 2026 23:08:54 GMT  
		Size: 4.0 MB (3997914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5316ef317f84bddb8e2b38aa027cd7f6aa0d9ad53db6f94b07d6184d1c1be9`  
		Last Modified: Thu, 26 Feb 2026 23:08:53 GMT  
		Size: 20.3 KB (20332 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; s390x

```console
$ docker pull perl@sha256:a0b0fae7a1db2d9ab8c3648b7947a1848ef456888a872196d556ac2dcf9a4f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61151510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a433eab4246041a904c8ffcbbd519ce4efa16d8f6df880c4e579921c39554846`
-	Default Command: `["perl5.42.1","-de0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 17:58:49 GMT
WORKDIR /usr/src/perl
# Mon, 09 Mar 2026 18:05:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.1.tar.gz -o perl-5.42.1.tar.gz     && echo '6f84e6dc8cce97181d1c6aeeb552c13775c91ded3c6c73743c9211af87b16bf8 *perl-5.42.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.1.tar.gz -C /usr/src/perl     && rm perl-5.42.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Mar 2026 18:05:22 GMT
WORKDIR /usr/src/app
# Mon, 09 Mar 2026 18:05:22 GMT
CMD ["perl5.42.1" "-de0"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07028da4c229f4b0388dec5c977dbc638094d639d0878b88f07d27fc9abb0347`  
		Last Modified: Mon, 09 Mar 2026 18:05:40 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a347779b340480e56b06f4d606bfac3933d52114e87fd3262760707f36bc5de7`  
		Last Modified: Mon, 09 Mar 2026 18:05:40 GMT  
		Size: 31.3 MB (31313062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216d0e878856819a6a6ba6b4362493fa4ef061c4dd6d6b106f6b4147bcd729f3`  
		Last Modified: Mon, 09 Mar 2026 18:05:40 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:486de716ec6996c96e0f045d055801c2153d552513aff3f020c07771003f54bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1781307cb2ab9a95d725e6ab70854cecfb31921c5cf179f03fcf1b3728bd4250`

```dockerfile
```

-	Layers:
	-	`sha256:ab371a5d3d835ab35c2a3a48f282bcde29926dcc6b92e03d5d7e40e449e0781d`  
		Last Modified: Mon, 09 Mar 2026 18:05:40 GMT  
		Size: 4.0 MB (4002940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9059b2c5139779bdf2cae366e58612e1f3a727dfadad12612b9468a73c0305c2`  
		Last Modified: Mon, 09 Mar 2026 18:05:40 GMT  
		Size: 20.3 KB (20252 bytes)  
		MIME: application/vnd.in-toto+json
