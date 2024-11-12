## `perl:stable-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:58cfdeaedf9ca1aa17ef9c976b16e6089abf9d096bcb8fd4840212a52bb2df93
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
$ docker pull perl@sha256:3acb6d9299dd913b100e002c964c4a32e7bbd7554c9c241006cb9ff8b8837637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57403633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bd09a21462a130875d35d5754b9b645545427d4d70b8dda2b33fd1030563ac`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbd79b5de9c1c75780d3cdf2ec17198c902a62b66c49d13db1a7d52e2d569c`  
		Last Modified: Tue, 12 Nov 2024 03:23:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abadc2aa39d2916fad313d34a6d2726e4f9e45159b0851adbf01b8acbd0313f8`  
		Last Modified: Tue, 12 Nov 2024 03:24:09 GMT  
		Size: 26.0 MB (25951808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf8cbd36a8fda5e2506a6ee3f8a5a3b9ca5b184793e3c55feb3494781c7e0c0`  
		Last Modified: Tue, 12 Nov 2024 03:24:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c669de6545b75f86c877d0cbc9bcc8039b5375bf7aeff124c5899c0107ce674a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4e5856f763cb4143e73d09c1dc81fbf23aa2cacaa1dc2c5265a3c16de96ac3`

```dockerfile
```

-	Layers:
	-	`sha256:13c997fe605b0da8eb0bd8045be9245e125ee51c5e50bef3fe1fda2df952f653`  
		Last Modified: Tue, 12 Nov 2024 03:24:09 GMT  
		Size: 4.0 MB (4005298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cb224b924e97c12f3fa927942f8c0ebb49e9822684e9365fdb40596da8e0207`  
		Last Modified: Tue, 12 Nov 2024 03:24:09 GMT  
		Size: 19.0 KB (18954 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:cf69499fe7bd248a2351dab2b5f73cef1b103bb42ed4fcac00ed32b6ff1c5510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49958775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb18cb2b57866dd119da2f75f7fb43719e8f7f18613b758cc701ca8f4cbbea9`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 20 Sep 2024 18:57:44 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["bash"]
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f78d99a3de34e91faa5092aae0e2c26d0628985f89ee5db652d387eb9e6cc8`  
		Last Modified: Thu, 17 Oct 2024 15:12:44 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b3365c278381b867ed0f869d64a2f39c578a72299a43a44a9deab22552f164`  
		Last Modified: Thu, 17 Oct 2024 15:33:57 GMT  
		Size: 23.4 MB (23368955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f07943a618caa4215e161b0235e4103f5eb4dd48bdf7c01e8140a6aeebba6e`  
		Last Modified: Thu, 17 Oct 2024 15:33:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:da408f7d616e6abb37c6c0ecbc28433581e221cc2c5d9cf3d8cb769343d0ad49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7888a1c5876a96c78051cc68a572e58c1da52d9e1d8a2a90eff4b21da70aa480`

```dockerfile
```

-	Layers:
	-	`sha256:e6c0ad7bb387284fdaf77bfc2e47822da99a3c9cbb9a8f6679059264b39ec664`  
		Last Modified: Thu, 17 Oct 2024 15:33:56 GMT  
		Size: 4.0 MB (3964190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e5ea3ae50391f3191646006dc86d902fabadf5c0e2d5a3845227ade42a75c50`  
		Last Modified: Thu, 17 Oct 2024 15:33:56 GMT  
		Size: 18.9 KB (18863 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:199bc33e7feca6a3ca060e218b436faf212e85595cc8c93b44b0426b4901e943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55153037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2bdda619f7e7fe83d16e69233bec25b6e1ddee283686b5047879a29d7ebb99`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591feb0874eac35869e3201fb6de6cd41276754487f7f5722a1f98ff0ae4a004`  
		Last Modified: Tue, 12 Nov 2024 18:55:24 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc3cb9afa0fcec248b588fd26e55fdacf802e95d552e4f1fb02b8fd0554ca3a`  
		Last Modified: Tue, 12 Nov 2024 19:06:28 GMT  
		Size: 25.1 MB (25061172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60873c7c94d36fac0869b4b087e40c4f478685eee2cee00cfcb944a2997ffeb1`  
		Last Modified: Tue, 12 Nov 2024 19:06:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c559034a009d5898d8990a832903b10775a539743d87a90cb7ce93b279a93648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71585ca259f7ba614d2ca5745253830cce0756b00e06aaeb26f6bd03eb159ea`

```dockerfile
```

-	Layers:
	-	`sha256:ad2edcfbb783098469ae0f9fd4b50f19043775be023e47585251c5d2310767c1`  
		Last Modified: Tue, 12 Nov 2024 19:06:27 GMT  
		Size: 4.0 MB (3979683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b26018bcfc9d77ae17afcd47180d26d53b82ad308f858177eae40fef4b070bd`  
		Last Modified: Tue, 12 Nov 2024 19:06:27 GMT  
		Size: 19.1 KB (19070 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:e5101e052da4dba4c9a5c8ed80d6e5f027fb60238f31dc13e2165381ef78afa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59926632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f1315b323108d3d1ca1724a6923cd96a8b1a9d0e07ae55d53c15fb2070251c`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c446544c47b55b0bd5902dc5f70d0e3b430ed7deee2c7cd8f15cc4562b90e0`  
		Last Modified: Tue, 12 Nov 2024 02:47:46 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2718f9d1ef0b8e47a7c0aedfa0c3b35afa4d8ffd60aee2b3c0292e706455198f`  
		Last Modified: Tue, 12 Nov 2024 02:49:14 GMT  
		Size: 27.5 MB (27503016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c57f6103a19c3187df5702f441ff76cdfdeaaab9b0e2f7ad21e49e6a2049e4f`  
		Last Modified: Tue, 12 Nov 2024 02:49:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:bd62071c4efffb91c548a278825ed81f495eaf270fc4cad4a266bf440bdf62eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f5f546ed4d7e1cb7861249d1d2b86dc39c188770a51d149e03942a29f8cb01`

```dockerfile
```

-	Layers:
	-	`sha256:8e7dd0108d0e5af631e41c9762887faf17c5ebf0491b513a69cdc2a41e61a0cd`  
		Last Modified: Tue, 12 Nov 2024 02:49:13 GMT  
		Size: 4.0 MB (4009516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edfcb0e9146e184bf35d68bbae00ae505d0e62213c7f6f6aca84d317d952c1b5`  
		Last Modified: Tue, 12 Nov 2024 02:49:13 GMT  
		Size: 18.9 KB (18917 bytes)  
		MIME: application/vnd.in-toto+json
