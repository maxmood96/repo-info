## `perl:slim-threaded-bullseye`

```console
$ docker pull perl@sha256:f2a9c866e213666ccb3d5835f8049ba3259313ec3908705fd1db14bea0e646e6
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

### `perl:slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:332ceae4ef8c651d5fc99d272d9b1aa0071ea2de84c1552c96bf5274886611c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55864403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef682f349ff171012e7f2a92236da7906b3ec54dd4d0fe13bd7c040b0f448ae`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e66ee0f0dd144baf50150e87dd9b8a62218eff30314e74781df40d1fe28f1ca`  
		Last Modified: Tue, 14 May 2024 03:03:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774988ccd7e43caa38d127816ce67b45bb34c939772ae6d18514b8521478ac5d`  
		Last Modified: Tue, 14 May 2024 03:03:57 GMT  
		Size: 24.4 MB (24430205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12276c7463f2aec16b0c0ecfc2f43faa461709521c6434627bdeefd88ca670d`  
		Last Modified: Tue, 14 May 2024 03:03:57 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b4f7aba41aaceefeea86afb31da3c51a84b3e1318e1a29ad0dba1353edd77e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eebe2971b8a85416329c875cb7a9830f42781e25de57b7279774b3af5de683e`

```dockerfile
```

-	Layers:
	-	`sha256:a43b53e72487290f1eb26ff8e432383cb01ee7bbae46d8d4b4cd07a498996239`  
		Last Modified: Tue, 14 May 2024 03:03:57 GMT  
		Size: 3.9 MB (3913017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e6db83e2ed3096b0d3b1d20e47d7282df5dc098a87e777e0ccebd95489c13d`  
		Last Modified: Tue, 14 May 2024 03:03:57 GMT  
		Size: 16.5 KB (16514 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:b2e1813c6dc0a9f49a08e7a03b802e2d659a59c782999448f4102d2367c3a59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51347457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac8e727f13c8b52e0e024a968d77bb12cb924069afe2ad9f6562ab697fdfd4e`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:4ccbd1f9bcc76d259ba2b235681f1b749e86690e8805ee49f9fb44abc9ff5dc2 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:2438f3883cb848a901cb08a6c99ec3ef261d41ca6f0d5321f274d995c58fa24e`  
		Last Modified: Wed, 24 Apr 2024 03:57:14 GMT  
		Size: 28.9 MB (28936577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a245b2574bb51828f8fdb8c09eaf2db112a669383430da943e9d18f17441673e`  
		Last Modified: Wed, 24 Apr 2024 18:01:21 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bab4f5b32773a784a4aef8954556e696713f1a9964fc12220e00ff547e17c46`  
		Last Modified: Wed, 24 Apr 2024 18:32:53 GMT  
		Size: 22.4 MB (22410614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51132b5a4ed992d12f8274718fc74ded407e6e4e71c13b5d003815398e1c746c`  
		Last Modified: Wed, 24 Apr 2024 18:32:51 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:1bcfe90a4c540e20a7e45f795975b87d9b1e9a977369098c263b76d008d71a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3900643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddb567ce9b940e28d4472ba6486ab261531b64a8276d4878dd033db2bd9e833`

```dockerfile
```

-	Layers:
	-	`sha256:a0093f55ba63440d9b2dcefee967f103cb397f3e5c03fe2e0568a848083368ff`  
		Last Modified: Wed, 24 Apr 2024 18:32:52 GMT  
		Size: 3.9 MB (3884220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:732e2dd7138b5dc14431272d55040bbf17caa0887a5678ffd2ec74369cbbda2d`  
		Last Modified: Wed, 24 Apr 2024 18:32:51 GMT  
		Size: 16.4 KB (16423 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:348189d43493ec2cd223554706cbe8c92eabb556b21480a596070596a79cb19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48407705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4641569272467eb19ac5daa7af9627a9ded83a43a2757939d8c1c0e70d3ebf67`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac66be9478d777106d8a4a8bafb1865146b4c82924180a3e59b9b94683b39642`  
		Last Modified: Tue, 14 May 2024 14:29:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b264f881cad2103c0d2bc133f5f78f12c6c99d7ee505632196aaaaa61f6433f8`  
		Last Modified: Tue, 14 May 2024 14:50:05 GMT  
		Size: 21.8 MB (21812947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62e0a03edeb31adccf76918b461bcacb7e409ac3d6e1d20075543860e675ae3`  
		Last Modified: Tue, 14 May 2024 14:50:04 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:cf3734edd8002bac0b4c9b97274f87a5daa85a3c1c625f7dd85477cf58d46dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3903373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf573b14f5940f33da11c4a785f162dfdc8049fa820fc7bbd766ef7210638ccc`

```dockerfile
```

-	Layers:
	-	`sha256:3930687e583c2dd834b607940723c6afc4020f8c4985d2fafd43da3d36b70ef3`  
		Last Modified: Tue, 14 May 2024 14:50:05 GMT  
		Size: 3.9 MB (3886948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a2dba9446824354edff1f5a7245c409768665f90b70f0fda894cbb84100f865`  
		Last Modified: Tue, 14 May 2024 14:50:04 GMT  
		Size: 16.4 KB (16425 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:2c216c2a05c446261821feaa2f62109540900a10f1f8cf3aa8d84ce3e90e1292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53632467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77f0521d22b682ef7e86cab809906174c048315d6ad3591e378eb9ed76d4f2c`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dbb539b13bcec9b4a2118f4147996ebff04dd60087c6206f3fd1a8e4510829`  
		Last Modified: Thu, 25 Apr 2024 08:33:58 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e333a72debe598bbc8a2e8a512244eff282d8414b2543f69de45274a66bf4c51`  
		Last Modified: Thu, 25 Apr 2024 09:44:38 GMT  
		Size: 23.5 MB (23544863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ea3952c366bf0cb9887061d456ae04a4c76f08c1c9dc64db1e7733ceaf2bfa`  
		Last Modified: Thu, 25 Apr 2024 09:44:37 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:3fbfcb14de66ec7bfd222d0720862535e00752d4d926f88ad47b97ecf8001683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3903684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4827047aef485236aa40c2570a5fa0e78515d1e98c58c02a1831962de66f44bb`

```dockerfile
```

-	Layers:
	-	`sha256:44c9ee95b14dfc7a8b27b8b405db9a0c9194cab5b7c7ce327ada73bf072fc843`  
		Last Modified: Thu, 25 Apr 2024 09:44:38 GMT  
		Size: 3.9 MB (3887325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69793ba20846d5c9b06315923db71ee780eae1a9a8fcca3eb68d34a213521fbf`  
		Last Modified: Thu, 25 Apr 2024 09:44:37 GMT  
		Size: 16.4 KB (16359 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:a5bef77390e4a8d937cb3ffc95d829668dbb75da492ca728be4ec02e6b26215f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58316801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd29b707ae5017f89902cc983ac3d306645b993949f7be309966e0d090f6c2cf`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7d30cb32011e8774fffc1bae3028511198f570559b90c022e3000e16e890a9`  
		Last Modified: Tue, 14 May 2024 02:02:20 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74da030be7dc2af880d9b7742205a818f37dfc3ddaa72f47a9add1c80fc5bdf9`  
		Last Modified: Tue, 14 May 2024 02:02:21 GMT  
		Size: 25.9 MB (25892492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13f35c442f14698d2de1268bffd82c58a2b4a2fe87558fd12f932bcc0983bd0`  
		Last Modified: Tue, 14 May 2024 02:02:20 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ff6f01c536d6cfb7caf4d64f7a2519085000be27a6df14a1058a7dea1edde8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3933748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7fd8d7bd9748e6c0f5035ca2805e977161396b23dd70c195400234f610b793`

```dockerfile
```

-	Layers:
	-	`sha256:41aed24da63b4a77dee6d197fb05aed3de2090624a33a2d9d0eebe27ccd763b8`  
		Last Modified: Tue, 14 May 2024 02:02:20 GMT  
		Size: 3.9 MB (3917268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e392658953244dad9e94c8b2c60225577204dc455adb07d3eb203b5d753fbf7`  
		Last Modified: Tue, 14 May 2024 02:02:20 GMT  
		Size: 16.5 KB (16480 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:5678191f31675fe306da8b1ab38dfdb68eb6c6fd6dd88597b0e2014390b123e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52989197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb6d0945d0513f33cdada6c2391e3c1921b219f04c5ff813946238d6592af24`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:87680940dfe26d5f4583964a639405d4e00c6a3f72863f7b7e18eca764a73c67 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:2d257022fa7c7f0c7879f59891b7e4277d67c9114b820f229207724d5e65d6cf`  
		Last Modified: Wed, 24 Apr 2024 03:26:43 GMT  
		Size: 29.7 MB (29652163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8258e1beb6e34ba884858fde8477e0ad3e23cd988398244bd20ec2cd663857`  
		Last Modified: Thu, 25 Apr 2024 02:44:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ff68f276f3d1d0034a7ab019d9c5e9c6006616dc093455ae962ceb74d10a74`  
		Last Modified: Thu, 25 Apr 2024 04:37:48 GMT  
		Size: 23.3 MB (23336766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f69ab49a494dd0353630e99720af5077797c995ad6a43c3d15ab5c9b4aeb34`  
		Last Modified: Thu, 25 Apr 2024 04:37:44 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:35d4bd3edb1ace1270af74c06a0a16c8de20c8e385a6945513f06ecbd115c87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 KB (16194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca813c6ff29746c7c270058a64ef698923a405a8683416a8d5caf16104c5fcb`

```dockerfile
```

-	Layers:
	-	`sha256:f731e5f84798f241dd38be2a60c1aadd9f2bf15b5e38f2b068b23e6f0cf9b036`  
		Last Modified: Thu, 25 Apr 2024 04:37:44 GMT  
		Size: 16.2 KB (16194 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:26c8fd86fdc21c919092138e022dc831fe175f85e66af02c7301146bbd204848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60028188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe23a95930167e7bcf4655ba3c6763aa706e668d2e7b54ca057f93819e3b6693`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cf0bdb960b363821547c618b640d1b7844769c456af185e7f75402d45bbbd8`  
		Last Modified: Tue, 14 May 2024 14:02:01 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4b122f4976334499fb7300a1b9d332b066addccaba15d40b748ef36271177c`  
		Last Modified: Tue, 14 May 2024 14:26:15 GMT  
		Size: 24.7 MB (24716764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8c017f1e9c132ae5320f9fc457adf2318fe575063fbeb3a7ce5360d64b3b9a`  
		Last Modified: Tue, 14 May 2024 14:26:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:96fe64fda81a20820bdfe6076af739384ba5f4d51c5ade8e7b264b81c34a5642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a7f6c66ac952f6148918a38e8bbd4cf45e427db3daf6f346bc04dca04d73b3`

```dockerfile
```

-	Layers:
	-	`sha256:cd0df8e6947e1fe587ca3804ac655a42f69e3122553aa5f9521fd6f684d6b299`  
		Last Modified: Tue, 14 May 2024 14:26:15 GMT  
		Size: 3.9 MB (3901784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9e0d864b90e47f4002bb29a7d815bba1c8dc3bcdc26d7490a9c7c4513403b18`  
		Last Modified: Tue, 14 May 2024 14:26:14 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:ddc0e1616cc70357c698e710423b4b1426e8851d1420636555add3f7a50ee485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53322016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72892346e1cc5677bd30ee5f68ced11908f6b0c27e117558c53d8291b5080ff6`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:acaea4e054f1ab7ae5cbc8f02c73b546c367aebfcc48c7fb4f0dd9f3628bc25e in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:6f588995519e0e04ef4c150b91ad96c3c85667869db0ad72e5a78d4fab796e70`  
		Last Modified: Wed, 24 Apr 2024 03:49:47 GMT  
		Size: 29.7 MB (29673934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9a80240e29f2e5d48455f7f7ec669e99c757751c116b1b2b87ff5933d6b0e1`  
		Last Modified: Thu, 25 Apr 2024 03:25:05 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84dc68e914b1c88e4c796efdb320aecd51ca7c62ed93dfbfa300212e59cbfd7b`  
		Last Modified: Thu, 25 Apr 2024 04:12:07 GMT  
		Size: 23.6 MB (23647818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3135c8769619c479c51c4c8d433945500ecfe59eb617900e8fa833a0e4e2a1cc`  
		Last Modified: Thu, 25 Apr 2024 04:12:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:9d60b2930a54585de355ca276cbd731100d64390fc8798f704495b06b523f5fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ac2ed504be97b965036e1ceb4b6570f48dfefc0462ba4269b6fd563d0300b9`

```dockerfile
```

-	Layers:
	-	`sha256:f0b1e05a43bb32a53fe04cc337604aff9da2f7fffeabf8b7dbe060fd890f8e48`  
		Last Modified: Thu, 25 Apr 2024 04:12:07 GMT  
		Size: 3.9 MB (3901709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b30f78cd622029b6bbecc1da217426264122c06d047b88a1af7f05e96982f5d`  
		Last Modified: Thu, 25 Apr 2024 04:12:07 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json
