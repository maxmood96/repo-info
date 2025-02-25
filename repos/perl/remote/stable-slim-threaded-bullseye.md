## `perl:stable-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:1b86d2dbb27b7f15af76e4000e01c4df1a65f7e49d19ce9eebc93163851d00a7
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

### `perl:stable-slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:3d0ed267bebdd7f896dc87cb084f5788aaa46176c3aa54dba6a25511460f3bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56176827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadb4aea64b278e5db6eeeed414ca67e0f66499c3b2f2cbdc860b4e921bcd3af`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.1.tar.gz -o perl-5.40.1.tar.gz     && echo '02f8c45bb379ed0c3de7514fad48c714fd46be8f0b536bfd5320050165a1ee26 *perl-5.40.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.1.tar.gz -C /usr/src/perl     && rm perl-5.40.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.40.1" "-de0"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ff56e7e633f3667999865e282ab5dd32020c55322af4b97bccccff634d60f8`  
		Last Modified: Tue, 25 Feb 2025 02:36:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d589055ca7483eb793f4a55ded37169802fdf18b53ebfbf114b7f663ccca497`  
		Last Modified: Tue, 25 Feb 2025 02:36:53 GMT  
		Size: 25.9 MB (25922629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522e3dde07edbf0514990a35e839a088d18238ebe10e4b04318b0f26172cd98`  
		Last Modified: Tue, 25 Feb 2025 02:36:53 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:656213bde6dbba37bbc47bb3769f04a967aa4599eec5694fc8abf76618129f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4018115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14f6bf4da0b1ce9a9cfb3e4533872bfb8926fd8f1c343d0dbd69e9f1bd3d55c`

```dockerfile
```

-	Layers:
	-	`sha256:f7be907e29d61d204eb2395e5b0c40e0e28bd266bf10c9fc32da07bae95130c2`  
		Last Modified: Tue, 25 Feb 2025 02:36:53 GMT  
		Size: 4.0 MB (3999166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f971675cae87b1e20b4979c8afa34dccdde0755bfda395cb31b81e747eca80af`  
		Last Modified: Tue, 25 Feb 2025 02:36:53 GMT  
		Size: 18.9 KB (18949 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:e904bb041185caa6015d97908690185f08d383c310dac5f3c5ba814ae2df2ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48683307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923b213e1a8666ee6019483b8d5232f6f3936b4a4beeecf16e9a85d501700457`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.1.tar.gz -o perl-5.40.1.tar.gz     && echo '02f8c45bb379ed0c3de7514fad48c714fd46be8f0b536bfd5320050165a1ee26 *perl-5.40.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.1.tar.gz -C /usr/src/perl     && rm perl-5.40.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.40.1" "-de0"]
```

-	Layers:
	-	`sha256:b0ca501b624d9dae81049df15e1024733ee21141b25f8ca123d98e0d13df5d12`  
		Last Modified: Tue, 25 Feb 2025 01:31:18 GMT  
		Size: 25.5 MB (25535432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02eecd66af283ad08b114032f0c6503139d48a1f443ae51af619b70b1d8a9d1`  
		Last Modified: Tue, 25 Feb 2025 07:59:16 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2969c72d63cddcf3bdaacdc3a63bf1a47cd328e8afde66cb28bf5234728a49`  
		Last Modified: Tue, 25 Feb 2025 08:12:49 GMT  
		Size: 23.1 MB (23147607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309a4e78bc5baf8563c0691d524a163e80239126028d93525f5e18cc117aefc9`  
		Last Modified: Tue, 25 Feb 2025 08:12:48 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c2162068b7fdf30fcefdf26b485c5a52711d3b180586ed04524697f624c0673b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20888ffb7b4ecfadee00ad50baaf5d8a0789fa3bc1786934e258c0989680d04e`

```dockerfile
```

-	Layers:
	-	`sha256:6cde55dc51d93182cf8a6fc13c937b9c78c4f01b63f16d4935e3b0fd891cdb53`  
		Last Modified: Tue, 25 Feb 2025 08:12:48 GMT  
		Size: 4.0 MB (3973171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f5fb65ff2b82fbe6cbebf11a93d414206125e73f785dc33af297bf49b0a8a0c`  
		Last Modified: Tue, 25 Feb 2025 08:12:47 GMT  
		Size: 19.0 KB (19033 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:5014b058c0b8aff2a8af28aac39adf563b713d3253c23dfa2fc908afe06ca3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53785508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1143043f3e704e048bca14a566dc9a8e61286ba68e529bebff982eb00d1678ba`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.1.tar.gz -o perl-5.40.1.tar.gz     && echo '02f8c45bb379ed0c3de7514fad48c714fd46be8f0b536bfd5320050165a1ee26 *perl-5.40.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.1.tar.gz -C /usr/src/perl     && rm perl-5.40.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.40.1" "-de0"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58491e319b39f2496349c4d9227508378814a9bc94d9337499f54401ffb59dc8`  
		Last Modified: Tue, 25 Feb 2025 06:37:40 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2eeac700e8853975e14a90ed13d857b23cc49fac1235674a92a7e80144127b`  
		Last Modified: Tue, 25 Feb 2025 06:48:30 GMT  
		Size: 25.0 MB (25039251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56810c6cea4a8f3e0450de1c840c68626f499a5c9b27f8fec9f6efb5bc404a39`  
		Last Modified: Tue, 25 Feb 2025 06:48:29 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:424d2901f21f49dc70e3120df0e57a019194a909c5a2511970589c10142544e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a76b13f76a47e3b5b122c93b29360a55a50d5d970ad0f3cd8c4c98cf1ab7b3`

```dockerfile
```

-	Layers:
	-	`sha256:21267c50140976cd3b08339c5625e112e539f413459161af810245f0d80f7439`  
		Last Modified: Tue, 25 Feb 2025 06:48:30 GMT  
		Size: 4.0 MB (3973585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:873dfb016990e4290eb24b39b0a3340b320417359604d3287416cc089c168f61`  
		Last Modified: Tue, 25 Feb 2025 06:48:29 GMT  
		Size: 19.1 KB (19065 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:eb64a65d999b5977bea080e0104881253b6c649ff1d2695a2f454a511779075b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58663630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c389be0f25382a3d6f245418c7e2ddf4127e3fae0e961ec44e421d228cd3969f`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.1.tar.gz -o perl-5.40.1.tar.gz     && echo '02f8c45bb379ed0c3de7514fad48c714fd46be8f0b536bfd5320050165a1ee26 *perl-5.40.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.1.tar.gz -C /usr/src/perl     && rm perl-5.40.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.40.1" "-de0"]
```

-	Layers:
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f968d31dba586a7f1f7d21066da6ee980dda68ad60b84e00420490213188d7`  
		Last Modified: Tue, 25 Feb 2025 02:21:50 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a224be0e24d0549232be54341271b8729e61408e0548b183fb17e7bbe3455c0e`  
		Last Modified: Tue, 25 Feb 2025 02:21:51 GMT  
		Size: 27.5 MB (27482934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e92597ab4442642d882134cff5a086df200d0b96c938e3cd10fde3145d472e7`  
		Last Modified: Tue, 25 Feb 2025 02:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:3b458451539384b3d22a061d2b57c1cd2eafa499efc68e0ebc6313c0a7bba88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4022287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da940c3554b9214919b28bb23ea22279586cf49dee90f1e4049f8e09d25f888`

```dockerfile
```

-	Layers:
	-	`sha256:2d7aea2500939fd6a241501444a2b5b4e49480600a8e88a9928c6ca463b7ac4b`  
		Last Modified: Tue, 25 Feb 2025 02:21:50 GMT  
		Size: 4.0 MB (4003375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ba5537823a18db968972daf40cfb8ce6fb3aece3f95b416ab01fd9ce2f98a97`  
		Last Modified: Tue, 25 Feb 2025 02:21:50 GMT  
		Size: 18.9 KB (18912 bytes)  
		MIME: application/vnd.in-toto+json
