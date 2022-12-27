## `julia:1-bullseye`

```console
$ docker pull julia@sha256:b4c8158782c8e9f7925d16ebb13908a52e2f1f18aa9372ca4f4775b0db326915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:38fd7bc589210e13b4ebbd9af4c9dac6ceeb4927f1d9d0eb6226005ef495cf72
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166926698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6848d1eb026fefee534343b75878af849a7d303574b8cf66d94d10f6c8067f9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:28:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:28:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 21 Dec 2022 03:28:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 03:28:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 27 Dec 2022 18:36:17 GMT
ENV JULIA_VERSION=1.8.4
# Tue, 27 Dec 2022 18:36:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.4-linux-x86_64.tar.gz'; 			sha256='f0427a4d7910c47dc7c31f65ba7ecaafedbbc0eceb39c320a37fa33598004fd5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.4-linux-aarch64.tar.gz'; 			sha256='dc4798c1ce8768fa35972e8b149ca3a85fc69e1074b609a72b2cfed5c4aa7050'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.4-linux-i686.tar.gz'; 			sha256='ea53fb0894ea92fd6749f58f7039c0d854f81dcc42899362bde191c9df3ee0c0'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 27 Dec 2022 18:36:36 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 27 Dec 2022 18:36:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Dec 2022 18:36:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6a345df56f2d45ba85a9454ae3220bfd6c0fcad5684fc4e21b0702744c651b`  
		Last Modified: Wed, 21 Dec 2022 03:31:24 GMT  
		Size: 2.4 MB (2426594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c486753e4be770fcbd59861e64ffdde30c61d7422f8d644d3460c3466a5980e`  
		Last Modified: Tue, 27 Dec 2022 18:39:02 GMT  
		Size: 133.1 MB (133102787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42e9678405e65fe364c52e8f00977ecce31a611af86c85607936a1694e3742b`  
		Last Modified: Tue, 27 Dec 2022 18:38:39 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:719ff23f340222364132897d946cd093e4a9f1b6805e87c7bca04cc1c05f9324
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159486794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84ec2bb0300f585f8c6d382ad1d8febcd88d5adea99e61e537e264633b698ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:17:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 21 Dec 2022 13:17:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:17:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 27 Dec 2022 17:54:49 GMT
ENV JULIA_VERSION=1.8.4
# Tue, 27 Dec 2022 17:55:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.4-linux-x86_64.tar.gz'; 			sha256='f0427a4d7910c47dc7c31f65ba7ecaafedbbc0eceb39c320a37fa33598004fd5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.4-linux-aarch64.tar.gz'; 			sha256='dc4798c1ce8768fa35972e8b149ca3a85fc69e1074b609a72b2cfed5c4aa7050'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.4-linux-i686.tar.gz'; 			sha256='ea53fb0894ea92fd6749f58f7039c0d854f81dcc42899362bde191c9df3ee0c0'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 27 Dec 2022 17:55:06 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 27 Dec 2022 17:55:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Dec 2022 17:55:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1820c90ffb2cc93d774b46935fe945b5ae6f1b067485375b13208bf3c98b00e6`  
		Last Modified: Wed, 21 Dec 2022 13:19:55 GMT  
		Size: 2.4 MB (2414247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb142d3c177b16e19c020b42c3366e3cafe3acb337f76463773811ef2a16f554`  
		Last Modified: Tue, 27 Dec 2022 17:56:21 GMT  
		Size: 127.0 MB (127027403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a9731a8b2c1312c969be7c06df9b061e3831da8b8348888f01e4ec90878e4b`  
		Last Modified: Tue, 27 Dec 2022 17:56:05 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:c17fa8709001358bbaef9ec020906950690f9ae75a2428d899cc7e128d4a3483
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164926511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec565560b0afc49c1218c2ceb505e13270a93e094b75076c8fdabf986d48987`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:22 GMT
ADD file:5f553fdf893bb3198d173c48f4531e9bfdbab61798c1aa8217fd80e9d686d7ae in / 
# Wed, 21 Dec 2022 01:39:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 07:52:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 07:52:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 21 Dec 2022 07:52:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 07:52:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 27 Dec 2022 17:49:33 GMT
ENV JULIA_VERSION=1.8.4
# Tue, 27 Dec 2022 17:49:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.4-linux-x86_64.tar.gz'; 			sha256='f0427a4d7910c47dc7c31f65ba7ecaafedbbc0eceb39c320a37fa33598004fd5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.4-linux-aarch64.tar.gz'; 			sha256='dc4798c1ce8768fa35972e8b149ca3a85fc69e1074b609a72b2cfed5c4aa7050'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.4-linux-i686.tar.gz'; 			sha256='ea53fb0894ea92fd6749f58f7039c0d854f81dcc42899362bde191c9df3ee0c0'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 27 Dec 2022 17:49:56 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 27 Dec 2022 17:49:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Dec 2022 17:49:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3228cb514e81f042720b7fd118ace0f279d1a4bc422b7e24189514a574dfa546`  
		Last Modified: Wed, 21 Dec 2022 01:44:46 GMT  
		Size: 32.4 MB (32375745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defa3a00676dd4766e52011f0a4665a910f5c8098d7fca0f93744f78138f5c11`  
		Last Modified: Wed, 21 Dec 2022 07:55:59 GMT  
		Size: 2.5 MB (2531810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9e85cd00ac3abd8bd67a9a9b9a68073eddaff4d4dec94e4d0bca2458216294`  
		Last Modified: Tue, 27 Dec 2022 17:51:54 GMT  
		Size: 130.0 MB (130018578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd91ec00d8661051683eb1e00a21b4ba803dfca1dd818585ffa034869b5c2dc`  
		Last Modified: Tue, 27 Dec 2022 17:51:35 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
