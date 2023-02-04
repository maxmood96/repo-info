## `julia:1-bullseye`

```console
$ docker pull julia@sha256:c3ccf26fab83fcd091c28750161beeb038f4a353032c8d4d2e06185558efbd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:26f99fe69ca1f70c2b769153da725bac32cfa524dd5cef14be793f9fd106f087
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167022333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feb39ff18ae6fa900ee3c1c3da852a620366148430a7b239fb362bab3eecdb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 06:02:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:02:55 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 11 Jan 2023 06:02:56 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:02:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 11 Jan 2023 06:03:50 GMT
ENV JULIA_VERSION=1.8.5
# Fri, 20 Jan 2023 01:57:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.5-linux-x86_64.tar.gz'; 			sha256='e71a24816e8fe9d5f4807664cbbb42738f5aa9fe05397d35c81d4c5d649b9d05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.5-linux-aarch64.tar.gz'; 			sha256='a1f637b44c71ea9bc96d7c3ef347724c054a1e5227b980adebfc33599e5153a4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.5-linux-i686.tar.gz'; 			sha256='f0edd61970710333cb5ac6491fbbc859436e5e9e84b014ae04f291bddf6a7e21'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.8/julia-1.8.5-linux-ppc64le.tar.gz'; 			sha256='13c121362e73cda8049a9b51b15c6d0d1dc66803db45ab1d5c46ea9c1b7440df'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 20 Jan 2023 01:57:13 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Fri, 20 Jan 2023 01:57:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Jan 2023 01:57:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fa56be37265448a2b510f943c9ac54b9a0beaa493933cc3ef983e8b3cec234`  
		Last Modified: Wed, 11 Jan 2023 06:06:08 GMT  
		Size: 2.4 MB (2426594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2476995bb4168b7a2c4dc675e597ee8cd390d9d4262723370b980ae672f056`  
		Last Modified: Fri, 20 Jan 2023 02:01:27 GMT  
		Size: 133.2 MB (133198393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06021a6dfd324af236582167c7db75a22b93a5a44a8d09b8de7b8b8b4bbe5ed5`  
		Last Modified: Fri, 20 Jan 2023 02:01:06 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f7e262c3745a35061ac242e7124d4c2dd147b2a8d755ffdc5ee4a3773bac2305
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159430625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7050f11a73ed1a303682d8cde139d15c2ae1ed719f621aff1cad57c08a0885a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:29:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:29:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 04 Feb 2023 08:29:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 08:29:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 04 Feb 2023 08:30:45 GMT
ENV JULIA_VERSION=1.8.5
# Sat, 04 Feb 2023 08:31:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.5-linux-x86_64.tar.gz'; 			sha256='e71a24816e8fe9d5f4807664cbbb42738f5aa9fe05397d35c81d4c5d649b9d05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.5-linux-aarch64.tar.gz'; 			sha256='a1f637b44c71ea9bc96d7c3ef347724c054a1e5227b980adebfc33599e5153a4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.5-linux-i686.tar.gz'; 			sha256='f0edd61970710333cb5ac6491fbbc859436e5e9e84b014ae04f291bddf6a7e21'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.8/julia-1.8.5-linux-ppc64le.tar.gz'; 			sha256='13c121362e73cda8049a9b51b15c6d0d1dc66803db45ab1d5c46ea9c1b7440df'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 04 Feb 2023 08:31:02 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Sat, 04 Feb 2023 08:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 08:31:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cbce9bf528576bb895c59d7b207130ef4e92417f2b708b562d3fd76a4b829f`  
		Last Modified: Sat, 04 Feb 2023 08:32:30 GMT  
		Size: 2.4 MB (2414182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8562475d0e63f6378191b9a2908ae3021b7d058b8a25c51e0f1ea6c1e1e37d5`  
		Last Modified: Sat, 04 Feb 2023 08:33:43 GMT  
		Size: 127.0 MB (126971275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fbc956db2430df7ba77520e27f4ce41516d528b008f43ff2770ef00806411b`  
		Last Modified: Sat, 04 Feb 2023 08:33:27 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:d33af0586167093b18e2c9372f601e33c68d18cadb82e71dc8fd0b3979231d15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164895813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c706afde022c6d79cc4ec8ca6e4ad1c349907fcaa4f3b7ca2055ba593af4f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 11 Jan 2023 03:16:08 GMT
ADD file:68afc7c49a947a9fb253ffeba9950cdc39e241f8a5cf0133043cfc612447f597 in / 
# Wed, 11 Jan 2023 03:16:08 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 05:41:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 05:41:50 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 11 Jan 2023 05:41:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 05:41:52 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 11 Jan 2023 05:43:05 GMT
ENV JULIA_VERSION=1.8.5
# Fri, 20 Jan 2023 02:25:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.5-linux-x86_64.tar.gz'; 			sha256='e71a24816e8fe9d5f4807664cbbb42738f5aa9fe05397d35c81d4c5d649b9d05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.5-linux-aarch64.tar.gz'; 			sha256='a1f637b44c71ea9bc96d7c3ef347724c054a1e5227b980adebfc33599e5153a4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.5-linux-i686.tar.gz'; 			sha256='f0edd61970710333cb5ac6491fbbc859436e5e9e84b014ae04f291bddf6a7e21'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.8/julia-1.8.5-linux-ppc64le.tar.gz'; 			sha256='13c121362e73cda8049a9b51b15c6d0d1dc66803db45ab1d5c46ea9c1b7440df'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 20 Jan 2023 02:25:11 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Fri, 20 Jan 2023 02:25:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Jan 2023 02:25:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:165165b78fad597abd0883f40adcaa0edcfe981a358deea181323680a07b7011`  
		Last Modified: Wed, 11 Jan 2023 03:22:01 GMT  
		Size: 32.4 MB (32375738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33635ddeb839f7e404118d0482fc8b3e7a90a11fb654de2bf61a000fe717928`  
		Last Modified: Wed, 11 Jan 2023 05:45:47 GMT  
		Size: 2.5 MB (2531793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3d3496dc021fc77120c76651928fc4454c2487bcc5b3eb307a12c4c616b2d0`  
		Last Modified: Fri, 20 Jan 2023 02:28:08 GMT  
		Size: 130.0 MB (129987906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c722d810b5616d87c526743073abd0f8726df99bfa7cc4ce43dae16fed812844`  
		Last Modified: Fri, 20 Jan 2023 02:27:49 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:290946f7e9f983f1f37ad39692889464f31e013a150bfec8933acfa9b9454a2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155921857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0212b948be19e607ae52f54859fd2b4af77b8053822576f8175144188199afe7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 11 Jan 2023 03:49:30 GMT
ADD file:3c7553fb5eda606d574ff6c08bc2213f9e6a68910043fe3087e4c1a04b65a18e in / 
# Wed, 11 Jan 2023 03:49:32 GMT
CMD ["bash"]
# Sat, 21 Jan 2023 00:36:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 21 Jan 2023 00:36:23 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 21 Jan 2023 00:36:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Jan 2023 00:36:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 21 Jan 2023 00:37:21 GMT
ENV JULIA_VERSION=1.8.5
# Sat, 21 Jan 2023 00:37:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.5-linux-x86_64.tar.gz'; 			sha256='e71a24816e8fe9d5f4807664cbbb42738f5aa9fe05397d35c81d4c5d649b9d05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.5-linux-aarch64.tar.gz'; 			sha256='a1f637b44c71ea9bc96d7c3ef347724c054a1e5227b980adebfc33599e5153a4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.5-linux-i686.tar.gz'; 			sha256='f0edd61970710333cb5ac6491fbbc859436e5e9e84b014ae04f291bddf6a7e21'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.8/julia-1.8.5-linux-ppc64le.tar.gz'; 			sha256='13c121362e73cda8049a9b51b15c6d0d1dc66803db45ab1d5c46ea9c1b7440df'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 21 Jan 2023 00:38:05 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Sat, 21 Jan 2023 00:38:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Jan 2023 00:38:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bbf81328aca90b7ddb122fc175443f5323674a9e51bbb00d5b1d683ef0b858f4`  
		Last Modified: Wed, 11 Jan 2023 03:55:33 GMT  
		Size: 35.3 MB (35268773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ef65440752118c4780abbcb0554efb404a2143ec50dff5776461de04c96f7e`  
		Last Modified: Sat, 21 Jan 2023 00:38:43 GMT  
		Size: 2.6 MB (2627374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f19e0f6f87007b2102df8d2b8a970e4cc6a345726f9dfd904e09bb8e3c1c80`  
		Last Modified: Sat, 21 Jan 2023 00:40:08 GMT  
		Size: 118.0 MB (118025335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75a179a66cdb4c991536bccc76796b85db56ff0d7f138194f8e61761f29e37f`  
		Last Modified: Sat, 21 Jan 2023 00:39:34 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
