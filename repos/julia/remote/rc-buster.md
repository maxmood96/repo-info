## `julia:rc-buster`

```console
$ docker pull julia@sha256:a7c28da55a294fb32af6c7d4803228e528bec0121e20eb69297b180de3c0c0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:rc-buster` - linux; amd64

```console
$ docker pull julia@sha256:d8bdf7843f1dab0f316bb38566803dc14f2f5a642e9a1399f6669c3a277c9ce7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178173826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0f159d72cf4eec8d4df9857ef59e6f20270dd5dd500648bb3cfb9dd564497f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:28:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:28:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 21 Dec 2022 03:28:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 03:28:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Jan 2023 17:34:05 GMT
ENV JULIA_VERSION=1.9.0-beta2
# Mon, 02 Jan 2023 17:34:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-beta2-linux-x86_64.tar.gz'; 			sha256='72c0bfaa457784c83495e9da3ab706ed5053ee4d287472e03ff869d8eb72e0ee'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-beta2-linux-aarch64.tar.gz'; 			sha256='1ee292e33cc777c781d382c46521bc479941510ce4934271e7ca7e124150922a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-beta2-linux-i686.tar.gz'; 			sha256='1d900a852661d2a1b19287d12b689ee580709ba46f60eb62e6146ed8a38f772d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 02 Jan 2023 17:34:25 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Mon, 02 Jan 2023 17:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jan 2023 17:34:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5877b4f7601a8f0fad481e5da54e1300b207bc19d4eb5b676de8a316c00aa77a`  
		Last Modified: Wed, 21 Dec 2022 03:32:00 GMT  
		Size: 4.5 MB (4469938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355d0fe771dcb3c87fecd631ef581e69e3ae2c4e68c3aeaf53e343f55f6525bc`  
		Last Modified: Mon, 02 Jan 2023 17:37:09 GMT  
		Size: 146.6 MB (146563183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b9452971e77c1db678d644170757eda81af8ae61e615faf843b7abc06c3456`  
		Last Modified: Mon, 02 Jan 2023 17:36:45 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:60444146370ce2f11bc55e28f853c7ba1c3dfddfb1e84bc28987c6006fe0950d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170872497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1b5066d1bdd5121e2b0f38ae7359024f760ed9887cb6dd3e1a8a8ad26cd4a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:02 GMT
ADD file:51788132818f0e1cbed57cd022358b0564ec0d9cab6d33e5ef53902645d53c98 in / 
# Wed, 21 Dec 2022 01:40:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:17:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:17:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 21 Dec 2022 13:17:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:17:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Jan 2023 18:10:33 GMT
ENV JULIA_VERSION=1.9.0-beta2
# Mon, 02 Jan 2023 18:10:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-beta2-linux-x86_64.tar.gz'; 			sha256='72c0bfaa457784c83495e9da3ab706ed5053ee4d287472e03ff869d8eb72e0ee'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-beta2-linux-aarch64.tar.gz'; 			sha256='1ee292e33cc777c781d382c46521bc479941510ce4934271e7ca7e124150922a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-beta2-linux-i686.tar.gz'; 			sha256='1d900a852661d2a1b19287d12b689ee580709ba46f60eb62e6146ed8a38f772d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 02 Jan 2023 18:10:52 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Mon, 02 Jan 2023 18:10:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jan 2023 18:10:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eb4ce5bba15e4b6fd353d7fc222fbe9c71d6881cefe1e10384c6c358d4b4eb90`  
		Last Modified: Wed, 21 Dec 2022 01:43:52 GMT  
		Size: 25.9 MB (25914906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9068b0201c422401a42169f4381a90c0ab51fd149b79234fb220e273ca2759`  
		Last Modified: Wed, 21 Dec 2022 13:20:23 GMT  
		Size: 4.3 MB (4348900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf9a9f5c317b3c42310e98809db3143392c33b2cb554b9940d9bef8154dcbfd`  
		Last Modified: Mon, 02 Jan 2023 18:12:16 GMT  
		Size: 140.6 MB (140608316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a927285787ce40a9901f985c583fe7974570c157904d9ec2da91ba2c8d9dbde3`  
		Last Modified: Mon, 02 Jan 2023 18:11:58 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-buster` - linux; 386

```console
$ docker pull julia@sha256:f6400da7bd974cd8c75ea2217d9465e1622818483a63f279e6a7531b32aab46b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176263782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae85d367065ef47a2ccd5d011862e5610a1ecc79b0c38f07a5c203fa7923def1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:45 GMT
ADD file:48a2a0e6cb166df412bb4f6ad30537c66bc6be97ce4c8fc582fd5ac8c6129b5a in / 
# Wed, 21 Dec 2022 01:39:46 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 07:52:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 07:52:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 21 Dec 2022 07:52:47 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 07:52:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Jan 2023 17:55:07 GMT
ENV JULIA_VERSION=1.9.0-beta2
# Mon, 02 Jan 2023 17:55:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-beta2-linux-x86_64.tar.gz'; 			sha256='72c0bfaa457784c83495e9da3ab706ed5053ee4d287472e03ff869d8eb72e0ee'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-beta2-linux-aarch64.tar.gz'; 			sha256='1ee292e33cc777c781d382c46521bc479941510ce4934271e7ca7e124150922a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-beta2-linux-i686.tar.gz'; 			sha256='1d900a852661d2a1b19287d12b689ee580709ba46f60eb62e6146ed8a38f772d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 02 Jan 2023 17:55:29 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Mon, 02 Jan 2023 17:55:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jan 2023 17:55:30 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9099d8a02dc0a7901931d2811fa3078b18ecd3a40a156cbcfd91629126463f80`  
		Last Modified: Wed, 21 Dec 2022 01:45:34 GMT  
		Size: 27.8 MB (27798412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7c476c6b6110495258a60775783d10613f993d83b5dc1f0891117813464e09`  
		Last Modified: Wed, 21 Dec 2022 07:56:32 GMT  
		Size: 4.6 MB (4619645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016168fea9e1a17c3e8d7273938def238fb3d8f9a6d62f27f7205e975b1fbc87`  
		Last Modified: Mon, 02 Jan 2023 17:57:36 GMT  
		Size: 143.8 MB (143845352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb68e36b0123bea71a24a52c884c5d0f9ca3392bbf305b74abb1a2baf218325`  
		Last Modified: Mon, 02 Jan 2023 17:57:16 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
