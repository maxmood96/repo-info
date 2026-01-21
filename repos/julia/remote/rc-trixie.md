## `julia:rc-trixie`

```console
$ docker pull julia@sha256:cd5d31e336687692a1a976e7c88fa445b093b9bd960f63585c202dc9ab040fe4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:rc-trixie` - linux; amd64

```console
$ docker pull julia@sha256:61f766f99cab043cd345ca5235830c7823940a54d8f22d6542849aeb2b8a4916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344600140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c482b0d41586fa720c6d7e559fd2a9c2ae6e11b384a64443277150ea291646f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 22:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 22:53:53 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Jan 2026 22:53:53 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 22:53:53 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Jan 2026 22:53:53 GMT
ENV JULIA_VERSION=1.13.0-beta1
# Tue, 13 Jan 2026 22:53:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta1-linux-x86_64.tar.gz'; 			sha256='4b501de5f7bdff4fd4ab186e2fae8608ea4cf840c6bbcee142362a1a32a0f354'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta1-linux-i686.tar.gz'; 			sha256='7875f846c550f332988ee7466a120e0ff1040b05d54d4889db496ef7cae5d131'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta1-linux-aarch64.tar.gz'; 			sha256='73624a83a7ac1effcfeaeaf9cd9668113b6ef3b3d6135f9e9259a8b83a9fd75d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 13 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 22:53:53 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49614a5022a79e397981d75fe974ae6aba48cf57155c5c6478b1c963575d73c9`  
		Last Modified: Tue, 13 Jan 2026 22:54:52 GMT  
		Size: 6.2 MB (6243797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef3fdd2e80996539d1403fa50b73bc11bc2931e08c83ae86d90f71f2f7be4b0`  
		Last Modified: Tue, 13 Jan 2026 22:55:28 GMT  
		Size: 308.6 MB (308582285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fd51241cb00598f1f654649bb981fc69fe4aea753aabd83e36bd52798fdbef`  
		Last Modified: Tue, 13 Jan 2026 22:54:51 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:00350a1fe9f3108e08ecac5844f2a6c29a79519f59156fe6769c40491e27d00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60616eef76f12fabd6e653af7ff8ac5e3ff48d835c8f0778b62d59a8177a1a93`

```dockerfile
```

-	Layers:
	-	`sha256:8dc99e4df1d2ab96643cedcea45288d1b388ffa88358829863700861a9d58a1a`  
		Last Modified: Tue, 13 Jan 2026 22:54:38 GMT  
		Size: 2.2 MB (2240877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4583a408853a6ac77cb76f2707a200955ddb536d98263faa4940dd1507035407`  
		Last Modified: Wed, 14 Jan 2026 00:03:29 GMT  
		Size: 17.2 KB (17188 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:776524eeb417bbdee7b6c64564cc1aefe1d88d299439e67fc283c904cf5c1d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.7 MB (368741037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09764b13ec1d7484e892c73ad864e8fe59122b6083dd10326b3155f7cd350b29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 22:53:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 22:54:08 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Jan 2026 22:54:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 22:54:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Jan 2026 22:54:08 GMT
ENV JULIA_VERSION=1.13.0-beta1
# Tue, 13 Jan 2026 22:54:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta1-linux-x86_64.tar.gz'; 			sha256='4b501de5f7bdff4fd4ab186e2fae8608ea4cf840c6bbcee142362a1a32a0f354'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta1-linux-i686.tar.gz'; 			sha256='7875f846c550f332988ee7466a120e0ff1040b05d54d4889db496ef7cae5d131'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta1-linux-aarch64.tar.gz'; 			sha256='73624a83a7ac1effcfeaeaf9cd9668113b6ef3b3d6135f9e9259a8b83a9fd75d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 13 Jan 2026 22:54:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 22:54:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 22:54:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2ad9fb1c4f035a2734fa3ea41def006a7954a6439e0f568f05e0e9fb20b7ff`  
		Last Modified: Tue, 13 Jan 2026 22:55:12 GMT  
		Size: 6.2 MB (6152014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae214f7fe8aa19f715c202c8ae4cd1822de34a615a5baf5d113be8c2dd9603e`  
		Last Modified: Tue, 13 Jan 2026 22:55:28 GMT  
		Size: 332.5 MB (332454612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0907b56c1f523e94bd986a592e2849ce4eddc9e6160bd0401ca98fa9d22229c3`  
		Last Modified: Tue, 13 Jan 2026 22:55:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:4e8ea14a899b2e0ae0a732c2343c0bce1beda172b6efabdd7280e969c2c3cd91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0911a60774636b03fde30313c4ca0ce6dc6ac3785077b1e0e0ec426efb7c76d9`

```dockerfile
```

-	Layers:
	-	`sha256:dc3ec1a4255aae968b0e73177bcd286f9c3d0208bbf3ed6ae42945f2459dd7ad`  
		Last Modified: Wed, 14 Jan 2026 00:03:33 GMT  
		Size: 2.2 MB (2241185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da78a8581d90ff9e9cb2bc5d3393b901168f81ee0d5e0a4bf837d6ae4430f7fa`  
		Last Modified: Wed, 14 Jan 2026 00:03:34 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; 386

```console
$ docker pull julia@sha256:400179d6bd7f94b01a867ae2ef12a8e7a515b9029e4bc563bdde4af3729031e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280682781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3628ba98296eeba449fd1a1bee753aa66c1c64f3f1fc71efdfde7b3489ead673`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 22:53:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 22:54:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Jan 2026 22:54:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 22:54:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Jan 2026 22:54:15 GMT
ENV JULIA_VERSION=1.13.0-beta1
# Tue, 13 Jan 2026 22:54:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta1-linux-x86_64.tar.gz'; 			sha256='4b501de5f7bdff4fd4ab186e2fae8608ea4cf840c6bbcee142362a1a32a0f354'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta1-linux-i686.tar.gz'; 			sha256='7875f846c550f332988ee7466a120e0ff1040b05d54d4889db496ef7cae5d131'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta1-linux-aarch64.tar.gz'; 			sha256='73624a83a7ac1effcfeaeaf9cd9668113b6ef3b3d6135f9e9259a8b83a9fd75d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 13 Jan 2026 22:54:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 22:54:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 22:54:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad64e4c6c8448a6c25978a70df1df64b32cc6d6de4669dc03264e0132cac80dd`  
		Last Modified: Tue, 13 Jan 2026 22:55:02 GMT  
		Size: 6.4 MB (6429262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff3f8ede76321fca7b77f555985f1ce06a216256b8f72c4cd1eed5458a9f5fa`  
		Last Modified: Tue, 13 Jan 2026 22:56:05 GMT  
		Size: 243.0 MB (242964670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a38b9b05a3f4af83acac23cc85c8ffdaacef692fa118dbaf24e2294108d689c`  
		Last Modified: Tue, 13 Jan 2026 22:55:01 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:acb2db96b6c8d4e22939f15ae80046918b00e45575a3db2e6f2e4e2b7772e361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b1fa634fa2cd6c43cc0705ff443050c57be699ee76ab6b6d5359b787a7b495`

```dockerfile
```

-	Layers:
	-	`sha256:37a0cd85f58d4a3aaf968f0966c7450747785902a93e085b8dade8db393ed699`  
		Last Modified: Wed, 14 Jan 2026 00:03:37 GMT  
		Size: 2.2 MB (2238012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d578faaee81b3e8839032ff8ffc147ab6b63ab177aa79abe8327d8df867a2e9`  
		Last Modified: Tue, 13 Jan 2026 22:54:50 GMT  
		Size: 17.1 KB (17145 bytes)  
		MIME: application/vnd.in-toto+json
