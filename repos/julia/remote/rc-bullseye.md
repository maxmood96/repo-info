## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:3e05f963d3307b9eedcfba69c11daefa25d8fb341a902bf239299537b644bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:rc-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:a679f0639e6105858e9a817d34a50358e7a2f9169d622f653c7cdf5bf2b31298
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180884516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb08823eafb96956ec300d08924179b863c8cc62b7c55fe3e50389a70d0ea`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 04:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 04:35:25 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 12 Jul 2022 04:35:26 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 04:35:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 18 Jul 2022 20:11:15 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Mon, 18 Jul 2022 20:11:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.0-rc3-linux-x86_64.tar.gz'; 			sha256='7c57ac9aabce9b3cdc0f7bb1c393fe8058b794ddbb4168fcb28800b6459aa815'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.0-rc3-linux-aarch64.tar.gz'; 			sha256='40ae51fe3d20b27b40163daef761c2565529554bca01eb38bb19532400165586'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.0-rc3-linux-i686.tar.gz'; 			sha256='047775e2f21facf288422ed7f60459c37b9083fadf24d2d6740fd965c7e940be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 18 Jul 2022 20:11:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fd67c2db61d5a227d0a8ef420059c5f50e0d7d5ce61259cafa0d0ea763fc82`  
		Last Modified: Tue, 12 Jul 2022 04:38:36 GMT  
		Size: 2.4 MB (2426022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7d6ea936c0c37a5c658898c67f054bb909755d886e5ae7715aa1b46e29d456`  
		Last Modified: Mon, 18 Jul 2022 20:14:02 GMT  
		Size: 147.1 MB (147091884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3419b7c838da3cf2da2a3070c1b297b5fefcb8656e762da947a1128e362e3860
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173195011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d13c472ca918e0200bcdfb1aa899015eac508464dff2a070b8c2dda14d93195`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 03:59:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 03:59:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 12 Jul 2022 03:59:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 03:59:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 18 Jul 2022 19:16:16 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Mon, 18 Jul 2022 19:16:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.0-rc3-linux-x86_64.tar.gz'; 			sha256='7c57ac9aabce9b3cdc0f7bb1c393fe8058b794ddbb4168fcb28800b6459aa815'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.0-rc3-linux-aarch64.tar.gz'; 			sha256='40ae51fe3d20b27b40163daef761c2565529554bca01eb38bb19532400165586'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.0-rc3-linux-i686.tar.gz'; 			sha256='047775e2f21facf288422ed7f60459c37b9083fadf24d2d6740fd965c7e940be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 18 Jul 2022 19:16:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2a4192ae9bb78ebb529080630339e86928828e842bbbd17c3dd7cf8ba49bb1`  
		Last Modified: Tue, 12 Jul 2022 04:03:22 GMT  
		Size: 2.4 MB (2412384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeeb4b9095cf7599099c7c9a78a06f9b094f59ccd91466704752ee8af1dd45e`  
		Last Modified: Mon, 18 Jul 2022 19:18:37 GMT  
		Size: 140.7 MB (140728401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:bb3a486fa405e3b376ce3ffc9a299f4e8c9d6d435476f1c4fe696379205de41a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178966380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75737d68c757cf3ee76e9802b0d53a669bc56e699a401f092203d914018f98e4`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Jul 2022 00:39:27 GMT
ADD file:7f2bf44013d7848f051407d854b68c0d415a5328a3f5d241fca3150ce23bde65 in / 
# Tue, 12 Jul 2022 00:39:27 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 08:44:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 08:44:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 12 Jul 2022 08:44:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 08:44:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 18 Jul 2022 18:52:47 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Mon, 18 Jul 2022 18:53:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.0-rc3-linux-x86_64.tar.gz'; 			sha256='7c57ac9aabce9b3cdc0f7bb1c393fe8058b794ddbb4168fcb28800b6459aa815'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.0-rc3-linux-aarch64.tar.gz'; 			sha256='40ae51fe3d20b27b40163daef761c2565529554bca01eb38bb19532400165586'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.0-rc3-linux-i686.tar.gz'; 			sha256='047775e2f21facf288422ed7f60459c37b9083fadf24d2d6740fd965c7e940be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 18 Jul 2022 18:53:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1c0050b86a85a326857dbfa0456b3321f92df7e98ca468c048ee3e60dd14c923`  
		Last Modified: Tue, 12 Jul 2022 00:45:18 GMT  
		Size: 32.4 MB (32373949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fcb888b2ca7532f4061b92646a6067a7828bf1ca63281ae9bf80dd400cb558`  
		Last Modified: Tue, 12 Jul 2022 08:47:54 GMT  
		Size: 2.5 MB (2529668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e6c9fadabe69a4c991a0c3de82a95b7246d0363f89db1e6bedacaffa405f79`  
		Last Modified: Mon, 18 Jul 2022 18:55:15 GMT  
		Size: 144.1 MB (144062763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
