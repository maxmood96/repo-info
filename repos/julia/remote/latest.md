## `julia:latest`

```console
$ docker pull julia@sha256:b01c9019855f2d9985d1d2eb4757514268be94891d90a5e1ad55c17908c18ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	windows version 10.0.20348.288; amd64
	-	windows version 10.0.17763.2237; amd64
	-	windows version 10.0.14393.4704; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:c38b3ce216b01d16bd1a1592392a8e024336859a7f8257b0dbf0a2e44177dcbe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153329374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8cdc51824337548d42fe66c55ec5d8957d563d9212eeadddc594b680c9fd28`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 09:51:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 09:51:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 12 Oct 2021 09:51:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 09:51:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 12 Oct 2021 09:52:27 GMT
ENV JULIA_VERSION=1.6.3
# Tue, 12 Oct 2021 09:52:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='c7459c334cd7c3e4a297baf52535937c6bad640e60882f9201a73bab9394314b' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='7cf08affbad206bd3c1ef8bc117bf0aa6ac95d1666bf4c06f9d530cff29b2067' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='df1a7e96f83b60fda54fd14713a373e37ac2d80fd11dbd708a77c8a22ab86e25' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='06e3d64813e4ba6019d8d79e918c48af4943700bd1eb689c481d82a64f8c280a' ;; 		ppc64el) tarArch='ppc64le'; dirArch='ppc64le'; sha256='a3cb6f58ee93bbd3bd72ecd45b9f37bf5e16e9c0ef30ba17c809ec7cbb84ee96' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 12 Oct 2021 09:52:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b8d869efaeb262f8cb654a2f48a3e342f88a5126dbb642f03e1a8bc2eb5dd1`  
		Last Modified: Tue, 12 Oct 2021 09:54:30 GMT  
		Size: 4.5 MB (4458487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bb6b59a0738627b87ccdf2470ea804c964349d3ed88380b5acb7ec3ce7776c`  
		Last Modified: Tue, 12 Oct 2021 09:55:29 GMT  
		Size: 121.7 MB (121731377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; arm variant v7

```console
$ docker pull julia@sha256:3c6a1d0af384f115d1889391c36df2f72f91b68399dac31b2728843f8ab6b782
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139347770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41946159713d6c99bda729d54dfd0830330ca603cc74b0c57f8d62a92ddcfacb`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:42 GMT
ADD file:fe1eaa1b1d760b3d250cb4ac331d26a261fc569f1694bd34e146f00874dc87e5 in / 
# Tue, 12 Oct 2021 01:29:43 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:22:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 12 Oct 2021 18:22:50 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 18:22:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 12 Oct 2021 18:23:57 GMT
ENV JULIA_VERSION=1.6.3
# Tue, 12 Oct 2021 18:24:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='c7459c334cd7c3e4a297baf52535937c6bad640e60882f9201a73bab9394314b' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='7cf08affbad206bd3c1ef8bc117bf0aa6ac95d1666bf4c06f9d530cff29b2067' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='df1a7e96f83b60fda54fd14713a373e37ac2d80fd11dbd708a77c8a22ab86e25' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='06e3d64813e4ba6019d8d79e918c48af4943700bd1eb689c481d82a64f8c280a' ;; 		ppc64el) tarArch='ppc64le'; dirArch='ppc64le'; sha256='a3cb6f58ee93bbd3bd72ecd45b9f37bf5e16e9c0ef30ba17c809ec7cbb84ee96' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 12 Oct 2021 18:24:45 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c0b5ba470cac8cfdae4633f5cddb3ba9350fe1d1b1507c4965a8224eb40e52c5`  
		Last Modified: Tue, 12 Oct 2021 01:45:52 GMT  
		Size: 22.7 MB (22739698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7094c2acb6418732c3212eda7f35443fe5b5879771194a48414da83badb9959`  
		Last Modified: Tue, 12 Oct 2021 18:28:48 GMT  
		Size: 3.8 MB (3806072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d07760a0aab18b5f5ee1ac473b6eaad4642c28d3b870decb63abfe61eae4a72`  
		Last Modified: Tue, 12 Oct 2021 18:31:13 GMT  
		Size: 112.8 MB (112802000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:cfe940b8915c4afa8822031db4dfe29f8b60cd72badd61fc615b547d2fdbc4ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145624462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24de6df4af202194f314a5536cb29300d095456ca8962ac5526e55ca054cb0e3`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:42 GMT
ADD file:f0d53027a7ba594477674127971aa477af3a2bc6bcddef6c0aa174953a5f2db0 in / 
# Tue, 12 Oct 2021 01:41:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 04:19:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 04:19:44 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 12 Oct 2021 04:19:44 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 04:19:45 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 12 Oct 2021 04:20:10 GMT
ENV JULIA_VERSION=1.6.3
# Tue, 12 Oct 2021 04:20:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='c7459c334cd7c3e4a297baf52535937c6bad640e60882f9201a73bab9394314b' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='7cf08affbad206bd3c1ef8bc117bf0aa6ac95d1666bf4c06f9d530cff29b2067' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='df1a7e96f83b60fda54fd14713a373e37ac2d80fd11dbd708a77c8a22ab86e25' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='06e3d64813e4ba6019d8d79e918c48af4943700bd1eb689c481d82a64f8c280a' ;; 		ppc64el) tarArch='ppc64le'; dirArch='ppc64le'; sha256='a3cb6f58ee93bbd3bd72ecd45b9f37bf5e16e9c0ef30ba17c809ec7cbb84ee96' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 12 Oct 2021 04:20:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:02b45931a436a68cadb742684148ed6aacbbf9aa21447b467c11bac97f92eb46`  
		Last Modified: Tue, 12 Oct 2021 01:49:07 GMT  
		Size: 25.9 MB (25908479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646da9ef0bea55352cd8492ddeadb7330f6a23e081ae88e466bdab3e0e391d50`  
		Last Modified: Tue, 12 Oct 2021 04:22:07 GMT  
		Size: 4.3 MB (4339015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4274d68a8f49282ca915ac3129aa6dd1a056ec009daffd7c4bab424ed7848f`  
		Last Modified: Tue, 12 Oct 2021 04:23:05 GMT  
		Size: 115.4 MB (115376968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:79f57ec489f4bdbe37cd7f5494f617379bb25b7fda9521e00de035517b85e013
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151745863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db891f22ad270fb2f05d1c9ad7727e2cb9e8a311cb32983ca55e8e36167aa191`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Oct 2021 01:40:17 GMT
ADD file:1b432d2306b487c59442b30c65ddabd08b45484c6ce09b0c25112c29f4a98f17 in / 
# Tue, 12 Oct 2021 01:40:17 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:13:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 02:13:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 12 Oct 2021 02:13:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 02:13:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 12 Oct 2021 02:13:57 GMT
ENV JULIA_VERSION=1.6.3
# Tue, 12 Oct 2021 02:14:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='c7459c334cd7c3e4a297baf52535937c6bad640e60882f9201a73bab9394314b' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='7cf08affbad206bd3c1ef8bc117bf0aa6ac95d1666bf4c06f9d530cff29b2067' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='df1a7e96f83b60fda54fd14713a373e37ac2d80fd11dbd708a77c8a22ab86e25' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='06e3d64813e4ba6019d8d79e918c48af4943700bd1eb689c481d82a64f8c280a' ;; 		ppc64el) tarArch='ppc64le'; dirArch='ppc64le'; sha256='a3cb6f58ee93bbd3bd72ecd45b9f37bf5e16e9c0ef30ba17c809ec7cbb84ee96' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 12 Oct 2021 02:14:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860d012fe46ce39c3737ace24d10d8ad65ae9c78abde6891ca6e97b0d7f271dd`  
		Last Modified: Tue, 12 Oct 2021 01:48:37 GMT  
		Size: 27.8 MB (27791445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3aaa4cbcacabf22501ccde8b2540b8dce4fa9b5722ee82168c66a8855a4c63`  
		Last Modified: Tue, 12 Oct 2021 02:16:38 GMT  
		Size: 4.6 MB (4610944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd66857956c78239cadcd50382f16705950ad5091c6ffa9cd11f7f41b32cf41`  
		Last Modified: Tue, 12 Oct 2021 02:18:01 GMT  
		Size: 119.3 MB (119343474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:edefd1e21ac467bc6f0456c9ece7f5a3598d9095a71c38908613a8a78f164802
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142396250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f33d199503119b17096a792af8f45d9969eca45022213d2e03e2ba29f776eb4`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 06:51:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 06:51:06 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 12 Oct 2021 06:51:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 06:51:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 12 Oct 2021 06:53:18 GMT
ENV JULIA_VERSION=1.6.3
# Tue, 12 Oct 2021 06:54:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='c7459c334cd7c3e4a297baf52535937c6bad640e60882f9201a73bab9394314b' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='7cf08affbad206bd3c1ef8bc117bf0aa6ac95d1666bf4c06f9d530cff29b2067' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='df1a7e96f83b60fda54fd14713a373e37ac2d80fd11dbd708a77c8a22ab86e25' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='06e3d64813e4ba6019d8d79e918c48af4943700bd1eb689c481d82a64f8c280a' ;; 		ppc64el) tarArch='ppc64le'; dirArch='ppc64le'; sha256='a3cb6f58ee93bbd3bd72ecd45b9f37bf5e16e9c0ef30ba17c809ec7cbb84ee96' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 12 Oct 2021 06:54:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6651b20c67f0204f1988da03e511f991ac21eeb0e84729f4676ef4984a7a6a3`  
		Last Modified: Tue, 12 Oct 2021 06:55:24 GMT  
		Size: 4.9 MB (4854320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422b813f1dcebc61860511e8c537ff6736ea1240878ed86921274fca19f8ae40`  
		Last Modified: Tue, 12 Oct 2021 06:56:22 GMT  
		Size: 107.0 MB (106994733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.288; amd64

```console
$ docker pull julia@sha256:429dbec3f353aa0015b323903dae262654ca919c91e743b070ff3b6f7bd2f1bd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2275759271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428ce259549ff6b45f0cd4c395f3c4207781b1be9a0a2fabdd4af7641bdd3b5c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 07 Oct 2021 11:33:56 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Oct 2021 12:26:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Oct 2021 17:01:04 GMT
ENV JULIA_VERSION=1.6.3
# Wed, 13 Oct 2021 17:01:05 GMT
ENV JULIA_SHA256=bc43b8729dd2d95d9d148ada989c8582a66e99af89fcc91d8ed41ee2f13a9985
# Wed, 13 Oct 2021 17:02:35 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 Oct 2021 17:02:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b03bbc71f9254a4ad2fba472595c859655b9d0cfefa638928416e277e0f0d497`  
		Size: 889.8 MB (889767519 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b201e45e5b11128e36517715f5b6ae98e5782737c1b112a5fae2aa83206f57bf`  
		Last Modified: Wed, 13 Oct 2021 13:23:57 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0f2508b4403e3b825eccab264714d98868d14ead98ed64fa473950bd27c21a`  
		Last Modified: Wed, 13 Oct 2021 17:17:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef78310b0d62a04f354b13562fe02e17f8b8387529a0965de157b191d5c1bd7`  
		Last Modified: Wed, 13 Oct 2021 17:17:15 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e500eb1f16011787148ddc42f641e0348ee8d41ac64b69514e2003454467e223`  
		Last Modified: Wed, 13 Oct 2021 17:17:48 GMT  
		Size: 134.3 MB (134287044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1cbfa5f501386dba18ee172c5f65308b3e5a9fca4f4ff549c0f5c30e898cfa`  
		Last Modified: Wed, 13 Oct 2021 17:17:15 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.2237; amd64

```console
$ docker pull julia@sha256:6baae7ada462711a86e181a26e126a2613e3e97ea93bc806c60bd0d16b6e83c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2820353444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cff4c0268872308f6366ac995eb6f55c862276d78e022ebeeacb2fafb6e96f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Oct 2021 17:02:46 GMT
ENV JULIA_VERSION=1.6.3
# Wed, 13 Oct 2021 17:02:47 GMT
ENV JULIA_SHA256=bc43b8729dd2d95d9d148ada989c8582a66e99af89fcc91d8ed41ee2f13a9985
# Wed, 13 Oct 2021 17:05:06 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 Oct 2021 17:05:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd51bcd895c539022738cf9b6924cf7c236ee23f22a7efe65827578f2f079fac`  
		Last Modified: Wed, 13 Oct 2021 17:18:02 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7c3f1c74a4c79c09a2e9a335f2bb9c5cf6b5a00abe376253ba253c9eeb4626`  
		Last Modified: Wed, 13 Oct 2021 17:18:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84630d8b1d8eec7b24be6999aa12009e5635dd00cebc2460bf6231367e9bc647`  
		Last Modified: Wed, 13 Oct 2021 17:18:35 GMT  
		Size: 134.0 MB (134028960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61c25cd57b68537aca1150e15428619025cc10454c4c6003cbb352c6d42e952`  
		Last Modified: Wed, 13 Oct 2021 17:18:02 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.14393.4704; amd64

```console
$ docker pull julia@sha256:179dbb071e4741ae3d51d11964a71d7736625f29d9acc42d3fb48c088c967110
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6406796921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c320aafdabbfbd33e6fc514b07df8f70cd399586fea1779887441782c19b90d8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 06 Oct 2021 21:16:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Oct 2021 12:40:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Oct 2021 17:05:15 GMT
ENV JULIA_VERSION=1.6.3
# Wed, 13 Oct 2021 17:05:16 GMT
ENV JULIA_SHA256=bc43b8729dd2d95d9d148ada989c8582a66e99af89fcc91d8ed41ee2f13a9985
# Wed, 13 Oct 2021 17:07:50 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 Oct 2021 17:07:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0c776a8e8e3c02d360995b7fa26a3fd7c0928965795fac57b69ff07418ab07bf`  
		Size: 2.2 GB (2202780626 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6974b1bd85ba3f9ce16d86231eced43f720fed9c13411d37584dfe7193bcde60`  
		Last Modified: Wed, 13 Oct 2021 13:27:57 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f3b780f6240c0128e9cfe3aea4a775b7ec0feeaddadf84d05febcc6701d4e3`  
		Last Modified: Wed, 13 Oct 2021 17:18:49 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ec36f3fa617309164c7252677b853529b268fab5c194663a56ef3f03d9744d`  
		Last Modified: Wed, 13 Oct 2021 17:18:49 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8359e8a573606f94acf4b5a2751d5f4709523720a4f6d19ac1fe6718e5549e7e`  
		Last Modified: Wed, 13 Oct 2021 17:19:21 GMT  
		Size: 134.0 MB (134024858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d56a85971301d7c2b025ff67e9066cda696a6327bf5953200eee9ac4706e3a5`  
		Last Modified: Wed, 13 Oct 2021 17:18:49 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
