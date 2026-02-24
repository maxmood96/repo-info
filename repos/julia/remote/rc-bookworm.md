## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:4f06ed8033e5f56c83a3dc3a860aa99c99acd367803ceebbe7fcf302290483b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:rc-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:62d3e803459247d44ca793e7d84b1dd247bd399232d3c73f18d598c68ebbd1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342728321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e605ff5ad7405773822a8d53925236934592b0fba6b72bc0f7fe4d4077e43b42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:04:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 24 Feb 2026 19:04:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:04:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 24 Feb 2026 19:04:49 GMT
ENV JULIA_VERSION=1.13.0-beta2
# Tue, 24 Feb 2026 19:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta2-linux-x86_64.tar.gz'; 			sha256='a12587225ccacf8988a3473535e73c7007223c5e3dba82ddce4efee2bf22db9a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta2-linux-i686.tar.gz'; 			sha256='ec17bf167ea51e7ffd7604e03c5c7fb8eb235e2cdf78f45a25cce8151cfd784c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta2-linux-aarch64.tar.gz'; 			sha256='2b0f8e396a0add65525daa038daadec3ee9f82b9ba02f09a4a59d6979202b932'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 24 Feb 2026 19:04:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:04:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:04:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a6120924233dfe2f3d255558b4f309610ccd25f6b41133c43cc4049ff62c34`  
		Last Modified: Tue, 24 Feb 2026 19:05:36 GMT  
		Size: 5.7 MB (5717934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13d0b882906b1eb0a6981caef8d510605cb7423b3c4c342f7a33525378198dc`  
		Last Modified: Tue, 24 Feb 2026 19:05:45 GMT  
		Size: 308.8 MB (308773738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee03697b83d862d7eaa749aeda4d2b54344c0b11f525a67400b413bd2d1e0b1b`  
		Last Modified: Tue, 24 Feb 2026 19:05:36 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0f0ea28f0f593d42ee6fef131a4aa9feacb73f481de5386eabd599f84a09e0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe13316cfa66646379ee2455e94bfc765a5a2415b3ffde2bb26e9fedca4da2d5`

```dockerfile
```

-	Layers:
	-	`sha256:7d2eace3311a827b955ae6b398dba6418564517ce18269da8472d55ecb57eba2`  
		Last Modified: Tue, 24 Feb 2026 19:05:36 GMT  
		Size: 2.6 MB (2568624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:819b591733d6cb442304653c57ab0d18bca6fac34a6410dc12c41e6f926eb43c`  
		Last Modified: Tue, 24 Feb 2026 19:05:36 GMT  
		Size: 16.3 KB (16319 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3ab73977eeef20e153bb596abd430818e109dde323d7b62a6766feb40cc489c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.4 MB (366416557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d462b4986d235e524a36a7967da6a26e329bb597013ac1866c7d8e6976f3b9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:08:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 24 Feb 2026 19:08:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:08:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 24 Feb 2026 19:08:02 GMT
ENV JULIA_VERSION=1.13.0-beta2
# Tue, 24 Feb 2026 19:08:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta2-linux-x86_64.tar.gz'; 			sha256='a12587225ccacf8988a3473535e73c7007223c5e3dba82ddce4efee2bf22db9a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta2-linux-i686.tar.gz'; 			sha256='ec17bf167ea51e7ffd7604e03c5c7fb8eb235e2cdf78f45a25cce8151cfd784c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta2-linux-aarch64.tar.gz'; 			sha256='2b0f8e396a0add65525daa038daadec3ee9f82b9ba02f09a4a59d6979202b932'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 24 Feb 2026 19:08:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:08:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:08:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f7c590af301828f72daa4d8bd0d314d57f12fb3fcf27602f35582102ee9387`  
		Last Modified: Tue, 24 Feb 2026 19:07:17 GMT  
		Size: 5.6 MB (5567910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d898842b884af4a5b4d657febe9600dd307b08d9f663fabbac0f3b095f4bb2eb`  
		Last Modified: Tue, 24 Feb 2026 19:08:56 GMT  
		Size: 332.7 MB (332732200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94e608e7561fb6ca3655f5da80ed73306b23640679948a775662f7a58cb15f0`  
		Last Modified: Tue, 24 Feb 2026 19:08:50 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:15413e85e1997fa67bbfbd78657a61f7333dd946853e317db70e8808780db776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2585313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9e86b5dba07d933336fbc2cfbeb6933801038e93c84ae2d23c943c9d7514c3`

```dockerfile
```

-	Layers:
	-	`sha256:55a8303185ce21f28325cfe26f2157b3e4510edfe73866c6da61c0f420bc3ce5`  
		Last Modified: Tue, 24 Feb 2026 19:08:50 GMT  
		Size: 2.6 MB (2568887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c859f115cfd0f113a7bb6e081e30088425f72fff314b2080439c6470fbc70cc`  
		Last Modified: Tue, 24 Feb 2026 19:08:50 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:72773e43cf42f55b11aa8e45bfb0976de8decc38f145e0d62a5f96fb4da950c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278027273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76917e794a13a918cfedd95b96e359896a0ca8e5430e7f02ebe90d25c99acf13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 18:57:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:57:56 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 24 Feb 2026 18:57:56 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 18:57:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 24 Feb 2026 18:57:56 GMT
ENV JULIA_VERSION=1.13.0-beta2
# Tue, 24 Feb 2026 18:57:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta2-linux-x86_64.tar.gz'; 			sha256='a12587225ccacf8988a3473535e73c7007223c5e3dba82ddce4efee2bf22db9a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta2-linux-i686.tar.gz'; 			sha256='ec17bf167ea51e7ffd7604e03c5c7fb8eb235e2cdf78f45a25cce8151cfd784c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta2-linux-aarch64.tar.gz'; 			sha256='2b0f8e396a0add65525daa038daadec3ee9f82b9ba02f09a4a59d6979202b932'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 24 Feb 2026 18:57:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 18:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:57:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bab6f574391274ab5dcfab8bda32d58ff3363c5f6d8b329979ceac5bd4afee6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 29.2 MB (29221705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650ee24ae35f5652defafb69cd03b1a4a9543bf293e5bf750a2c2d4a9f4a0638`  
		Last Modified: Tue, 24 Feb 2026 18:58:29 GMT  
		Size: 5.9 MB (5878856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a500b26db6e958e8ac7a29c2a5e256451e26df6692a7c80f1da2b493b84d65`  
		Last Modified: Tue, 24 Feb 2026 18:58:33 GMT  
		Size: 242.9 MB (242926342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290eae818ef2ae5f16765a8b0bef415418400fc106c8d007a84112df15c701ef`  
		Last Modified: Tue, 24 Feb 2026 18:58:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7ec5e9ad6b8524b12883c300afee41ef16dda402b5b610a85bf658752b95c9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7740600f7acdfe2e5fb51bb38725974ac700861510de87cab82d2cb16ada3dd`

```dockerfile
```

-	Layers:
	-	`sha256:ae4e760565edf4c9559a9490492b21e0e0b314014cde856f9b003f0bd3f7f778`  
		Last Modified: Tue, 24 Feb 2026 18:58:28 GMT  
		Size: 2.6 MB (2565776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9caba20664e562df1864ea6811e2d54bcf883c58702f90c0bf68da127592c792`  
		Last Modified: Tue, 24 Feb 2026 18:58:28 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.in-toto+json
