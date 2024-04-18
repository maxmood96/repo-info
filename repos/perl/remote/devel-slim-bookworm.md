## `perl:devel-slim-bookworm`

```console
$ docker pull perl@sha256:aae871057c105de9411abe4f026671f45bd14d75b687bb5c961ec6994aae8584
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
$ docker pull perl@sha256:20b983ad0cea078d4702aef002ce053d817664fb550de7cfe0e9cdcbcbadac96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57892436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a07c7552a3f74292a60c80af63c6a5fb8e7f2a5a53d371346d20dad3536463`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2323aaf7c8a8373e691b0e430bf7bcdda3bbe6ab044a1a943ec655e591623fef`  
		Last Modified: Wed, 10 Apr 2024 03:01:26 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0c47369c7dd6d8ab85c0e2449c19575aa5a50926c8f9d73c25e0f931896901`  
		Last Modified: Wed, 10 Apr 2024 03:02:05 GMT  
		Size: 28.8 MB (28760810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f04e43bf285df4edd8ffc21fbf0f94cae2b0a5132f36672556fe71891f8ccd9`  
		Last Modified: Wed, 10 Apr 2024 03:02:04 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:e0d9feebcea75a6fb98acd49802e1a79b50c1157615fe6e7f84454d719d6d3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3735859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a730e0421c8473eca0c00c80ade040c4ff0dcf7e990f7938442e65cec92d080`

```dockerfile
```

-	Layers:
	-	`sha256:8d702d03d424558d589364787aae117080d0f9f600e1add8bffdf5320c68559f`  
		Last Modified: Wed, 10 Apr 2024 03:02:05 GMT  
		Size: 3.7 MB (3719132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50966940c3f6f3f7561bab55f8cb0b991048b27b9e525b6e1c1042cca6929c1c`  
		Last Modified: Wed, 10 Apr 2024 03:02:04 GMT  
		Size: 16.7 KB (16727 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:9c70da73cd626e28b0c47859d0cbc3102de1cd23aa381a96f68ef39930102251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52747218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadde4021064c6fac171851da5e2b958af54c37c72dc2918f68611d28107221c`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcb8727cbcd2d4f1efb13db12765fa4a12b869e763d6dac4449aa6314271c36`  
		Last Modified: Wed, 10 Apr 2024 16:59:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdad96d1692e119724221ecc6bb01e3a0b15b1b0ee31cffbe991e3baa7e65dde`  
		Last Modified: Wed, 10 Apr 2024 18:51:15 GMT  
		Size: 25.9 MB (25856387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d43e9dfd436c823b3288c6ca7f1a04753fb7dcac8ee42ae73ee4631c63d90e`  
		Last Modified: Wed, 10 Apr 2024 18:51:13 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:098b46d7dc7c194960bbee2d5e36d6d527b43d405b0a77e0b1c5f1edb7391ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3706041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e466d314a4c839ac4d433e06db34f14ec75eb97cbba735b7f7a4508c452d0880`

```dockerfile
```

-	Layers:
	-	`sha256:b3a83c731cf110c87549ba0a8baae9c289ffc1abfd9c243712c773ae693d2e16`  
		Last Modified: Wed, 10 Apr 2024 18:51:14 GMT  
		Size: 3.7 MB (3689395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad2131d952de1474ea7ef798397128f73e59afa7b79a16390c143db9e53156e2`  
		Last Modified: Wed, 10 Apr 2024 18:51:13 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:ae93d0aaf379f2094e6f8c1069fce5a2792953bc3ce05ba9382d825d1429cebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49805486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82347a45b5fb9290dbea1de65223a8fcfc4a254cf7a356a0cf2bb4703362514`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c249e0cc017adb48f327da241dd5fe27cf1818bab7ed6d6b93fa8058086ebe7`  
		Last Modified: Thu, 11 Apr 2024 02:03:15 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921704340cf8ac2915edb9db3fe42fbd0b4ec1dd5e95b997b57ca593500caa6a`  
		Last Modified: Thu, 11 Apr 2024 05:27:44 GMT  
		Size: 25.1 MB (25082295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0247cf0d8f2926f64772d649ae8def0bf4b2811e7dc1e3cf7eb2a627cd542552`  
		Last Modified: Thu, 11 Apr 2024 05:27:43 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:451977f8d1a073e2f6e5c64b27a79935843b39334462cf58f19621a386d43d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3705799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0760b9f8e1c0afd768b1381a929b5c4cf06244fd0ec2db61600adceafda41d71`

```dockerfile
```

-	Layers:
	-	`sha256:148a45de91a0d8a7caa70ea0b63f6735b23c86279a0e3f53c6304660c686f36d`  
		Last Modified: Thu, 11 Apr 2024 05:27:43 GMT  
		Size: 3.7 MB (3689153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8779097d3f51e0bbd092baedad507c48ec37b7c902156a4b07d64de900a30c9e`  
		Last Modified: Thu, 11 Apr 2024 05:27:43 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:b91c1ca67c6798f00080df22505c0053ecab3c27e11c561c2313cfc70640da06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56711620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec00cd631cf307f0fcb409cc3af6b8dd6a131ebff10660a361c0bb94e842e1f`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe961d440955688f8659df672f0d7478ea5e34abc65767f0d6c2df2b2d4c6522`  
		Last Modified: Wed, 10 Apr 2024 17:05:31 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd2d8245c1cc280baf74b79e953a4d831b26753b8e07d5cd4ddae2ba031603b`  
		Last Modified: Wed, 10 Apr 2024 19:58:20 GMT  
		Size: 27.5 MB (27549197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462505e27170d815dbbd45afee34d418a97d3b03dc2ddae65f1b4dbef1a14584`  
		Last Modified: Wed, 10 Apr 2024 19:58:19 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a949d0f42495b0ec4744dfcb7cb141565e51345c84bc6d4d9ffd958dc58c5548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3706864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acaef3c1bc89e170f2d353d855916f4950faafdf4b1cd1ef9a73507a5a06ea10`

```dockerfile
```

-	Layers:
	-	`sha256:6f68eb19a3a3336e5fae8fb42635e326b61c4a28bc2a480db7ea3731d28bf32a`  
		Last Modified: Wed, 10 Apr 2024 19:58:19 GMT  
		Size: 3.7 MB (3690290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d66c9399edc9f99d57793b8d8ad64c9627cc5b43b27db2274dd0b269bf0dd47`  
		Last Modified: Wed, 10 Apr 2024 19:58:18 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; 386

```console
$ docker pull perl@sha256:de0ca1739435c44637a0914b8ba384c798f7dae6d87c6c08a373bf103c130047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57896886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e2e65b98952b26c241afff322a64c76173b441434aece21fd776932dfde754`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0b100ebdd7ec2f22d1ef81b2569c253dfd80f3fb9562dba5740d5df93af510`  
		Last Modified: Wed, 10 Apr 2024 02:00:46 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ccd43ae3ffc351b647f5f1ae46060673ad276f880021b8b71ffc0910ce7cc1`  
		Last Modified: Wed, 10 Apr 2024 02:00:47 GMT  
		Size: 27.8 MB (27750105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7681382e2276eb25891590f4b4fe5a33b4fb8e5d218bd9028a5b5d604123885d`  
		Last Modified: Wed, 10 Apr 2024 02:00:46 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:5c63c69a041ed5d21392dda08dc30868e2d2fd9ac69cda979f0434de26663f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb66a95fe90835366cc6573d17385ef759382c82e774fb666a58aeca0a7126e1`

```dockerfile
```

-	Layers:
	-	`sha256:53f57bd03c94ff6f73e6c9bf567ce77a9ff3fbf78b81094750c2480a2b79a90e`  
		Last Modified: Wed, 10 Apr 2024 02:00:47 GMT  
		Size: 3.7 MB (3713025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e425602b3f015f8ca0440bf4645f2862560e95143089ebe286db44635ffc3c81`  
		Last Modified: Wed, 10 Apr 2024 02:00:46 GMT  
		Size: 16.7 KB (16688 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:519650f0c474ba66b6947d9065979324128b102fd169e5f4541a33bbfec8b7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56037193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702f5effda72b5711ee795dc40cc01f1f283e15ef45e4bd9cd9dd1a77926812c`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:c07831a1f2abb22986c788bb198b484a259e7e68ee8b03da0daeb4b41d8d83ce in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:a99180cf1634aa211024be7ce3258cac9c0823e82f09b97870da9d9b21ea68ca`  
		Last Modified: Wed, 10 Apr 2024 01:21:58 GMT  
		Size: 29.1 MB (29124665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecf89cb254e2f5656809db8155c1d50808738b00ff076d579f23844524ec120`  
		Last Modified: Thu, 11 Apr 2024 02:53:22 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad17ecda2e750f3abbddd5fc5bcb798148386b65da45071ae235e9bb348d3a21`  
		Last Modified: Thu, 11 Apr 2024 07:24:46 GMT  
		Size: 26.9 MB (26912260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334612727179021a5e2b8cac2cbfac758faf7db7fd428770c70554925442b0c7`  
		Last Modified: Thu, 11 Apr 2024 07:24:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:4d0ab0c1112cfd56f9354de56f635e70984891cc503774e1bab5abc98d3a94f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 KB (16420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7836608b77d9c3bcb18cc9073a36c457ff572d1742a9dc3a43e693dbaf38229b`

```dockerfile
```

-	Layers:
	-	`sha256:4c2f7ca6c89b43cce6cc6ac7fcfb8ee1b3c17028bb8c9341a66c122406b08ec5`  
		Last Modified: Thu, 11 Apr 2024 07:24:43 GMT  
		Size: 16.4 KB (16420 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:a1ab6fa687d3987a659b95c1a8a5936f2e256c73777d6de86627e8770f8117f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62433529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c29c372f62158fc061c8ea443d0ce7067b5270fde76e0acf43b336c40482f5`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ac7e27cfc922464a219c5f40ab2b8831291168f409f5a6cdd769573c9e5dbf`  
		Last Modified: Wed, 10 Apr 2024 19:39:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95f31ea11de4fda52b7bcd8ad934b4d974657570f12efe78632ac1cb57ec0c7`  
		Last Modified: Wed, 10 Apr 2024 20:50:07 GMT  
		Size: 29.3 MB (29308426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a346561c3c63c1c7a7cccaa4c5c2150c2464f786e0354a207b097c5d9a4214a`  
		Last Modified: Wed, 10 Apr 2024 20:50:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:e723e981aa30e09a1879c91b99afd9edeeb490ae4a8d02f42d35552323e9e8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d525fed0fe4c3c99d6e23aa86cca5ad1ba1a5afb0bb75945ee98b04a71eaad`

```dockerfile
```

-	Layers:
	-	`sha256:0cc7b9a2c7b7679c3d34f950976ec78983a1f1abc7b398a0a225a044bddd370e`  
		Last Modified: Wed, 10 Apr 2024 20:50:06 GMT  
		Size: 3.7 MB (3704835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7289fff7c3a3eea5a81275eef4981eb81171c63ae0954c3291ffa23941a61d95`  
		Last Modified: Wed, 10 Apr 2024 20:50:05 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:4d0fc49a2bc227c51fd5fd4009e5dadf2e9b5cd8a57d93b9033b08ca7eef50b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54783966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a65f06e681ea3e981e7fda9c4ed061a3e7802d6ffedc3d5105ae7f5b517e8c6`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:0e66ba8384d53d3671a6a148f8bad9decf482a97ef81d0740132e74b8e30c670 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:06d33788df65214dbd82280e1b49e32ce4580d4f3df100d32090f4eae8ccd99c`  
		Last Modified: Wed, 10 Apr 2024 01:48:29 GMT  
		Size: 27.5 MB (27494178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94da905217dc55d867ea4d85c8c1ab64ebf87d8be81345ca85d4ef400c96c069`  
		Last Modified: Sat, 13 Apr 2024 05:28:38 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2684f9cc3c95de0909707f3ac30ec6652315abef019be3ccaf026d85dae694`  
		Last Modified: Sat, 13 Apr 2024 11:31:53 GMT  
		Size: 27.3 MB (27289521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea36cf135e65cd79a05a0e6def8bf7d163af9de4ecbd908677acfb517228004`  
		Last Modified: Sat, 13 Apr 2024 11:31:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a42e8943666e10a3c5ddb5137c5b7306a07341d7e8755b7812e73541809aeb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad830c54aed21948a54c0b72e18c547403dfa5a2714937f002d1b6a1cf33eb`

```dockerfile
```

-	Layers:
	-	`sha256:873451c8da3795236bfc275e843e709f46e6d35f8f98543088fc3773768cb0ce`  
		Last Modified: Sat, 13 Apr 2024 11:31:52 GMT  
		Size: 3.7 MB (3707402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338686ef3609fcbed464065f9728b0c5261c51e061743a612a5522ee0ffcf9fd`  
		Last Modified: Sat, 13 Apr 2024 11:31:52 GMT  
		Size: 16.6 KB (16560 bytes)  
		MIME: application/vnd.in-toto+json
