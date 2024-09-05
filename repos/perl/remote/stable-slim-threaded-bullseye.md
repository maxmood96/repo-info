## `perl:stable-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:2d82ab2a25a4c5c8f4405aa482522090708012c6021d81787267f02c5a733fba
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

### `perl:stable-slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:4fb0483da181ebf01fbf20b64e7f2d14803a49fae4f3a1a824411ea4bc030b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56222404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeef81c086979a5aa46d1023843bf4ca6531b23b02916dc2eb7b3cdf1edda14c`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f14495fefcef85466d64e83a33e76929784189fd7df35c153df4cececbdc980`  
		Last Modified: Wed, 04 Sep 2024 23:16:25 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e6693bafeda8bea40886e39b3f687da4deeeb6b7c24439feb4befdce263a14`  
		Last Modified: Wed, 04 Sep 2024 23:16:25 GMT  
		Size: 24.8 MB (24793464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f3cda32bc07c61ee3963888752ca7e0407306c662580c2711079df1c29ecaf`  
		Last Modified: Wed, 04 Sep 2024 23:16:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:620fead0f57e6f19d3a5ffcdfacf03f42ad6117dc184e802a06c67fcb29a73f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852b0a72389f713f84a91b3613550e1285342d6d0928081cdb2b58b07f56c6de`

```dockerfile
```

-	Layers:
	-	`sha256:0c01cb0c41451f0e94d3db09b0e24343036eced06405bad8c05a72dc833f9faf`  
		Last Modified: Wed, 04 Sep 2024 23:16:25 GMT  
		Size: 3.9 MB (3934341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22bdb7ea0b0ef97dcd7dc2c495dfaa27dac78bf88adb21c3d6e56df233866f01`  
		Last Modified: Wed, 04 Sep 2024 23:16:25 GMT  
		Size: 18.5 KB (18537 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:c4db2c85ceee044df38759d14c6d73eccc40ed7fb6a1a716c14d10cca4d357f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51704649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b56bf45cfc46f9f9274e4227297adede42ff487aadc5207a0fe5ed2ef5077`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:b6f3f19f4bd2bf78068380b3cd10d72519ced99a2b5abe830b4729df341dcfdf in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:c8ed7888c72e20491bc1a05ae8b473757ca4d400de33029eab69bacfb9dd933b`  
		Last Modified: Wed, 04 Sep 2024 21:52:15 GMT  
		Size: 28.9 MB (28924911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c583beb80e6f7ecfb8f1db6d2235cecf4965d351990190717b574ea357b1f0a2`  
		Last Modified: Thu, 05 Sep 2024 03:47:59 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed247e92ff75d075ab2ec7f98633d0e8417e0c3c7ad3d9e26238a67a13d85c3`  
		Last Modified: Thu, 05 Sep 2024 04:03:08 GMT  
		Size: 22.8 MB (22779473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9028711f161692f3f371b2a9cfc8f9d1e5619f3a1bbeeab889c448e94cd7c2`  
		Last Modified: Thu, 05 Sep 2024 04:03:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:46bb4262ba9b59855bc17a17e5ad4a11fde8cef5fb83ed4df91061d774a24af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1f036d63bbe2b39f80a68a9e62fc1bc5e0fc926ba500211899b4c4860b1452`

```dockerfile
```

-	Layers:
	-	`sha256:a3eaa02f11a529b9fa28d0d7b34370efb648377a065d482770ba7623e09458b4`  
		Last Modified: Thu, 05 Sep 2024 04:03:07 GMT  
		Size: 3.9 MB (3905554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a322fc48faa69c553d3327f9f5bcbac66d2aff693c05d1cfca51659c88afb25d`  
		Last Modified: Thu, 05 Sep 2024 04:03:07 GMT  
		Size: 18.6 KB (18615 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:d895240829176141d9babe46f9746877954dbddad2b55bc0ff7c1c72a1ebd04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48760717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb48a28b72ad417074e0feb2a087c2b1c35e639b7f194e280542ef30dca2db28`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:55 GMT
ADD file:9f6a2e97ea42608bfeab22c77e01d6614f64a00a2be04ed1cff9909375d517a8 in / 
# Tue, 13 Aug 2024 00:57:55 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:1a1ab1e12ebdbe1b5383067049fc746bcb9b882bd309b8befaa11c47eed5d4dd`  
		Last Modified: Tue, 13 Aug 2024 01:01:38 GMT  
		Size: 26.6 MB (26589215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1705edffcf0f99170984d5e897d8f2209d3d07e9917f9bb477107523ab0fa2d`  
		Last Modified: Tue, 13 Aug 2024 12:53:01 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac95455cece4666a3841f0a11b77235da66e72941c455fafb7909eec443127dd`  
		Last Modified: Fri, 30 Aug 2024 18:56:38 GMT  
		Size: 22.2 MB (22171235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6752cdbb1b7425b3f656b4d8f40ac42aaf1c1043eb24264c3bc1f33601950c5d`  
		Last Modified: Fri, 30 Aug 2024 18:56:37 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:3c2d2953df3aae14082375517bb4b973b9a795b7ccb41eec117c2c728f34da30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3926885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a0eb7dba9315b7d90c1d57891e2ad32c56628403b7b7d17f389d07b3144349`

```dockerfile
```

-	Layers:
	-	`sha256:9c660507abb5ca7264df7a71edf78168f2114c49d42e71dfe8efa98020193eb2`  
		Last Modified: Fri, 30 Aug 2024 18:56:38 GMT  
		Size: 3.9 MB (3908272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18951d281f1bc072931644eb0526a9c0d7b2e44425a7d28c260a1c9ba8eac1ed`  
		Last Modified: Fri, 30 Aug 2024 18:56:37 GMT  
		Size: 18.6 KB (18613 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:788fe599ea4b5b251ba439263c15361699df0b9fcccf0e355d14bd6fafdc6ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53979801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897debc4d28b52a32b80202165efa9a056167688c55f1aa7e12fad2a00c7b6bb`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:06 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 13 Aug 2024 00:40:06 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6768f1223e6d26a4bbcdca7648240e8023a2dc4f4871f0ccf3daf94475a188`  
		Last Modified: Fri, 30 Aug 2024 18:19:24 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a391366c4a15976ebbad2e49441cf47d1bcaa2a7fdf418e92947139d6ca1376`  
		Last Modified: Fri, 30 Aug 2024 18:44:07 GMT  
		Size: 23.9 MB (23903444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029afbc9f215416c6e56491a2f96122b6ee10c85b23928a53cc14515e1fb9f51`  
		Last Modified: Fri, 30 Aug 2024 18:44:06 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:6543f18d170089625ae3c6273222098772d1d739fd229abcdd4c3658f61ab4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bfdee94934830a0b872ced3d601f282b4075677a632570a261204a4686dbd8`

```dockerfile
```

-	Layers:
	-	`sha256:6f89a336859c394bc9024d9859315211d9a03b13cae742aeff8f067fb8b11953`  
		Last Modified: Fri, 30 Aug 2024 18:44:07 GMT  
		Size: 3.9 MB (3908714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fed3df55fa2fd21400e706b869291bb40fdd3d7f026b400228dbc464ed5982`  
		Last Modified: Fri, 30 Aug 2024 18:44:07 GMT  
		Size: 18.9 KB (18858 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:f8a2d30e020082555d13ebc6cecad5b4059a92b9672085dfa57b5af6a1839039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58672947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b06a61b678e4945a62670ca8cf084fdec19f49de86ac47af172015cf6ffd71a`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098619f0a501eb5c72538f80df934d05534d97e87133f95d7274a3b11c463d92`  
		Last Modified: Thu, 05 Sep 2024 00:26:43 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489037fba8603e9a6bf2a98adaf4c4137bb4fcebc61a0f4dc7a0a232137a73b9`  
		Last Modified: Thu, 05 Sep 2024 00:26:43 GMT  
		Size: 26.3 MB (26259367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c062483613db85dba044c57a091144a039cce83ba078d14975a703e58be2c9`  
		Last Modified: Thu, 05 Sep 2024 00:26:42 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:7e79fb35971d9a474f9c78c5f4e6e3416a7d5120f741b67183f12bf711948ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3957095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5515942f32307ee84bae8753f0e215fad9d95ad1255a94e520e36676af910bf`

```dockerfile
```

-	Layers:
	-	`sha256:a2883bf9f61da623fadd7e99f1deea136684fcb5ef3b269411a03089b7cb0580`  
		Last Modified: Thu, 05 Sep 2024 00:26:43 GMT  
		Size: 3.9 MB (3938592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e515c50a71e1c15f61f39ada77905137429ae8e7a85d78a96949cd8ad23dc35`  
		Last Modified: Thu, 05 Sep 2024 00:26:42 GMT  
		Size: 18.5 KB (18503 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:4c15d432febec404d9418586c9257137c3d395b3c4ddcb56e828ae18220a6db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53347580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42b69dab43bff0958c50310298acd2586b7f5340a5829e65d1d7a0a2a7a29f2`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:12:29 GMT
ADD file:d4b92daa2701c7af077c4c89b2b1f5a97cfc6389c09e049b3bdaa36454653bbd in / 
# Tue, 13 Aug 2024 00:12:34 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:15b8bd5d9ec350cbe23bbccddd5284b3cc9139e037500a63a02025354518d5c8`  
		Last Modified: Tue, 13 Aug 2024 00:23:52 GMT  
		Size: 29.6 MB (29646095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa7099e1bedef4abac5565314aa663115d1958638c57948643a95b56b2a7c31`  
		Last Modified: Tue, 13 Aug 2024 21:21:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411468c72a9f9b3f024cd2a3bfc9848fe78126d7e055303deefaf5844e4e73e4`  
		Last Modified: Sat, 31 Aug 2024 08:44:38 GMT  
		Size: 23.7 MB (23701216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec589542b257d8e2f4e5075ea84d8cff1cb9e53f37f736c69003b378c8f39099`  
		Last Modified: Sat, 31 Aug 2024 08:44:35 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a7307b616333bdd61c698be752fd584390d8c9de0f5aaaea21cbda31a599d454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5704d2bdb3ee135248667747316404ef00901242f1205d64bd5aa8ea9c2e86e`

```dockerfile
```

-	Layers:
	-	`sha256:d1fdc632eae77f060ec23018e21d4c9a75a67ff44e767710589bde88254e063c`  
		Last Modified: Sat, 31 Aug 2024 08:44:35 GMT  
		Size: 18.4 KB (18383 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:cba6cffd9f5020891bb7ba651c4bccb96c9365719a0fbb52b9b0507ead8a5224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60375210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18a9328fee8e8a4d586b93f2380967063539686bc1d46cbe9f09ef30625ebe7`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05a4dfe7b57aa553ae464260d6d528d00a65a9704395de98bb0c889034560a8`  
		Last Modified: Thu, 05 Sep 2024 01:29:06 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b44c49ea123c5b65ec02d05bd662248db293a739c39cf422db8dad0c6c48c84`  
		Last Modified: Thu, 05 Sep 2024 01:43:26 GMT  
		Size: 25.1 MB (25075674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c482c082c5d83f80447d5f7a34aa5e8a55fa3c5d0b046f33b41a5704bcb613b0`  
		Last Modified: Thu, 05 Sep 2024 01:43:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:8dc9d2fcb20fbe8bf5a01b0afb2764ac5982e569974c85f2e70f2b42554a9315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0822ef5e2412307fcb173a00f49dc455a6b96d316d399b7bd777a911c202b9`

```dockerfile
```

-	Layers:
	-	`sha256:12a51bc72fd86f6c421743b32a726705d9c74cf0756683d5fff987a705c01ba2`  
		Last Modified: Thu, 05 Sep 2024 01:43:25 GMT  
		Size: 3.9 MB (3923108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c701f40e1c5791d4a3ebd74dc9702e411fe2c2f312fa250fe55851ca9f5b2d4c`  
		Last Modified: Thu, 05 Sep 2024 01:43:24 GMT  
		Size: 18.6 KB (18581 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:866434a6fb62298c2763855cba6d3a08c4588545855d6dabc06b253bf79b80d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53680685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7945420d511135b72f56f5fd62bde921a5549862f94204d60e00f4dab07d7f6`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020be505ef141fc8471875e5886dc028ab0e7c3349550b8a6177f7accbd871f9`  
		Last Modified: Thu, 05 Sep 2024 03:16:20 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2636f1bede17901378443c93c64d536cbc80cc03717c57e1fb534a3c2bcb6776`  
		Last Modified: Thu, 05 Sep 2024 03:31:16 GMT  
		Size: 24.0 MB (24016973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac519d6463c7a7e9d00338b6e58ac63dfd32d964c2c200c66c8eab1926cf400f`  
		Last Modified: Thu, 05 Sep 2024 03:31:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:898275a706d4884b00467a9ca4554356955a534f0818c1a957de67230f104975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e79ae85979bf97acca7cf0d4440d6f48578838cf9202f9151250bbfe7157191`

```dockerfile
```

-	Layers:
	-	`sha256:ba1d7b121d2689a1d5ee3ff35ab819db16fef463a07cab1f31ee2f0bf669ca35`  
		Last Modified: Thu, 05 Sep 2024 03:31:15 GMT  
		Size: 3.9 MB (3923043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9dee902d3cca80372724369552a31e6f63a4ccaf6c0db39610ad1ea87b0e019`  
		Last Modified: Thu, 05 Sep 2024 03:31:15 GMT  
		Size: 18.5 KB (18537 bytes)  
		MIME: application/vnd.in-toto+json
