## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:4993a4c2c46c3d77f8f87d916ffa61b52d512e99d72c545bfdeddf977b73705d
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

### `perl:devel-slim-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:d292832133a3ae4a9dea0ea04d4cf1ba32fc42e0e16f11630a1d6bfb0bdddc3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56161676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f3283422d28dbde3752740094ef6da2b1d31fbdd7a7a1bbeb5e7ebbf967715`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b997f2d5a324156917f41eb2f4a370a09036571bee009f97ad62eb222a49df`  
		Last Modified: Tue, 13 Aug 2024 01:27:29 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7993aca696e81d9835ceeda3ff79b7f3b58921e99d9a6d986fad421d489c5774`  
		Last Modified: Tue, 13 Aug 2024 01:27:29 GMT  
		Size: 24.7 MB (24733125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7baded348d04f57223b40ced0327a669c8a0c0347807fba6a785d98f76a350`  
		Last Modified: Tue, 13 Aug 2024 01:27:29 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:7c4dcfad0fd1b68e3fcb93c24f43502cfb98b8074391a88bb190ef37636ca66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36296141ec0ba76e3615f24e31bd594878d39eace26924f0d3ca8856999c6102`

```dockerfile
```

-	Layers:
	-	`sha256:0dfcefe4378e69ac38122a23f16eda5538724aca8dea586d537aff2953840e17`  
		Last Modified: Tue, 13 Aug 2024 01:27:29 GMT  
		Size: 3.9 MB (3933629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:507ca05ec95e394beceaf44670d0564eca749f8a81cbdec373cff616a624d3d5`  
		Last Modified: Tue, 13 Aug 2024 01:27:29 GMT  
		Size: 17.4 KB (17360 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:ad5d456032fe44ce6f3892c6fd716c96a8d15754abef32c183c13c2e06415445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51677328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff857f564c6c5bd129db8f7767f4c603b8af82c33b90b2a55dd8110107fbf83`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:56b9d2d0e0360f64ade3cbe073b446e10c8e6bd253b761c16b5f319a8103d181 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:5b04226d50f1c00a6c8950192ad70a2038016868ab6ffb162ad447e35e67a3cb`  
		Last Modified: Tue, 23 Jul 2024 00:02:06 GMT  
		Size: 28.9 MB (28930588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66647c1f3ce664aaec353a91e99652d845681b6ca7432e025c53648644e5839`  
		Last Modified: Tue, 23 Jul 2024 08:31:25 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe5a41b9dfa7e880a0545fd0dcf71f1320bb99de37a47cb1c76ca0feed8c7d6`  
		Last Modified: Tue, 23 Jul 2024 09:58:00 GMT  
		Size: 22.7 MB (22746473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1e23a4c95568889117e523862ea6a5b9efb365b06d152b49d8c1a75f7e88f8`  
		Last Modified: Tue, 23 Jul 2024 09:57:59 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:61830e949ee574a6616a4a318f22a949ac32687fad894c79f95ec6af804a86b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ea04d0b1b7ddc43d3e383d0f45e084799ad10fde5ed97196b43e0cef46a439`

```dockerfile
```

-	Layers:
	-	`sha256:77240699de4335137e21d074a57831960848d5e2c2f9eb8b4e2b6d972ebe2629`  
		Last Modified: Tue, 23 Jul 2024 09:58:00 GMT  
		Size: 3.9 MB (3904826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd005d7b4065c787c885df9d5d78dec11840744d2ce6072939e40dc814ddbcfd`  
		Last Modified: Tue, 23 Jul 2024 09:57:59 GMT  
		Size: 17.4 KB (17421 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:820aaa0ff5c1acf2b5bb21656da23c58aa23b7a6737d275754fe759eaaa2ac4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48739095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9910471e034894e0865ca9e3f244ff1bdba9376ac2b6eeea4e98dad6c85c1b5`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a8cc186c41214e293c47fedcd8aca489d4fbaae7b1b4731b3e51cf40bf665`  
		Last Modified: Tue, 23 Jul 2024 23:49:29 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252c09bd2bf559ebb8b0536126007955f895845b707a0033180030d3597919ff`  
		Last Modified: Wed, 24 Jul 2024 02:39:30 GMT  
		Size: 22.1 MB (22149696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abd740c7b8489beb0480772e9d8c2d639096583f556a260d3fc5f863aed1651`  
		Last Modified: Wed, 24 Jul 2024 02:39:29 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:7f96e9012dcc310c63b1442ea6d0b886b0a814da9d041e9110fa08c13803025c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177a6a8ebac58358b3939761a5c3dd3bb09419322220e82430be0bcdc23aa128`

```dockerfile
```

-	Layers:
	-	`sha256:340933e4befb3346894475e06b020afa25b972ff69fffe62f7ffcaf2ef60f597`  
		Last Modified: Wed, 24 Jul 2024 02:39:30 GMT  
		Size: 3.9 MB (3907544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3c1026452d55633d640456a58fc9f8af4cfa19b3ad63161a2ed7e2506022cf`  
		Last Modified: Wed, 24 Jul 2024 02:39:29 GMT  
		Size: 17.4 KB (17421 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:b427be96c11637bb5f957f5bd1ec3d7491feec7ed97d9cc8c6a9829392b20afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53948969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98aedf0e223500df86dedb65570e4c59c623d90a8298c48e04409292394bfce9`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2fba8b3e699b11527bd79eb822a74f9453273be25bc67c416f8f208d6f7e1b`  
		Last Modified: Tue, 13 Aug 2024 08:08:21 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fddf07d081ac881deb25c6409023319395a4babff631f84584d7eea4a76536c`  
		Last Modified: Tue, 13 Aug 2024 09:17:11 GMT  
		Size: 23.9 MB (23872616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf415c49ef4093a462fb81a416f4b4b39aab2b7b12806e11a1b21674b2c80f7`  
		Last Modified: Tue, 13 Aug 2024 09:17:10 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a0c39af62bba6a838fc948a73ff90c7e382f44070474d436888a70de307e3d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c145fd3094f7963ac66d0178cb4006d3dad29244f54205c7d907a3693d36c167`

```dockerfile
```

-	Layers:
	-	`sha256:a2acebe377c1b6caa3032e08b43c08c1b56ecce3c036e4fe14245b5d27f880f7`  
		Last Modified: Tue, 13 Aug 2024 09:17:10 GMT  
		Size: 3.9 MB (3907978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21fb86542b94202d03d7c9e174c89a6bf8963457040c5c1a84689a5e5f998b23`  
		Last Modified: Tue, 13 Aug 2024 09:17:10 GMT  
		Size: 17.7 KB (17657 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:b93d029c19dadc1fb50f31bd4886a41dfbaf11673d98064f77054b460e3c2dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58577778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483ab660f1408ff2c7b6293c7c883fd0cf0780f61d69f297de06f4728f2405f5`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:1fff23531e74037071ba9be4ee63db5ccfd9c3823dceddfee08bed3fdeb6dea1`  
		Last Modified: Tue, 13 Aug 2024 00:43:17 GMT  
		Size: 32.4 MB (32413784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b997f2d5a324156917f41eb2f4a370a09036571bee009f97ad62eb222a49df`  
		Last Modified: Tue, 13 Aug 2024 01:27:29 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6a089334d7ee9654c9ac3ffe214907118f50a7e2a563a383de63e301738c63`  
		Last Modified: Tue, 13 Aug 2024 01:28:09 GMT  
		Size: 26.2 MB (26163729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea9ca07fab0123a694cb3844a496336e64d2eb26dea35a7e42f8c84ea108687`  
		Last Modified: Tue, 13 Aug 2024 01:28:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f3e4b28944f8031a97915c4885e1632b89992d5c46a1a6cfea955dbedf20d215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3955226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71aac72663d562ee7fa105504145d8288e5b3142075da96fa01f5dcc80c633ae`

```dockerfile
```

-	Layers:
	-	`sha256:154f5d809e474b802b62330a9b75ee9567c33f9d01932fd10d7a87db2ff27edb`  
		Last Modified: Tue, 13 Aug 2024 01:28:08 GMT  
		Size: 3.9 MB (3937890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17858db615827026dba8ce1d8007b973de85a0597e8a041288ba12b1917ffebf`  
		Last Modified: Tue, 13 Aug 2024 01:28:08 GMT  
		Size: 17.3 KB (17336 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:4788e703f76b41e3d66e48fd434372bc00526de4f133fba135692a0297d226bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53289539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f441d811a05b4d4906da1c2899be47fbb61407d5d222780a9650e2a348a46889`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:aa937b31fe693810c8c6e110de59ba07264dbc020fabac9e1ac045df57efc0c3 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:83b27ea307774a387b0a5203cb6aa8f117e44bb5321ed6c8de8b0a0c43d895ca`  
		Last Modified: Tue, 23 Jul 2024 00:50:32 GMT  
		Size: 29.6 MB (29646085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb90bf7b619d2e1072a53d37d9dbbaf5d82e14e1e95b279042ae1c13c18fcef`  
		Last Modified: Wed, 24 Jul 2024 11:57:45 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0679d1e090608c13d1da4930311c0c95511a0be06642c6664a8bcc2c4795700d`  
		Last Modified: Wed, 24 Jul 2024 17:10:05 GMT  
		Size: 23.6 MB (23643185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ade7c086f44bd337305178cdd4a2a638680895971e8529a1746d9c062320507`  
		Last Modified: Wed, 24 Jul 2024 17:10:02 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e0bc656b6b1dbd8089fea6412f30fe3dd7a3c8944e82ef53732ebd510363f221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7508ea41b6510811f16a79a57cf6d071a1d73a66c8a1f831948732870410a85`

```dockerfile
```

-	Layers:
	-	`sha256:977c0f0d532a5a00439f39f0234a11d28dcb5ee1df4b3c986f2bae603cff7154`  
		Last Modified: Wed, 24 Jul 2024 17:10:02 GMT  
		Size: 17.2 KB (17189 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:5b0b0a491471ac0d751fda960495581cbcdd6de118576f4de9c86516dfc60bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60292343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d543f1eeb2fce52477c4f2c7872f126eb1a97d1d0f5d4b4c84cdab8b09eca6`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bc485c5dc2434020075fa18edd35615c27de13f1c496740ca708f1cdb619c9`  
		Last Modified: Tue, 13 Aug 2024 07:47:40 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc915f4bf5e8209d62c2983129a1701313dd2c8e75f0901212894d820edfdf`  
		Last Modified: Tue, 13 Aug 2024 09:13:01 GMT  
		Size: 25.0 MB (24986945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831170f8c77b0079844a24b1613e415926b13bbd891aac7ab914a3da4b4c614`  
		Last Modified: Tue, 13 Aug 2024 09:13:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:208036fe2d4255231da00331aef5edc28711c323e4a9ad4d2e7d2c4da68a71c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90e1e5155c67af87275d81ef9710aafa3f242b4695563969708fae1ac584e4e`

```dockerfile
```

-	Layers:
	-	`sha256:f60a406542c76dd91dd6f4b50c7ccf5e580f8d738d616ba9238ab08322bfe4f0`  
		Last Modified: Tue, 13 Aug 2024 09:13:01 GMT  
		Size: 3.9 MB (3922384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2870192745eadd6b563dd27dd309011fb0d4c38b010671ec8f57da6fa515821`  
		Last Modified: Tue, 13 Aug 2024 09:13:00 GMT  
		Size: 17.4 KB (17392 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:c3827b2721930f0c98848a5d068e0e7e5ffe9563aa36c6a49c1884a49911c5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53627146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b5e8a8fadc6966839f561e99c901e35840b776e90e8ba5bd41e9e43ce0e997`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:a473fc09ddb0d1045f7f330f3a48b9cfe65ff9ea65cfa5c8262a8a5be9d4db75 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.41.2.tar.gz -o perl-5.41.2.tar.gz     && echo '4b8fb14e213cd1b0a6715c3d2d08a833a2ce51ca793f14acecf4799d3a651771 *perl-5.41.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.2.tar.gz -C /usr/src/perl     && rm perl-5.41.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.41.2" "-de0"]
```

-	Layers:
	-	`sha256:83ea1b2f9d26c88827c9a658387c782a21fca528fbf7418f1a4eaea9a9818bdf`  
		Last Modified: Tue, 13 Aug 2024 00:47:58 GMT  
		Size: 29.7 MB (29668965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453cf4e5d557020589bfe0a40163967bfd8c8323adb32248a1c6f4a9a421dcee`  
		Last Modified: Tue, 13 Aug 2024 05:59:30 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5655ff1c956d221d3f04daac271d57a75e8b90cefa9ab84034a279055c718257`  
		Last Modified: Tue, 13 Aug 2024 07:24:34 GMT  
		Size: 24.0 MB (23957917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a0d1050be0f3ddf1b2d3ce87ea7cab0cfe475447d1c3ccfc3fa838d6e749c3`  
		Last Modified: Tue, 13 Aug 2024 07:24:33 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:6125a1e15d47cd968875b926eafd56373fb77e6afe5388de1640fe4eceb6c45c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb345842abfecdeb1517303562a008d70564adf9b444e2417512e15803f7deb7`

```dockerfile
```

-	Layers:
	-	`sha256:b7e83661ec8c70b5ae17a65fc3594da8d71e543ddfa4a1f8724b35e8d8b9bba6`  
		Last Modified: Tue, 13 Aug 2024 07:24:33 GMT  
		Size: 3.9 MB (3922331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7337001e5efca56f9705f86859a73682156e34ee94f30fdbc120127d485af34f`  
		Last Modified: Tue, 13 Aug 2024 07:24:33 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json
