## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:f2fdfd7aa0c27e394334b570669898f4fa91bb65c0a2f3489fbef3567927d66a
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
$ docker pull perl@sha256:e777944bd866dd32576b523849e1d0f1f28b48a6f13e663ed004f5800c6b80d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56227333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bfc146132ea52ca5379d813b057e199016556a590e5e9f9ed8bfceac2bd301`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbde0c8cf4d4351f93d69f6a5fa674249566de83d7cde918282ded178bd7d97`  
		Last Modified: Tue, 12 Mar 2024 02:06:38 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05648fe5f863fd72a581d95ac5c8f633f70ab9c03e0b714d305455e838c5414e`  
		Last Modified: Tue, 12 Mar 2024 02:06:39 GMT  
		Size: 24.8 MB (24804577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d41b4a276f4fd20216c477fb03c5b3df1f99dce4ac7512509346392c9d93be9`  
		Last Modified: Tue, 12 Mar 2024 02:06:38 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:8c908486d7bb49f58048d0947615f86b9e96da5a6937a731600439fce2836443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43983026600c0cd32c1d1b7b44259e8be8e97a5885949f9a0e9610156ecd7387`

```dockerfile
```

-	Layers:
	-	`sha256:13110ca590ed8a2f7a59fc903b4fce90731002484d845a47287a7f4d3c53c7ea`  
		Last Modified: Tue, 12 Mar 2024 02:06:38 GMT  
		Size: 3.9 MB (3912135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd7348e44a2334cafa7c088ea6c0d401d88a153e9e75719f99e98f862a075626`  
		Last Modified: Tue, 12 Mar 2024 02:06:38 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:9ec3a729249591d1aa4588ac5687ba511af3a1b94f3e81ecfe3981d19aab9e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51733260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b34bfb5f161990071eeae34d685c2df922fa35041f9883f465ac85adb865aa`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:90e7b77db704f73ce102dcbc0f6cbe5d778409a08ca0d29224ab736a76537669 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:5f50de7913c8d45142222ead3575799095853dd5af08b7c42fe0f070c5947afc`  
		Last Modified: Tue, 12 Mar 2024 00:52:28 GMT  
		Size: 28.9 MB (28924563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b670589f0af3f19325dffd077f65c60d3960566a2b323cde63e6991d391a149`  
		Last Modified: Tue, 12 Mar 2024 15:35:45 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c6dc9eb01597e9655a6978d22911aef5dd1c14d5baaa0ee37f443b88431588`  
		Last Modified: Tue, 12 Mar 2024 17:55:29 GMT  
		Size: 22.8 MB (22808429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcb70752b4c87e8ef4e43d8dda1ea3277c886c78ba2d7107f62c811bf39844e`  
		Last Modified: Tue, 12 Mar 2024 17:55:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b9e9da737a6b5de4f69c60cc355f5fb47af92da141c8df614329395ae7bb62dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3899049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15133b67eb86427d5a3e4386a76b98bbd9662d684c75d7d1eb5769129771b579`

```dockerfile
```

-	Layers:
	-	`sha256:7e0a60ca988706635c20c83999a41391841ee22c164e62ddc6d831cfc70f8ba8`  
		Last Modified: Tue, 12 Mar 2024 17:55:29 GMT  
		Size: 3.9 MB (3883334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e2f83b4d5dafa7e36a088356fc99b895336d7af9149a3d2ba0a080ff25992da`  
		Last Modified: Tue, 12 Mar 2024 17:55:28 GMT  
		Size: 15.7 KB (15715 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:90f2040977ae12844553c3472d58ba26632b5a1123dbfc2ec4ae5550a65cea17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48800665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1117c8b87c20968c4daa7371ce17382372e02991ced354a9cc5edb91eb30644c`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:f0436b046c7a5f796efae4d2d2be5a99ad212807e4aa49fc8cc372a4c4c8c4b0 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:5b16029f28c496dabb357a7310d24f957046a925411ccd44eca962c03f85e38e`  
		Last Modified: Tue, 12 Mar 2024 01:04:23 GMT  
		Size: 26.6 MB (26582714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475c25e9dac719893224a1cd5c8dc1762f32d0d860b64613e5a47f29710b6baf`  
		Last Modified: Wed, 13 Mar 2024 01:25:53 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3a686f4620a31ad7c0f3997a773d225b2472168cb2c3f305cd7b78a3e7f188`  
		Last Modified: Wed, 13 Mar 2024 05:05:49 GMT  
		Size: 22.2 MB (22217683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb8f30bf56285cde39edd1215cbca893e560547dd58b9e2c80becc900c2b8ca`  
		Last Modified: Wed, 13 Mar 2024 05:05:48 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:3179de8d7438f7429ecdb3b429b94e1419f52e2162af7895f9af6e3a9a1a2a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3901767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85047352df4aab23f6b67ce49b27c69edb3b26e7effa1c295a41ec79a2b67bce`

```dockerfile
```

-	Layers:
	-	`sha256:32e07ab65ff28ea2900e0c62e9e18087a329b7e4b83e903bb7ba3c166ef23f4e`  
		Last Modified: Wed, 13 Mar 2024 05:05:49 GMT  
		Size: 3.9 MB (3886052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7046068a611aefb906ca798d1ef1a8c189147eedb0bd80792268e1d5eb70e99f`  
		Last Modified: Wed, 13 Mar 2024 05:05:48 GMT  
		Size: 15.7 KB (15715 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:d7b09b3f7ea3db7e7d3c34955f2c08d0a92039375dfe5694c29cc6f2441ee931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54010396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4149a70508b882be781645f340f74c541e3a8dc6580cdead0904df837bd2b332`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96543ff7344cb637d3f3562c307cf897cbc222515d013ea586c43ea451f17a55`  
		Last Modified: Tue, 12 Mar 2024 23:07:19 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896030a35a32539f823fb1782b37d7e3816558e13dc18f51711a85277ca81978`  
		Last Modified: Wed, 13 Mar 2024 03:09:54 GMT  
		Size: 23.9 MB (23939011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43298040e0c7b83d56ca6a9dc5cb568a0ef75f9a4f9f65434a681722126b9ee8`  
		Last Modified: Wed, 13 Mar 2024 03:09:53 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:805d83a31415efede28f43f014e7b9ffb9f70c7c3a7dd45f034c5940da4a4460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3902113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea65d34ff1ab5f4e25cfaae6bcf18b669ae7f61527802f542ce8ae19e52e422a`

```dockerfile
```

-	Layers:
	-	`sha256:994d25f6dce8ed81dcf6cb6ba6dc40022bac195473fd1fe7fba8e20756f541ac`  
		Last Modified: Wed, 13 Mar 2024 03:09:53 GMT  
		Size: 3.9 MB (3886451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e899cbb90858f747d38ecccdc24c063a48072a1291cd38ae5ae06ebde133e33`  
		Last Modified: Wed, 13 Mar 2024 03:09:52 GMT  
		Size: 15.7 KB (15662 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:6953a8be9fbc6447c388c37d886456c642389604e875b9f921bddfe001e7587f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58636190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdcfa29c4fab2984040af08b97132d1c617431bb25841f865afe1282e9bad17`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:515cf6a96eea91239bc61e64b973eb555a9299d1053e3c6cb694d8bafa627086 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:4276507bfa4980b432cd9334306e3335cf1bbc8e6dea45aad2ae9ec091223f03`  
		Last Modified: Tue, 12 Mar 2024 01:03:30 GMT  
		Size: 32.4 MB (32407589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a220ecf8a32c1d40994c53331dbb94f511209f0a682688552b34666eeed13a`  
		Last Modified: Tue, 12 Mar 2024 02:07:00 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125b30c45a1e25e283de6f20093f09696f56cee9bd9116b0f3c41e5bc3ab13b6`  
		Last Modified: Tue, 12 Mar 2024 02:07:01 GMT  
		Size: 26.2 MB (26228333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18892533fa5e6d3d08c078e3957697928a71cdfb7a48f5cb4b6ec54b8f4b36e7`  
		Last Modified: Tue, 12 Mar 2024 02:07:00 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:a110902b31c1c44e406ecbcd937891dddf11ecb6084fe06f37a0eac21bf272f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a4916bd6df62fec131c40db27dbe25a75f252a30d02b9554735c41bf97eed9`

```dockerfile
```

-	Layers:
	-	`sha256:f529bf06d5d7f69bc3897af4141adfe979baafc5b80f298fcefffde5e336cdfb`  
		Last Modified: Tue, 12 Mar 2024 02:07:00 GMT  
		Size: 3.9 MB (3916398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:040c2f2f3f21a99affbbb84874cfc888aeb6b80bb9671fd506ad4a5e86ed8a1e`  
		Last Modified: Tue, 12 Mar 2024 02:07:00 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:a1ea3e62c66fcb364646c706329d7b3e0d873b76f9307b21855e81676a6d4091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53341575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c7829e5c791b433f43dab6d5411acae6f02685a255c179b515cb59766304d7`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:a42bb6c1ce6dd3579b82e6f04b91787c20ac276a10c0bc36d42b2b260789343b in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:ade123ee9f81df730fd8edfcb3e77a2032d0f4380f0cb466cccda650f64f9560`  
		Last Modified: Tue, 12 Mar 2024 01:18:36 GMT  
		Size: 29.6 MB (29640502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f6117b377a412f78d6343911ec533a23e82b770b04947782a3da9f6175317d`  
		Last Modified: Wed, 13 Mar 2024 05:05:10 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b10038ea818a6ef43f90d4626a49afd5ea066adcdd046a74db4c5b9a8c8944`  
		Last Modified: Wed, 13 Mar 2024 14:07:47 GMT  
		Size: 23.7 MB (23700804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b877276717a332e150c144a0c8cb3f98d44a29e072bcaf47aeef699d126b333`  
		Last Modified: Wed, 13 Mar 2024 14:07:44 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:2a38139e7fddddf60be4f48db6ce7753c4bfde94c5d7326905f33b9fa4db7294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3e27937089e4cb17ef1bb4ab131cfe1db455e3d4f24460c5e18eb94f90bb1b`

```dockerfile
```

-	Layers:
	-	`sha256:c1d2333e348a83f87b699537ba74f9eea6282c586ed8d60e8d52b4d308466398`  
		Last Modified: Wed, 13 Mar 2024 14:07:44 GMT  
		Size: 15.5 KB (15487 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:491a57dceb1bdc943304a2c30ff3adc9a33b9bc855c06e5676c4ad3151b22b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60346202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb22e4b5fe8a23a1ba3debc2d0eacf7970f5a9e9da7bcfe8d089130550459d7b`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a7e7152ecf714cde62c8fd8e3ba92f1a840753d61e7dfc0d5e581ebdc5174b`  
		Last Modified: Wed, 13 Mar 2024 03:06:31 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55cbcfa0be61d270a65ff0a36c5fa42673d282d034fa60ad4317c65216809b0`  
		Last Modified: Wed, 13 Mar 2024 05:44:42 GMT  
		Size: 25.0 MB (25047927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec21a6101497bb232f69aad0aef448f4b5686a3b4cbe7c266d67eb816653eea1`  
		Last Modified: Wed, 13 Mar 2024 05:44:40 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:0da869a72b73bd8aaf58295addb90a2cc13e6d8f978cd8ff1c2d43db37701324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f47f3b9f5f857362246c8571ea971e2cab27efc5ffb448ba86ead912775501`

```dockerfile
```

-	Layers:
	-	`sha256:4c6c6447249e42a9b53e39b392c88d925573362c4a22cfd52b4fec8dbb9e880d`  
		Last Modified: Wed, 13 Mar 2024 05:44:41 GMT  
		Size: 3.9 MB (3900892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a6c30d9732f86f073844d341023e3df8c938f42dba309997d91066adc84947b`  
		Last Modified: Wed, 13 Mar 2024 05:44:40 GMT  
		Size: 15.7 KB (15686 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:35e547d9a31bf0841276f073c2e1c3018d359841c305b7d1b9bf77efff1f1d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53677221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8fc17d5e7c9f5234315b07fffb9d4f1856324bef90d9e322f1b6823e05de52`
-	Default Command: `["perl5.39.8","-de0"]`

```dockerfile
# Tue, 13 Feb 2024 01:06:13 GMT
ADD file:08d247ddc5feae7a34870daaf7096c41de9c1bb9fc04bc305db02fe94b34d2e5 in / 
# Tue, 13 Feb 2024 01:06:15 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/R/RE/RENEEB/perl-5.39.8.tar.gz -o perl-5.39.8.tar.gz     && echo '25f8b4db7a7d91c051b1c2594ed83c291c74c1012da559a8d580755b598bb7e3 *perl-5.39.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.8.tar.gz -C /usr/src/perl     && rm perl-5.39.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.39.8" "-de0"]
```

-	Layers:
	-	`sha256:2ac5fae051fa0d97737a12baa9ac705d62ae16e9a4ae39eed54e3f977616ce05`  
		Last Modified: Tue, 13 Feb 2024 01:30:53 GMT  
		Size: 29.7 MB (29660168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75e6830cf0f38e67c061f6b41fa477c04816afb6ab159f3556c578338b09356`  
		Last Modified: Thu, 15 Feb 2024 06:59:02 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b23f828cfba71107163cb191a73fe472b8808ef6fac5e19655e9c0312d84818`  
		Last Modified: Fri, 23 Feb 2024 19:34:07 GMT  
		Size: 24.0 MB (24016786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91969123ab4069140f30e02a49e99a7101f44d25fe176d81428d2194c0763ad9`  
		Last Modified: Fri, 23 Feb 2024 19:34:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:74f31983eaf179523d4057bcbe1ea2dc105c22c3be87cc8978cf20e3f1e81d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f62e40d7c5584d1301d9761cf8f3283be87ec25b1aee9a82f451e0124b77189`

```dockerfile
```

-	Layers:
	-	`sha256:895445d7a519036db7496a2845d3882bd881a5560c5a8d03ca5ecf7c68b9520b`  
		Last Modified: Fri, 23 Feb 2024 19:34:07 GMT  
		Size: 3.9 MB (3900839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae30044b6ee4f54ee76ed25fa68728e58861b82c08f4096b70d197d550483400`  
		Last Modified: Fri, 23 Feb 2024 19:34:07 GMT  
		Size: 15.7 KB (15654 bytes)  
		MIME: application/vnd.in-toto+json
