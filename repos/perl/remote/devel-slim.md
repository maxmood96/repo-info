## `perl:devel-slim`

```console
$ docker pull perl@sha256:21a1f0310608afb2341db71343924977041a96bface040d079695f5f5022ba48
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

### `perl:devel-slim` - linux; amd64

```console
$ docker pull perl@sha256:20f8c940288e570ce22d2947250cc4dca9453ac7cddda118f6c9ad82faf7e279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58396855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847b4ea5de6374bd5e2156829ad3df5baf5e96733b632e9e6249c2cdc09a9bce`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add148775c63aceb73cc2407260c144f6323a2532c545fa4d6614d999ef87107`  
		Last Modified: Mon, 17 Mar 2025 23:27:42 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035f863ee725b6c84d3b0226c18f4ddf59b2fa85623a8faae0e28320c944ab1`  
		Last Modified: Mon, 17 Mar 2025 23:27:44 GMT  
		Size: 30.2 MB (30191723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5abf921379588a2f9ef86f89998590acf3f8009be3c3cdfd637a2f890fbb3a`  
		Last Modified: Mon, 17 Mar 2025 23:27:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:a150a73ece3b96c4813184a1233c51f403a806880fd5effbbe2f9af3dbf903c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3827192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96b9e6062d4729c7c71c937fa00d14394e478cd236bb981999e0c4847886038`

```dockerfile
```

-	Layers:
	-	`sha256:e7ac822afb4b8c9a68599bf8b36b3c8820539f48722e8d759751a191581e9f42`  
		Last Modified: Mon, 17 Mar 2025 23:27:43 GMT  
		Size: 3.8 MB (3808026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffa4881d47bfddefb61696152ed254cb0cad11a24f43122007a14fe0f6f60bb4`  
		Last Modified: Mon, 17 Mar 2025 23:27:42 GMT  
		Size: 19.2 KB (19166 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:c337217d184eb79cb2c3c7a1287cc91c32b9efdc71a1bf0c953795c7e64af82b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52997890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771bdf085fbfe22af202a1642662e6b54cc660ccf279add2c2d9a88171b5162e`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57e5a38cba11d2162fe937f6726ef758e83391c0e761a1ae2e589383bf5b98c`  
		Last Modified: Mon, 17 Mar 2025 23:22:18 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21946422c4ae8f143777d44d0e57990e9385d73a538bd1efcbf785e8c5a5bff`  
		Last Modified: Mon, 17 Mar 2025 23:28:44 GMT  
		Size: 27.3 MB (27261770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9101ef931ad4c05794045155180e21688affa50ac2cc6f9490d281ccc75024ca`  
		Last Modified: Mon, 17 Mar 2025 23:28:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:e436b8c056f5fb46eda95ec37a21b822f863057379b73553e40033bb51a46505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3797851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e359ac6d12aa76201c31a9c208e1e726c86ab0db0bee85dad9f3b74d6cadefd`

```dockerfile
```

-	Layers:
	-	`sha256:2b294b220915d0f3453a542978e0de4fa0da2e3c05595b2e3ab151142a19acf2`  
		Last Modified: Mon, 17 Mar 2025 23:28:44 GMT  
		Size: 3.8 MB (3778593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af8c645467648247861296c7cd5c34b2a2b49fd9fb3ef52106a8322c6085e229`  
		Last Modified: Mon, 17 Mar 2025 23:28:43 GMT  
		Size: 19.3 KB (19258 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:c8dc6f9c18aa2563bbb7b59e48c49eb623414b87a68648885282307d8024a4dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50271714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea00dffb86e86f3e36350cc50619204736d5abe7eb81c16e634fdc024c039e6a`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3394c13f54007861cc3d5c1bdb5bef2e42e04d9a5acb7516e85d3737cec6f841`  
		Last Modified: Tue, 18 Mar 2025 01:27:34 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86131e6e37bb19169c7a216955b88d6e59737fad9a54e9169c642287190ccd34`  
		Last Modified: Tue, 18 Mar 2025 04:13:19 GMT  
		Size: 26.4 MB (26356361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbeeb6ca855a9678b7f5b2d809c1d81ce55c19d1025642ab42a98403951c73fb`  
		Last Modified: Tue, 18 Mar 2025 04:13:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:2493023eb1a0f69d370cf77a8a8e6bbdf79b7d6cb4a40a8b1e655fb9a22709e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3797383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b111e5f9c1402e2289a99c0eceeba00e514e2c842705e17d74ae76d1bb672c3`

```dockerfile
```

-	Layers:
	-	`sha256:953713e18c2b2917da9617ca063a036cfd0baf775e59127cfebbd8293faa7e2f`  
		Last Modified: Tue, 18 Mar 2025 04:13:18 GMT  
		Size: 3.8 MB (3778126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9565b92655995e5c4378f7c736ad94fa469085e88ae8f2b2aebaba289eb457`  
		Last Modified: Tue, 18 Mar 2025 04:13:18 GMT  
		Size: 19.3 KB (19257 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:29bfa72bf3e4d9445af69e78884b7ca2f3e63bf75f422637e640fe9894551177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57057037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e815626cc61587c1e61b5a675185ab8efb844c351e33cd0e8aefabd845c669`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d732be4541f5de484aa428996ee0e74379202f2f4066838b3d323ccf5cb0e18`  
		Last Modified: Tue, 18 Mar 2025 02:50:25 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721173290864cc06fb60353ae18ff8278ceeb759e35d465cb1945b2b5b256d32`  
		Last Modified: Tue, 18 Mar 2025 03:59:45 GMT  
		Size: 29.0 MB (29012733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb35678725a92069d1c0084e830edb3d91852d58b2ca5de039c332f39bf35e45`  
		Last Modified: Tue, 18 Mar 2025 03:59:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:a093b433d39d41d6448d2a396b098b0783255e8c8ffee0365bcbe0aac4f85899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3798593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9406bbe91baa3d36f3c74c61545dcf506e15a4d00e8652ef43887b18866be27d`

```dockerfile
```

-	Layers:
	-	`sha256:70698395e4c55c011384d7ee9bc464e4c4ba816611a1d2dd0f68037b6a5f9ef3`  
		Last Modified: Tue, 18 Mar 2025 03:59:44 GMT  
		Size: 3.8 MB (3779299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880be0e40ca4da45765fdd6b07510f2292109696268f889db249cf0afb4fe7b7`  
		Last Modified: Tue, 18 Mar 2025 03:59:44 GMT  
		Size: 19.3 KB (19294 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; 386

```console
$ docker pull perl@sha256:f1fd936f29fa3dc3e9863dfb3849b76fbaa173e88df35b43446c3af291361d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58508534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763d213ef58abd77ed120cb10d4a1fa0eef52bc3d3558a8d6e9d2de6f4e23ac6`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b09419ac8bc6d61c4891b7d127a10e27da13e0d1244be54d4efd780c532173`  
		Last Modified: Mon, 17 Mar 2025 23:35:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300997134e683a8c24d97bb94d8b6436dc23cc097f432e667633d9346494e3ad`  
		Last Modified: Mon, 17 Mar 2025 23:35:58 GMT  
		Size: 29.3 MB (29318739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9754443b8fc18706defbfad575ddb1d951c3fc7dc94ad92b799a4d545cc62880`  
		Last Modified: Mon, 17 Mar 2025 23:35:57 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:e3db7888dfd526b716e7a90e24420947fac8a239a602c92a1997773e986bbd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3821014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05fa924cd4939498523d13aacbfb1753ca25823d0c027befd4b9b8f415de375`

```dockerfile
```

-	Layers:
	-	`sha256:7e888664de32e982004a5f6bb288ca2470853e6a980954278d80603f3abf7982`  
		Last Modified: Mon, 17 Mar 2025 23:35:57 GMT  
		Size: 3.8 MB (3801890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab5e462ecc434370c733458afb53110428ca0c290124f99859cf788a30fa7b86`  
		Last Modified: Mon, 17 Mar 2025 23:35:57 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; mips64le

```console
$ docker pull perl@sha256:1cd5011a37a9e30c057cd212345f1c4ffbfc1e59aa4de9f795a4201b6a5cf459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56858563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83946b3fea68f4d2bd387fb67be7a7e9baa228cf9cee7ead3eb653867e432a58`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0675e2adae55a2dcd0b7572a1efdaee3ded6169572c86b56f61eb070e5ed44ac`  
		Last Modified: Tue, 18 Mar 2025 00:06:18 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078c4bcde58d6edb59c4a226bba137b94019165dd9dc276a719c40330770ed86`  
		Last Modified: Tue, 18 Mar 2025 02:31:25 GMT  
		Size: 28.4 MB (28368841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a8011ec49b73f2b03aaa50805d0d10e4ee22b497457e2a8862192f6aa57a6f`  
		Last Modified: Tue, 18 Mar 2025 02:31:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:c73afb0c8d7dd55b8c4264ab27e65bd9ff6d44249e1134a4ad7e3ded074dd2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57f1116bf7ab9856268176cb954a35409ce7a3472a0863d5abaf01815aa432a`

```dockerfile
```

-	Layers:
	-	`sha256:9e40aee6bbdef717441b84e49ca0cb0d28889500d72da96e8dd3bdfd3126da72`  
		Last Modified: Tue, 18 Mar 2025 02:31:22 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; ppc64le

```console
$ docker pull perl@sha256:f94c8c024602cdf0c3c11850ce43868d19e6c2ee2b9e93f6830392271f63d6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63041198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b297d27556bb13a0a6954c4d34b26ad683682e6648622f4a571ebc36c0c963c4`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d309cb1c6fdced6a5008059599591b67b9498e1f0385f485d26bf5faeb5c13`  
		Last Modified: Tue, 18 Mar 2025 02:26:02 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12716152c425b8ae40133f04955f6c86c038a1f7c18aa7db46a4afbc8b2baa25`  
		Last Modified: Tue, 18 Mar 2025 02:35:31 GMT  
		Size: 31.0 MB (30993119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f2665a7a7aee197550d382d87530c33f7192590c1e8acb820b1bc13391dde`  
		Last Modified: Tue, 18 Mar 2025 02:35:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:54bef5dd31b9f819ba2a673ca56344d279b840b5d9bd2aeb7558c9d36ad50b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5afc3b0b4bc0836dbc2996aa031b6366f40930426485bdf4525d9d1564d078b`

```dockerfile
```

-	Layers:
	-	`sha256:2152c60f9bf5f085b085e5b985304eeabb7bbbac142125ad2237996afffae71f`  
		Last Modified: Tue, 18 Mar 2025 02:35:30 GMT  
		Size: 3.8 MB (3793834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75b079af1fc11604181d904e3d331da25e2dccd9604b5e7973f92d7de18bf24b`  
		Last Modified: Tue, 18 Mar 2025 02:35:30 GMT  
		Size: 19.2 KB (19222 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; s390x

```console
$ docker pull perl@sha256:e62c5a6f3ec2b0ce12f0eb53f3139b982de5f1b15bf65e416da5e233e75aacc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55600162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547bb35f43f80f448c00a41a14d1f84337f5dca4cc51f36f1f0c96b424e593c1`
-	Default Command: `["perl5.41.8","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.41.8.tar.gz -o perl-5.41.8.tar.gz     && echo '2b13022a1b3e4648ffbdc51812e6b83cd7990095771989a236ec4edb2a55604e *perl-5.41.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.8.tar.gz -C /usr/src/perl     && rm perl-5.41.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.41.8" "-de0"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b0d8f53b8a2a8483c813bdbc43ede4e2bfea1936c1b73a999c5904701a1993`  
		Last Modified: Tue, 18 Mar 2025 01:41:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c75498a08b03ebc6f856cd664410c70530d286234214dbe6998076e23d6734`  
		Last Modified: Tue, 18 Mar 2025 01:55:59 GMT  
		Size: 28.7 MB (28738838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aba869dd1041915be5515e0ca72fed447b31ae33cf1bdbc5fa7768effb580e`  
		Last Modified: Tue, 18 Mar 2025 01:55:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:f23bce87662911b9324f7bb08cb20bbe94c0aeda1b1a38579864a1a65159c317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be27f53e1e55ce723daffda452f248472ccf3874a2ca874235bcc29d562115ce`

```dockerfile
```

-	Layers:
	-	`sha256:068cfe8bc299ab1605013311595a8491932e8a7c56c82c75412f3b0e9c12f13a`  
		Last Modified: Tue, 18 Mar 2025 01:55:58 GMT  
		Size: 3.8 MB (3796191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb932fdf05c6119c5b59e262b3e07c2e20e5ea6ec685243a727ea42bf3e9a338`  
		Last Modified: Tue, 18 Mar 2025 01:55:58 GMT  
		Size: 19.2 KB (19166 bytes)  
		MIME: application/vnd.in-toto+json
