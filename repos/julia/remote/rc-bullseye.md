## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:34f3093bb4db01274965e65f1034e6206b08c0ade945dbae23cabac031d96225
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
$ docker pull julia@sha256:8cce6707d47d43879a39e2f199a9918eb246551e42e350d981723ad99fdddccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327799219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:defc955cf9afad2a46423accd77774ea2f08d15912a69479293d53185e8674cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7788d7ba8056db589f6180378e3da5ccce8a835f6fb261cb089b943e5d5bed67`  
		Last Modified: Thu, 05 Jun 2025 22:51:02 GMT  
		Size: 2.4 MB (2427445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f45ddeba98301554710f20a944e5203693fc90f1a29fae8da86d8cf7c215e1d`  
		Last Modified: Fri, 06 Jun 2025 00:03:11 GMT  
		Size: 295.1 MB (295115462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621bd1d09ae53eb0bcaaa5e546643fdce531f5c925ff5009bbc2b7bab1ca9f19`  
		Last Modified: Thu, 05 Jun 2025 22:51:20 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:ef165fd8f643f238cf90d336f628e5367c21c5bec2f16d33e0ab3a1b0ad1addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2754056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d19b4d1e424aa8e7ffd347019e129a4f1f4a2ae5c7a2d25197a260f9d823ea`

```dockerfile
```

-	Layers:
	-	`sha256:fe195b2a27334632e2cb7cfbedc631ab2fe5a0dab62fbdcd26c4b80258474eb7`  
		Last Modified: Thu, 05 Jun 2025 23:03:06 GMT  
		Size: 2.7 MB (2737680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49d2299b0c77b0d776549141037fa7d9a7a710f923b652ea0b9d43328382212d`  
		Last Modified: Thu, 05 Jun 2025 23:03:07 GMT  
		Size: 16.4 KB (16376 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2081c77acf8e929810ae4af5b83cde326c35f575452dd933204bbaf435149961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (347997178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cbe8e1b59eb2180f8e21aa21961edede96d148922ebe972f02f527d4c0b3d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbe1af0af3a3cd67231d5b053421840f37cf540aeb5dea875d6031f76ed763b`  
		Last Modified: Thu, 05 Jun 2025 22:42:35 GMT  
		Size: 2.4 MB (2416915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2915bda14d49fd6b4d26b57df31e0f42d0014c06156c5bce1e8256c3409383d`  
		Last Modified: Fri, 06 Jun 2025 00:03:42 GMT  
		Size: 316.8 MB (316833633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd282db401ab5cb3885260b75806c119715ceeb9d2585c73aadbf6ad1495922`  
		Last Modified: Thu, 05 Jun 2025 22:42:35 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:06156e227144df14e87b44f38c8cad1244303dea214d366ff17a3e85d825f036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2754415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb9949be09aed705c4b3ed9cc8528de4cd396211211c93f58b6dc753385fa2c`

```dockerfile
```

-	Layers:
	-	`sha256:1bd1b6b1b21c540d7251d95a4eba9a843472031b4f9828956f3e3d097cce53d2`  
		Last Modified: Thu, 05 Jun 2025 23:03:12 GMT  
		Size: 2.7 MB (2737931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:948fe4ee6cc15bc67fbf3154afa740f63df2740f1032814f3111fa12270a6631`  
		Last Modified: Thu, 05 Jun 2025 23:03:12 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:8683b2bcb727dbdd945a25c1eee4334447677de16dc3fc2e1e9536e897422cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.9 MB (270935525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5dde06d3c6416dbab645d241135f04328bc3a9bc718d6f2e0a0dd17e4b18051`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
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
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Tue, 03 Jun 2025 13:42:18 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0f8e04b435055773a6f583893af27185a5df06aceef11303ad2055b787b23`  
		Last Modified: Thu, 05 Jun 2025 22:40:57 GMT  
		Size: 2.5 MB (2534647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f5055ef5e079f8157e6de7eabead029c5a59ecb758d5fee0cde751481af1a2`  
		Last Modified: Fri, 06 Jun 2025 00:04:09 GMT  
		Size: 237.2 MB (237211308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7696e82494ce02e3d1d954e2311ff115223334d1f620e6e5e75dfabb016970e5`  
		Last Modified: Thu, 05 Jun 2025 22:40:58 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:784a4247e4365cd7ee4466c4053829b73d42502eb910346390ced361dd36eccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3350ed25068691093e4ff236c972ffa51374439707e1df8e9a78c3798001af82`

```dockerfile
```

-	Layers:
	-	`sha256:bf51c3b20cbffb9c88c12bfd1f71b0c6c3f4602ef4d5f379e149ff1399cd6f48`  
		Last Modified: Thu, 05 Jun 2025 23:03:17 GMT  
		Size: 2.7 MB (2734840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff29c9aa55279de4cd75bdd8d301fc034f352230893ac185ebf0d9c989fc15b`  
		Last Modified: Thu, 05 Jun 2025 23:03:17 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json
