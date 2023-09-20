## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:c32250c63a24e054f3dbb99638b4671e750c4b51d62a1910e2d1feb3e9ad4e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `julia:rc-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:aced9497b48df48cffd39a2285799c8f755e5b463aa5f0706c32e2fe8b2c0e9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203525925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7e53e1793735b3ca2edfd2909e95f115d2a39b37daacee9b3c4657b4bd0981`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 06:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 06:00:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 20 Sep 2023 06:00:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 06:00:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 20 Sep 2023 06:00:30 GMT
ENV JULIA_VERSION=1.10.0-beta2
# Wed, 20 Sep 2023 06:00:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-beta2-linux-x86_64.tar.gz'; 			sha256='f1a17f5a52980c167416cbe4eda14419d818f3b76985401154a3a567879d6477'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-beta2-linux-aarch64.tar.gz'; 			sha256='38e7c07a0c3f124497da62d81dc6bf58dbce8a6a3f0542ba52aaac54ed238351'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-beta2-linux-i686.tar.gz'; 			sha256='adc781af2ee5981988f0551672170b1610c4af1262495f4ecf19602da0ed579f'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-beta2-linux-ppc64le.tar.gz'; 			sha256='4b51efbdfe958e754f982c618825cd95b5c3421da3486ef8bc4c83b90270e06c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 20 Sep 2023 06:00:49 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Wed, 20 Sep 2023 06:00:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Sep 2023 06:00:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367fb88c49f7b83d4855d02c927645b5ca3e4d7c865455789eeb0b0cd5ea70b5`  
		Last Modified: Wed, 20 Sep 2023 06:03:44 GMT  
		Size: 2.4 MB (2426728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b9ad6045ef520ed3889a78ffc336f431101f362f6309c914c54f0718bf3e1`  
		Last Modified: Wed, 20 Sep 2023 06:04:09 GMT  
		Size: 169.7 MB (169681113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13fdee11f78619bb562eee6457bb1521050a9384457d1aee5d5da0280711316`  
		Last Modified: Wed, 20 Sep 2023 06:03:44 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:265ece3ed26da64af0ec48a2b5f75b69ddea1b2cf96b84878826f3046bbecaa6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196589929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad479ce48d2dd39d98d2d76e852893b3d7a7cef0fbe980605fe2c5d0480b2066`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 12:09:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 12:09:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 20 Sep 2023 12:09:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 12:09:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 20 Sep 2023 12:09:03 GMT
ENV JULIA_VERSION=1.10.0-beta2
# Wed, 20 Sep 2023 12:09:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-beta2-linux-x86_64.tar.gz'; 			sha256='f1a17f5a52980c167416cbe4eda14419d818f3b76985401154a3a567879d6477'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-beta2-linux-aarch64.tar.gz'; 			sha256='38e7c07a0c3f124497da62d81dc6bf58dbce8a6a3f0542ba52aaac54ed238351'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-beta2-linux-i686.tar.gz'; 			sha256='adc781af2ee5981988f0551672170b1610c4af1262495f4ecf19602da0ed579f'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-beta2-linux-ppc64le.tar.gz'; 			sha256='4b51efbdfe958e754f982c618825cd95b5c3421da3486ef8bc4c83b90270e06c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 20 Sep 2023 12:09:22 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Wed, 20 Sep 2023 12:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Sep 2023 12:09:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a79191cd5b087ed753f4773aa313f183a381a7b7327a871244596bee4bfa725`  
		Last Modified: Wed, 20 Sep 2023 12:11:52 GMT  
		Size: 2.4 MB (2414375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bfe436fac5a3c08d995cf6b29ccc25528ad4e0c1a36112f40d8db039d0f070`  
		Last Modified: Wed, 20 Sep 2023 12:12:11 GMT  
		Size: 164.1 MB (164112313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e37296d19dbc8b99efda9e715a4ffe342dde90959a1c4e8727486cc762936a`  
		Last Modified: Wed, 20 Sep 2023 12:11:52 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:5a7fb9e282f23bac8df827377960224dabc816d77c1b945cc906a5cdc260ce57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191006875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018cfd657b81388e50e6472be0559dc0cbfb820f3da23d5369737f67127ceb2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 20 Sep 2023 00:42:18 GMT
ADD file:51db29acb4893b446fcf8a93f7fa809201b49d6ea62a009ab14002cafd3ac4a8 in / 
# Wed, 20 Sep 2023 00:42:18 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:13:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:13:08 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 20 Sep 2023 15:13:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 15:13:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 20 Sep 2023 15:13:08 GMT
ENV JULIA_VERSION=1.10.0-beta2
# Wed, 20 Sep 2023 15:13:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-beta2-linux-x86_64.tar.gz'; 			sha256='f1a17f5a52980c167416cbe4eda14419d818f3b76985401154a3a567879d6477'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-beta2-linux-aarch64.tar.gz'; 			sha256='38e7c07a0c3f124497da62d81dc6bf58dbce8a6a3f0542ba52aaac54ed238351'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-beta2-linux-i686.tar.gz'; 			sha256='adc781af2ee5981988f0551672170b1610c4af1262495f4ecf19602da0ed579f'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-beta2-linux-ppc64le.tar.gz'; 			sha256='4b51efbdfe958e754f982c618825cd95b5c3421da3486ef8bc4c83b90270e06c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 20 Sep 2023 15:13:36 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Wed, 20 Sep 2023 15:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Sep 2023 15:13:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:091eb56f13f4be91ea9416e1b67e2c1f228b5e023f447dda2d3f5c56e57ff871`  
		Last Modified: Wed, 20 Sep 2023 00:47:36 GMT  
		Size: 32.4 MB (32397092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb68a3d175d1465b84e2c9740177c8ac0dd797e1a669bcb92bbb6532f695598`  
		Last Modified: Wed, 20 Sep 2023 15:16:53 GMT  
		Size: 2.5 MB (2532522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad57da183a1daf86907dcbb82ed63cae9008238fd8ee8807e718fcaff9d362ee`  
		Last Modified: Wed, 20 Sep 2023 15:17:27 GMT  
		Size: 156.1 MB (156076886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56692f52020c3bce36391744ef9a38cbcd6751c52719d06a1cb73350150862e7`  
		Last Modified: Wed, 20 Sep 2023 15:16:52 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:0cd1b74f4b5c9610b318327617de29bb6d3d8a1f13b2919eef6b76c7c95aa9ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191619203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9227e00a628121f82e3f0e7e0eafcc178fc82905bdfa431a0f5a8c4931eae547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 07 Sep 2023 00:18:05 GMT
ADD file:bf50998bef8a71b4723f6c17cc5c3e929d9c3b7a71b56060fea91ea0cd3502c4 in / 
# Thu, 07 Sep 2023 00:18:08 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:08:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:08:26 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 07 Sep 2023 01:08:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 01:08:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 07 Sep 2023 01:08:29 GMT
ENV JULIA_VERSION=1.10.0-beta2
# Thu, 07 Sep 2023 01:09:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-beta2-linux-x86_64.tar.gz'; 			sha256='f1a17f5a52980c167416cbe4eda14419d818f3b76985401154a3a567879d6477'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-beta2-linux-aarch64.tar.gz'; 			sha256='38e7c07a0c3f124497da62d81dc6bf58dbce8a6a3f0542ba52aaac54ed238351'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-beta2-linux-i686.tar.gz'; 			sha256='adc781af2ee5981988f0551672170b1610c4af1262495f4ecf19602da0ed579f'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-beta2-linux-ppc64le.tar.gz'; 			sha256='4b51efbdfe958e754f982c618825cd95b5c3421da3486ef8bc4c83b90270e06c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 07 Sep 2023 01:09:29 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Thu, 07 Sep 2023 01:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Sep 2023 01:09:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2365f3cb8bc5e18258159454852d941d92577738f79c1b5594afaec8481b47f3`  
		Last Modified: Thu, 07 Sep 2023 00:24:24 GMT  
		Size: 35.3 MB (35291070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4763a9dca659fe70ee1f5710903bfed94beb26f6d9179c949a6683fd983fe4df`  
		Last Modified: Thu, 07 Sep 2023 01:13:35 GMT  
		Size: 2.6 MB (2627565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fa5349a74dd94924d0cf48af3c9f594c386a9fc9cd0e107e1849472c9421f7`  
		Last Modified: Thu, 07 Sep 2023 01:14:16 GMT  
		Size: 153.7 MB (153700196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f52d35227c2202b6f7e20e1c49cc127b6fa903e837f173a650c723b2de4b0c`  
		Last Modified: Thu, 07 Sep 2023 01:13:34 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
