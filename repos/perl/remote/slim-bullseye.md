## `perl:slim-bullseye`

```console
$ docker pull perl@sha256:b00effc47918874bc3956fda1df4422758d2017395e50a20719d90cecc5b3bbd
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

### `perl:slim-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:d74f042261175955353500c6584505801d09d09eeb4632a04da23215f00a5afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56163756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53639deda605718b6fe16e379be66c1652448b75d5fde3735053123a708108c7`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f392507cd69632717f0fd937cd5c4ae7fb623da743d62a4985bedfa8ce65c3`  
		Last Modified: Tue, 23 Jul 2024 07:27:30 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0591f132b4702ef4a912ff0a62702597ac550977ca0d7d0ae52c71bcfaa78ef8`  
		Last Modified: Tue, 23 Jul 2024 07:27:31 GMT  
		Size: 24.7 MB (24735159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fce481081d9b6b582fc645acc0e336f657863dce8a168043fb9a93fbd6fd85b`  
		Last Modified: Tue, 23 Jul 2024 07:27:30 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:dd618071a5f75c949a36d58572ee6fbca1fda26a8925c79502d24b776bfac382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca3e1f4d4d1790e16b87284d68f7bcbec81440bd532228df9a61c4e7fbb003`

```dockerfile
```

-	Layers:
	-	`sha256:4a4580a3d628d4dcc8a61b1bf6377d9aad26bc9579e26d274076cf47a4372880`  
		Last Modified: Tue, 23 Jul 2024 07:27:30 GMT  
		Size: 3.9 MB (3934251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d60e69215148866ad0d2641a0c7d79cff061c234cbbbe227f9f6b51cf094bd22`  
		Last Modified: Tue, 23 Jul 2024 07:27:30 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:3bebce3ccb25e83e8bcfe22b714be01d905aba224da596309d1a413dd5054474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51677448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80962394774e673598e84a20125f4bba4463b376806ad3d2c01b33ab981124fc`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:56b9d2d0e0360f64ade3cbe073b446e10c8e6bd253b761c16b5f319a8103d181 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
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
	-	`sha256:6cd0177a65a38a7565ca0a0c16d62dc3d2fa95e0e93cdef7179d51955b89a1a2`  
		Last Modified: Tue, 23 Jul 2024 08:31:26 GMT  
		Size: 22.7 MB (22746593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6a77458769e2fb6573a92bebbb67a9aaec71b6b0983618cb38513d89309489`  
		Last Modified: Tue, 23 Jul 2024 08:31:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:9e7e882cbb45c05b6f5c596ed4f6d6ce956c4f2b6287a0a39b64461fc774554e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05abd77900d8d8c1f0e88720f2802157ce52cdadee478f434955dea30e6d683`

```dockerfile
```

-	Layers:
	-	`sha256:cb93b740c3371ce8f25e9f27aaf1a300693b36a13b8d1d9aa79b59dc3b74be64`  
		Last Modified: Tue, 23 Jul 2024 08:31:25 GMT  
		Size: 3.9 MB (3905464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb1bb6971948617ca1c46ca23a3bfe456bac0d376ad0e024dd1431f1981fd58`  
		Last Modified: Tue, 23 Jul 2024 08:31:25 GMT  
		Size: 18.0 KB (17990 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:9ea1033c21f54373d0697b508e90488804821174e9f176e5b1db4c73bde2a2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48737548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e28d76ec4739db3198e0bf9f20342c214ff301e801c711bdd70402e256c2d6`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
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
	-	`sha256:354fe590a5ca79c22c8c16bd73d40707287ec668c29e887ffb88217e892a3b44`  
		Last Modified: Tue, 23 Jul 2024 23:49:30 GMT  
		Size: 22.1 MB (22148149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7edcad7c07afb15f288d380996bec404c396d11550cb637bc8a8feb47b6886`  
		Last Modified: Tue, 23 Jul 2024 23:49:29 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f9626ac8eb264cb2654e7e3d58c038dc56a5552c46729d29fbdddc3f725d8d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3926172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592a6a8cfb2a294e54f0eabf3c93b370d81ec841fc43c25af87992c473dd5217`

```dockerfile
```

-	Layers:
	-	`sha256:942ef9ff05fd81dda48cb58f3ae50de1a3a9a85f62feb06c6595b84d55d468f1`  
		Last Modified: Tue, 23 Jul 2024 23:49:29 GMT  
		Size: 3.9 MB (3908182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d991286deba0d094cbfdbe468b3d5e0cef6fe21f18219510fee11ac8ddac9fc`  
		Last Modified: Tue, 23 Jul 2024 23:49:29 GMT  
		Size: 18.0 KB (17990 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:4b10a3478685e8fd4494b73b889164ddd9c76baf6441203c16461fc4e14f54ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53953737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc604aa8b9c868e900003a01df5e6a01c842a8715cbe55b1561eed83e3cdaae7`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece3dd88229cb7c04fd86720e827b333669f51a2ee41967294dc743daff00b2a`  
		Last Modified: Tue, 23 Jul 2024 22:32:08 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ee5873440042cbfe94c414d9848249d56be9073a3d73e17100190390901f6`  
		Last Modified: Tue, 23 Jul 2024 22:32:09 GMT  
		Size: 23.9 MB (23877385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8d56765366c60800d3b70f76735ba88ffb77d7c6fc1dad71faa6e189166b25`  
		Last Modified: Tue, 23 Jul 2024 22:32:08 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:7a931c15e18b9e278d095f8dfa4b997d5e7572b10fb44d3786d1f218b44bf0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3926857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f802ebaa859cac9a014b4d3f08287f48c2d1cc0b5d7b360702cd69c12e4b8f`

```dockerfile
```

-	Layers:
	-	`sha256:fc09615067e5148435d93b0cef1897d265c2d1873712116ceca1442d99fc92fa`  
		Last Modified: Tue, 23 Jul 2024 22:32:08 GMT  
		Size: 3.9 MB (3908624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c2e7e08c199510d92c0030865e958b12a336bf6965568814e4ffc1c6ed44c11`  
		Last Modified: Tue, 23 Jul 2024 22:32:08 GMT  
		Size: 18.2 KB (18233 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:51e811496aae1ac970f0aa2632491084b0045b424ac7deea5bec0fbc9d0473e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58576540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95aa04f507b83a55f75f85668ae2e587517c8b1b3f48164f0fced5db5811f199`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe32e1ca1f96c482bc84e2514fda8821defdfe719e9ca77892bea67bfcd7a53`  
		Last Modified: Tue, 23 Jul 2024 06:25:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933a8b3eb22cb7fbd744626288de38a3e26a30164b59d4da615143ce2105a67a`  
		Last Modified: Tue, 23 Jul 2024 06:25:16 GMT  
		Size: 26.2 MB (26162465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c10ab17d48724f775a7a6440f3db0c28a617350a11cc73030579a6764dfed54`  
		Last Modified: Tue, 23 Jul 2024 06:25:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:022aaeb7d4d1e2421e0a2f7f0098f6054a42b4c975a6c95d17137dac5f7d6af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3956380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e654fddafc8e0c0362630e70fb3f3b98a37ec554bafeb50b7d95324399b5c7bd`

```dockerfile
```

-	Layers:
	-	`sha256:5682409d0f41a0691c01d13ab76a179222f48b196d00f53c0dd0bc79753845c5`  
		Last Modified: Tue, 23 Jul 2024 06:25:16 GMT  
		Size: 3.9 MB (3938502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f80839bef974688cd986b04bac14089bfcc2736a6b32d3db49a4cb306ccdfa9`  
		Last Modified: Tue, 23 Jul 2024 06:25:16 GMT  
		Size: 17.9 KB (17878 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:21a3c53fb128a13d0d98126eee7f0587301de74294eeebd0d9f7ca5a93f96d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53288467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c302e45c105a41e09061c57bb7b5bfc832cdbff666d99ea00c2f83ef38afd94`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 01:19:38 GMT
ADD file:791d05eca72cc81080afbb76c7f3f02a74893142203b6aada9e3170404049223 in / 
# Tue, 02 Jul 2024 01:19:42 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:59602b870d8ca1e13dffda9de0c5f866f86ff35c1e595ea481bb1b2c48c18b8e`  
		Last Modified: Tue, 02 Jul 2024 01:30:52 GMT  
		Size: 29.6 MB (29639850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e830ff5f589a4c6e301f10ed8a1ac9ef66ca2626f5799b4880e926e14ba83af`  
		Last Modified: Mon, 22 Jul 2024 21:42:47 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c9b0a47be09ce9767e796a2b8167f70bbfb8e79fbded9f682bfce41e9b7022`  
		Last Modified: Mon, 22 Jul 2024 21:42:50 GMT  
		Size: 23.6 MB (23648351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea131f4e8ec096a1f3081a28af0f2ef58ac996547ff213b0e34ee540a568cfe3`  
		Last Modified: Mon, 22 Jul 2024 21:42:47 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:09f43c5c263c3cadad3e0cb7318bfaca6063250304da518bcd7355b1b3205ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 KB (17759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc6ba68cb99ecb6680ddae028dd8c1f5f142a01eed684d3558ec0dbd8eaf801`

```dockerfile
```

-	Layers:
	-	`sha256:2eda3d3feafb7cc6c3bdb50dfc6999acded99318e289045c7e50465ed70532c9`  
		Last Modified: Mon, 22 Jul 2024 21:42:47 GMT  
		Size: 17.8 KB (17759 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:16c60f549d3c437e1984067919a34f82a456c302251435a980f531f692e7a77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60294175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846be37599837a7d98d32a3de7ffd5b9cf09f2836b8d6a0bcb42d95fc40b57db`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b13390f73cc9a8d336ed123d1e1c59cf672505e174b2098c59de21a7ce91e66`  
		Last Modified: Tue, 23 Jul 2024 20:06:31 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bf0de913c831bed24b2c23c975a8a254616dec81c25646bc8c8c256f5555f9`  
		Last Modified: Tue, 23 Jul 2024 20:06:32 GMT  
		Size: 25.0 MB (24988704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8952a1c7145db23fbe35b17eda6ede7c7631eaa75c073f1df60710d9cdd633bf`  
		Last Modified: Tue, 23 Jul 2024 20:06:31 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:37d0498736a1b96f01396912088a0916f3c76e037d1da535690b72ab5f61d7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d5aebfa2746d2fa39358571482b3cae90c0f5d9df3014d0e0a8ca87f5b0c24`

```dockerfile
```

-	Layers:
	-	`sha256:e3a997b3e935ab7088820adae6560488505a4eb6d55f6b451f13566880dd90ef`  
		Last Modified: Tue, 23 Jul 2024 20:06:32 GMT  
		Size: 3.9 MB (3923018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0578a318403a7480231591816af92b9218a80303f3b1bd014403d4208e0e459c`  
		Last Modified: Tue, 23 Jul 2024 20:06:31 GMT  
		Size: 18.0 KB (17956 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:c61309fc2e7616447437f9c16950c4bfc224919324f0e04db7c750a05aed8b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53631626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc7ed2d07e5ab80ee2bf23ebf0131e6bc4d1b9438e8f230c67937c46c0133d8`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:c9cf6ed72c109eb68384476670cda2086783dc0a2ea6379cb1a662b3c8509591 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:de4a305fc1af45cc7ae97020dfe639e8990f6d00b7e0ef222c4cdd720f0fc373`  
		Last Modified: Tue, 23 Jul 2024 02:33:12 GMT  
		Size: 29.7 MB (29669018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf94d6b35849c4e38dfd9727021755e090ca2dbd3b3ee2d4a3678a8b4ef302d8`  
		Last Modified: Tue, 23 Jul 2024 22:45:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac29482372108a49040b9be5c1f118e72d41eb11416832ede0bab51a678c274`  
		Last Modified: Tue, 23 Jul 2024 22:45:17 GMT  
		Size: 24.0 MB (23962340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8973592f32409eb6e9cd240cc4ee480dab117875b2b5e5239e776f520a7bf35b`  
		Last Modified: Tue, 23 Jul 2024 22:45:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:76ddcee7e2368f4c408040062fb92a96654553ed0f2cc363b1ff6836cb2d22e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af780a1999df9d4ddac47da3f10e342e1ddc23d1dac37f68dfcf243f83e0847`

```dockerfile
```

-	Layers:
	-	`sha256:fda4d03694de7bd7193d00210094eb0e18e9774bf800bbb9d8d9e380ca281daa`  
		Last Modified: Tue, 23 Jul 2024 22:45:16 GMT  
		Size: 3.9 MB (3922953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e479abb9f90db1852ee2a561c306af2a70cb0cb3936a0e122191dbf92f29ca`  
		Last Modified: Tue, 23 Jul 2024 22:45:16 GMT  
		Size: 17.9 KB (17912 bytes)  
		MIME: application/vnd.in-toto+json
