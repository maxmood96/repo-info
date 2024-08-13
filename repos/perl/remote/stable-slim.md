## `perl:stable-slim`

```console
$ docker pull perl@sha256:00587d259a07fca94c17ba0d5e9a2505c5bc56a072ed9b5192775c7e3d36384e
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

### `perl:stable-slim` - linux; amd64

```console
$ docker pull perl@sha256:a0429f46413a4418d753ed562b9e433e5b25a9051e4d06c3e9b56c9690b74dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57791186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dec4a74eb7dca5c7e83edd9371417e492afda1dfffeeff6005aff8807dc95c9`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e744cad52ef0294631e950274d18b5448ee92acc3f6b802afca2d17c16abf6c0`  
		Last Modified: Tue, 13 Aug 2024 01:19:23 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48168afe9a4bb2cec2125f9f7ac16aabfd2873f3638bfe3b4170198d160668c8`  
		Last Modified: Tue, 13 Aug 2024 01:19:50 GMT  
		Size: 28.7 MB (28664688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156dfd2dc4e688e8c3cd23c1a78b18dd7e296136553e804f6ba7cb0d5914dd8e`  
		Last Modified: Tue, 13 Aug 2024 01:19:49 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:f0f8e304d3e3e01a878aca3d5bcb5717e5b6c0e235e2d0a56e6582cb542e6513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3762135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ff157771622f0f6650ec88daaf84f7f126d489f4031b67d1c48c15a75c6e52`

```dockerfile
```

-	Layers:
	-	`sha256:8ec586a1c117793ec29a59e751819286205680fe1c92a53c0f108bf71e02bb1b`  
		Last Modified: Tue, 13 Aug 2024 01:19:50 GMT  
		Size: 3.7 MB (3742732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0778875932f029191a958ecbcca085b25ab780a3ec15e6c15febda42abceb41`  
		Last Modified: Tue, 13 Aug 2024 01:19:50 GMT  
		Size: 19.4 KB (19403 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:ae0fddbfae06ec2ba6b7ea89f1b55c8b7ccba403acf261ec8e6ab3a932429905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52661370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a9a126112cefd20e3a2ba7e86e35610ba8a362760428772b67b0ec3e514ac2`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
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
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285f79bbc1df7e0d943cf06d95562c4e28b718ee9e34c116b9be23f5b5478b68`  
		Last Modified: Tue, 23 Jul 2024 08:24:18 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1445ff7dc3658942d68dcd85e0258bf65a71c3390dda932eb89754cd6dee04`  
		Last Modified: Tue, 23 Jul 2024 08:24:19 GMT  
		Size: 25.8 MB (25773804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc18749c12c16d7ea1f67306c13ba9eaba733b009c0d622d04fa829c8e217b5`  
		Last Modified: Tue, 23 Jul 2024 08:24:18 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:f4a2be38f97230c6c9456cf038da7ea22735e3b2922b7671d54379f273468dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79de661539fc8d59a0aab7f75ef1131791db89fa8c1cb70eef952b1f8608ec83`

```dockerfile
```

-	Layers:
	-	`sha256:66bf9363d3b649b62f26c1d100ca742834fdfd7c512a64ed319a029a49a69268`  
		Last Modified: Tue, 23 Jul 2024 08:24:18 GMT  
		Size: 3.7 MB (3713170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5efb308a8ec1341427735fe85c5838cf229a840405812b2d2b697017913c36c8`  
		Last Modified: Tue, 23 Jul 2024 08:24:18 GMT  
		Size: 19.5 KB (19522 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:c9a724c929c1ddfeaa097257c7f536f2a8df2db4fa4d37ca9202d894f29d33df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49704120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674ab616270b88d215fd6ee4c7eff545a92b0a7cd4ed6e6b3fc8abc5630fecf5`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
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
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4feb632771abbe21f4e6a0135dc4434d1753290265a4e55b492593837e1ff0`  
		Last Modified: Tue, 23 Jul 2024 23:42:29 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe02acebd7ed95937ef077760ebdd95145df6a078d13b370eff1a8ad78b3f31`  
		Last Modified: Tue, 23 Jul 2024 23:42:31 GMT  
		Size: 25.0 MB (24985652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7520cecfd26c7459fabb8b69349e9849d9008bbdfec0799f81393f43b4b03aa`  
		Last Modified: Tue, 23 Jul 2024 23:42:30 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:6b23d26c6f04ec6287e14cbec754038694a273f49bf6e0b09f9a028f04f1d394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6145cd5ab6157d32a46de53d80487d9977cf60950bfcf92b62658a8868c52f`

```dockerfile
```

-	Layers:
	-	`sha256:b34ebb83caebb9e79a232cb6a784369d047e43bc01168052c0a83a118662c03a`  
		Last Modified: Tue, 23 Jul 2024 23:42:30 GMT  
		Size: 3.7 MB (3712785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1092f43303bbdafd55a6da0c46f459409c3500d67e1da5f9689c1a606c5683a`  
		Last Modified: Tue, 23 Jul 2024 23:42:30 GMT  
		Size: 19.5 KB (19522 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:b9608513ad80adfe60b87efd204b0c491df0f245dc87897d07ac3af26d8b756d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56617287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f733e6900005c03781aa01fc4eec6b65287b195617eecfa8051cbc4aef964497`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
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
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3329cb1ed736506c9c14da27c42be96d80f06b8e06c458be617b8686993adb5a`  
		Last Modified: Tue, 13 Aug 2024 08:03:00 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000edd49f111d1fe809977ecdb0f0b72a37c27efa509360ee12155ce0f28c3bd`  
		Last Modified: Tue, 13 Aug 2024 08:03:02 GMT  
		Size: 27.5 MB (27460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9924dd236afec20853e266942f7409cdf9336c1058895ea277d8b144a5f91a`  
		Last Modified: Tue, 13 Aug 2024 08:03:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:1192924dbc062e8c6b5a5d55787b590006bab484cc1222d5a104434f9d787920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083b86660a3c18571daf7db29f84fef373a1c7c761e5bfa486a7b173b776eb36`

```dockerfile
```

-	Layers:
	-	`sha256:f8009f366e33469b335b05399ae650528c2ad0f817e6088b172d6b8cb29644f9`  
		Last Modified: Tue, 13 Aug 2024 08:03:01 GMT  
		Size: 3.7 MB (3714003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:286691e1ab6c2cebac02d9c1ef8c56b08bf5513d4570b4f243f9f3a2f17ca259`  
		Last Modified: Tue, 13 Aug 2024 08:03:00 GMT  
		Size: 19.8 KB (19785 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim` - linux; 386

```console
$ docker pull perl@sha256:d2c2eae6cc0411e7f3da1b18cf8fb82567f4164df9fc252d5ec220559019adb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57813814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd58b25de666e6c982f6321e0849958e0f2a2b1b43c492c1230f7cd459c39f1a`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
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
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662322e5aa62dd765caec4125a1aaf85950f3b7efa326122ce8e97656a16b12b`  
		Last Modified: Tue, 13 Aug 2024 01:21:04 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be89a2c899c02ccef81f79b541c097c76a0d44a47d1ffbb4944e4165c79e6f1`  
		Last Modified: Tue, 13 Aug 2024 01:21:05 GMT  
		Size: 27.7 MB (27669267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e206789983029f8229bb5396d3cc3c66dcaed8e5e328a2a2d006bca25963f274`  
		Last Modified: Tue, 13 Aug 2024 01:21:04 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:3ba9e5331dee0df916261b9b424a2b315f9e4c1af9a69a5141c36fb71c74f779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3755950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3039e18a13bc7be1d40664358c29989165f5a12883992bd2d011e5c5fc2740d8`

```dockerfile
```

-	Layers:
	-	`sha256:366af283366cbd121e6899b73fe363919bf041082faf819075f954475af45b24`  
		Last Modified: Tue, 13 Aug 2024 01:21:04 GMT  
		Size: 3.7 MB (3736605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f05849a88dfef6b78bc25d444fb96a8a1c68dfdb2dd8224c127744e0e89b495`  
		Last Modified: Tue, 13 Aug 2024 01:21:04 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim` - linux; mips64le

```console
$ docker pull perl@sha256:3c2e19a06234e3e1be63bcb5413cec36210d62ae86e91e5bb292b4264228c101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55947449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f263c0f592559b27721cab4e7bbabf0ad416af8cecfbe0a9f1018bda57f67e3`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:6b0de87e15c6880fed3a8430d23a511322519e32c50677c24f4597141e3a85ff in / 
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
	-	`sha256:f8de7af9de8596141237ef7c589f08f773ca8ce07671b2bd7e192055d5165f74`  
		Last Modified: Tue, 23 Jul 2024 00:49:06 GMT  
		Size: 29.1 MB (29124926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69171642196c0e7706f5b3f2898257b0c088307511cf48448e2a10ca88a49aae`  
		Last Modified: Wed, 24 Jul 2024 06:01:08 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca76285c0a959b62941f9ede5d2766f3e9e5f9671fb183fc226bf88b339ba6f`  
		Last Modified: Wed, 24 Jul 2024 06:01:11 GMT  
		Size: 26.8 MB (26822255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414f5adcc94367ed16f230a6d478cb47b894ba5d5407801f2309f05cf0105d15`  
		Last Modified: Wed, 24 Jul 2024 06:01:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:c9070f4c604efd795a02456203ab5854244a7f8eb640987dbd1e72bbf8bf63b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca01e17a5f5ab50b91b2d3747745d34c6827ddc69bfb51b7be36bcad09045c2`

```dockerfile
```

-	Layers:
	-	`sha256:a156f760a0144a4db582e5412bb20dde201efd25e79b0c8e27266a7c8a2481f5`  
		Last Modified: Wed, 24 Jul 2024 06:01:08 GMT  
		Size: 19.3 KB (19296 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim` - linux; ppc64le

```console
$ docker pull perl@sha256:95f8ecf85a7bdf6f13eafc835598d1447f794cd625b37b19cfe1b990aac7eaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62346606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7123e74c68dd87616d43caa93e6a6a8e7cf9750f8f2a7386075f33c1afd1be29`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
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
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbf790a2cc70b98208e17a0e590068cfc95bb6c79c6fa5070b032fc5c7ebd6c`  
		Last Modified: Tue, 13 Aug 2024 07:40:45 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717cb0857877901664e0561c69c896226834a81f655366826cf2779acaf7d7fe`  
		Last Modified: Tue, 13 Aug 2024 07:40:46 GMT  
		Size: 29.2 MB (29224040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d275fe428f98db53966ddbde87a00773f7da689f1abfa04de38cc244ec96a351`  
		Last Modified: Tue, 13 Aug 2024 07:40:45 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:c8067d35af25332320f2cb1b6a58888b7045a15a233015fc55622c2cef31f02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71b26d97e802869a0580f539740eb1d90c2965ef66d136c6a4abd03a7d7bf1d`

```dockerfile
```

-	Layers:
	-	`sha256:0af8e999cd395b8136158265d58b12ed06a65cdd552d638c8de00ae520e628db`  
		Last Modified: Tue, 13 Aug 2024 07:40:46 GMT  
		Size: 3.7 MB (3728459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd74408043b5aa976aa30f64b8554d056e7ee6dd78ba4e86cf0f960ad90f44ec`  
		Last Modified: Tue, 13 Aug 2024 07:40:45 GMT  
		Size: 19.5 KB (19478 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim` - linux; s390x

```console
$ docker pull perl@sha256:4849386f29c5bf63805d8dfe5fb75ecfd4b127975290fa87fe218042b0546d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54696477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8d58caf35fb711eeb044e0d81caddb2c0e3d7667c6aaeeed285789716d9752`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
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
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3efa56e79c2a86d582a5fb5dff3638836ea479d7ef911ff9079bec51e9c30f`  
		Last Modified: Tue, 13 Aug 2024 05:53:20 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68eb8e21024bbccf2f2263c24f447e95f4bb5992c40395a7bdfeb5d3755563d0`  
		Last Modified: Tue, 13 Aug 2024 05:53:21 GMT  
		Size: 27.2 MB (27206114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734a1a19d2147fe53d6eec4bf3287c28a18fab0ef14be22eca7896a66eef22d4`  
		Last Modified: Tue, 13 Aug 2024 05:53:21 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim` - unknown; unknown

```console
$ docker pull perl@sha256:973cec44518014fcaa84e298ee87cdbb27b36a633844d1ab46bc16beeb0ade52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2109f552a19d42777874757521def424e95808f581ad5d925215d48b4f309a19`

```dockerfile
```

-	Layers:
	-	`sha256:4c3cd9c5dd1172b1f508f5a505fe4b1e2c4b22009605254e69ae195818ada57e`  
		Last Modified: Tue, 13 Aug 2024 05:53:21 GMT  
		Size: 3.7 MB (3731002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df0f288b1fb3c20ea94f7e40a46132fcfbefa154c5bb97f8c426cfa595a83b1d`  
		Last Modified: Tue, 13 Aug 2024 05:53:20 GMT  
		Size: 19.4 KB (19404 bytes)  
		MIME: application/vnd.in-toto+json
