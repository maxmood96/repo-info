## `julia:rc`

```console
$ docker pull julia@sha256:6844e4b7fd91119f50b31961fec83610d4bca3e90291eeefa43588a120df08d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:b29c2c7de3317786ec5f96ad3a18a08239c4bde57326ab751a91ff03369232c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291532202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814c4dbd22f26d33d99529333c1c18d35f8f36099a0412355e667ae5e9ff985f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 26 Sep 2024 05:59:16 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Thu, 26 Sep 2024 05:59:16 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 05:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 26 Sep 2024 05:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc4
# Thu, 26 Sep 2024 05:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc4-linux-x86_64.tar.gz'; 			sha256='fdbd1aae595bd90f20b01cffe7ec34afcd25568b6351888065c934923ecfa042'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc4-linux-aarch64.tar.gz'; 			sha256='bc87e519a7f4d1633ca38db2b6bafd58f7025601202291a8ab6dd680101ad44f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc4-linux-i686.tar.gz'; 			sha256='dbcb66e774c71daf53d8b2582d30352c8696f05907e82b64a49754f718447196'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc4-linux-ppc64le.tar.gz'; 			sha256='06892cc4172e4e7a62051e68acd1a664da5e8e0cdd5f4902c5cad679ac27890d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 05:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b36249088c8cc5ec53f02e1abac490065d8b604fe779e22a6946178e50fc660`  
		Last Modified: Fri, 27 Sep 2024 06:02:44 GMT  
		Size: 5.7 MB (5712617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fe9a286915af9f12228c32c915c92c853edd95c246a39d569697e15e7d58f6`  
		Last Modified: Fri, 27 Sep 2024 06:02:50 GMT  
		Size: 256.7 MB (256692943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e51a5972ef04068cc0eaa2bbfbf088a0a10aca7d99277e84efc1507c93b7bbe`  
		Last Modified: Fri, 27 Sep 2024 06:02:44 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:7ae1818acdba29fde436bb2095b83308d37636ab23dce231cabf226fe6a456a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2452748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0154ed52338f5a8e1607530bb92e161925267813b9c4da8f10ebe1645810fd0`

```dockerfile
```

-	Layers:
	-	`sha256:b962abfd1495987b9b2facefc09b5ea91237fae74b75cad0a071f81db85ea777`  
		Last Modified: Fri, 27 Sep 2024 06:02:44 GMT  
		Size: 2.4 MB (2435057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bdb7dac4f9c5c488da2231e1017a9dbccf0073df2be651b691b365ffea87c82`  
		Last Modified: Fri, 27 Sep 2024 06:02:44 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:938df2ca271859de49c39f22c01d1d9c3782118a887d8792088f87fc877c9b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288205091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007ac7abfd012903e53eee39ff0da00ec4838f46580df4b5c105ce983f5d5b1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 26 Sep 2024 05:59:16 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Thu, 26 Sep 2024 05:59:16 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 05:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 26 Sep 2024 05:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc4
# Thu, 26 Sep 2024 05:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc4-linux-x86_64.tar.gz'; 			sha256='fdbd1aae595bd90f20b01cffe7ec34afcd25568b6351888065c934923ecfa042'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc4-linux-aarch64.tar.gz'; 			sha256='bc87e519a7f4d1633ca38db2b6bafd58f7025601202291a8ab6dd680101ad44f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc4-linux-i686.tar.gz'; 			sha256='dbcb66e774c71daf53d8b2582d30352c8696f05907e82b64a49754f718447196'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc4-linux-ppc64le.tar.gz'; 			sha256='06892cc4172e4e7a62051e68acd1a664da5e8e0cdd5f4902c5cad679ac27890d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 05:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cf2cffac6bd44b0b139097cfe17e7b533b5a86fbffff9abfa0e088d1424142`  
		Last Modified: Fri, 27 Sep 2024 15:11:45 GMT  
		Size: 5.5 MB (5537204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2c60b90fd9792565c044ebfe176b789e62aa5ad82a0f173a76b3bc961c4389`  
		Last Modified: Fri, 27 Sep 2024 15:11:50 GMT  
		Size: 253.5 MB (253511149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1685dd847695c6c36daac9376f67aed1fecb1320fd8d56a617f19eac191182`  
		Last Modified: Fri, 27 Sep 2024 15:11:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:1af8ccae9d365dd4d33bf8b9c147fba7dfee63d22c1f9190cd2b53a444182dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7d821b2f48dcdaa71415361613157febb8847af2e9ed81f40e20b5a0f3ee99`

```dockerfile
```

-	Layers:
	-	`sha256:2e10d709bea44c5ae2a8beb380faedefd7e38a1238430f9ec5aeeb7702a84ce6`  
		Last Modified: Fri, 27 Sep 2024 15:11:45 GMT  
		Size: 2.4 MB (2435355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3d9dc1f0e82f95f7cc07bec75bcb42345724b82d02937a7f8614458864cd238`  
		Last Modified: Fri, 27 Sep 2024 15:11:44 GMT  
		Size: 18.0 KB (18024 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:bccf481994cb9097fda7e8b601f98f32373329252ddc429dc1a167b6dafc08c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270475593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c053bb01413831d857afb128ece06f29a307f837e9a1930afc20a7591ecf2596`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 26 Sep 2024 05:59:16 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Thu, 26 Sep 2024 05:59:16 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 05:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 26 Sep 2024 05:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc4
# Thu, 26 Sep 2024 05:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc4-linux-x86_64.tar.gz'; 			sha256='fdbd1aae595bd90f20b01cffe7ec34afcd25568b6351888065c934923ecfa042'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc4-linux-aarch64.tar.gz'; 			sha256='bc87e519a7f4d1633ca38db2b6bafd58f7025601202291a8ab6dd680101ad44f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc4-linux-i686.tar.gz'; 			sha256='dbcb66e774c71daf53d8b2582d30352c8696f05907e82b64a49754f718447196'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc4-linux-ppc64le.tar.gz'; 			sha256='06892cc4172e4e7a62051e68acd1a664da5e8e0cdd5f4902c5cad679ac27890d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 05:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc72c2eadfde7d89f66c6b4378e3b957e47651ef16c7b4df4a801ff8ccf45b7`  
		Last Modified: Fri, 27 Sep 2024 09:03:02 GMT  
		Size: 5.9 MB (5870483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516584bc422114589ceb5b14a94a35383ea46c386c86072525a79fd9a4ddc229`  
		Last Modified: Fri, 27 Sep 2024 09:03:07 GMT  
		Size: 234.5 MB (234460527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467216a6096999d6ac6e131381fe55dc38cd6d6712d2950c2cb5b64359510ac3`  
		Last Modified: Fri, 27 Sep 2024 09:03:01 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:918b65384f10d2b847b0b1dc144b83cf1ecd24b6a6412ed91289f54c6c901a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2449788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fffc5461a6a117f33a7b4c02497a056be8189404de36ce4009f82cefd28b032`

```dockerfile
```

-	Layers:
	-	`sha256:fc92ae4b4921e3e1e31a37620cf19677ee5b837398942c24054567f7cfd51ec1`  
		Last Modified: Fri, 27 Sep 2024 09:03:02 GMT  
		Size: 2.4 MB (2432139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ba1ce092dd4a0b21ca84133e7dace2cc104df1e6587ee9ffd99e8aa802cf2b2`  
		Last Modified: Fri, 27 Sep 2024 09:03:01 GMT  
		Size: 17.6 KB (17649 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; ppc64le

```console
$ docker pull julia@sha256:d35c60192965064d94023a2029824dccd13efa56e34af401be1b176597f2a3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283883432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49dcbeb2bfc224549fb5c6fd496d7f16358a125c20006ebbb1e73bb67466b3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 05:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 26 Sep 2024 05:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc4
# Thu, 26 Sep 2024 05:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc4-linux-x86_64.tar.gz'; 			sha256='fdbd1aae595bd90f20b01cffe7ec34afcd25568b6351888065c934923ecfa042'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc4-linux-aarch64.tar.gz'; 			sha256='bc87e519a7f4d1633ca38db2b6bafd58f7025601202291a8ab6dd680101ad44f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc4-linux-i686.tar.gz'; 			sha256='dbcb66e774c71daf53d8b2582d30352c8696f05907e82b64a49754f718447196'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc4-linux-ppc64le.tar.gz'; 			sha256='06892cc4172e4e7a62051e68acd1a664da5e8e0cdd5f4902c5cad679ac27890d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 05:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d424b429b246dcc7c2c35da69e78023b09bce5be5133a9d35a34655a959e19c`  
		Last Modified: Fri, 27 Sep 2024 01:18:59 GMT  
		Size: 6.2 MB (6247878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5cafd82d33a1aadc2e8545c98f7c94cd152e606ccd05047a480cd892f4e4ba`  
		Last Modified: Fri, 27 Sep 2024 01:19:05 GMT  
		Size: 244.5 MB (244512821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc6ad90c209e26bc493ebbef999a62589b61444304ec010796fd8904568f46c`  
		Last Modified: Fri, 27 Sep 2024 01:18:58 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:00cab981688e0fdc18f372cc6bce23080fa1c8a57a210b77ba026449c2dba32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7fce562431ed048de5d5420f66874178acd5198f2ffb7473989033bffc17fe6`

```dockerfile
```

-	Layers:
	-	`sha256:94934dcd55d360f5c762ca73f51812fb86653f72df5b2ceaadbac09a9e84d107`  
		Last Modified: Fri, 27 Sep 2024 01:18:59 GMT  
		Size: 2.4 MB (2439476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b11af87de74f7ca4824600a9386cd86f96cf6192dcf340b9d9a8e833a622da7`  
		Last Modified: Fri, 27 Sep 2024 01:18:58 GMT  
		Size: 17.7 KB (17742 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:35a86c812bf628fb0d57b23f41577f4128481313c59bb13424c059d0b803ebd6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714813472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8f677d649794ca9bd0b54895cc4d5a76f671ca0a4c318e5f410914d42e8447`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 26 Sep 2024 23:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 26 Sep 2024 23:58:06 GMT
ENV JULIA_VERSION=1.11.0-rc4
# Thu, 26 Sep 2024 23:58:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-rc4-win64.exe
# Thu, 26 Sep 2024 23:58:07 GMT
ENV JULIA_SHA256=8db57de418602e300e8332b7140498cd3f72ce841bbd16135b20bf1f0cada689
# Fri, 27 Sep 2024 00:00:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 27 Sep 2024 00:00:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f903642668f734897abc460d44dd08deec9dc38623b685d8d09eb8cf630bc94`  
		Last Modified: Fri, 27 Sep 2024 00:00:19 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d275bd801bfda68beede2930292c5a969e388ba326f13308ac15a03a9bdba0`  
		Last Modified: Fri, 27 Sep 2024 00:00:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0933520c1d651ad54fa7b6a5a0e8985c0f38cdeee95fa4e98a361db392d2da13`  
		Last Modified: Fri, 27 Sep 2024 00:00:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87140fa53f4ce1594a5e3fb9f18a10085109783ffc8a7a6eb5b47dbb7ebbaba0`  
		Last Modified: Fri, 27 Sep 2024 00:00:17 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932d9916e7a519cc1fe7703f62666821d0a161b18ee6f4505a5b58d827ff0b7a`  
		Last Modified: Fri, 27 Sep 2024 00:00:47 GMT  
		Size: 252.6 MB (252614573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cac0016497e277302fec19b617390d469467c3904225f04591157be3ddf269`  
		Last Modified: Fri, 27 Sep 2024 00:00:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:3edd929277bff87fc0270d01950692a7365bf68fe3302e5ebdc699ab8f854c50
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1972859734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755d978735d7a741916de4fea883ce9d206296421f32bcddcd5249f58f275cfb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 26 Sep 2024 23:58:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 26 Sep 2024 23:58:18 GMT
ENV JULIA_VERSION=1.11.0-rc4
# Thu, 26 Sep 2024 23:58:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-rc4-win64.exe
# Thu, 26 Sep 2024 23:58:20 GMT
ENV JULIA_SHA256=8db57de418602e300e8332b7140498cd3f72ce841bbd16135b20bf1f0cada689
# Fri, 27 Sep 2024 00:00:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 27 Sep 2024 00:00:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35117ec68f95d8a8d623a3a16323f1cc81eb3592a89d6e765b5bc893fe4d9f75`  
		Last Modified: Fri, 27 Sep 2024 00:00:47 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9980c7a8d890c07bc321932a88d18be5d517374cddf6903b6be90efd4397a490`  
		Last Modified: Fri, 27 Sep 2024 00:00:46 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91db49ec533d67be0da7d3c542d54b84132cd8b2eeb07acde4b3b343599af0f5`  
		Last Modified: Fri, 27 Sep 2024 00:00:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d70e15820bef6aef46a060f411028210487aacb52c37e1e72cd1c594bbd51c5`  
		Last Modified: Fri, 27 Sep 2024 00:00:46 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039ae3ea8f7ae6c2f2a5d2700dc4110a84d562a79e034774fbd7006435b55b21`  
		Last Modified: Fri, 27 Sep 2024 00:01:16 GMT  
		Size: 252.6 MB (252584875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b464f8705cf5f8c2a9b6190fb285ce30bbdfbc20d42bd449f65c3ca706f70`  
		Last Modified: Fri, 27 Sep 2024 00:00:46 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
