## `julia:buster`

```console
$ docker pull julia@sha256:f03f0483c92cd91288bd22632745d10e1b84b62fdbfefebf70d6aeb56b1cdabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:buster` - linux; amd64

```console
$ docker pull julia@sha256:001ebbcc5eb516e7fcbffda57ce68cd460a7c8a39faae9c0e529a388f222610a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163956765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5146534d2aff7fcfa472a7ead3c849336ecf367d23532392be9f713e17965641`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:18 GMT
ADD file:30180333dcb9028c0d2776f05042f6f309238b100863a050f3981fb80604e871 in / 
# Tue, 06 Dec 2022 01:21:18 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 08:38:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 08:38:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 06 Dec 2022 08:38:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 08:38:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 06 Dec 2022 08:39:14 GMT
ENV JULIA_VERSION=1.8.3
# Tue, 06 Dec 2022 08:39:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.3-linux-x86_64.tar.gz'; 			sha256='33c3b09356ffaa25d3331c3646b1f2d4b09944e8f93fcb994957801b8bbf58a9'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.3-linux-aarch64.tar.gz'; 			sha256='dbffb134a413b712d4a8e1ee8e665ea55edb0865719a1bad9979123d6433acc9'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.3-linux-i686.tar.gz'; 			sha256='3604051bf434e7a9ecfc306826d363216f835d22103baf5c31bb70f196dac625'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 06 Dec 2022 08:39:31 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 06 Dec 2022 08:39:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Dec 2022 08:39:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6eab20599fab240a56b06125a77b4921dd39662d3b9f9008da7306531772a1d0`  
		Last Modified: Tue, 06 Dec 2022 01:25:52 GMT  
		Size: 27.1 MB (27140356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ab6b9b1247dca5b7760f4aed09beef46f8b7fe376a683dd1aa92d595549bf0`  
		Last Modified: Tue, 06 Dec 2022 08:41:46 GMT  
		Size: 4.5 MB (4469913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b20e3554c505473f307e70c9d3b871c3f5318d68c98090a2cdf95160239a62`  
		Last Modified: Tue, 06 Dec 2022 08:43:17 GMT  
		Size: 132.3 MB (132346119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c970778140ac3993e58e831810011d9c129c911ab1ed7d709d5260f66ad538e9`  
		Last Modified: Tue, 06 Dec 2022 08:42:55 GMT  
		Size: 377.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:aa1611cd432f70ed681d62ded778d8df298b3cfb0a7063627cda43e10003008a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156643178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8527ab47dca28161dd42c3ead020a762246220d0d47c51e18a05fc0070311bd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:34 GMT
ADD file:764288ad3920160093c500e1a7277f174a656030bbe3a0511e7925e84495b6ee in / 
# Tue, 06 Dec 2022 01:40:34 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 03:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 03:52:09 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 06 Dec 2022 03:52:10 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 03:52:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 06 Dec 2022 03:52:52 GMT
ENV JULIA_VERSION=1.8.3
# Tue, 06 Dec 2022 03:53:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.3-linux-x86_64.tar.gz'; 			sha256='33c3b09356ffaa25d3331c3646b1f2d4b09944e8f93fcb994957801b8bbf58a9'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.3-linux-aarch64.tar.gz'; 			sha256='dbffb134a413b712d4a8e1ee8e665ea55edb0865719a1bad9979123d6433acc9'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.3-linux-i686.tar.gz'; 			sha256='3604051bf434e7a9ecfc306826d363216f835d22103baf5c31bb70f196dac625'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 06 Dec 2022 03:53:08 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 06 Dec 2022 03:53:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Dec 2022 03:53:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b473b36a3d93c888196b326b1aad1f802bb6a9fa6fcbc5d2614d99a67899d587`  
		Last Modified: Tue, 06 Dec 2022 01:44:33 GMT  
		Size: 25.9 MB (25914951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba26d62983e6105a54f3cb653bb0a56c93691ba75eb6eb6c813cfff342f7f2ba`  
		Last Modified: Tue, 06 Dec 2022 03:54:43 GMT  
		Size: 4.3 MB (4348930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c934d6fe4f9e4f07a8f239952c6d1c5927b49ff9b547586d7315b63022347cfe`  
		Last Modified: Tue, 06 Dec 2022 03:55:55 GMT  
		Size: 126.4 MB (126378924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd0ff0364902439922eec347db3d70d75276d66706e3eb476fbd2e4061bec2d`  
		Last Modified: Tue, 06 Dec 2022 03:55:39 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; 386

```console
$ docker pull julia@sha256:e1b7c9e483acf8800e11d7b98709cfce33ac81dc7e7c11f810a5a299618fc010
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161706906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e1092d40503f468642713755d3aadbcb42e1bbedd26b6dadeeac5226c4af89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:21 GMT
ADD file:d1161a047b155d436f12a377ddf5a4a85ad0d20ac1f3f5d4444259a8773d6ef5 in / 
# Tue, 06 Dec 2022 01:40:22 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 14:10:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 14:10:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 06 Dec 2022 14:10:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 14:10:22 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 06 Dec 2022 14:11:22 GMT
ENV JULIA_VERSION=1.8.3
# Tue, 06 Dec 2022 14:11:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.3-linux-x86_64.tar.gz'; 			sha256='33c3b09356ffaa25d3331c3646b1f2d4b09944e8f93fcb994957801b8bbf58a9'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.3-linux-aarch64.tar.gz'; 			sha256='dbffb134a413b712d4a8e1ee8e665ea55edb0865719a1bad9979123d6433acc9'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.3-linux-i686.tar.gz'; 			sha256='3604051bf434e7a9ecfc306826d363216f835d22103baf5c31bb70f196dac625'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 06 Dec 2022 14:11:41 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 06 Dec 2022 14:11:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Dec 2022 14:11:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:da96e1773ee343324a0519eb38b71097e939e2d40d51ae4f19dcd9932b7cf638`  
		Last Modified: Tue, 06 Dec 2022 01:46:27 GMT  
		Size: 27.8 MB (27798436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11831b2deead33f358d580704ac2eb329b995a1324f23ddba94f246ff0348752`  
		Last Modified: Tue, 06 Dec 2022 14:14:05 GMT  
		Size: 4.6 MB (4619640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374975587b837d8ab7c85a0f2f658a9633332e3610949e92701501dbe4bdbc75`  
		Last Modified: Tue, 06 Dec 2022 14:15:29 GMT  
		Size: 129.3 MB (129288455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b0f8c5750ae775f76a1aa62d1303d2328891e65d670e59f0227c1e9557e618`  
		Last Modified: Tue, 06 Dec 2022 14:15:11 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
