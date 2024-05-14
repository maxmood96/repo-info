## `perl:5-bullseye`

```console
$ docker pull perl@sha256:72fdc447c6ae21c37ca1b3e7fab2982c3535060034f7d0422c3ff615f6b0e0f2
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

### `perl:5-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:22e91a9586cd502bcd0b8f009ca0027dcc1ed23c6c4c43bf9eca2dc376307695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.1 MB (338111160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889d790e3bb58a8112a9838fb6921acadebc08fd8d2c80a334911305c30995e2`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b037c2b46ab4e54a261a0ca65b12b93e00ca052e72765c9cc4caf1262a2b86c`  
		Last Modified: Tue, 14 May 2024 03:05:30 GMT  
		Size: 54.6 MB (54589605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6043113e1c69109f845390049c3534bbf0249241ce681aafd8e6d4bc4306dcb2`  
		Last Modified: Tue, 14 May 2024 03:06:01 GMT  
		Size: 197.0 MB (197014118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9afecdcba525329cc5fc13beea47d77c0581bd5bdcd474d297af719bd4c956`  
		Last Modified: Tue, 14 May 2024 04:03:47 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee2de214a230577f610c34f3c44699325b0147461bef52448802213eb0f6757`  
		Last Modified: Tue, 14 May 2024 04:03:48 GMT  
		Size: 15.6 MB (15642905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10f8e5b394cc797dca1f3d8fb0b2cff31004ba34d21e250f7569eb10ca9e531`  
		Last Modified: Tue, 14 May 2024 04:03:47 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e3be0244b0fb43adb2d7d90b8095d84a83aedac84e48436ca8cf5b40775c9253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f71d857f426a87548ccc6d0e68ea1d7205cf4dfb76725f5d29de676f0320587`

```dockerfile
```

-	Layers:
	-	`sha256:811a3bcfdc298e335c5d76e25e743922c526a7dc4efc25a2ab8f0233db5536c5`  
		Last Modified: Tue, 14 May 2024 04:03:48 GMT  
		Size: 15.0 MB (14974538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10b3f1568a3cfb9a34b5701a72cf1494f15b400049c6689238fd0ac56681b4f7`  
		Last Modified: Tue, 14 May 2024 04:03:47 GMT  
		Size: 16.3 KB (16307 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:ee36c4ff7632b4892d2b8299aebac8914e01302d39757d111f39f803dc2ff436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310454923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3f61b3bc02dac80b63ce45fdf7ebd809422638ef46bdae098c6bfb7f95411e`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:74e1eadc44e9ed60fef85028d1af7cc94cf71327c3173769ec9d74b29e4e19c6 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:bf31f3332f7a686a69b7a5dd4c95c8f289bd767f54d9be178626f04a40b1d56b`  
		Last Modified: Tue, 14 May 2024 00:51:55 GMT  
		Size: 52.6 MB (52602710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62dd30089ebb575f8eaa5d60cef9d41adabaed93cb054f7b1db47072859eb02`  
		Last Modified: Tue, 14 May 2024 01:23:00 GMT  
		Size: 15.4 MB (15376278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a236e767fe9ffe05ea096e155f4751d0f234211ef6dae223a22f311a6d8c2060`  
		Last Modified: Tue, 14 May 2024 01:23:17 GMT  
		Size: 52.3 MB (52330199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31197eac3efc2f96a29f1e2fee22a1ee86df97c3fbfba3e488f95d5c9fa67bb1`  
		Last Modified: Tue, 14 May 2024 01:23:51 GMT  
		Size: 175.2 MB (175212599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3ffbb1112aaa6f8d65bdc20ea51ac56db221cf12f514ad631a3e08245d6902`  
		Last Modified: Tue, 14 May 2024 15:17:48 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaffb20b3b6436dc2112e0ba8a7e3121d649c8b15f8954230ef00766b1036f6`  
		Last Modified: Tue, 14 May 2024 15:17:49 GMT  
		Size: 14.9 MB (14932873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3da13240cb8c0de2c5bf993e9c908a8708ab8b6286eedc9d231eb5a860d9675`  
		Last Modified: Tue, 14 May 2024 15:17:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:af0940e4fc1f2208f28a7066b2d743f2512ef3bb4f9c05b06c9bf54a232f113c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14786780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c467f04c178f6b101f6c32aa2f88ed0b9b3d0a49f7506d66b34556ee917173f`

```dockerfile
```

-	Layers:
	-	`sha256:26424652cf61d8755aa585fa8f72077847c97c81baccad784534cfaab11cccea`  
		Last Modified: Tue, 14 May 2024 15:17:48 GMT  
		Size: 14.8 MB (14771057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060572fb87ee48d97eb7eb62bbcc1f20577c7574ef111f61744ef8ecc93fa2a4`  
		Last Modified: Tue, 14 May 2024 15:17:47 GMT  
		Size: 15.7 KB (15723 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:6c31e522828fc5245c167ca324a842a6de543a730667ec0615871dc1e7d32751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297673182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca94d90beb9e3ba8a02d7d05411b04236d5751610cda74dfb7c4be6b14132b1`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:59046a1e0987059e779fff5a0f35e03203c109d778a75058e9474705d3fcfdff in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:853e2341066ebc3a07d3c44ebac8c3ce40daf429fb9cc3f49f2d35115e9cc93f`  
		Last Modified: Wed, 24 Apr 2024 04:11:34 GMT  
		Size: 50.3 MB (50255574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5d5c1aa98981d0ab503d79e97e4eeed8435372346757065a98c291d66c74df`  
		Last Modified: Wed, 24 Apr 2024 05:03:57 GMT  
		Size: 14.9 MB (14880390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94741efe025699cbcd617a32ea95a4fea8cfaeedfa3b93bd9cbc7ed02063a74a`  
		Last Modified: Wed, 24 Apr 2024 05:04:17 GMT  
		Size: 50.4 MB (50359575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba251a5fa80ede4ef9bfae4161563b58236318c68e2a17d1cbd5afa4ba9a2c68`  
		Last Modified: Wed, 24 Apr 2024 05:04:53 GMT  
		Size: 167.4 MB (167442932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfde6d35b63b2d415c746b5efba90a9250bf964a1b5efcb13d9fb66a128613bf`  
		Last Modified: Thu, 25 Apr 2024 08:16:33 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d4a02cdb7179d77b57e23fd12ba988efb274604f20d5a7554e527196415e0a`  
		Last Modified: Thu, 25 Apr 2024 08:16:34 GMT  
		Size: 14.7 MB (14734443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca59e2c8df50b8c54b2996caa023a3952c1cb8852f97f8eee38d67e4ad336c96`  
		Last Modified: Thu, 25 Apr 2024 08:16:33 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c68d6b32cdc89d215294ab3acd39b8e3682ffa197d2c3b5546506837f3a02b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14792108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0d68c019e21146826c38859b12b13ccb400d1465688862d9f0c489f596a589`

```dockerfile
```

-	Layers:
	-	`sha256:fe2e90d8c3664f2cce84726b14b8d9eaa974a6878384663addc4fef9c3846e89`  
		Last Modified: Thu, 25 Apr 2024 08:16:33 GMT  
		Size: 14.8 MB (14776385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ce850e03a21a0d35c32bbf4e07066f8ec1b6fc3d3a78678e38ff7182f46e24`  
		Last Modified: Thu, 25 Apr 2024 08:16:33 GMT  
		Size: 15.7 KB (15723 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:d6141cce5b4a425fcc055ddc42b349af2c576e5960ad0b801a9b6b1ecd53da42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329678757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba6973c911f80fc9421a366428e6ac76af70e210687e7e94e47858fed2dc812`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33008ff0928e624ce22cedd5d004edd66b80372bfd1223e8900206330213ee34`  
		Last Modified: Wed, 24 Apr 2024 08:42:31 GMT  
		Size: 15.8 MB (15750623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36972983386f768dbeff5de37af34ed4e2f59541b2e3c43575f29758c3591923`  
		Last Modified: Wed, 24 Apr 2024 08:42:45 GMT  
		Size: 54.7 MB (54696233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3224178d7041e10ec03b66358ce4ba6bb5aeaf26b593f3e8672ca38f7b70769e`  
		Last Modified: Wed, 24 Apr 2024 08:43:09 GMT  
		Size: 189.9 MB (189912094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c46663f8cdbb36345fbcdb13cb9b6b9b6dc466a56f1a20544e324a04b1efb5`  
		Last Modified: Thu, 25 Apr 2024 08:17:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b50a08639f8b032425590cd0784043cc02579d23a323f25290fbd9cf6102a98`  
		Last Modified: Thu, 25 Apr 2024 08:17:45 GMT  
		Size: 15.6 MB (15579582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596ccd5bf65986e85a115a7e08776793bbe3b8e99a4ff594ba425c524ba27424`  
		Last Modified: Thu, 25 Apr 2024 08:17:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a281583686a19d339d6aa15327ad163336c19f67f1c379d25481455ca1142310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c25823962b0eedc09bb99917d4c4823f87722943f49a683dad4a4403141b2d`

```dockerfile
```

-	Layers:
	-	`sha256:2651b51371a8b482ed4086de77a71027e39dac414b75d1bde39b8529257887fb`  
		Last Modified: Thu, 25 Apr 2024 08:17:45 GMT  
		Size: 15.0 MB (14976958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b58e5f3d2b7bf0e0c7f0e231dba907bf901fe4af47242364fab1c968ea59c55`  
		Last Modified: Thu, 25 Apr 2024 08:17:44 GMT  
		Size: 15.7 KB (15657 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; 386

```console
$ docker pull perl@sha256:a1ebadf6dd5efcd3d036e50df6065e20f1ae4edcba59d7a7eb9a1636d80d8ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.3 MB (343304114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411395d2ab8fad888a0e942bd4bbdfeb3af8dc9b81c114dd0834b4634ff61cde`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:f45ff600062e56788dec8eb7a1a4eb58c56391243efecfc62b3f911f35ce7517 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:531ff4ee4f75fb0b1990fd185259fbec17670ebea9c3011de30a27e2de08c387`  
		Last Modified: Wed, 24 Apr 2024 03:43:58 GMT  
		Size: 56.1 MB (56076550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76062ffe019e6bfc91f0fe0510211f961184446e120461504dd7066278dbfb88`  
		Last Modified: Wed, 24 Apr 2024 04:42:41 GMT  
		Size: 16.3 MB (16269075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41af9e34185ddf73f8ecb610526409cc80e34f0aab2c2078a0effbe14be251`  
		Last Modified: Wed, 24 Apr 2024 04:43:06 GMT  
		Size: 55.9 MB (55929331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409c343ec37d7971f52aa446a2e4bdf1947c24ac26c712f8d041bbde1de773ac`  
		Last Modified: Wed, 24 Apr 2024 04:43:51 GMT  
		Size: 199.9 MB (199892179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a9e94a701c5b8f7f516a157816c728b0cd63c1263aae1027b3c50ba0ef2103`  
		Last Modified: Wed, 24 Apr 2024 06:06:37 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f303df4d1c1a4abdb50b7ad8b8d849d5e384dc453c409314d15fab07504f5d5`  
		Last Modified: Wed, 24 Apr 2024 06:06:38 GMT  
		Size: 15.1 MB (15136712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4caebf58bbc02d4831d99a71b68e8b2578e7493e93408f6f80272dbb26ae98`  
		Last Modified: Wed, 24 Apr 2024 06:06:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:85248d6869b13666bcdab08bbc6b1dcce4589ecab04b53e6990052a28c0ab7c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14979590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15465344e1ac571790ca528413b5186f6a404efa6d7b1bc9bc31ac8fae21a0f4`

```dockerfile
```

-	Layers:
	-	`sha256:b797b2f3f2f3f24c4594c7463cc79085c0d58236d65f6a5307fb0821cbdf53e8`  
		Last Modified: Wed, 24 Apr 2024 06:06:38 GMT  
		Size: 15.0 MB (14963316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f11a0b3ce4ec4bcc05afacfa4c3756d917315d504d23702e653c8d472dd8dd4`  
		Last Modified: Wed, 24 Apr 2024 06:06:37 GMT  
		Size: 16.3 KB (16274 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:c65d4b487607466331b6477f683a229c9b696fa7a7c433a74bbf0e1fa4d287ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316115076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ca13d00b0bd9c8d499b2aca3b9a680c4b8e129b4b610cbab05141661d91580`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:d071b57187646d0653c08b1eb289840e8f9b901923339a0c04c87c0cddd93a41 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:1d0c8a1684008e75383df0eb74516bfb1122de8ea4827b46099c12fd8e762fd1`  
		Last Modified: Wed, 24 Apr 2024 03:26:04 GMT  
		Size: 53.3 MB (53322762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef66439aec687b7a8ad9504639d4dc09b9a41905f4c10f7f1ad91621be986e11`  
		Last Modified: Wed, 24 Apr 2024 04:33:48 GMT  
		Size: 15.5 MB (15530679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef55801539f5fb3d517667902d6e294fada12da96de5074aeb0f507b672b652`  
		Last Modified: Wed, 24 Apr 2024 04:34:32 GMT  
		Size: 53.3 MB (53312459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0097da42a5b48e64c566c76ac1c53a4a8085fe9c6f5d921ae73c60587bc2df0`  
		Last Modified: Wed, 24 Apr 2024 04:36:29 GMT  
		Size: 179.1 MB (179100458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a99c52ec7de1534b3f2a738de29b5d58500b75f3251fc20ea000a636878fdc`  
		Last Modified: Thu, 25 Apr 2024 01:51:58 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699f81a780a52ad622211079ba0646987129a44571c4c4afc4fa508b171836f2`  
		Last Modified: Thu, 25 Apr 2024 01:52:00 GMT  
		Size: 14.8 MB (14848451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ab395dae584c549019d0a49a7e6655097506744ccd42a8213ebbcda8ff14e9`  
		Last Modified: Thu, 25 Apr 2024 01:52:02 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:5c00a41bc2fb09b0a82b53bcd67e8b16ceb7eea56c190e91df80040aaf32540d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 KB (16155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cedd36344a03d4a899db05508e0b4f5f04138794676167d2f3b74f12853164`

```dockerfile
```

-	Layers:
	-	`sha256:213989877ffbf016ff203d26188bd7df69107eea41db765bcf9d523de681ab34`  
		Last Modified: Thu, 25 Apr 2024 01:51:55 GMT  
		Size: 16.2 KB (16155 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:e4e2c624858dcd3fad542943570b7447347a4da00ef02586961a5b7f53beb84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.6 MB (346588256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ffe1fa88ef8f541d60f561c65177a0ed508fa5f9d490b96c94025a876af2c8`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:f5283c61db1fea68c9d742ae60d7572775bfb46d2e8a92659edbd0c98e083a93 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:aac3759e46343ae5d9b035355707bd07abf04ff80e3d29e689ea89cc78633190`  
		Last Modified: Wed, 24 Apr 2024 03:27:06 GMT  
		Size: 59.0 MB (58968197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc915aadd544630a28ea807628347805a6b8bc6f250feae34a46f66ac5228d3`  
		Last Modified: Wed, 24 Apr 2024 04:24:14 GMT  
		Size: 16.8 MB (16767223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87809a577847ee55cd1298464ee16a72985d1700dcf4e546db6fca794086d7c7`  
		Last Modified: Wed, 24 Apr 2024 04:24:32 GMT  
		Size: 58.9 MB (58873993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b19380d6722f8bacf55a08edef5ab2bef7d748909aa0109770daf96177909f5`  
		Last Modified: Wed, 24 Apr 2024 04:25:08 GMT  
		Size: 196.3 MB (196343705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430c1b7959568dea00bc322cc26652dfc1fd7ce58ae79ea6acacc03517d2906a`  
		Last Modified: Thu, 25 Apr 2024 04:10:39 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9864f8291b9a176cda38d8475fb113d3c48701757b0bb363d2b9a15107c97c6`  
		Last Modified: Thu, 25 Apr 2024 04:10:40 GMT  
		Size: 15.6 MB (15634871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de2e7a573971fb0a619c1b9db0450260e531268ff35198f3654ea71248fa297`  
		Last Modified: Thu, 25 Apr 2024 04:10:39 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a9a9efa1a4f8a3eae2ea7271b3227b3b6f4b3f6c0de1ff2070dc64b80d64ba51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14959489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d5f5804d922d502904be69551012afb83fa408c25be91334e73457dc91f140`

```dockerfile
```

-	Layers:
	-	`sha256:15f9985c3672b407f949669f9c892558631bf433d5b601189ad2a76852c6b194`  
		Last Modified: Thu, 25 Apr 2024 04:10:41 GMT  
		Size: 14.9 MB (14943801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:924dffa77d2860287921d45fc54e3e7e6981bd9496701e797c4e97553acf2b90`  
		Last Modified: Thu, 25 Apr 2024 04:10:39 GMT  
		Size: 15.7 KB (15688 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:b7ac8f4d648e93b68efd88d9372610326a36b64b1dac0eb59a72929788d00153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (312039163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f861e2b8d8f627bb5eb2ccaac88a80ca136be81ceddd7f62dc076908ba1cc214`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:e0a1fc1de1477cea6fe41bdd15378013c680928cad3988dd16926cc1562c775e in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:b57a10abb081ff40e5bb34246c3875a71b8d258f767c4f8384d7054b1bc42725`  
		Last Modified: Wed, 24 Apr 2024 03:49:31 GMT  
		Size: 53.3 MB (53337419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ed92794c4710c20ea615a0e07fe947837768482be7bcd9d1fccb335072a92`  
		Last Modified: Wed, 24 Apr 2024 04:24:03 GMT  
		Size: 15.6 MB (15642846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede0318d2197701d71929fa882d8d64bdc0c65ee6bc9abd4bd4063694d92acb7`  
		Last Modified: Wed, 24 Apr 2024 04:24:17 GMT  
		Size: 54.1 MB (54076626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c3f9b4c72abaa52996d64ffc8754f8500b075a8a677c0fe59c310548e9af5c`  
		Last Modified: Wed, 24 Apr 2024 04:24:43 GMT  
		Size: 173.0 MB (172994116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3c686234ad41f7385f7365304073ab1fdbb9a52f17aa8d88ff9551d4677db4`  
		Last Modified: Thu, 25 Apr 2024 03:09:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d2d120230de889461916c097e24f643777bcfd40ef97f01fb791b5ba0e05d6`  
		Last Modified: Thu, 25 Apr 2024 03:09:12 GMT  
		Size: 16.0 MB (15987890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330e8a15a021db6856e96092ff14c7e2936fbd864afd0c46a0257d67d0c2a35d`  
		Last Modified: Thu, 25 Apr 2024 03:09:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:66dbe97a1a51683145b5691177c942452fa5007d204b14dc826624e8aee5d6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14811808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b80139b76eb6ca3c232f37fd7048c806b27d2ac5a8d4bb56405f3da0f1c93d`

```dockerfile
```

-	Layers:
	-	`sha256:618c141fdf6f6bf302ac6c491e24897e495480edd82c9b25c8951a572c5ebf59`  
		Last Modified: Thu, 25 Apr 2024 03:09:12 GMT  
		Size: 14.8 MB (14796164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:628bc79550ae90466a18628fba58de9baaeb08ca3a0a00d63aa4f6e169b62760`  
		Last Modified: Thu, 25 Apr 2024 03:09:11 GMT  
		Size: 15.6 KB (15644 bytes)  
		MIME: application/vnd.in-toto+json
