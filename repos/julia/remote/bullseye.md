## `julia:bullseye`

```console
$ docker pull julia@sha256:60b422c7a807d291d3f10f052c4ac11b130840735f036049c51d9b34fafd6cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:69d6c2c7275c2e89e21926cd9135a7a2b57a491e74e6a9379705d15b63c74c35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182827861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75c2f11cc80f1fc271aebb1dff7cfa5508d2522a6db51e3c84efabcb47b8870`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:57:09 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 28 Jul 2023 01:57:10 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 01:57:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 28 Jul 2023 01:58:03 GMT
ENV JULIA_VERSION=1.9.2
# Fri, 28 Jul 2023 01:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.2-linux-x86_64.tar.gz'; 			sha256='4c2d799f442d7fe718827b19da2bacb72ea041b9ce55f24eee7b1313f57c4383'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.2-linux-aarch64.tar.gz'; 			sha256='682397f8895149f0e283f0b27bffc6694033bdfb19f9366c80f6efdf3685f27c'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.2-linux-i686.tar.gz'; 			sha256='08d1f72d92772c9a1074196a4651e06ccadc290d6d1e316fb25a43e585c14db9'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.2-linux-ppc64le.tar.gz'; 			sha256='b03080f0f8aeff395de932b90716cc71cf93b6fd21c993e87bf0f6cfef25510d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 28 Jul 2023 01:58:21 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:58:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:58:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7f6872df1bd24cfa97aa1b34c6013e8f69087c5b24e1d12980c96d316bf7b6`  
		Last Modified: Fri, 28 Jul 2023 02:00:25 GMT  
		Size: 2.4 MB (2426714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d03461b73e55166e8d94d817384fd54adc8c8b4593ef8cc529241ff836d0ebf`  
		Last Modified: Fri, 28 Jul 2023 02:02:00 GMT  
		Size: 149.0 MB (148983168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9ac25470e8af71760522db24fa506ce1efc355b7684a1a4ab9d4599b36eb72`  
		Last Modified: Fri, 28 Jul 2023 02:01:38 GMT  
		Size: 377.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9888851b1b77fd6e410d3117dae0317a0c0be5bd0d21a262974bf9495ee3afa7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175594585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d0308fe93d89dd05ad164988adec1c66b66d5a1274fe6ca592f2ba69108700d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:20:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:20:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 28 Jul 2023 14:20:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:20:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 28 Jul 2023 14:20:56 GMT
ENV JULIA_VERSION=1.9.2
# Fri, 28 Jul 2023 14:21:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.2-linux-x86_64.tar.gz'; 			sha256='4c2d799f442d7fe718827b19da2bacb72ea041b9ce55f24eee7b1313f57c4383'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.2-linux-aarch64.tar.gz'; 			sha256='682397f8895149f0e283f0b27bffc6694033bdfb19f9366c80f6efdf3685f27c'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.2-linux-i686.tar.gz'; 			sha256='08d1f72d92772c9a1074196a4651e06ccadc290d6d1e316fb25a43e585c14db9'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.2-linux-ppc64le.tar.gz'; 			sha256='b03080f0f8aeff395de932b90716cc71cf93b6fd21c993e87bf0f6cfef25510d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 28 Jul 2023 14:21:14 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Fri, 28 Jul 2023 14:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 14:21:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b783b889c195e4bf85ede29ba17c731d5df4f9fc3c44509bfbab37e327b8a`  
		Last Modified: Fri, 28 Jul 2023 14:22:54 GMT  
		Size: 2.4 MB (2414436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30857cab386f2c394334ae11734c38e1c2057a9d6c73a3513f066c582924334`  
		Last Modified: Fri, 28 Jul 2023 14:24:12 GMT  
		Size: 143.1 MB (143116943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f55978434a468429b2fc4ebdd81994ecac9ad8b47f804ea36915d9796c6b773`  
		Last Modified: Fri, 28 Jul 2023 14:23:55 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:6a079bcbb2b6c85ff3e71792c40c5cbb15aacdec9c94788a2c5dfc4bb3b884cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172540807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b086a9917c499ce530fc1f50541776f659edad23f2680a7ad37b8d40d99e62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:19 GMT
ADD file:1b873519e4db5a8c03ce73348afdd01ea06bbc550a0a873f4c3f9ead4db3c27e in / 
# Thu, 27 Jul 2023 23:39:19 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:05:38 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 28 Jul 2023 00:05:38 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 00:05:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 28 Jul 2023 00:06:45 GMT
ENV JULIA_VERSION=1.9.2
# Fri, 28 Jul 2023 00:07:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.2-linux-x86_64.tar.gz'; 			sha256='4c2d799f442d7fe718827b19da2bacb72ea041b9ce55f24eee7b1313f57c4383'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.2-linux-aarch64.tar.gz'; 			sha256='682397f8895149f0e283f0b27bffc6694033bdfb19f9366c80f6efdf3685f27c'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.2-linux-i686.tar.gz'; 			sha256='08d1f72d92772c9a1074196a4651e06ccadc290d6d1e316fb25a43e585c14db9'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.2-linux-ppc64le.tar.gz'; 			sha256='b03080f0f8aeff395de932b90716cc71cf93b6fd21c993e87bf0f6cfef25510d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 28 Jul 2023 00:07:08 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Fri, 28 Jul 2023 00:07:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 00:07:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e929cbc32ad44888448591b293bf4b9f260f11c666001b727228b58fd1774225`  
		Last Modified: Thu, 27 Jul 2023 23:44:12 GMT  
		Size: 32.4 MB (32397129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f129b548b0d2debb0e935acd46277b66111ffd177685c26acce98552ccffa1b`  
		Last Modified: Fri, 28 Jul 2023 00:09:09 GMT  
		Size: 2.5 MB (2532565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90471c054846d2b70d38b72e6bbe487318c66ecf7ae93fb72c556c2927dbfdf4`  
		Last Modified: Fri, 28 Jul 2023 00:11:00 GMT  
		Size: 137.6 MB (137610737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232b9a527939a8088bc824df161d34fcfb55b19997bff4aa477dba7d706eba03`  
		Last Modified: Fri, 28 Jul 2023 00:10:32 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:eea016ee7f154f3a1002f989dbfd822c65f44502cb184c9b37be26dba8c37598
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171241767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e548f84b257ffc905b92e96ef6e5f762eb037b700890b7581c375f6b976b2f78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 27 Jul 2023 23:23:41 GMT
ADD file:bc63550bad6e6b1e46c01c4911ac409a0a01e632b56a9a846fa2d7c86d8bb292 in / 
# Thu, 27 Jul 2023 23:23:43 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 07:46:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 07:46:26 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 28 Jul 2023 07:46:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 07:46:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 28 Jul 2023 07:48:21 GMT
ENV JULIA_VERSION=1.9.2
# Fri, 28 Jul 2023 07:49:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.2-linux-x86_64.tar.gz'; 			sha256='4c2d799f442d7fe718827b19da2bacb72ea041b9ce55f24eee7b1313f57c4383'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.2-linux-aarch64.tar.gz'; 			sha256='682397f8895149f0e283f0b27bffc6694033bdfb19f9366c80f6efdf3685f27c'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.2-linux-i686.tar.gz'; 			sha256='08d1f72d92772c9a1074196a4651e06ccadc290d6d1e316fb25a43e585c14db9'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.2-linux-ppc64le.tar.gz'; 			sha256='b03080f0f8aeff395de932b90716cc71cf93b6fd21c993e87bf0f6cfef25510d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 28 Jul 2023 07:49:10 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Fri, 28 Jul 2023 07:49:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 07:49:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:90fff1cd317dd6511bdf25cbc4f6797ea09a5bc0657b6e1d88772d885bed1da0`  
		Last Modified: Thu, 27 Jul 2023 23:30:33 GMT  
		Size: 35.3 MB (35291031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096e5df7e483e61b22458f3cfcf4af61ed501b4d8dd3553ebd774c0e5a89e6ee`  
		Last Modified: Fri, 28 Jul 2023 07:50:45 GMT  
		Size: 2.6 MB (2627579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d702032c8f5bb98fa9fe98e1bdc56e871fed183656482cd4950d5bf087a77c`  
		Last Modified: Fri, 28 Jul 2023 07:53:17 GMT  
		Size: 133.3 MB (133322782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbeada61d518a4759fc78e2f5c3caee428401392dd55499f7282353d6ce4a88`  
		Last Modified: Fri, 28 Jul 2023 07:52:39 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
