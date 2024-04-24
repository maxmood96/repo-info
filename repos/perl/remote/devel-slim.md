## `perl:devel-slim`

```console
$ docker pull perl@sha256:a167df9ae371ad1cd420c99207617ef2ef50d1f030ec0493bfd7a38ce13a4ade
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

### `perl:devel-slim` - linux; amd64

```console
$ docker pull perl@sha256:3fb4cf13f24a47c87ba0e63a347398e2034be28f122049932e23648a2f9201b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57717285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ddac45a805ddc692c51b16dd4142f2025804b45c2726ef9f0c63d4e5e4f45aa`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
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
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdfac6363d83cf6583da3a58dac39fccc57ac57ccaeb2f5709a85657a5030da`  
		Last Modified: Wed, 24 Apr 2024 05:03:32 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e11ac7bc8a536784ed00f78f502e0917ff63e565eca606fe595d4bcffd46b98`  
		Last Modified: Wed, 24 Apr 2024 05:03:33 GMT  
		Size: 28.6 MB (28566539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9adc6989ee529e41472cb2ce3adf2ebb4c93d350e31f2cef5b115c4834b8832`  
		Last Modified: Wed, 24 Apr 2024 05:03:32 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:dfe0ca2a46cf33879365a3543329e5c9a869179aadc4dad6c46f4c96434a8c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3735976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cb23fa78e06ebbad1c39d49b57d71dacfc65d4875b132215f2c7bf6bd7437f`

```dockerfile
```

-	Layers:
	-	`sha256:0343efed2559d435f7e1904e3c623db88e96c8b9faecad0e7eb9e86223f85fae`  
		Last Modified: Wed, 24 Apr 2024 05:03:33 GMT  
		Size: 3.7 MB (3719246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d53fd2bcc3d3d30482d8f113680ca6e8dbf4e49645c1e953fea47f136fb32bb8`  
		Last Modified: Wed, 24 Apr 2024 05:03:32 GMT  
		Size: 16.7 KB (16730 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:a9d04f076898b7ad3d072cc02491ab8a3d86782af5214bdcc1683f824c50eeea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52571643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38340aef3bf0aa49b01d87ab2abb05449a74f10a95331ec1bd93c6ba3664f62f`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
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
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa002d450c5ab1d539a38a7c86c6c2e5adbc71da7588db05ce9cf451447a4fd`  
		Last Modified: Wed, 24 Apr 2024 17:54:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb825379cca6d45328df27116c0a512bf63932c4b0bb01467c5ea466cdbcf67`  
		Last Modified: Wed, 24 Apr 2024 20:20:00 GMT  
		Size: 25.7 MB (25661348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7aeba847a5afb21b383c117d85dd0caf6a2245a76f1109bf24e53b31aa4b14`  
		Last Modified: Wed, 24 Apr 2024 20:19:59 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:487ff09b10028b9a7ce19581800e5b4ce0440b0c38b790d39296666958e5189c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3706158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5f337cb3d3144e3206f12f111a24013c89d9bc6eaff1062d7bb08a9d0d8ea`

```dockerfile
```

-	Layers:
	-	`sha256:a1f3ddf8d2bd436f9f183126bce3acc1f08c9ff62ad77cd82b424259995350d5`  
		Last Modified: Wed, 24 Apr 2024 20:20:00 GMT  
		Size: 3.7 MB (3689509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c409d9386426e4967863b72d1ab8510301e6bed1e6fd83d81c5771879cd7fadc`  
		Last Modified: Wed, 24 Apr 2024 20:19:59 GMT  
		Size: 16.6 KB (16649 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:0191de19b1238263c9c6445dcfe38f4cf7281a23766c253e11820586e618f62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49630512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb85321fc1137e9c3ea1f99a5c68b9fe8823d3630a306dfa3ba771a1f5877cc`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
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
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b51872060208912f28244a31d373751f410c53d744c327127ec76ca92009e89`  
		Last Modified: Wed, 24 Apr 2024 16:58:21 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700a205aa89b2ac3889e1e0e422276306651ab14cfeedcafee552f181ef1ad8b`  
		Last Modified: Wed, 24 Apr 2024 20:01:09 GMT  
		Size: 24.9 MB (24889805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6601720cf4e17ec885c2a1d61bb92d83ce9ccb2c4b0b410a49261f5f9eccf491`  
		Last Modified: Wed, 24 Apr 2024 20:01:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:0d9de5fa90f5e5bda63fcc9c7d00598af1e74ddbd660cc7654c0e44cedae42b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3705917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7aea425cb72348c5df7d298b90d39884921bc976205c53d25008750e0435701`

```dockerfile
```

-	Layers:
	-	`sha256:1581e6a5c2338837772530f025ca78e20465808cd9f5a4220760dd3c6a3dc9ac`  
		Last Modified: Wed, 24 Apr 2024 20:01:09 GMT  
		Size: 3.7 MB (3689267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16a4a2d836d386438c07b1ffcef23d5c545b4040015f7c5ba772f4795c37d461`  
		Last Modified: Wed, 24 Apr 2024 20:01:08 GMT  
		Size: 16.6 KB (16650 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; arm64 variant v8

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

### `perl:devel-slim` - unknown; unknown

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

### `perl:devel-slim` - linux; 386

```console
$ docker pull perl@sha256:039843d0ca64a0580e58458ddf0683a9aacdb2f14d334d8b3f02096a1ce8b50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57721943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808f1c5e36a31be28e99b985f7af1397e8f483894bc2651736e941e046e691be`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
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
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951a0636b6255aef1df5fc7a13301f741215b42b0f252c98e64b40c20bc551be`  
		Last Modified: Wed, 24 Apr 2024 05:04:38 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535c7c39f2ded13d0be5ea7977484ea3744060181592e7f9ce52fd10e0f492ad`  
		Last Modified: Wed, 24 Apr 2024 05:04:39 GMT  
		Size: 27.6 MB (27558491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ed777972dee1e5513c1cf2796c7bb799e415fed98faa7c16e8a1dbe29ee141`  
		Last Modified: Wed, 24 Apr 2024 05:04:38 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim` - unknown; unknown

```console
$ docker pull perl@sha256:0e9b83b1dafe0176548f5c68089210e6b590414a83be6c77addfcc17703ea0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f79187c09ec32f04025b963742c4b7f6d5412a8c7e97c17e8b01950ebd75a1`

```dockerfile
```

-	Layers:
	-	`sha256:767b25d304fc910dfce10758d2906cd4684908a8bf11ea905ed5b83156b5f927`  
		Last Modified: Wed, 24 Apr 2024 05:04:38 GMT  
		Size: 3.7 MB (3713139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:312b2133897373197d2857cef17338e05d5cf1c55ffc905ec0e333d4f201c569`  
		Last Modified: Wed, 24 Apr 2024 05:04:38 GMT  
		Size: 16.7 KB (16692 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim` - linux; mips64le

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

### `perl:devel-slim` - unknown; unknown

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

### `perl:devel-slim` - linux; ppc64le

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

### `perl:devel-slim` - unknown; unknown

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

### `perl:devel-slim` - linux; s390x

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

### `perl:devel-slim` - unknown; unknown

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
