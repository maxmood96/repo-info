## `perl:devel-slim-bookworm`

```console
$ docker pull perl@sha256:432705992dcb510faa82cfd26eae5553294be182033d87268375854bd8e8be2b
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

### `perl:devel-slim-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:3c2e137b43bae94ef7e0bdeacb93528644730933f4eb3503804c5da44281af3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57787005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4459fb950b78037587ce94fd22600ce153345eea61893003a0288ca258a6a6d`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
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
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd11a38aecccd159ff58548bccd2e16523609769ff5e046b805f7b81f524d60`  
		Last Modified: Tue, 23 Jul 2024 07:28:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6d2419f7c652c968b518ecd3e5d44e30691f21d9aa1ae27b4a49d0481548a3`  
		Last Modified: Tue, 23 Jul 2024 07:28:57 GMT  
		Size: 28.7 MB (28660452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751ac079906323200c6a6f89cc2d039af729828aa2df0291fdde06233fb06800`  
		Last Modified: Tue, 23 Jul 2024 07:28:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:7c685edea95c9904690c0c19cd8f7c52f2bd3a23ac819958bd576ebf1cec6850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d521e52561014e9157f8e4a1a15bcc64b45950f4643dd618f009432d52df8eb`

```dockerfile
```

-	Layers:
	-	`sha256:13c1486490ed6119b99d09c99a48e153446c52ed32a1eaf1304be6ca2e5304f4`  
		Last Modified: Tue, 23 Jul 2024 07:28:57 GMT  
		Size: 3.7 MB (3741524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e82a9d470500ddd877558e48c734cb02d5134a4eb57971ee32f559cac6115d5c`  
		Last Modified: Tue, 23 Jul 2024 07:28:57 GMT  
		Size: 18.3 KB (18266 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:46ed75ab6b64aa107e4b6f73a546696f0fe22089938855924ffc4ee2cdf1d380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52667171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37268308bc55706d00a547176f9ea3d59584851fef2d68b844edd2cb4a2c267e`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
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
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285f79bbc1df7e0d943cf06d95562c4e28b718ee9e34c116b9be23f5b5478b68`  
		Last Modified: Tue, 23 Jul 2024 08:24:18 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5759962ef3d68bdeb6f65aa7b43e79501803b04550e5225258a73c5e9db7b51`  
		Last Modified: Tue, 23 Jul 2024 09:51:07 GMT  
		Size: 25.8 MB (25779605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcd27da1b35b0a5e39bd853ffee8a06cd27c6cffb05142a1e3c080eb010948e`  
		Last Modified: Tue, 23 Jul 2024 09:51:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:fc7a1844398d9ded1fc5d8a61fdddf737bdf7c6b6821781ec45f2c4550891bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa07eaea3e0de9e1facebb68eb7ad8a09e41723979959d13b7cefb3b17ea00a8`

```dockerfile
```

-	Layers:
	-	`sha256:9a054aef599c3c36cf4b1c63489d4832b99608d63debec5781b184f22b649dc9`  
		Last Modified: Tue, 23 Jul 2024 09:51:07 GMT  
		Size: 3.7 MB (3711930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b57ddd085461bc6d8aff8ac70941edea780a20524184fff575d7b9eb26c153`  
		Last Modified: Tue, 23 Jul 2024 09:51:06 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:72577fd4a2c89a11094149906d4cec34f3f9dd3d8e9f6cf880aca45410140bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50615616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed594b30d9da4dac5c62d100c54d8d5e827f8c8239654169899877b0dcebd36`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/perl
# Wed, 03 Jul 2024 14:39:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.1.tar.gz -o perl-5.41.1.tar.gz     && echo '7dee38af601b0ba3f3730cb812cdbc799c921da440cb0ce96dd7a4f508b1a6f8 *perl-5.41.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.1.tar.gz -C /usr/src/perl     && rm perl-5.41.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/app
# Wed, 03 Jul 2024 14:39:46 GMT
CMD ["perl5.41.1" "-de0"]
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af963df78e4082e2f93e40fcc3ef5501fd998fbf9f6ef837fe9e4eef08d83de`  
		Last Modified: Wed, 03 Jul 2024 16:29:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1f09b2595bc3dc4dfda90e257fc843cd3fc29906e03627f3e3edbf6a21f6f5`  
		Last Modified: Wed, 03 Jul 2024 19:11:46 GMT  
		Size: 25.9 MB (25897178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599c4ce9a8988a29c79d2ea22e987423bd5723c426abfc594e76fa0683b5cdc4`  
		Last Modified: Wed, 03 Jul 2024 19:11:45 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:29e37098a0fa86d91c490f2b3d56c06082160cd700b2eb833ab021e025f54376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3707528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99898f505b79d516c44f9fcdecf2a366267392d0955009af3d606663838ea868`

```dockerfile
```

-	Layers:
	-	`sha256:280a81027b5cccb95c59dc3b568d0fd526948aa9a7351d491dc581e304c51fa7`  
		Last Modified: Wed, 03 Jul 2024 19:11:45 GMT  
		Size: 3.7 MB (3689295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca776ef0d5e8bc45773a3e48fa5cfed03a3fb4b174ddcb41959410f39a29cc6`  
		Last Modified: Wed, 03 Jul 2024 19:11:45 GMT  
		Size: 18.2 KB (18233 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:1f4379ed74fd0e35e229547d6204a78753b39cc59176b0afcde5b78750385385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56613329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53e3894a973dcfc81998fb466d0512e9b1bf98cb90c2ed8f4dcaf60dbde5112`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d7b1b05c3dfb6c37b5824741ba52dc43a7c12886ba89fbb9a40c4434267b4d`  
		Last Modified: Tue, 23 Jul 2024 22:26:26 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac0d416dd2e111b86044c1dce27120d8e99f4b1658b8e3f666df5f596b1ca42`  
		Last Modified: Wed, 24 Jul 2024 00:33:30 GMT  
		Size: 27.5 MB (27456490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00dca1bc1d1c2a8eee7117054c265d3e4c12600e241cb1f63adcdf43e60a532a`  
		Last Modified: Wed, 24 Jul 2024 00:33:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:1e914a6b481aea5080ace914c0bf55ec7165f1b62d42bfb7021653b87db0d2e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfb3d345b4c0cbcf6fe13a94c09a4a24969b7f4ff41efa8c69f3cc206798262`

```dockerfile
```

-	Layers:
	-	`sha256:1b4d3d9af044aaf6dc6bebd5fbf264c35607cc83b8c920917b77b130fa3c4ba5`  
		Last Modified: Wed, 24 Jul 2024 00:33:29 GMT  
		Size: 3.7 MB (3712747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aff39badbc40dbd0408dbd5d7b9a325830ff684683fb02c667745e6b26a6888`  
		Last Modified: Wed, 24 Jul 2024 00:33:29 GMT  
		Size: 18.6 KB (18598 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; 386

```console
$ docker pull perl@sha256:09ebef3059c2afb790ff17760a145f9de84a72a4f9c3a28c9244dc056f1a8979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57813949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ca4df8abba39fed34ec8d1249c24503ac0feb7881882edc215948f74278ebf`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:9b63a9d86a51a3d56d700d09e1152578d700ba4453d852325d8eb9896534f3ba in / 
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
	-	`sha256:7fa64a47f35cb425a1275bff76c45df3b76d3ff6b07911737090b82e4f221e93`  
		Last Modified: Tue, 23 Jul 2024 03:57:51 GMT  
		Size: 30.1 MB (30144309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7aabbeac9e5f69c0636f4a042b278f6a2b078c8e5ed4d32a5bb0a7eb7e885d3`  
		Last Modified: Tue, 23 Jul 2024 06:18:14 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b86d118b6cbda653a436024425bbac59f58131d21509b03ac4c84c39722cbd`  
		Last Modified: Tue, 23 Jul 2024 06:18:15 GMT  
		Size: 27.7 MB (27669373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df896acd5212fe547b7b25233b7c9465f0e87f8ca8f1098df7182b5e5f0dd0f`  
		Last Modified: Tue, 23 Jul 2024 06:18:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:b71afe1c08025026f2cfdec6b7ebbec312a8bcedfe4f2e2dd5944a013be31299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3753644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a52eccb9436b3033e4c7c6b6dd2b9f68fb97567af51b032b24cf09ccc008f80`

```dockerfile
```

-	Layers:
	-	`sha256:3e3dab02b9a664fb84ecedac61630e09d787e4713db2828a1167abed045c94fd`  
		Last Modified: Tue, 23 Jul 2024 06:18:14 GMT  
		Size: 3.7 MB (3735417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d957179042b71f1f4c96fd8fd10a7f41bd0560ab777f102a06ce0e2934307e8`  
		Last Modified: Tue, 23 Jul 2024 06:18:14 GMT  
		Size: 18.2 KB (18227 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:763702c2a0083c0166ce5a410bd136019669a555acbbdc975388f584363ea93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56878037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea01ce2c43d416081aa5547d7d20fc0403c5478c4752fd08f0aae233d60dee76`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:23 GMT
ADD file:9a0f0c8ed27f6f2bb89272036da4d44a63dcaf43fb03528dd2d970fbe64ccc92 in / 
# Tue, 02 Jul 2024 01:18:27 GMT
CMD ["bash"]
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/perl
# Wed, 03 Jul 2024 14:39:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.1.tar.gz -o perl-5.41.1.tar.gz     && echo '7dee38af601b0ba3f3730cb812cdbc799c921da440cb0ce96dd7a4f508b1a6f8 *perl-5.41.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.1.tar.gz -C /usr/src/perl     && rm perl-5.41.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/app
# Wed, 03 Jul 2024 14:39:46 GMT
CMD ["perl5.41.1" "-de0"]
```

-	Layers:
	-	`sha256:cbefe199012545da86e0f461f1964dea0c9bab400e37766ee5f32b967423cf0b`  
		Last Modified: Tue, 02 Jul 2024 01:29:29 GMT  
		Size: 29.1 MB (29124929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e98d895105e0bd56275cb11711f34b173ed76fc0e049d6f426643b28e1932ea`  
		Last Modified: Thu, 04 Jul 2024 11:47:01 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a50677092a325da2dcdd635f12634ff8dde38820269eb3960b265a4d3f610c5`  
		Last Modified: Thu, 04 Jul 2024 11:47:04 GMT  
		Size: 27.8 MB (27752843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8dd5966088224b6492d5699a2bdfb759d6782448c773836d37feb91e0b0c74`  
		Last Modified: Thu, 04 Jul 2024 11:47:01 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:1eee865791162785e2c3cf63c46415c8e445a3f53afabfce1236fc2ede80c4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ef6e520b91324205a34af653fde178d712132ed2ef6643e0984bd389d254f5`

```dockerfile
```

-	Layers:
	-	`sha256:5778423a273f8620c7cbbcc892ffc02b6f5f563a290a9bbe0bf5f5e846bcaa44`  
		Last Modified: Thu, 04 Jul 2024 11:47:01 GMT  
		Size: 18.0 KB (18003 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:029d0a92ed8ba530f706b0191ff29db0768ddefc72e7c8854a969127ddb7dfb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62348420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40418f08f009dd674254f151745ad18608eb8b95afeecee2ea723e2f18e7f6c6`
-	Default Command: `["perl5.41.2","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
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
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0cb411c15df4d2ceb091e80225e9184fc322db7d7a6be00850ff7591a08a14`  
		Last Modified: Tue, 23 Jul 2024 20:00:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac092d0653ba44547ddd676c49137a1704ac0409a59c2ccdc19e33782596cda9`  
		Last Modified: Tue, 23 Jul 2024 22:38:01 GMT  
		Size: 29.2 MB (29225877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dad437814940cea47f1d08e12294ec2e884872fddbb6f47073c79ebd2e6c05`  
		Last Modified: Tue, 23 Jul 2024 22:37:59 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:ca6082cd784b96779746ad4514c5ff1a05060acccedb594c87874b78e106c0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199ef7d81e097266017d5378829f60098f98fd2731f5a2fb6b4b5dc53c6f46c7`

```dockerfile
```

-	Layers:
	-	`sha256:9b91832d0825d26e3ad2ef2ff09fd0ac6c248883f436dc5f537a7fd4e45a5f13`  
		Last Modified: Tue, 23 Jul 2024 22:38:00 GMT  
		Size: 3.7 MB (3727227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:196c0503109a22110a5923599d8a39cee6b4bd55ea4cf4cbe01708475f7fcff2`  
		Last Modified: Tue, 23 Jul 2024 22:37:59 GMT  
		Size: 18.3 KB (18316 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:afc6ee8404f03cf222e3ccaa3bf733b071dfbba409340caa0735e069449e5ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55613068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7088e39dcde9b0ee5acac654fd6e7132cb1b285d00e0fc9d62d1130663422865`
-	Default Command: `["perl5.41.1","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:46 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 02 Jul 2024 00:43:47 GMT
CMD ["bash"]
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/perl
# Wed, 03 Jul 2024 14:39:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.1.tar.gz -o perl-5.41.1.tar.gz     && echo '7dee38af601b0ba3f3730cb812cdbc799c921da440cb0ce96dd7a4f508b1a6f8 *perl-5.41.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.1.tar.gz -C /usr/src/perl     && rm perl-5.41.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 03 Jul 2024 14:39:46 GMT
WORKDIR /usr/src/app
# Wed, 03 Jul 2024 14:39:46 GMT
CMD ["perl5.41.1" "-de0"]
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95572dffeeb27b417d1030f4bdb3d7561b01ba80cb3180b3cfee6e3e589086f`  
		Last Modified: Wed, 03 Jul 2024 16:29:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61843c1fba4c46a30fee90d7af46c52a164b54cd57ec744568dff7556cd55d8`  
		Last Modified: Wed, 03 Jul 2024 21:20:02 GMT  
		Size: 28.1 MB (28122712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8f832a0fca5c21f28ddd6957681328f0bb1939e94fcdf2f028d6adb49ef804`  
		Last Modified: Wed, 03 Jul 2024 21:19:59 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:670b880a39e3a77c54b1b74288a408920c96b3940271d714cee18c8dc64c7215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcc735bc457a5b8a207426b50bb098bf7fdce090be888c030196d261c198d71`

```dockerfile
```

-	Layers:
	-	`sha256:4b6927b278f617a93735f25c0f354fbadd98b11d472efa33e38c17e6ebdb45c0`  
		Last Modified: Wed, 03 Jul 2024 21:20:00 GMT  
		Size: 3.7 MB (3707544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d5015ae9698ba6011c852fb9e28fb6dd4b66b6f68b39874893d02a9569be51`  
		Last Modified: Wed, 03 Jul 2024 21:19:59 GMT  
		Size: 18.1 KB (18147 bytes)  
		MIME: application/vnd.in-toto+json
