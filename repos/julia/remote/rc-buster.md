## `julia:rc-buster`

```console
$ docker pull julia@sha256:af08cb880655ddcf724ae0a3fbbc51c30dee5c29225d1567141e5f3324cb6059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:rc-buster` - linux; amd64

```console
$ docker pull julia@sha256:8adedc79a39371b9323766b8cd2dff258a688bdccd36ad46451a30d06eb88bfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180382679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0101e26d8eb4e86843d9ca434cac9e006b5df7f4b5e7c1afb29a94993c66e5e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:25 GMT
ADD file:e614539607055bdbde0cc1a94ef9783fe3627c8553ef1b21071ecb5c27ea27e4 in / 
# Wed, 12 Apr 2023 00:20:26 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:41:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:41:00 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 12 Apr 2023 10:41:01 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 10:41:01 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 12 Apr 2023 10:41:01 GMT
ENV JULIA_VERSION=1.9.0-rc2
# Wed, 12 Apr 2023 10:41:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-rc2-linux-x86_64.tar.gz'; 			sha256='664f3b50c16c089e9e580958107b4a8e8d1af8206242993601bb3447b4d3541c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-rc2-linux-aarch64.tar.gz'; 			sha256='2e8325f1c7e14bf2f36e84ef1ed61b51e8a674c8d2cc0f1166b95f3b345e4a3f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-rc2-linux-i686.tar.gz'; 			sha256='96bd3db4ab1e846de7f48177521b8c8768bd80e484ed7fd7591a39753f7f9a02'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.0-rc2-linux-ppc64le.tar.gz'; 			sha256='4444ecd58bfeed61a969a32cec94df8860cdb02314bc09c10af6958fdd5d4c31'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 12 Apr 2023 10:41:18 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Wed, 12 Apr 2023 10:41:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Apr 2023 10:41:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9fbefa3370776b7ec7633cf07efc14cc24e0c0cd53893ad0e7e3f44ffdc1bedb`  
		Last Modified: Wed, 12 Apr 2023 00:24:22 GMT  
		Size: 27.1 MB (27138920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ce4548760a286750aa25db08d3d11804194a8ef009fb719e71180c1903fd5a`  
		Last Modified: Wed, 12 Apr 2023 10:43:43 GMT  
		Size: 4.5 MB (4471672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c31180f5e02429975df9245b0705ac5ba11394908e3396787f3e9e281c79b6`  
		Last Modified: Wed, 12 Apr 2023 10:44:04 GMT  
		Size: 148.8 MB (148771715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bd26cc8bc320c832e007796dccc7ee03b3cef5db250e2b38fbc5d437c680d7`  
		Last Modified: Wed, 12 Apr 2023 10:43:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:928f0aebe2debb8001cfe0d3e20d9f311b89e768f72a66147037b0997c8961f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173157960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7671fbc963d3393931d4657840b8f6fa68ffcc1f583423e27e7eefb54e9c796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:02 GMT
ADD file:39d4ef5cc48487567b857a8527ab3c106b5099eafffbeaa8b70df450fb8409e3 in / 
# Wed, 12 Apr 2023 00:40:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 03:36:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 03:36:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 12 Apr 2023 03:36:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 03:36:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 12 Apr 2023 03:36:30 GMT
ENV JULIA_VERSION=1.9.0-rc2
# Wed, 12 Apr 2023 03:36:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-rc2-linux-x86_64.tar.gz'; 			sha256='664f3b50c16c089e9e580958107b4a8e8d1af8206242993601bb3447b4d3541c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-rc2-linux-aarch64.tar.gz'; 			sha256='2e8325f1c7e14bf2f36e84ef1ed61b51e8a674c8d2cc0f1166b95f3b345e4a3f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-rc2-linux-i686.tar.gz'; 			sha256='96bd3db4ab1e846de7f48177521b8c8768bd80e484ed7fd7591a39753f7f9a02'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.0-rc2-linux-ppc64le.tar.gz'; 			sha256='4444ecd58bfeed61a969a32cec94df8860cdb02314bc09c10af6958fdd5d4c31'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 12 Apr 2023 03:36:47 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Wed, 12 Apr 2023 03:36:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Apr 2023 03:36:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:27bec964ec41cf69bd5df2ffd45c27623ae4bb0eb6f9f366179f7ac9b47d9840`  
		Last Modified: Wed, 12 Apr 2023 00:43:11 GMT  
		Size: 25.9 MB (25922011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caebb9e72b49936f1cc0878df82b4c402468f0b3b0d907d218682cb0a732ddc0`  
		Last Modified: Wed, 12 Apr 2023 03:38:56 GMT  
		Size: 4.4 MB (4350374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b3a052db73894e61f99f3ba17695065f4871093ad9f81f76de90702913fce4`  
		Last Modified: Wed, 12 Apr 2023 03:39:12 GMT  
		Size: 142.9 MB (142885200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b75269beaa1f58c22f22ebd4b2f878004c637d69fda9df1cc7f50f95ab125f`  
		Last Modified: Wed, 12 Apr 2023 03:38:55 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-buster` - linux; 386

```console
$ docker pull julia@sha256:8161a3541a12c26f1b1e0c85dc3b27d5b9dcc4b90c919ac7476ea64da0cd2c52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178319533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6e1794a5bd60a521fc64c56bf8f85fb5858415af1cbe2e7c12eb2db1cddcd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:21 GMT
ADD file:0f4c5475f636be52b419806a7ea7d8d81fc1203c9228544c1324e79277739a3f in / 
# Wed, 12 Apr 2023 00:39:21 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 04:46:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:46:22 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 12 Apr 2023 04:46:22 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 04:46:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 12 Apr 2023 04:46:23 GMT
ENV JULIA_VERSION=1.9.0-rc2
# Wed, 12 Apr 2023 04:46:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-rc2-linux-x86_64.tar.gz'; 			sha256='664f3b50c16c089e9e580958107b4a8e8d1af8206242993601bb3447b4d3541c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-rc2-linux-aarch64.tar.gz'; 			sha256='2e8325f1c7e14bf2f36e84ef1ed61b51e8a674c8d2cc0f1166b95f3b345e4a3f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-rc2-linux-i686.tar.gz'; 			sha256='96bd3db4ab1e846de7f48177521b8c8768bd80e484ed7fd7591a39753f7f9a02'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.0-rc2-linux-ppc64le.tar.gz'; 			sha256='4444ecd58bfeed61a969a32cec94df8860cdb02314bc09c10af6958fdd5d4c31'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 12 Apr 2023 04:46:47 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Wed, 12 Apr 2023 04:46:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Apr 2023 04:46:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ae6c02ab25c72d784ae8832cdcb583320ab9a3046938adc3c659ae607da19b43`  
		Last Modified: Wed, 12 Apr 2023 00:43:29 GMT  
		Size: 27.8 MB (27797581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa7e73320fde4fc6eed1e22276ef0b7a421f47840813265507e667163d653a4`  
		Last Modified: Wed, 12 Apr 2023 04:49:34 GMT  
		Size: 4.6 MB (4623303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bad21f205203b237d9744960a5a377d3a08269202e5927337ba6cd128873f4`  
		Last Modified: Wed, 12 Apr 2023 04:50:03 GMT  
		Size: 145.9 MB (145898276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3330f9c169bdc0b4fce2f9e06a353cc2d14ef5f40b754b8e2b71a3b6e6f04a`  
		Last Modified: Wed, 12 Apr 2023 04:49:32 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
