## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:6a6e9aa88d09038b3313ef9d93f392f26718bd7c83c99552747bf24d8d29a579
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:rc-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:64ab64547f4d9be0b150e535b11400473a56a524940186cf6678afe7afdb275a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327799221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be295d62f8f70b1f5e97c8d622ec67f98f4411f52ae1af353669a677cdff23ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 05 Jun 2025 17:59:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Jun 2025 17:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_VERSION=1.12.0-beta4
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta4-linux-x86_64.tar.gz'; 			sha256='cead6a6ff3464af359258579a3ff6fb1d6f65aa93cb7b32b00691c23752f1cd7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta4-linux-aarch64.tar.gz'; 			sha256='e8ae058e3534a979de94688786f546060bbc676ac06035cd4350fbc53a1ddc21'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta4-linux-i686.tar.gz'; 			sha256='748eabeb5a31b9eb096b641010d1a0a9bf63283f58425734660c1056ba790e55'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87011af0da583ed9bc55901fcf994e4a506174a8422e9ad594399e7d297e7d45`  
		Last Modified: Tue, 01 Jul 2025 02:13:33 GMT  
		Size: 2.4 MB (2427368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145609d373b731a7967c04703c8b5870385f2a36c96083065e143c61770dfa9c`  
		Last Modified: Tue, 01 Jul 2025 12:54:53 GMT  
		Size: 295.1 MB (295115434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd07a9880769aad4aacb8bfd4059a68a21c0d355804dacdc41a94ad6b784e70a`  
		Last Modified: Tue, 01 Jul 2025 02:13:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:cf1776b1788733830f9771cb1a20249f3329febfed1f3a305ad5311eef2a6c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b984dd2d96f205d14e9002852cf9da2f415e9dd0258deda18ef74816538ea96f`

```dockerfile
```

-	Layers:
	-	`sha256:eb8688b4ab697890b05cbeef144894e93cd32e3de63b8df352f4cbcb2a2d3c40`  
		Last Modified: Tue, 01 Jul 2025 05:04:00 GMT  
		Size: 2.8 MB (2828027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93fe453c5a274c38af946faa4f4446117d1816b9c82b372fb1f954051ab28e84`  
		Last Modified: Tue, 01 Jul 2025 05:04:00 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:04288b2af5b72fa971cb670260947ae4861f033c4af998d48820a25711462685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (347995388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af76801d2aeeea2bed90ab2bf29c12c1a9cca1dcd13e9b75babcd8fc280bbb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 05 Jun 2025 17:59:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Jun 2025 17:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_VERSION=1.12.0-beta4
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta4-linux-x86_64.tar.gz'; 			sha256='cead6a6ff3464af359258579a3ff6fb1d6f65aa93cb7b32b00691c23752f1cd7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta4-linux-aarch64.tar.gz'; 			sha256='e8ae058e3534a979de94688786f546060bbc676ac06035cd4350fbc53a1ddc21'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta4-linux-i686.tar.gz'; 			sha256='748eabeb5a31b9eb096b641010d1a0a9bf63283f58425734660c1056ba790e55'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774daeb812e5fece3d60f17b2d0db8aef8f2a19eed94fbbca46c4e49239e2a5d`  
		Last Modified: Tue, 01 Jul 2025 03:02:09 GMT  
		Size: 2.4 MB (2417209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfb00191fec6faa56a11e4dc1b7ad073017e92164e0c2874f9bebdda759dda7`  
		Last Modified: Tue, 01 Jul 2025 13:22:53 GMT  
		Size: 316.8 MB (316833669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6262f8f1d62bb460ef2524f75789143942a6e2bcfc74cbd5e13c8d3cf1a60c`  
		Last Modified: Tue, 01 Jul 2025 03:02:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:7c69adf842c5a8a8163d7f2ae2821511237adf1be917416a7f7026273d229294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c08a16cc853fd69b7b46bdbebeed8ed3c344911fe45dc673f38fe4266065a7`

```dockerfile
```

-	Layers:
	-	`sha256:cf3aab9851eebdaa57c68df57c3a1fa47085f6d7838986f5aebeb20162190c43`  
		Last Modified: Tue, 01 Jul 2025 05:04:05 GMT  
		Size: 2.8 MB (2828278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a43965b4f5f6a56f61ac97a1f4a84b490544db274449a9e5d973ee1fc6f682b5`  
		Last Modified: Tue, 01 Jul 2025 05:04:06 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:8ed29d2e38a0be60dc9608477419a352c26e4b5619925078cd6c6db680120eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.9 MB (270936042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860d74b91f02e4796467face3e53f6be7a0c3a2ae8927b3cde960a8eb3cea873`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 05 Jun 2025 17:59:29 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Jun 2025 17:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_VERSION=1.12.0-beta4
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta4-linux-x86_64.tar.gz'; 			sha256='cead6a6ff3464af359258579a3ff6fb1d6f65aa93cb7b32b00691c23752f1cd7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta4-linux-aarch64.tar.gz'; 			sha256='e8ae058e3534a979de94688786f546060bbc676ac06035cd4350fbc53a1ddc21'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta4-linux-i686.tar.gz'; 			sha256='748eabeb5a31b9eb096b641010d1a0a9bf63283f58425734660c1056ba790e55'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:40be1da6146972d9df50a98eef7b5c0f729cd95a3a38782418f354f3b9355a9a`  
		Last Modified: Tue, 01 Jul 2025 01:14:57 GMT  
		Size: 31.2 MB (31189680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073e78d85bc2fa0563bcf3153a2a51d75ad0fa260b1fc82059d98a7c01ca141c`  
		Last Modified: Tue, 01 Jul 2025 02:13:40 GMT  
		Size: 2.5 MB (2534628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8374a96d9a857aeffcebac5aa21f08aa23501623694dc66dea519b475cc96d`  
		Last Modified: Tue, 01 Jul 2025 13:29:49 GMT  
		Size: 237.2 MB (237211365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6b792d7d959a1eb419f59e96c98fba8857b8b540693cdfec5372d7c5ad82e5`  
		Last Modified: Tue, 01 Jul 2025 02:13:32 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:72086d3a8944480a14a8201ac3e3357fcdbdd418b3e35aff332c9e131d949dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2841535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e5924e7deac65f62015640a4b2d2fbd402edbf21bdac1b5b9951635e5bf60b`

```dockerfile
```

-	Layers:
	-	`sha256:154acb1e19b09c248d99678680d4f870852f7f9892350e9f75a283c06d68d932`  
		Last Modified: Tue, 01 Jul 2025 05:04:10 GMT  
		Size: 2.8 MB (2825187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54e3c3e720e4c96852b3284e7c217cf470882b497c47d4348989b2eadec7bf0`  
		Last Modified: Tue, 01 Jul 2025 05:04:10 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json
