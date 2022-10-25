## `julia:1-bullseye`

```console
$ docker pull julia@sha256:135ec9d2368558d7e21389d38824aa7488aa2c0935782658f1256a66d3eab2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:8bc458159a1a042ec9b17b37adeaee790bd846ce44217259f5fa909adce4e206
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179665234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f289b02a4357499bc19c146bab18d31ee4316acea81c99e336f8e1e17f5a4f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:03:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:03:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 25 Oct 2022 04:03:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 04:03:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 25 Oct 2022 04:03:05 GMT
ENV JULIA_VERSION=1.8.2
# Tue, 25 Oct 2022 04:03:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 25 Oct 2022 04:03:24 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:03:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:03:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7651a4eafde60c5b7340b62d3a487d24763411b1b12790fe5fe7e18254628`  
		Last Modified: Tue, 25 Oct 2022 04:05:19 GMT  
		Size: 2.4 MB (2427488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a2e876aaed727e54f75f918e366a05644e54c73d7d783d9bdb256d654a801d`  
		Last Modified: Tue, 25 Oct 2022 04:05:40 GMT  
		Size: 145.8 MB (145817335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b55bcc3c6466df3d68d47e63a47dabcc2a2afe1701f4bf3bd3f228794292919`  
		Last Modified: Tue, 25 Oct 2022 04:05:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:df238bc9f49bf5583a53b1e5fb21ed4bef28d1a222ecd35dd2c54b158fe47a17
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171904700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1406b63346f54583a062124054cb8b4cb389bb51065db3ce2536deb9ab27e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:00:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:00:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:00:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:00:57 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 03:01:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 20 Oct 2022 20:39:59 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Thu, 20 Oct 2022 20:39:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Oct 2022 20:40:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2853a97676f7285584a0e561896a3873d942cfd731777779419c84fa1d8c86ea`  
		Last Modified: Wed, 05 Oct 2022 03:03:25 GMT  
		Size: 2.2 MB (2209648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7967c76989deab03d588e123221ba7846685870b5827aca9d26a0f9d0660f2`  
		Last Modified: Wed, 05 Oct 2022 03:03:45 GMT  
		Size: 139.6 MB (139630278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3188104e0e85f00aeff2345e19b1f11cbcd342cbe80b39cc8bcfe9b5828cb7`  
		Last Modified: Thu, 20 Oct 2022 20:41:04 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:73800540e76f340272223723027ea0a5206d434a8a1ed0b4848feb475a1582b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177438884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64332faa1f56b3bcf8d8ce792389cf7ec419650137bdc020f843524d3e530f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:09:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:09:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:09:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:09:39 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 02:10:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 20 Oct 2022 20:38:35 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Thu, 20 Oct 2022 20:38:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Oct 2022 20:38:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3c219fc5cf0f7f315d7d4da59f0bcd3faf7f26e4fa4fe36fe6ac7906b61c12`  
		Last Modified: Wed, 05 Oct 2022 02:12:12 GMT  
		Size: 2.3 MB (2326721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b43bbfe1015f385874c054b3b87a961620ad44585f6c3d9c1e8399eac99c33`  
		Last Modified: Wed, 05 Oct 2022 02:12:30 GMT  
		Size: 142.7 MB (142715495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bdd59ff45c452827f5947a60caea9ac66cd1fac139eb05e39c788b7593f4a2`  
		Last Modified: Thu, 20 Oct 2022 20:39:42 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
