## `perl:slim-threaded-bullseye`

```console
$ docker pull perl@sha256:e61e71a850d257b3f7fd49c5032211ad256cd6b18bc0cbbf310f1e1685d1a3ec
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

### `perl:slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:360207b44b754660956e9c475ec24f35233e621bf8a0193fda644578d5a7f71d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56176787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d5178414bf67fa8218b71f62045f4f28a4532b7d1c6967f8287ebf17e64c65`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d4826adb5dfb75b347fed09e5b8626da6d2eebfd297febfdc0b80daa853e40`  
		Last Modified: Mon, 17 Mar 2025 23:27:17 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977f408a77dda5fdc6889418c41e671666051881f73ea88c7353a9aa0f202ec0`  
		Last Modified: Mon, 17 Mar 2025 23:27:18 GMT  
		Size: 25.9 MB (25922684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498f7615087ba2b0d81a5f919b758f1bbc7ca0af008a7025f4f8ab26e8b31bcf`  
		Last Modified: Mon, 17 Mar 2025 23:27:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a22ac648183912b70b53df307f62f0991c34d521df94b1eafd7105e38d8be4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4018115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb37b5120843199ac5633af7be51b2f83ee72041b873700c65442b3970e5b508`

```dockerfile
```

-	Layers:
	-	`sha256:ac13967765eb6bc5b1f841aab4ba23730d4a9b64d65f62aeb56349078a9e7559`  
		Last Modified: Mon, 17 Mar 2025 23:27:17 GMT  
		Size: 4.0 MB (3999166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d627896ab9d79d955d145b984410f9f4f19d5dcc80ae6e0df40243a883feba`  
		Last Modified: Mon, 17 Mar 2025 23:27:17 GMT  
		Size: 18.9 KB (18949 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; arm variant v7

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

### `perl:slim-threaded-bullseye` - unknown; unknown

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

### `perl:slim-threaded-bullseye` - linux; arm64 variant v8

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

### `perl:slim-threaded-bullseye` - unknown; unknown

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

### `perl:slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:ac8f2db5cb64cd66c55b2c434b656147275691f8fb2f3a16e1be2dae75ed7d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58664173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f92706dcf60b7ec0d5199e6437c12afde4147f3ce01bf82e0091b35b1fb1b1d`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Wed, 22 Jan 2025 03:53:54 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0134a1800ffea58896eb9f6fc4d0026606b4f875704d101ef029ef7dae540a`  
		Last Modified: Mon, 17 Mar 2025 23:34:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56c7b771ac694ad682da5feeac6912fe5dc169cc697c8aac224656ef9b7824c`  
		Last Modified: Mon, 17 Mar 2025 23:35:56 GMT  
		Size: 27.5 MB (27483569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6535afd5cc9e63c8756225ab2af12735ff1e3c639fe851df6f64669d5011729b`  
		Last Modified: Mon, 17 Mar 2025 23:35:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e03b93d3557337a2ac3cfe5f58f5c81ec282619e224eb630269cbbf7646da089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4022287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216925b161bd952ca6bbe66ba0a2d25f950f73317ab7c9712c0d7034f112305e`

```dockerfile
```

-	Layers:
	-	`sha256:ec1e27b65524d8e692db2fd20a2c04826784b4c1940a049069bce7a81a229a92`  
		Last Modified: Mon, 17 Mar 2025 23:35:55 GMT  
		Size: 4.0 MB (4003375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77a7186d513789eb04e219c423e525ad34a5e3ec52c50698613b52c07d9af77`  
		Last Modified: Mon, 17 Mar 2025 23:35:55 GMT  
		Size: 18.9 KB (18912 bytes)  
		MIME: application/vnd.in-toto+json
