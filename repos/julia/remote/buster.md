## `julia:buster`

```console
$ docker pull julia@sha256:bafc7390861d720f22b3b41058edac013bddb73c84e74e625cc5a846593ce9b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:buster` - linux; amd64

```console
$ docker pull julia@sha256:9515ea986cd6eec487627c197788830ee79957e8c2552544ad4a643ad47c33f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144664262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df58abd9ed1aba8228ed8618f946bca19e9f54251f6c2d333cf46e74eb151013`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:21:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:21:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 10 Sep 2020 12:21:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 12:21:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 10 Sep 2020 12:21:16 GMT
ENV JULIA_VERSION=1.5.1
# Thu, 10 Sep 2020 12:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='f5d37cb7fe40e3a730f721da8f7be40310f133220220949939d8f892ce2e86e3' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='751d7b62ebbcecbc9c8ef7669b1b7e216eb9d433276fa00cfb28831eca9ee27b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='6b37a2bee2dd464055dfda9bb8d994e7d4dca9079a47f6818435171c086ab802' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 10 Sep 2020 12:21:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27e46e0dbc60c328799c3750fc4b5f047a48dd243bf0fd9f61e5c0bbd1bd454`  
		Last Modified: Thu, 10 Sep 2020 12:23:31 GMT  
		Size: 4.4 MB (4436652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cab429b2a8d4a697e7a40023bb7fd809e64aacf937c1ea3fd716d8f1817c166`  
		Last Modified: Thu, 10 Sep 2020 12:23:58 GMT  
		Size: 113.1 MB (113135449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:0b5eef12ecc84eb20cb678e5854d06c8afeaf74047e8b97f518caa9c9952de81
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135646185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f2896f59e1d2f6697de79d938adb6cb765c4d5f232368a1a885f843f3cc87d`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:33:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 04:33:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 10 Sep 2020 04:33:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 04:33:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 10 Sep 2020 04:33:15 GMT
ENV JULIA_VERSION=1.5.1
# Thu, 10 Sep 2020 04:33:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='f5d37cb7fe40e3a730f721da8f7be40310f133220220949939d8f892ce2e86e3' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='751d7b62ebbcecbc9c8ef7669b1b7e216eb9d433276fa00cfb28831eca9ee27b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='6b37a2bee2dd464055dfda9bb8d994e7d4dca9079a47f6818435171c086ab802' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 10 Sep 2020 04:33:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa8a2767214a191c7e5d90165d1b4fea0754980858f5cc1825e9c4ee3718b2c`  
		Last Modified: Thu, 10 Sep 2020 04:35:43 GMT  
		Size: 4.3 MB (4315170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8572887c715acc9bff2553a81a53ce38125398398f92133a2bd2660a16bde9`  
		Last Modified: Thu, 10 Sep 2020 04:36:14 GMT  
		Size: 105.5 MB (105481690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; 386

```console
$ docker pull julia@sha256:1f2588ea2d59d4f47e36333f59d0d7bcaa3a723918d4d7004f273affd1756f75
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142423708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9b99db0f1158fb16452871a537a7441dcf0c541ddfec1a5aa15f141c0c2248`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 02:31:01 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 10 Sep 2020 02:31:01 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 02:31:01 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 10 Sep 2020 02:31:02 GMT
ENV JULIA_VERSION=1.5.1
# Thu, 10 Sep 2020 02:31:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='f5d37cb7fe40e3a730f721da8f7be40310f133220220949939d8f892ce2e86e3' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='751d7b62ebbcecbc9c8ef7669b1b7e216eb9d433276fa00cfb28831eca9ee27b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='6b37a2bee2dd464055dfda9bb8d994e7d4dca9079a47f6818435171c086ab802' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 10 Sep 2020 02:31:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d15a5e478ea028bdc6e5f21750df0edc415af5e08534c8edcce495cdbfb6d`  
		Last Modified: Thu, 10 Sep 2020 02:33:12 GMT  
		Size: 4.6 MB (4585930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93349198f14a30e235f617f2cb17fbb93746ae889e7bd1101606282d13c937f0`  
		Last Modified: Thu, 10 Sep 2020 02:33:54 GMT  
		Size: 110.1 MB (110087444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
