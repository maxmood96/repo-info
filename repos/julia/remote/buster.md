## `julia:buster`

```console
$ docker pull julia@sha256:545e46d55f89ea5f813493cd921f467258e5a6afa8d455c16311e409edc36a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:buster` - linux; amd64

```console
$ docker pull julia@sha256:bc7b2de50f45a52ee81d8134c7ccb1d8489e2de90d2b9780e6566844d0896808
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180539134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5932c10cb605fab6d27b692b463641566772e309a3f84130756f927aff83e3dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 03:58:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 03:58:56 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 23 May 2023 03:58:56 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 03:58:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 09 Jun 2023 06:31:01 GMT
ENV JULIA_VERSION=1.9.1
# Fri, 09 Jun 2023 06:31:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.1-linux-x86_64.tar.gz'; 			sha256='cde14a58f899251f30cfced87055626f44845780659ebe8d50cbc4c67b31997c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.1-linux-aarch64.tar.gz'; 			sha256='b643ccd3e2a5960f7ce7055243743d0a39badda3974bce3d77861dd363badd10'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.1-linux-i686.tar.gz'; 			sha256='662111251fe82fca5a23321cbe218d98c23683e76dc32e1a9756aa436de97890'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.1-linux-ppc64le.tar.gz'; 			sha256='391aba8e239bfa29c1d96e2d81d6ec50ab5b924ac2132ef934c556e0a3329fc5'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 09 Jun 2023 06:31:23 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Fri, 09 Jun 2023 06:31:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jun 2023 06:31:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4add0b47570fa87476e546a69dfdf17243a2bdfe9059e797eaa71e66a594c750`  
		Last Modified: Tue, 23 May 2023 04:01:08 GMT  
		Size: 4.5 MB (4472118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b77d6de018a508622b570cd459ca3f8acdcb52dc63a0da69ce8c01a1fadee3`  
		Last Modified: Fri, 09 Jun 2023 06:33:27 GMT  
		Size: 148.9 MB (148928066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc64f31da26123c792af82fdf102092bfccc4589cf76a933450b18bfabc62bb4`  
		Last Modified: Fri, 09 Jun 2023 06:33:05 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:e8c290c50ee1b41f0028a785777f69ada573c7ea23aa2e01d47d79ec33635dc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173370434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedfed366a3ba9d8de408ba9e06f315c54ddd90771d6c02814c41d95a43b68d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 07:22:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:22:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 23 May 2023 07:22:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:22:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 09 Jun 2023 06:47:26 GMT
ENV JULIA_VERSION=1.9.1
# Fri, 09 Jun 2023 06:47:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.1-linux-x86_64.tar.gz'; 			sha256='cde14a58f899251f30cfced87055626f44845780659ebe8d50cbc4c67b31997c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.1-linux-aarch64.tar.gz'; 			sha256='b643ccd3e2a5960f7ce7055243743d0a39badda3974bce3d77861dd363badd10'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.1-linux-i686.tar.gz'; 			sha256='662111251fe82fca5a23321cbe218d98c23683e76dc32e1a9756aa436de97890'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.1-linux-ppc64le.tar.gz'; 			sha256='391aba8e239bfa29c1d96e2d81d6ec50ab5b924ac2132ef934c556e0a3329fc5'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 09 Jun 2023 06:47:47 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Fri, 09 Jun 2023 06:47:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jun 2023 06:47:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aede84ce70d75f756a336175cf392a724bb6b750af8d1dd335c6c4522ba2891`  
		Last Modified: Tue, 23 May 2023 07:24:31 GMT  
		Size: 4.4 MB (4350752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edefe960f913d5254857e4fd048fc7a20cbc89372cf0d4aeed4ed72caf23c6a`  
		Last Modified: Fri, 09 Jun 2023 06:48:49 GMT  
		Size: 143.1 MB (143097563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6216ca776b96f099c11240a425af35ac549f8d0327319e95a2a69fa1cd246a33`  
		Last Modified: Fri, 09 Jun 2023 06:48:32 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; 386

```console
$ docker pull julia@sha256:255f7543d0e6dba32bffdc3ae60e70270c061eb49973957af547ba0e6261139a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178248531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056069102655d640917bef51c63d30efa8aac4fecf2bb3f8da960cee2a11c3f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 May 2023 00:40:01 GMT
ADD file:96715cff0e3569a2a1d7e203f0797ed4880da7714d455e25f032c67bff27221f in / 
# Tue, 23 May 2023 00:40:01 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:29:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:29:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 23 May 2023 02:29:36 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:29:36 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 23 May 2023 02:29:37 GMT
ENV JULIA_VERSION=1.9.0
# Tue, 23 May 2023 02:29:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-linux-x86_64.tar.gz'; 			sha256='00c614466ef9809c2eb23480e38d196a2c577fff2730c4f83d135b913d473359'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-linux-aarch64.tar.gz'; 			sha256='0a14315b53acd97f22d26d4a8fd2c237e524e95c3bec98d2d78b54d80c2bc364'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-linux-i686.tar.gz'; 			sha256='add391830b50df8d84f11ecf9e0fdd3d0fd420ba08737640094696fde64a22be'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.0-linux-ppc64le.tar.gz'; 			sha256='f32197fdd7b8e34d26d91cc46fc2fa040e07b02e61d22c0cedbc5e7e3d0363d5'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 23 May 2023 02:30:00 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 23 May 2023 02:30:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 May 2023 02:30:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3c2058520f8e2dee0c8d97a0e68335849888066e5d0d1b82b6ef302541b5c874`  
		Last Modified: Tue, 23 May 2023 00:45:13 GMT  
		Size: 27.8 MB (27797210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7678dd0b30ea1ab93eb8bcc35bcf334b795b36c9b74173148a7dbb8d70fab701`  
		Last Modified: Tue, 23 May 2023 02:31:53 GMT  
		Size: 4.6 MB (4623824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83a140272f2611b1f4445691bb0ac4abbb87dd9d4ac6f5f9d505bf97ece32fe`  
		Last Modified: Tue, 23 May 2023 02:32:21 GMT  
		Size: 145.8 MB (145827125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01965ecc75242364a50d7ecb78bc7ae189013003af9f27b68e7bbdff182061b7`  
		Last Modified: Tue, 23 May 2023 02:31:52 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
