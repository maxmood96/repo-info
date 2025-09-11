## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:15e70aa9ede5a30ee2e2b5a0a66b7d37c5351b120d121986903b5618a34ff745
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
$ docker pull perl@sha256:f2c996a2d65f8f1cf05e3aac8e88800f3b2d9e8676b25f130d5225d060fe81c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56450680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb34c09dd8bf3a6a4140ae30aeb57bf030df6dfb80444d64371079a76fda3b89`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644e1bc2769f184f376ff7a1b7966d5ac7ee07cb1e27b44d184e2c3c849e0b8c`  
		Last Modified: Mon, 08 Sep 2025 22:53:28 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05808f9c29c5f00bd9e4e63018bf8fa4c4ea6f46e1825502faed60ffeafa1970`  
		Last Modified: Tue, 09 Sep 2025 00:32:49 GMT  
		Size: 26.2 MB (26194347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60fa4d8de4e354e27207ecfa6a6efb7001acd50fecf04bd2761559418c172eb`  
		Last Modified: Mon, 08 Sep 2025 22:53:27 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:981186b007edaedab26231696374c4747d8ef3902a59ec9925c9e09128252d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4138925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265adaa826528d5e0f1fd2128707ff7f206a90cb38d4e35b0148a8ccba08a4cd`

```dockerfile
```

-	Layers:
	-	`sha256:6976e210a005f79abe162a95e652b43b59ed02e24db1e2264a04e0e01532a791`  
		Last Modified: Mon, 08 Sep 2025 22:42:53 GMT  
		Size: 4.1 MB (4120643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9703741e68318718623454b21391fc826fcb81eea4784df8f5e23b572fbfe6ec`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 18.3 KB (18282 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:fa1d7ee823b9bd76fa6f1c6fc1664c47d1b486bbad5e98498f170ccc266507fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48992531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc3a29ceab05cf0147e08a8beb28a6a07072e72130bdde1ce2fb364fa5057df`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1757289600'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:6060ada35559867e583ae59d61cbfce25e84350e0631f50a795fd6d2b2c5651b`  
		Last Modified: Mon, 08 Sep 2025 21:24:07 GMT  
		Size: 25.5 MB (25544079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ac925a4610924abe9f1eeebc66bd972635a9b1026c9b47ee0af18fd933bd3e`  
		Last Modified: Thu, 11 Sep 2025 19:22:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684d0e07d8ede5e207466b982a7b9f896aca4574db7b74b48d33c2106c719884`  
		Last Modified: Thu, 11 Sep 2025 19:33:36 GMT  
		Size: 23.4 MB (23448186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0657771e4f2c86c2aebc6551b49158c78790f8a97092f62851c5d8e87df2754`  
		Last Modified: Thu, 11 Sep 2025 19:33:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:8bf579ad1710681235d2c2408aca80256cbcbf28fc1767c2c04fc84451dcff57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799c57bf263333aac099823ce0d9dbd4033ebd61715ed351b278f7178e7eb23e`

```dockerfile
```

-	Layers:
	-	`sha256:ba08e0255c7b734f617b524ad2a3a7eb3b9b2060d1f2e380c2aaa34139b01025`  
		Last Modified: Thu, 11 Sep 2025 22:46:43 GMT  
		Size: 4.1 MB (4094632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:570ceeb377c0bf66325343b649ed7765e5c522e4b87f7b05193dfda44a6bc80a`  
		Last Modified: Thu, 11 Sep 2025 22:46:44 GMT  
		Size: 18.4 KB (18354 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:8d3593ae521c1fb1ac7736303343ea400a4b7cf5cc6133d3ee081283c5073ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54074887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eedbda8b564720083b040b2d2d27b3592ef05df1baa3bfa8b95e96cb33c8d1`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a11a7af700b84fb6ad4bb570f08966836a47b5f72bb4aa83ed26775c4340f5`  
		Last Modified: Tue, 09 Sep 2025 00:09:25 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5d7a92b378f5fd6515123bf22442a456ed128a1922e4622a207634c00b59ae`  
		Last Modified: Tue, 09 Sep 2025 12:34:27 GMT  
		Size: 25.3 MB (25324165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f082d3c042081ad2450d0d8e236079dc22eb1fa3e0d956baa9914ee82680f7b`  
		Last Modified: Tue, 09 Sep 2025 01:47:52 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:742971d315b0a04ca215c3ec7e4dac01a41e4b3176fb5fbfe0c57b313263c91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e90f1d1a1b2d9c7fced7ad2601aa19eb4898261eb06ada2890bdda13e5f4ae`

```dockerfile
```

-	Layers:
	-	`sha256:4654a6b115765c47182904a81d303b6383e2e27a3f842f994bb0b1128342f408`  
		Last Modified: Tue, 09 Sep 2025 04:41:53 GMT  
		Size: 4.1 MB (4095038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85cd5b54fa7e6199ea4ca1ec0881af4fd354efb567d23a52862ca3837c915354`  
		Last Modified: Tue, 09 Sep 2025 04:41:54 GMT  
		Size: 18.4 KB (18374 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:47ded7e6cf327bf2c811dfdc54369d1e115a55c866dd586b44656589a92383db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58887311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d1059ae56674121c3f8004eb3e271102a9afc2a0687900a1007fab91c37a07`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1757289600'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:0f000710188b00f8cdc72241f34c956ada0679ed3e9fe2689e605404fa0930b8`  
		Last Modified: Mon, 08 Sep 2025 21:24:20 GMT  
		Size: 31.2 MB (31189738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b5edbd6fc4343945b2f5ea28e58b32b80e4c6d6f1dd7acc11abb961fac77c6`  
		Last Modified: Mon, 08 Sep 2025 22:08:06 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea2cbaa80e36dc2952565318999039cb65d809262c8c9d0f1f7911214c183d`  
		Last Modified: Tue, 09 Sep 2025 12:34:31 GMT  
		Size: 27.7 MB (27697308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5836769e879859e51d0c183407d5629e18376802c6385c881e8809c0212d054a`  
		Last Modified: Mon, 08 Sep 2025 22:08:11 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c41b5440b1219826f1838846d2fe7e4cc0ebdcf658293e45604d140a89fcd3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216b6d977eecbd2beae64be57fbdb901a6bc045e39c5ab06c084adadf2348db0`

```dockerfile
```

-	Layers:
	-	`sha256:eee1e65c39fbfe3942c3f9fdd8897e23890e0fece9c9aa85d1809a6920517123`  
		Last Modified: Mon, 08 Sep 2025 22:43:07 GMT  
		Size: 4.1 MB (4124925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a3635ac85086eb99f9e2fd96fecbd32ab93c8db46695d21d895b26db9eb1d7`  
		Last Modified: Mon, 08 Sep 2025 22:43:08 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
