## `perl:5-slim`

```console
$ docker pull perl@sha256:178a029f9da961ff36db9344686ea5a247db82684652195f20f6bc201cdfa3e7
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

### `perl:5-slim` - linux; amd64

```console
$ docker pull perl@sha256:2486de0c86ba6abab68522311fb0a010249d8728105dc00c52fd619ff1a76774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57796060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f04dbf99936a20eb176e70ed249f31ba9b5ddc0d63081ce2b6a374d730e8db`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189e04809c191c3ad63d94caeaef463151dad4d79533807cf223b70caff33b0e`  
		Last Modified: Wed, 04 Sep 2024 23:19:08 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678fd826db01cb097ac7a3858f77ddd6915d55ef5cc66ae2caa82e3052c22e88`  
		Last Modified: Wed, 04 Sep 2024 23:19:10 GMT  
		Size: 28.7 MB (28669311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d10f7527779ee8d65659b85e1501d55e6fed73cadf75909d1bdb565d5bae36f`  
		Last Modified: Wed, 04 Sep 2024 23:19:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:05650f6595cc4443b0be42c38859a85c6a7b6fece6eef19426492985ddb0b70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3762628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53d3eeccc370c705fb8762032d971f203504ebd863910f73e0ddc372e5fbdad`

```dockerfile
```

-	Layers:
	-	`sha256:14ea143565f0a9021e85f9b037baa2094da99931b1cc0b800a2af03b5fdb3f6d`  
		Last Modified: Wed, 04 Sep 2024 23:19:09 GMT  
		Size: 3.7 MB (3742736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9929c124bc696ba333210a9fdbb3f88a3821a0159d6450ebf1e3e7f2cd462cf`  
		Last Modified: Wed, 04 Sep 2024 23:19:08 GMT  
		Size: 19.9 KB (19892 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:c1b318e8b4029bcd74ade1b4699a61b7f181eacda721f176b6234495dade262b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52665673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124dfbfdb855229176fcc11be9b3224fab380977580bebfbb1c29253f80efd7b`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83e3763c3015113b5770ffa9e9254b4751b03fbbd833e55608804eef4fdf7d5`  
		Last Modified: Thu, 05 Sep 2024 03:41:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df3aa0532ad42df2456b65ba22a290e002b3080367d66950cc5aacd05a50c4a`  
		Last Modified: Thu, 05 Sep 2024 03:41:55 GMT  
		Size: 25.8 MB (25777998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cbdfa098c13bfea90705462451298f8beaa6d04ff3f90df3a5816c89a39389`  
		Last Modified: Thu, 05 Sep 2024 03:41:54 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:408ef46e826e77bfa820a0b612d7cd2872da657046e55625c89b1c1a52598bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae930bb3a748e49709fc00832849d018e7618d2c94f2b01fb6f72db46e75212`

```dockerfile
```

-	Layers:
	-	`sha256:896a955336d83475f41ec9ebda9ab25464bf8911fec39be59a3e726916a9d684`  
		Last Modified: Thu, 05 Sep 2024 03:41:54 GMT  
		Size: 3.7 MB (3713174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fe8e8bab8509268108e9d11bc41c7acf00884e080b7e333ef04a4a12d07fd95`  
		Last Modified: Thu, 05 Sep 2024 03:41:54 GMT  
		Size: 20.0 KB (20010 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:ca640973faaaf664e255e307adbc28aacf021f0be1ca4e7db4ffbe27893268d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49704443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb9337f656a7aad70411379b332a3ab316c3a3a5e474509a0e2b97e52032667`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286f85eaac31ce80d7f89c91985374093e44d6e26b6a84dc28cda35148727505`  
		Last Modified: Tue, 13 Aug 2024 12:45:56 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3ebf06e549d189584edc9065e64de3c04288f55e41b28e8c5618a5ef3e6e2`  
		Last Modified: Fri, 30 Aug 2024 18:18:56 GMT  
		Size: 25.0 MB (24986035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0f2626ca8050aab5d5a40ec270d567f2a83b775b2037abd19fef4b2fb02feb`  
		Last Modified: Fri, 30 Aug 2024 18:18:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:5483b9517b3c9380670f54f5ffb78286ebb06134dfd3faf3abb5fd8b800e6731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524d9c6d046ede9242e58a055c8c97da2b201322df34077328a8646c16b9e579`

```dockerfile
```

-	Layers:
	-	`sha256:fd8aeb92cf94f479cb803e0ec8c2c7b43e56423a5bbeae2c1b28ed4917f3dc8c`  
		Last Modified: Fri, 30 Aug 2024 18:18:56 GMT  
		Size: 3.7 MB (3712785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6914de457e16cae8d38ace353c123d98071ec66f1c4f3fa5998e783d48f79523`  
		Last Modified: Fri, 30 Aug 2024 18:18:55 GMT  
		Size: 20.0 KB (20009 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:1242fb7d5b0f39133be864e39fdc06ecb884ecc83e69d4328d13a14c457f0e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56617462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f250375c6547ed2892b73146d780fd25ab4e95757678f18e494eabfa7ae7156`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab597e8392b11fe7ca4a47cf01a5b0a45a3b02007f73ee9ff0b6caaca32b7fb`  
		Last Modified: Fri, 30 Aug 2024 18:14:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954108bacdb8797d28136b352c5bd242a8b7ee48cae520e79d6b6a7fe52b92d9`  
		Last Modified: Fri, 30 Aug 2024 18:14:10 GMT  
		Size: 27.5 MB (27460666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efda1a306ad2ee3999e166c49eefdecc5cece6fae1d9aa5e02fed859ceabbb9a`  
		Last Modified: Fri, 30 Aug 2024 18:14:09 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:bb4f2f1a69898504927ba5925bf0d09db8088ea84ef88e7b872440f8168482ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3734276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1fce0a764c274454f1001b01510682f09333678e67da41e212afaa95768861`

```dockerfile
```

-	Layers:
	-	`sha256:4baded39fb18507616d550a6e45d139df4b21e1fb2ccc49e8f5b62b7e4f6c838`  
		Last Modified: Fri, 30 Aug 2024 18:14:09 GMT  
		Size: 3.7 MB (3714003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a90781fe3c01ed2bb60faf7a6f4599875a0f0261fc3683e1f1f0a84a236d9e`  
		Last Modified: Fri, 30 Aug 2024 18:14:09 GMT  
		Size: 20.3 KB (20273 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; 386

```console
$ docker pull perl@sha256:681c72f8531f90578f6a00bf02fd0fce64bceab5d9eaaf4c8dbf37ec9bf442d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57817443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14287c116db8fab60ad0799e71822d2a8c49d1cfd31d965e31e345fa58b6c1d1`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be41c8d3c1e9de7af8d507b7d501f26477d0f1ff564d29ec37811f923c4cb8bd`  
		Last Modified: Thu, 05 Sep 2024 00:25:12 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1b14e47dc47dc13521349f3bb088bb224a966cb78ea2c1b1d0f492deec1b6c`  
		Last Modified: Thu, 05 Sep 2024 00:25:50 GMT  
		Size: 27.7 MB (27672884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1e11f225047c57fd941235e3cb55cba5bc24a1c1cb35bbbeac7016ff1f31ab`  
		Last Modified: Thu, 05 Sep 2024 00:25:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:a16f3fe0cbe405f8278d4096e309127275df64bb010aeca23b9264498c971784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704fbc617c8eb70e8252573905db5040ca4fdacad71dc1bb6cc5b16aa7950ac6`

```dockerfile
```

-	Layers:
	-	`sha256:3eb1ecdaa25b5106661f0c385a899e17ed508c5f13bc22cdc8bddef7d2249f3a`  
		Last Modified: Thu, 05 Sep 2024 00:25:49 GMT  
		Size: 3.7 MB (3736609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ad2854a2fe98947dca390dcb7bb3647c998add19766ebd18d937e9f578cbdd2`  
		Last Modified: Thu, 05 Sep 2024 00:25:48 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; mips64le

```console
$ docker pull perl@sha256:f958ebe156a8256d1a8d30a49351b726fe935a086e356bfa48ce8a3766443724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55947310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a9a4d4495c7e5d849a4b5731e234f63bb8fbaa2211c6bbaa4d5bc4f1468d51`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:09 GMT
ADD file:2fad80cfc89f7b624d81eb445f9c64e4cd3f190b85d89f40c33eb7e4bc562c6d in / 
# Tue, 13 Aug 2024 00:11:14 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:e8ebfef8c6b7f6250b54eec0d5d1ae5d66f60f418704f4094cb9291dc214be0f`  
		Last Modified: Tue, 13 Aug 2024 00:22:29 GMT  
		Size: 29.1 MB (29124941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbba02a877500d4e9aac9fe733acdfaa6eabbd68deb911fde6ed7063aacaf7e`  
		Last Modified: Tue, 13 Aug 2024 20:56:23 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989620f1300fd058babe51295594d4e5c31c395cd00445ffa235dba0b49027cf`  
		Last Modified: Fri, 30 Aug 2024 19:14:27 GMT  
		Size: 26.8 MB (26822101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4140e4e2730e8252fcb1a16f7a6e2cc390ac4164209d93e68bb67def6de1203`  
		Last Modified: Fri, 30 Aug 2024 19:14:24 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:696514e7d3c757bf1ee4663f2b83ef55be45d7a6d3110ebc5c2ebbabeef4d0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17deb3e8d29963ae8f3f4126b97a4af15ac0cfa029016b8a55c7b1476a93bf78`

```dockerfile
```

-	Layers:
	-	`sha256:515f306ae077fa45c916e002404ad2b0c8f57777fc6b47514492ca8b7c56b8d3`  
		Last Modified: Fri, 30 Aug 2024 19:14:24 GMT  
		Size: 19.8 KB (19784 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; ppc64le

```console
$ docker pull perl@sha256:a2204905d78ac74d6c6643a442467c9d7891494998686347fbee6e6e451223c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808f060cb2b901e3f14eaef3ccdb7e21441802f0435518b4506b6900734d4455`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e077182d775e08c3d4709ad38c4d0dfddf9316046cfbdc0c6ec9550cc2b8b0a`  
		Last Modified: Thu, 05 Sep 2024 01:21:57 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9534a24107b2271939f4c083fb5c15d54c459b78d6b24aac3c1f48827d6fa9`  
		Last Modified: Thu, 05 Sep 2024 01:21:58 GMT  
		Size: 29.2 MB (29240412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7254b2d390f9bd3b67c9677c5b849862df5b054b733d8a982902e31a1ce7be5e`  
		Last Modified: Thu, 05 Sep 2024 01:21:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:3fd136c6730e8ca7c57d4b9227ab9385559109ea97cf80b6c4e9fb84e5b721da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251ceb408597ff23da5a9c9299473186b26cec43093bf95e34552842da339a4a`

```dockerfile
```

-	Layers:
	-	`sha256:ecaa47d2cf46a389aa263ea1f6f835e50f009664fa97bbe440edfdc49877def9`  
		Last Modified: Thu, 05 Sep 2024 01:21:57 GMT  
		Size: 3.7 MB (3728463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53e725295f38552be9cf1f81340eb5834ff13f422d703c58330fb7bdd5c2b77d`  
		Last Modified: Thu, 05 Sep 2024 01:21:56 GMT  
		Size: 20.0 KB (19966 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim` - linux; s390x

```console
$ docker pull perl@sha256:27cf2a71da390dd0e24e8d0c83dde7811dcaa68cb2488dd0b644bc8ba591ebae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54698871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5e6ef38e5bdd5edd7a84c3f281bf9adf1677358f4fe2a7cb25540df8a7ef0b`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 30 Aug 2024 09:24:08 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["bash"]
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/perl
# Fri, 30 Aug 2024 09:24:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 30 Aug 2024 09:24:08 GMT
WORKDIR /usr/src/app
# Fri, 30 Aug 2024 09:24:08 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5b4928b2a810fcd721fc12f54789a0998cd9ed5bcf75e1459afaa9c8100ea7`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c10f2669e9f4e3b80201cc37fa4621c8b779846c1dddddaff31f4cbfd93701b`  
		Last Modified: Thu, 05 Sep 2024 03:09:52 GMT  
		Size: 27.2 MB (27208286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ae56008b82ab85e26769402da8359b63f5eb7150d760b63897cb130abd528`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim` - unknown; unknown

```console
$ docker pull perl@sha256:277cf611b56da8c01f386f3ef1ebe5228c41c9620ce5b803157c9f85eaf0d4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b507bb2006036433c69d112819fc82b637e01fb80e5a206475af4d432ed0e7`

```dockerfile
```

-	Layers:
	-	`sha256:b342c3748a271df0b416fc88ed8e75b5c9280a5d18deace5b31677c876e7e998`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 3.7 MB (3731006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ba787d91626290b4c49622946c0e8505e528996c0a93fbc045c4cba05cccf95`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 19.9 KB (19891 bytes)  
		MIME: application/vnd.in-toto+json
