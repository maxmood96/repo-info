## `julia:bullseye`

```console
$ docker pull julia@sha256:f2eccd55c64dd0c540ac94d49baff3083e01e84e903e18953f2a48a1b54d8502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:1ec06e453ce9787ec2edaf86a3021bc749d8a6114743a2dc5ddfbd77d626a47f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182723797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27fd1fdcb7c426f7c48388393a2c7a77dc909a0c9817e8af4c561160e8a980a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 09:58:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 09:58:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Aug 2023 09:58:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 09:58:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 26 Aug 2023 04:05:22 GMT
ENV JULIA_VERSION=1.9.3
# Sat, 26 Aug 2023 04:05:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.3-linux-x86_64.tar.gz'; 			sha256='d76670cc9ba3e0fd4c1545dd3d00269c0694976a1176312795ebce1692d323d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.3-linux-aarch64.tar.gz'; 			sha256='55437879f6b98470d96c4048b922501b643dfffb8865abeb90c7333a83df7524'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.3-linux-i686.tar.gz'; 			sha256='e968d04a8b91e2bdcda307dd9dc26e7589b6c8f9598b2410856c95a706d84b10'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.3-linux-ppc64le.tar.gz'; 			sha256='15bcf163813d9a561ef50c77d1135135455c85f2dbd27a910400332edb959dc4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 26 Aug 2023 04:05:40 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Sat, 26 Aug 2023 04:05:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 26 Aug 2023 04:05:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61aded178ba476c5d182b60e52edae6616cbaf5e09980250e129db7d9c4adec`  
		Last Modified: Wed, 16 Aug 2023 10:01:15 GMT  
		Size: 2.4 MB (2426694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560301608d0ac95ce1116c3939d462cf93057c0b2dc9623e06d76e105b2dd692`  
		Last Modified: Sat, 26 Aug 2023 04:10:33 GMT  
		Size: 148.9 MB (148879049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9db21172827e826b6fcb25e06bac8129e86b6cc6cd4b6b8a8bd356a8434963`  
		Last Modified: Sat, 26 Aug 2023 04:10:10 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:fe0bd65214ef0bb3447d1a553d3d55232112955179c41598ec6dc4ff44923dc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175584276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0680b0f2d415dc803ef45da0b1a8d03ac902684669bf4da46bf0073d8756163`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:41:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:41:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 07 Sep 2023 06:41:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 06:41:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 07 Sep 2023 06:42:11 GMT
ENV JULIA_VERSION=1.9.3
# Thu, 07 Sep 2023 06:42:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.3-linux-x86_64.tar.gz'; 			sha256='d76670cc9ba3e0fd4c1545dd3d00269c0694976a1176312795ebce1692d323d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.3-linux-aarch64.tar.gz'; 			sha256='55437879f6b98470d96c4048b922501b643dfffb8865abeb90c7333a83df7524'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.3-linux-i686.tar.gz'; 			sha256='e968d04a8b91e2bdcda307dd9dc26e7589b6c8f9598b2410856c95a706d84b10'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.3-linux-ppc64le.tar.gz'; 			sha256='15bcf163813d9a561ef50c77d1135135455c85f2dbd27a910400332edb959dc4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 07 Sep 2023 06:42:30 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Thu, 07 Sep 2023 06:42:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Sep 2023 06:42:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91e352c797b92c14fe4289171ed872687fcea213c1bbd8ec45646fd0d73cd44`  
		Last Modified: Thu, 07 Sep 2023 06:44:04 GMT  
		Size: 2.4 MB (2414375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a200316816083e87258e2e83c5f870dacaccfc710b620a2f1f392c8cc07bf5e5`  
		Last Modified: Thu, 07 Sep 2023 06:45:19 GMT  
		Size: 143.1 MB (143106626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e4cfaac3651350af43ad3bc6f53b25b3eaddacbd32c61f6484988d335907e4`  
		Last Modified: Thu, 07 Sep 2023 06:45:02 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:fcb7eae6c63e53041ae659c237983b677b6ccd707e8b97938af612a06148717f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172546337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf639df95300021bf99a1df5b9f0e855acd17afafeba4c7368f13ffc5028f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:23 GMT
ADD file:fa0abd37650f364ecdf67d446b3fe2ce58fac1ad53beb5263b4f230fad58931e in / 
# Tue, 15 Aug 2023 23:39:23 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 09:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 09:29:25 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Aug 2023 09:29:26 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 09:29:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 26 Aug 2023 06:01:13 GMT
ENV JULIA_VERSION=1.9.3
# Sat, 26 Aug 2023 06:01:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.3-linux-x86_64.tar.gz'; 			sha256='d76670cc9ba3e0fd4c1545dd3d00269c0694976a1176312795ebce1692d323d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.3-linux-aarch64.tar.gz'; 			sha256='55437879f6b98470d96c4048b922501b643dfffb8865abeb90c7333a83df7524'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.3-linux-i686.tar.gz'; 			sha256='e968d04a8b91e2bdcda307dd9dc26e7589b6c8f9598b2410856c95a706d84b10'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.3-linux-ppc64le.tar.gz'; 			sha256='15bcf163813d9a561ef50c77d1135135455c85f2dbd27a910400332edb959dc4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 26 Aug 2023 06:01:40 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Sat, 26 Aug 2023 06:01:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 26 Aug 2023 06:01:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f6edc1df8dbb4cb778380e62ce1680ea580c1b213c048642bb7adaafa4cc6d73`  
		Last Modified: Tue, 15 Aug 2023 23:44:11 GMT  
		Size: 32.4 MB (32397200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363daa537b5ac9e8288052a7c3caf6b4426146c870bd55aab53e5c234e5faba1`  
		Last Modified: Wed, 16 Aug 2023 09:32:58 GMT  
		Size: 2.5 MB (2532575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2532f0963e4d53598f2e0b08daa86b37ba9acf0f95c0ec85da63de716ea1c47`  
		Last Modified: Sat, 26 Aug 2023 06:05:10 GMT  
		Size: 137.6 MB (137616186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c792f270b69d1df0ad9ae619511a90cfb21a16bcbaff77374382cc3a041a0db4`  
		Last Modified: Sat, 26 Aug 2023 06:04:36 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:80a065ba9bbdfeadfc832a2b357ee36d8277916624d24d1b2202daf0e116812a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171136386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b960bf2139783bbf02acfc08d7efaad86a6a91af6f8fe5adaf4bec7c3c7ca821`
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
# Thu, 07 Sep 2023 01:11:13 GMT
ENV JULIA_VERSION=1.9.3
# Thu, 07 Sep 2023 01:12:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.3-linux-x86_64.tar.gz'; 			sha256='d76670cc9ba3e0fd4c1545dd3d00269c0694976a1176312795ebce1692d323d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.3-linux-aarch64.tar.gz'; 			sha256='55437879f6b98470d96c4048b922501b643dfffb8865abeb90c7333a83df7524'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.3-linux-i686.tar.gz'; 			sha256='e968d04a8b91e2bdcda307dd9dc26e7589b6c8f9598b2410856c95a706d84b10'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.3-linux-ppc64le.tar.gz'; 			sha256='15bcf163813d9a561ef50c77d1135135455c85f2dbd27a910400332edb959dc4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 07 Sep 2023 01:12:14 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Thu, 07 Sep 2023 01:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Sep 2023 01:12:16 GMT
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
	-	`sha256:d8cb8a431de14cca092929095a60c073bf1a51530f23708fef564c6572bc1a9e`  
		Last Modified: Thu, 07 Sep 2023 01:15:55 GMT  
		Size: 133.2 MB (133217379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9c2aabcf9437494388405be666a9c99223d1a8795b5943248797a02efbd4d4`  
		Last Modified: Thu, 07 Sep 2023 01:15:18 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
