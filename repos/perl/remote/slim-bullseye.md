## `perl:slim-bullseye`

```console
$ docker pull perl@sha256:05b9074d0bd0e11977adfd7eeb6938fabf5e2ba1d8ad749269064c1fc12ede8f
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
$ docker pull perl@sha256:8199467ddcc75d72451a371ab8ac7ade15e62877c6051f84fda095303f1cb584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56164919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3d1464da6574dd7b87f73f834728fb564658d3de3a1f206f84e70bd7d21b67`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e744cad52ef0294631e950274d18b5448ee92acc3f6b802afca2d17c16abf6c0`  
		Last Modified: Tue, 13 Aug 2024 01:19:23 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc9443dfcd32423f54960dc6c4cc2c0b342fba1e1ef4a78219eb575b5052d51`  
		Last Modified: Tue, 13 Aug 2024 01:19:24 GMT  
		Size: 24.7 MB (24736366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbef0bb3b2de589bf0d16b62be5c1fb7b7e036c39347f95e73377e4f123d289`  
		Last Modified: Tue, 13 Aug 2024 01:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b061df82c014b297bbe8e6af6d0ac82651d1ad520b724c0e337bf5e40c019a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4a52f7e55e9581d0be7d2f9ca36ddbc274f314d49b8e7c12377a8219dde06a`

```dockerfile
```

-	Layers:
	-	`sha256:d8052399f7a7cf2d3e39432860b2d1eab6c50965c8456a7082c2fd147ae1d6c0`  
		Last Modified: Tue, 13 Aug 2024 01:19:24 GMT  
		Size: 3.9 MB (3934251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca38610018bfd3cefc66831d0fc06c28e50b1f981c3b43a33522849be0dc2a2a`  
		Last Modified: Tue, 13 Aug 2024 01:19:23 GMT  
		Size: 17.9 KB (17912 bytes)  
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
$ docker pull perl@sha256:7fe1f621612f6a69055fd30c409fa1270aa2dbd732288c05c9ef0c16c4c83c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53953516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14ed321a74df46f923742ecc8b46a4454f8cc9541e63b58c0273b29ccc08318`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2fba8b3e699b11527bd79eb822a74f9453273be25bc67c416f8f208d6f7e1b`  
		Last Modified: Tue, 13 Aug 2024 08:08:21 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c93ebbd6d6e65e0c0e17d73578e2b762cecd779d29c737512f4cf9c190f0a1`  
		Last Modified: Tue, 13 Aug 2024 08:08:22 GMT  
		Size: 23.9 MB (23877164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d829554f21493b4c528521c2043589d8c456718fc4b4e0d96113dff57bb1df5`  
		Last Modified: Tue, 13 Aug 2024 08:08:21 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f2ca9a5f8301fae0456adca96ae0bb8d4084ec711a0295d5c463e3d04e4501f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3926857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8868a11c6f23720f9fb8aaacb816e63a9597fc656c7079e6c92769eed07ce017`

```dockerfile
```

-	Layers:
	-	`sha256:482550392fbe374285635993a6f316689e0af996ceb4694708f4e6a80b0d4ed4`  
		Last Modified: Tue, 13 Aug 2024 08:08:22 GMT  
		Size: 3.9 MB (3908624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af36936683def9bc97b689f43426aaf98d6c64ea0ec6b3b2dcdf8aee5218be4d`  
		Last Modified: Tue, 13 Aug 2024 08:08:21 GMT  
		Size: 18.2 KB (18233 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:9210bd46d007cf8456fce7efebca3793e28fdd56f5eff0c1554f903b7e102775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58576507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de595c15db5729c2ef1fa61d03846aefa12c5fc3d4b1c975b0b1e5723f15ef8`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
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
	-	`sha256:1fff23531e74037071ba9be4ee63db5ccfd9c3823dceddfee08bed3fdeb6dea1`  
		Last Modified: Tue, 13 Aug 2024 00:43:17 GMT  
		Size: 32.4 MB (32413784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb946aebc46c989300c75b25abb5f0a6c05a297c6bebf5d710cb7e693001b0a4`  
		Last Modified: Tue, 13 Aug 2024 01:20:14 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfdf2c2569e0fc3ee3c28987737a786e491fd01cfdd8b7f7fbcec3cb2e464be`  
		Last Modified: Tue, 13 Aug 2024 01:20:15 GMT  
		Size: 26.2 MB (26162457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4918da01c06dd4e165527800a4d1d2cc629bf3f19648aabdbcd31a804357b125`  
		Last Modified: Tue, 13 Aug 2024 01:20:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ecfa62ca165307d5b67f4bfee3f95482320c1ee3bd613b6d5ac335f956996cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3956380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4aaca92b5e66c62dce80aeedc139ddf61858b2bd0ba3a4eb6c789b125997fef`

```dockerfile
```

-	Layers:
	-	`sha256:312a1beb664712017f7111a868f9624cf3fa4f9ed2ad41583493909b10c26437`  
		Last Modified: Tue, 13 Aug 2024 01:20:14 GMT  
		Size: 3.9 MB (3938502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:801475d2bf11cff5fe036b13dc211b2ac5bfd29ad31ae27f717d495da7889afb`  
		Last Modified: Tue, 13 Aug 2024 01:20:14 GMT  
		Size: 17.9 KB (17878 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:a77fd085a5af1cc5adfcf9925bcaf185b96846109296d0a1fa62ae6553ef72fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53294510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711551e6e71bdd0e444bce9ce9d171c137969b2e409a79b8627615f6f2c561f2`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:aa937b31fe693810c8c6e110de59ba07264dbc020fabac9e1ac045df57efc0c3 in / 
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
	-	`sha256:83b27ea307774a387b0a5203cb6aa8f117e44bb5321ed6c8de8b0a0c43d895ca`  
		Last Modified: Tue, 23 Jul 2024 00:50:32 GMT  
		Size: 29.6 MB (29646085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909375433d8dfc200abd8c6d00404950a9a76a721bf893ba9962c9520b9ca1b5`  
		Last Modified: Wed, 24 Jul 2024 06:26:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1893900fccce7bb7427b12c96e34a0cd5d345f546e7b2b961526c85fd14cfedb`  
		Last Modified: Wed, 24 Jul 2024 06:26:46 GMT  
		Size: 23.6 MB (23648158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ed84386067c5da7baccad458aa994cd2d1179a7dc197784b621184fd2d0067`  
		Last Modified: Wed, 24 Jul 2024 06:26:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c7e3193af99483067266a2e249a62aae2aff9457065c2649d9a0ac31103c9b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 KB (17759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739296413bb06969044b007cbb215a3f889b44a77e0ff5e9a2bd73817f359ae1`

```dockerfile
```

-	Layers:
	-	`sha256:2c8c89480c170cc31289932fbf73fc5c6ed387417100da4d7b37489e055bad94`  
		Last Modified: Wed, 24 Jul 2024 06:26:44 GMT  
		Size: 17.8 KB (17759 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:6f00a2b7207b06194f68b7ac6c935634b2feaed692d98164fdf153da9af66dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60295792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8538dd725bf1f8ed8c7b3b67c4c6c93bf875710d0d2904188426d71972e7c5ac`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
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
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bc485c5dc2434020075fa18edd35615c27de13f1c496740ca708f1cdb619c9`  
		Last Modified: Tue, 13 Aug 2024 07:47:40 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1abec416e0e5b1ee2d304f727d634b20c19ee84a752880e4bd64e2c5af691e`  
		Last Modified: Tue, 13 Aug 2024 07:47:42 GMT  
		Size: 25.0 MB (24990395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce642a560df4e26c225428f9c2f17528045025ad1f593f78df0439ed74732611`  
		Last Modified: Tue, 13 Aug 2024 07:47:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:77bae30335de25b6d08a895c7c61a09624cde97721a55f3e041383458afed89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c898d61355bb89b87b758087357324eb764122aefa36db6e7ecd6b06fa88c7b`

```dockerfile
```

-	Layers:
	-	`sha256:462bf60969fab4eace3072aec0bc43535cc924fc951894314ee21a36c1d91b3c`  
		Last Modified: Tue, 13 Aug 2024 07:47:41 GMT  
		Size: 3.9 MB (3923018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888003c554105c9cdaefe4167fdc71d1664719ba1eaf36e4f344a07527f61708`  
		Last Modified: Tue, 13 Aug 2024 07:47:40 GMT  
		Size: 18.0 KB (17956 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:2a25bc0340ff7a2186ed882b43e5694a8dde9ea1cafc751fb73634814b8fc2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53631861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f535c3703098119143e114d21783e5397a0a5b42df864e3445497cb2adf537fc`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:a473fc09ddb0d1045f7f330f3a48b9cfe65ff9ea65cfa5c8262a8a5be9d4db75 in / 
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
	-	`sha256:83ea1b2f9d26c88827c9a658387c782a21fca528fbf7418f1a4eaea9a9818bdf`  
		Last Modified: Tue, 13 Aug 2024 00:47:58 GMT  
		Size: 29.7 MB (29668965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453cf4e5d557020589bfe0a40163967bfd8c8323adb32248a1c6f4a9a421dcee`  
		Last Modified: Tue, 13 Aug 2024 05:59:30 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f27d067eb7e380c5e21599a7fa02323269326c448a145301458fd500913a6a`  
		Last Modified: Tue, 13 Aug 2024 05:59:30 GMT  
		Size: 24.0 MB (23962632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314f1e970829eb984babc2d6f8a822694e8078a4f30c8b6e43c5d4b37f80118a`  
		Last Modified: Tue, 13 Aug 2024 05:59:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:2e7ea77bab4b3175ac79d5e6ce216e2150c84a67a399b2ed6fe6c38868b04357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87316f4b858b0fac590dcc9d86ff6011cbc0719f0d21f2c686d199a53e6462a8`

```dockerfile
```

-	Layers:
	-	`sha256:c60c0fa8a9b59721753a6e3b35823c532c8118cd174e1ba64c136dafcb289ead`  
		Last Modified: Tue, 13 Aug 2024 05:59:31 GMT  
		Size: 3.9 MB (3922953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b743554f334f41bac502a8b4a8fba9a74d177c2cdd8d5eb403edd0a851908616`  
		Last Modified: Tue, 13 Aug 2024 05:59:30 GMT  
		Size: 17.9 KB (17912 bytes)  
		MIME: application/vnd.in-toto+json
