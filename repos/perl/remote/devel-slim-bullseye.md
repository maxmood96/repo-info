## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:d1577cffd488cbf0453c8bc5740b02228bf8ec3d396d08f2aed5a13b7fc9bc3d
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
$ docker pull perl@sha256:30631b4e830fc8307623a16f355628f93c20e7bbe1ab6eb01fefc4851383e3df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56398317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12646b6b309ecfddf45e98a55dd932481a71da94dab342d91efc20a321362628`
-	Default Command: `["perl5.41.12","-de0"]`

```dockerfile
# Tue, 06 May 2025 02:04:37 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/perl
# Tue, 06 May 2025 02:04:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.12.tar.gz -o perl-5.41.12.tar.gz     && echo 'bf10191d1206a41e5a7b57fa072d80e2f9ba391a1331835f20a299cd797660bc *perl-5.41.12.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.12.tar.gz -C /usr/src/perl     && rm perl-5.41.12.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/app
# Tue, 06 May 2025 02:04:37 GMT
CMD ["perl5.41.12" "-de0"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15699aa70e5a56f7d106ea03b0250754442f1660ae80fa18f19d4f646d68852`  
		Last Modified: Wed, 21 May 2025 23:32:04 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fe0461ec21613dd49a46cb31ef683768c065aa0460ac4b882b99ddc8952ae3`  
		Last Modified: Wed, 21 May 2025 23:32:05 GMT  
		Size: 26.1 MB (26142111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07ce46db764900a4d40d5bf619f2c4c0709aa4271a7be00b89e9bad3676356d`  
		Last Modified: Wed, 21 May 2025 23:32:04 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:02f417545ddeaa38b63de8203a029c1d17bea95f6e934cc151e8a8f07f28645e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4042940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6905a47bc64152dd65171a6a513c81af2ce3589c7e5fb3d3e1f3383fd001f9`

```dockerfile
```

-	Layers:
	-	`sha256:b4b10d389721349eb7e03d671110377603c0adca19d23b6d70be48739185bdde`  
		Last Modified: Wed, 21 May 2025 23:32:05 GMT  
		Size: 4.0 MB (4024664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6e90d55430a3352ff588e7c213cc03a11e3bb8217c83a16de59a0e84cf792d`  
		Last Modified: Wed, 21 May 2025 23:32:04 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:cca86248dfc309d3fd94430aac0476bc5ec2ca623e9d1488f8413e81e377199e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52749228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8179f35ef41c6b9ac42d2e77a499e16feb23ab40dbba694ee70d4c1c6858e6df`
-	Default Command: `["perl5.41.12","-de0"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/perl
# Tue, 06 May 2025 02:04:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.12.tar.gz -o perl-5.41.12.tar.gz     && echo 'bf10191d1206a41e5a7b57fa072d80e2f9ba391a1331835f20a299cd797660bc *perl-5.41.12.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.12.tar.gz -C /usr/src/perl     && rm perl-5.41.12.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/app
# Tue, 06 May 2025 02:04:37 GMT
CMD ["perl5.41.12" "-de0"]
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec1a2611b151e1ec1cf0ef40e5fd497c5c9b8695f6903b37001848a87064be2`  
		Last Modified: Tue, 29 Apr 2025 04:24:30 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44059c72680eb019a9490d9b1db262ae5dc66d81d1fec9ffedd0087ca4669e6`  
		Last Modified: Tue, 06 May 2025 17:39:59 GMT  
		Size: 27.2 MB (27206535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0593b882101bc5436bc8c0ceab1ca10916b69679282aa7202eb25f2fd158bb4`  
		Last Modified: Tue, 06 May 2025 17:39:58 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:481c59541c5c682d8577a1a98b60171bbbdb16510b0f31be0c12acb9ce9d3941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0927602a5e720b8613750bfdfe96de5b4a638e90e6257f601b9d09c2460a1`

```dockerfile
```

-	Layers:
	-	`sha256:c09dfd294752bc0542a57424fba50acb1616988af65ff7014a29c734c57e14c6`  
		Last Modified: Tue, 06 May 2025 17:39:58 GMT  
		Size: 4.0 MB (3975660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1af14ea4756efa67a9a828f9fbb0f8c13e9214a6c63ed193fafb0a93b63e5c1`  
		Last Modified: Tue, 06 May 2025 17:39:57 GMT  
		Size: 18.3 KB (18344 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:beb723e33e23c09918f7bad0409b9df589ad2c840a5a8f8156950638201b41b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58180886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828bb131915f6184dbde98fa5c19c51d21c956ab7fe2a25e40485b1b71d34dd8`
-	Default Command: `["perl5.41.12","-de0"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/perl
# Tue, 06 May 2025 02:04:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.12.tar.gz -o perl-5.41.12.tar.gz     && echo 'bf10191d1206a41e5a7b57fa072d80e2f9ba391a1331835f20a299cd797660bc *perl-5.41.12.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.12.tar.gz -C /usr/src/perl     && rm perl-5.41.12.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/app
# Tue, 06 May 2025 02:04:37 GMT
CMD ["perl5.41.12" "-de0"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895ac38237bbe6af7dd8a0c28fc45e1ad5371403a3f63c77a574b8a5edd3704b`  
		Last Modified: Tue, 29 Apr 2025 20:41:03 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e271b958a0f1ad674839faebf96299748d3f6c7570b4d53865ca97be07eee552`  
		Last Modified: Tue, 06 May 2025 17:34:39 GMT  
		Size: 29.4 MB (29435974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc77dbe4577106dfb58ebca35153d27041a77c00b64365c74028a146021b3afb`  
		Last Modified: Tue, 06 May 2025 17:34:38 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:21cb9b5a687c1ab264566645734f62bb43bcf8fe416b5bba995489e92ac391a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4726b0ded65f339c679477e13f14e4c7569da4e4eb2e937487c025dab86758`

```dockerfile
```

-	Layers:
	-	`sha256:b20c3abf88d57aa3dd51ac0ecfe447e77885ef46e6df32ec73219a0938029774`  
		Last Modified: Tue, 06 May 2025 17:34:39 GMT  
		Size: 4.0 MB (3976066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72a8aee93d136c0f244455b2e0bb2faf45c2da40777696a65766e43fe09b2e27`  
		Last Modified: Tue, 06 May 2025 17:34:38 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:532f7317c697829b580c52feafde5177f2ecb6effa9fa3c3ad362bfcb6ded414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58843516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5463ad938b2f3c39d91cb019a49066c93cb98224d5f294117bb4827446c82648`
-	Default Command: `["perl5.41.12","-de0"]`

```dockerfile
# Tue, 06 May 2025 02:04:37 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/perl
# Tue, 06 May 2025 02:04:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.12.tar.gz -o perl-5.41.12.tar.gz     && echo 'bf10191d1206a41e5a7b57fa072d80e2f9ba391a1331835f20a299cd797660bc *perl-5.41.12.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.12.tar.gz -C /usr/src/perl     && rm perl-5.41.12.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 06 May 2025 02:04:37 GMT
WORKDIR /usr/src/app
# Tue, 06 May 2025 02:04:37 GMT
CMD ["perl5.41.12" "-de0"]
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c0ffd4e6bcceb8028c89e335968ed82a8494a13767fb2d9e73d13f26a7034e`  
		Last Modified: Wed, 21 May 2025 23:29:34 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7683b17790d26aacb4c2abddfc144710f95b0ac3c58809c2109e626822d1b3fd`  
		Last Modified: Wed, 21 May 2025 23:29:35 GMT  
		Size: 27.7 MB (27654051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d7197e18cfc4755c1adfab249f896df6018322f4de0053f37a08d1084faeb9`  
		Last Modified: Wed, 21 May 2025 23:29:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:057e77efb0dd3157f00c98a015f034198507a60be3a17d457ae7d9b8faaa7758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4047193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99864d07efafe09d0b8a5863810efc20e8ecbc8b88d5af5006c628999d4a98ca`

```dockerfile
```

-	Layers:
	-	`sha256:22accedb0e0b662d4eb7e57852c3b88b3800158bbd2fc93708fac7be527c8578`  
		Last Modified: Wed, 21 May 2025 23:29:34 GMT  
		Size: 4.0 MB (4028946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a086513e248b5fb5d1263ac9b01d2e7cc43d42c7dfbfb251c718b15c8d28141`  
		Last Modified: Wed, 21 May 2025 23:29:34 GMT  
		Size: 18.2 KB (18247 bytes)  
		MIME: application/vnd.in-toto+json
