## `python:3-alpine3.22`

```console
$ docker pull python@sha256:b4d299311845147e7e47c970566906caf8378a1f04e5d3de65b5f2e834f8e3bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `python:3-alpine3.22` - linux; amd64

```console
$ docker pull python@sha256:084182bab6c2e39b58715a171c882da2d2429b200447110ae4842dec787b7a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16793935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36479b0aca0690d8664b8b38c0ddac210991e35abc7305840e8eba02524ed98`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79d6683f2c03ff26a006bee4a16160ef68a397cf43d44cc98d203b412dac4fc`  
		Last Modified: Wed, 04 Jun 2025 18:03:22 GMT  
		Size: 460.2 KB (460217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45f97f3a84945a3893f1db63e1508e8f1311eaebd822f9eebdb0dfe53f82c93`  
		Last Modified: Wed, 04 Jun 2025 18:03:24 GMT  
		Size: 12.5 MB (12536624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b632c212d72393d6d14b469494c5cbb8a9670813e05b05a089019627ad5329f`  
		Last Modified: Wed, 04 Jun 2025 18:03:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.22` - unknown; unknown

```console
$ docker pull python@sha256:2ed0925c3cbcf0174840b1847ff8bc954da5bf960ba923bcd4b27c9017498608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.3 KB (650276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb50720ca68bfea436858fec2f552e7a33e7eda3f5bf554e1a74f29d2b9d8405`

```dockerfile
```

-	Layers:
	-	`sha256:b839a3e6bd964c5408342bc983533e7e7800ae7c136a5d9dbc70f7f7d2bd1ca0`  
		Last Modified: Wed, 04 Jun 2025 18:07:01 GMT  
		Size: 626.3 KB (626288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66757aeb6ae880488849ae2f351205947554661df11e38bdc834448ae2eff856`  
		Last Modified: Wed, 04 Jun 2025 18:07:02 GMT  
		Size: 24.0 KB (23988 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine3.22` - linux; arm variant v6

```console
$ docker pull python@sha256:b68ddb9dcc05e19e806e33836864862de78bcb108a746d44b2d5e3726321657c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16119416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18773ae516b14e4722c3eb50726d4bb1a9e7c48c47dfb85c2c9d2df78b66f3c7`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98acbd7f9e3e356a86b42927a55a7407697b0dbfa8ed1ab2909fefaf2f6f9ddf`  
		Last Modified: Tue, 03 Jun 2025 17:26:51 GMT  
		Size: 461.0 KB (461005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c311227735d18d4e17d89349df58febf805f6a7b2544a636f8e2d288e2e850a0`  
		Last Modified: Wed, 04 Jun 2025 17:15:07 GMT  
		Size: 12.2 MB (12157233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4ed6f2eedd57bfcbd07b8e63b13e4f72dd5743f3a2ae09bb430c273c53cead`  
		Last Modified: Wed, 04 Jun 2025 17:15:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.22` - unknown; unknown

```console
$ docker pull python@sha256:28bc446b18d7685155da8ada8c1fdd4a8adbee8ad82fde71f3a40885dcbb3778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 KB (23907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35156fd2c046cdf04a586fa46f30829177a2c5d4f7d44b63fb8b72e1a4f6ae7`

```dockerfile
```

-	Layers:
	-	`sha256:3fa92908da4fa193babc0ca1ace08b73024be50d93d758ecaecc5cb5bd69ecb3`  
		Last Modified: Wed, 04 Jun 2025 18:07:06 GMT  
		Size: 23.9 KB (23907 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine3.22` - linux; arm variant v7

```console
$ docker pull python@sha256:a2677329762d07d8b396215210d9898fad1a2dd868cfe23a28c70cd08e72eeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15509614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbcfc62754c4e9b36572450ebfbf57806d0c78a64a0127299c2f06d8fe36865`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490b11ee21ee9fedd87ddac5b20d81719683e487be7171f318e7c813764fe276`  
		Last Modified: Tue, 03 Jun 2025 13:59:25 GMT  
		Size: 460.2 KB (460220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4553a4f5fea98f58a7a1c674ab347ff70acb86709aa25434d7096703efd9c575`  
		Last Modified: Wed, 04 Jun 2025 18:37:13 GMT  
		Size: 11.8 MB (11829965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856dc7585719f2323a56108391511589a56fc7fb39b9ef3144a6dee8822627c8`  
		Last Modified: Wed, 04 Jun 2025 18:37:12 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.22` - unknown; unknown

```console
$ docker pull python@sha256:7d0516ad79d9f5404ceb66dd5126544ea936347ed7979ed46189061f927cea8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.5 KB (653468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b5df63f0aa4b3b9695ff9201c4b7476922cb5f415c7b686c95db60d0408f78`

```dockerfile
```

-	Layers:
	-	`sha256:f3e9febea1f9ba7045b1507de8cc532e67b81f87e75b21f3bdb3d6a8e68a4fe7`  
		Last Modified: Wed, 04 Jun 2025 21:06:30 GMT  
		Size: 629.3 KB (629346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1423ec9273fc758d2fb2f95da3a8568bad2df4a4329fcb8c48b3b31dadb4fb6`  
		Last Modified: Wed, 04 Jun 2025 21:06:31 GMT  
		Size: 24.1 KB (24122 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull python@sha256:d236c9962b0b55c603d462b9811c89eafaa8f2c0c03331cc8ea3dc49753fa3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17150951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bd6be6df5d59ffd00cf3240ea893d94fbc086f77a4e9cdc65b783087b09441`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af073699363458487c4151d77486824bd6582c1386b74554976345d24bbcd3a5`  
		Last Modified: Tue, 03 Jun 2025 13:34:08 GMT  
		Size: 462.1 KB (462093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce47c3bb2edaa4753529f65a400882b0793b4cb68a2b3c32eb5c6cf19faa1bed`  
		Last Modified: Wed, 04 Jun 2025 18:04:37 GMT  
		Size: 12.6 MB (12552670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8921f3a4ba566051b873385e4c5c24e6eb94c4ef71b799c136206e5785ccb712`  
		Last Modified: Wed, 04 Jun 2025 18:04:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.22` - unknown; unknown

```console
$ docker pull python@sha256:b59c8389170fe4729e34e695509c3b230015c7e030d93e3091d78c8a186f9210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.6 KB (650561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ed51ee57afe3c4ee0ae76a69c472c77d308aa97a8bbc1c3284d14976c35984`

```dockerfile
```

-	Layers:
	-	`sha256:64fe4e2944328d7a38525d272f031041e6bcc0c3bf809bd7481dc69a0510aa03`  
		Last Modified: Wed, 04 Jun 2025 18:12:09 GMT  
		Size: 626.4 KB (626392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e265571eb6c426d4b12cc376ccaa01df595771b923eff13d65196b0a806df264`  
		Last Modified: Wed, 04 Jun 2025 18:12:10 GMT  
		Size: 24.2 KB (24169 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine3.22` - linux; 386

```console
$ docker pull python@sha256:507a6ebd3b1698e51de9b29047b736feec32478c815b52a159b7fea6ab3dbad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16868137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8791f87572b24cbd62d8641919ffafbe1b0f1d919fb9fff43920e4874cac30b4`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7c041585e2b8b74f3925a141eb43b55983caeb2939c6d6c6c283fcf0804ab`  
		Last Modified: Wed, 04 Jun 2025 18:03:31 GMT  
		Size: 460.6 KB (460633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b7fcb1118a2a04d0a31b7b7def5def690251b34cfd5fe52465186cb33bd262`  
		Last Modified: Wed, 04 Jun 2025 18:03:32 GMT  
		Size: 12.8 MB (12791229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cd1160ef891e7e83d85b7a645de6ff31fc4c240e04fc7272b0cfcaefada864`  
		Last Modified: Wed, 04 Jun 2025 18:03:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.22` - unknown; unknown

```console
$ docker pull python@sha256:77aa4189d38ae089f2da10def65f52d19fc2908bf9f2e93b9a4a46fee4944182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.2 KB (650174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af42e9398796045934472db84c2007ae268a6eeafb5a0677201a1f59e66d266`

```dockerfile
```

-	Layers:
	-	`sha256:50b3dbce6181275162f85e673ab388c31ac3915c368b9c99e6a0d9bf628e186c`  
		Last Modified: Wed, 04 Jun 2025 18:07:15 GMT  
		Size: 626.2 KB (626243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fceb7593d181c72894e46079064b5ba2425d637b6975fa9c2a1104435a8e9c1c`  
		Last Modified: Wed, 04 Jun 2025 18:07:16 GMT  
		Size: 23.9 KB (23931 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine3.22` - linux; ppc64le

```console
$ docker pull python@sha256:85b6d9f103f144e40ac79360f587aa1390d38e5081c2b6c4bfa02712238d6863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17454325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3d6114e5942b5b6595d036522681bd115047923279fcebf3d269b8c47362f4`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f48677c5d1a39856430bfce5e53e0ef5ef0f335b02584edf4af5f6d69ba3b2`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 462.6 KB (462600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f64f4166dc29274d656ae0c1bf43365e4ddcf3328a9afadb2e0a97aaf52752`  
		Last Modified: Wed, 04 Jun 2025 17:50:30 GMT  
		Size: 13.3 MB (13261291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d87cf3c0934ed33e12198c0f92e858a667bbe87b196a36d154cf695e013919`  
		Last Modified: Wed, 04 Jun 2025 17:50:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.22` - unknown; unknown

```console
$ docker pull python@sha256:a5251655e5b918b2658f3b9212109f49ccbf67dabfc4e2738651be8b15eadde9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.5 KB (648453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e65cd4f9219c14871b8776daa52f4ddf7cc59090d88125583065df1d93ba239`

```dockerfile
```

-	Layers:
	-	`sha256:e467f918a8c5a0c9c915421e4dbd5f1698db578dbfd8e8f84c92192d2f15278d`  
		Last Modified: Wed, 04 Jun 2025 18:07:20 GMT  
		Size: 624.4 KB (624395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf39ce30a1eeec1b87f297596008c1d8d0f9b8335dc40c738ab5d56a15d0368a`  
		Last Modified: Wed, 04 Jun 2025 18:07:21 GMT  
		Size: 24.1 KB (24058 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine3.22` - linux; riscv64

```console
$ docker pull python@sha256:327c26bf1f2e532de4672243f0c7944357b043349252efd1af02bb846dcfb3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16579599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea7d5dfef1da43c730d4d5cc78a44225718503900a5590ff4f1a63014a5405d`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343a026726fe75f0771026946b211c01b78752dc7965fc084d1ddbd62c4fd75d`  
		Last Modified: Tue, 03 Jun 2025 17:08:14 GMT  
		Size: 460.7 KB (460659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9708db898bc7a19a8ce775995d169ce7fd6c5a47d024f7706995f7f1c56b28ae`  
		Last Modified: Wed, 04 Jun 2025 17:42:17 GMT  
		Size: 12.6 MB (12604880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6e3410af928c83ebd3ce0f463ba9c5342955dfa38adf52c972c6a47dc17823`  
		Last Modified: Wed, 04 Jun 2025 17:42:16 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.22` - unknown; unknown

```console
$ docker pull python@sha256:8da6f63707e41572895fc15f6bca8033560b72f35aba91eb67865a9eb27778ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.5 KB (648451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3e6a3a9a4d5ae5b5184f82f09bec06958b509abf44a3ca467ef00186fc0274`

```dockerfile
```

-	Layers:
	-	`sha256:f3f6063e616e10d2787c16bcd2a1a3cccc183bca4820ab3513b5034ecda1cc7b`  
		Last Modified: Wed, 04 Jun 2025 18:07:24 GMT  
		Size: 624.4 KB (624391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c35a3feba7c1b1c6aaa7fe26db64b9df8989b31098c91a9ae37bc3563c638822`  
		Last Modified: Wed, 04 Jun 2025 18:07:25 GMT  
		Size: 24.1 KB (24060 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine3.22` - linux; s390x

```console
$ docker pull python@sha256:78a52f8e240b164061bdefd1b979c5679bc586bc52ed01e58f0210364bd85015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17104222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48055fea4a5003314405a07743f37aa22aa7d221261dd2944fcede1892e8406`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ace8d3eac9e183dedbedc0f4f39f1cededed0957f3c813561de40b77f65ca`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 461.2 KB (461180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafc3a3f2ef0b4dca78b431223611b20169358d227b57682b82c16947e0c4d0a`  
		Last Modified: Wed, 04 Jun 2025 17:42:54 GMT  
		Size: 13.0 MB (12995265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caec32e711505746c68f34f947f7558d82032f913d2d9404d9e0f069262602a4`  
		Last Modified: Wed, 04 Jun 2025 17:42:51 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.22` - unknown; unknown

```console
$ docker pull python@sha256:bb4c12f8ce4b86c4dab50c6c743642ed85ed19134a8de46fe3e965fb313f879d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.3 KB (648325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a91a8ebb43b98e331595d1b7ca9dd03a0fa133636f73d1cd6b22830226f93db`

```dockerfile
```

-	Layers:
	-	`sha256:75d3b87a9ebc2d61e85ace76971ca7c4fdf3567d3eaf1a9184fdddb2e7db8240`  
		Last Modified: Wed, 04 Jun 2025 18:07:29 GMT  
		Size: 624.3 KB (624337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afa8198a0205ce18b2f8e0828acc41fa69f2a3519eef5cc780aa3c029ff1e826`  
		Last Modified: Wed, 04 Jun 2025 18:07:30 GMT  
		Size: 24.0 KB (23988 bytes)  
		MIME: application/vnd.in-toto+json
