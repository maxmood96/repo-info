## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:0d5a5ebeea5141877d9a00b1dda60377466ad6efafbe34dbef4a2c22a2aaf9b1
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
$ docker pull julia@sha256:5c478cc8cb5a38617364746e98e9b115522b7ef3d47a4f42e4ac65955bd9f0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321580286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6948f44d54f1caf29eb0fc76c06758866acdff5619bdceaf3939519403828aea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sun, 13 Jul 2025 23:59:27 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Sun, 13 Jul 2025 23:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 13 Jul 2025 23:59:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Sun, 13 Jul 2025 23:59:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 13 Jul 2025 23:59:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sun, 13 Jul 2025 23:59:27 GMT
ENV JULIA_VERSION=1.12.0-rc1
# Sun, 13 Jul 2025 23:59:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc1-linux-x86_64.tar.gz'; 			sha256='cffec86c06803cb53a77048caa3f9802feb3affd2eb08be94d913b261c25309e'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc1-linux-aarch64.tar.gz'; 			sha256='bdf2988615df11d04338078c83443dc3122ece0c19f6513e5a959518daa76592'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc1-linux-i686.tar.gz'; 			sha256='e6ee828c91bd8841e7d08d3dcfa755994d7501efb27a75306fab0ba3e438b872'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sun, 13 Jul 2025 23:59:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 13 Jul 2025 23:59:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 13 Jul 2025 23:59:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8394a3cf0ff613112034f4f42f1194424b0a0480e974eb0a90ea2a6f1558a9`  
		Last Modified: Wed, 10 Sep 2025 01:31:19 GMT  
		Size: 5.7 MB (5716180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7c4c536c04455d30aae1c33b7df119b086d734478e65fc47fe14e9d96d42ac`  
		Last Modified: Wed, 10 Sep 2025 01:31:38 GMT  
		Size: 287.6 MB (287635388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778ab5ecd40b5ab1361eb7fe71af0051f9f34e0e4a688a0f10d8034f6b914462`  
		Last Modified: Mon, 08 Sep 2025 21:54:41 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b900d243ab505827c481d2d4043d4486060bc15ab32d49661c903333af827d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf1d4d47411d30ca2b0625fb3ab79a47d70d37b7b9d70295ce78aba205f1493`

```dockerfile
```

-	Layers:
	-	`sha256:2f7163d6e4ec702f7222ddfed7d7ead15d37eded977fa776024452c64e672e69`  
		Last Modified: Mon, 08 Sep 2025 23:04:13 GMT  
		Size: 2.6 MB (2567402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c35f42e9235a26d600a927707e1b1ad987b44dd382f651bf95dc82a4074cd312`  
		Last Modified: Mon, 08 Sep 2025 23:04:15 GMT  
		Size: 16.4 KB (16353 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:7025466a431ea24d5b61efaca802ece0ca3db1faa8327a94343351eef2b3b933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341681854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a13c8a63c7475b9c095595dee4b2724ba05578c94ccd6a1038e50ad4d65e3d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sun, 13 Jul 2025 23:59:27 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Sun, 13 Jul 2025 23:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 13 Jul 2025 23:59:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Sun, 13 Jul 2025 23:59:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 13 Jul 2025 23:59:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sun, 13 Jul 2025 23:59:27 GMT
ENV JULIA_VERSION=1.12.0-rc1
# Sun, 13 Jul 2025 23:59:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc1-linux-x86_64.tar.gz'; 			sha256='cffec86c06803cb53a77048caa3f9802feb3affd2eb08be94d913b261c25309e'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc1-linux-aarch64.tar.gz'; 			sha256='bdf2988615df11d04338078c83443dc3122ece0c19f6513e5a959518daa76592'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc1-linux-i686.tar.gz'; 			sha256='e6ee828c91bd8841e7d08d3dcfa755994d7501efb27a75306fab0ba3e438b872'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sun, 13 Jul 2025 23:59:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 13 Jul 2025 23:59:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 13 Jul 2025 23:59:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eae7ac2cdc03ffd23d1778eeca664fe6f215dc4a9ef0db32e6768c621910506`  
		Last Modified: Tue, 09 Sep 2025 02:40:00 GMT  
		Size: 5.6 MB (5567146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1669a808d25219ed39fb156cba738cfb21ab617ae8b1ac7e2a065601ac40605e`  
		Last Modified: Tue, 09 Sep 2025 19:10:08 GMT  
		Size: 308.0 MB (308012244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642121d3981ff3e76ce2173dc85eb01d4d7f5ba4d9fb8510296e68a92fd6b4e7`  
		Last Modified: Mon, 08 Sep 2025 22:03:33 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:44a75059187dd7ed09f8369fc03798ef739cd8bcd531d2161a4c327b16c5a7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b7432b72c41a4d35678c819bc6f8229b3f8c05ef99c47175fa6d4d44d7b3ba`

```dockerfile
```

-	Layers:
	-	`sha256:b45646e4b73cfe2989343a903527c6c8a2cde763a53b8b255789ec6603cff6b1`  
		Last Modified: Mon, 08 Sep 2025 23:04:19 GMT  
		Size: 2.6 MB (2567665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb152e0b065dad69c9457d6eeb736510a9bb301e375504d984cf11701ef9c70e`  
		Last Modified: Mon, 08 Sep 2025 23:04:20 GMT  
		Size: 16.5 KB (16460 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:cf3b9006694aca8611dcf5c13f440c4378b5358d80f4497d7cc39cdb7eb82cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (266026254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f166b1ef2e48fe02477baee1fc2291176159eb3c0e9c5645acf39422ad2d6bac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sun, 13 Jul 2025 23:59:27 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Sun, 13 Jul 2025 23:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 13 Jul 2025 23:59:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Sun, 13 Jul 2025 23:59:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 13 Jul 2025 23:59:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sun, 13 Jul 2025 23:59:27 GMT
ENV JULIA_VERSION=1.12.0-rc1
# Sun, 13 Jul 2025 23:59:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc1-linux-x86_64.tar.gz'; 			sha256='cffec86c06803cb53a77048caa3f9802feb3affd2eb08be94d913b261c25309e'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc1-linux-aarch64.tar.gz'; 			sha256='bdf2988615df11d04338078c83443dc3122ece0c19f6513e5a959518daa76592'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc1-linux-i686.tar.gz'; 			sha256='e6ee828c91bd8841e7d08d3dcfa755994d7501efb27a75306fab0ba3e438b872'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sun, 13 Jul 2025 23:59:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 13 Jul 2025 23:59:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 13 Jul 2025 23:59:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:dc2a09b0db8b98044474925cacc9c009aa76e5883edf644cc36c3f6a2e3917ac`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 29.2 MB (29209634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7142a622b0c94214980e1f52f2773db33c55a24921076e7795ac3a39253e0d16`  
		Last Modified: Tue, 09 Sep 2025 02:37:43 GMT  
		Size: 5.9 MB (5878056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e9d05d735ebb09a14d6cfbf3a6c6a97bb028849dd4919de45dcea6dcb943fa`  
		Last Modified: Mon, 08 Sep 2025 21:13:53 GMT  
		Size: 230.9 MB (230938197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9719905cc16cf37677bd0d91050f56d76fc610d2d62b6041192d694232b54ca3`  
		Last Modified: Mon, 08 Sep 2025 21:55:52 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f95eb7e8f00dabdc6dff0e12f3ce0b0f29e077df77bda25e2c9434e5db629321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2580878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce49acd9257f9cbc80ee68ea7e847b2086894c01a7c458ca86e5ff44ea2a458`

```dockerfile
```

-	Layers:
	-	`sha256:4fbb0529f14e0f3bdec063e6f6fd62eecbd93608e5da6be6b545cda32b931545`  
		Last Modified: Mon, 08 Sep 2025 23:04:24 GMT  
		Size: 2.6 MB (2564554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f67f1ada29473edfda502819b6c966bc0a529d5254b3f1f600c76fb8edf7fedd`  
		Last Modified: Mon, 08 Sep 2025 23:04:25 GMT  
		Size: 16.3 KB (16324 bytes)  
		MIME: application/vnd.in-toto+json
